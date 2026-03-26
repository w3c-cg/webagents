# Simple agent scenario

Simple agent scenario, with a single agent. No agent-to-agent interaction.

An agent's goal is to find light sources to brighten the place where its owner is.

The agent is perceiving its environment by "listening" to local beacon signals that locally transmit a single URI. The agent capture the URIs and dereferences them whenever it conforms to the beacon signal specification (there may be need for a security layer, but we assume for this scenario that the beacon is trustworthy).

The agent dereferences the URI. Its goal is to find, from this URI, the existence of a light source that can be switched on.

The agent can only switch the light on if what it gets from the beacon URI corresponds to a description conforming to a precise ontology, and where the description uses specific classes and properties.

The agent expects to find an RDF file where there are instances of a specific class of WoT Thing (for instance onto:LightSource) that have a capability to generate light and a WoT affordance to switch on and off the light. The agent may have to rely on reasoning to infer that an entity is actionable, that it can emit light, etc. The agent may have to dereference more URIs to get enough information.

Several questions have to be answered: what does the agent look for in the description? When does it decide to follow more links and when does it stop? Of course, it can stop if it succeeds achieving its goal. But what the goal is unattainable (viz. there is no light source, or no light that can be switched programmatically)?

Example of how this could work:

 - the agent is materialised by a running process on a mobile device
 - there are beacons that transmit signals to nearby devices
 - the signal consists of a single URI
 - when the agent's device recieves a URI with the beacon protocol, it dereferences it (i.e., issues an HTTP GET requests)
 - assume the mobile device enters room 101
 - a local beacon issues a signal with URI https://building.thecorp.com/room101
 - there is a Turtle file at this URI with the following content:
```
<https://building.thecorp.com/room101> a hmas:ResourceProfile;
  rdfs:comment "Description of room 101."@en;
  hmas:isProfileOf <https://building.thecorp.com/room101#this> .
<https://building.thecorp.com/room101#this> a bot:Space;
  rdfs:label "Room 101"@en;
  rdfs:comment "Meeting room in the main building of The Corp headquarter."@en;
  hmas:hosts
    <https://building.thecorp.com/room101/lightbulbs/1#this>,
    <https://building.thecorp.com/room101/lightbulbs/2#this>,
    <https://building.thecorp.com/room101/heaters/1#this>,
    <https://building.thecorp.com/room101/electricshutters/1#this> .
```
 - now the agent needs a strategy to find the right thing
 - the agent assumes that all beacon URIs identify a profile for something geolocated (such as a room)
 - the agent looks for the resource that the profile is describing, following the hmas:isProfileOf relation
 - the agent is only concerned by resources that are hypermedia agent platforms (a type of entity than may host actionable entities)
 - the agent thus further looks for entities that are hosted by he platform
 - the agent must find an entity that can be switched on and off and can emit light
 - in the case of this example, there is not enough information
 - but the agent may dereference the URIs of the hosted entities
 - <https://building.thecorp.com/room101/lightbulbs/1#this> dereferences to:
```
<https://building.thecorp.com/room101/lightbulbs/1> a hmas:ResourceProfile;
  rdfs:comment "Description of the northwest lightbulb in Room 101."@en;
  hmas:isProfileOf <https://building.thecorp.com/room101/lightbulbs/1#this> .
  <https://building.thecorp.com/room101/lightbulbs/1#this> a onto:TPLinkLB130;
    td:hasActionAffordance [
      a onto:SwitchOnOffAffordance;
      rdfs:comment "Toggle device between being on (switch closed) and off (switch open) and returns true iff device is on."@en;
      td:hasForm [
        a hctl:Form;
        htv:methodName "POST";
        hctl:hasOperationType td:invokeAction;
        hctl:hasTarget <https://building.thecorp.com/room101/lightbulbs/1/switch>
      ];
      td:hasOutputSchema [ a js:BooleanSchema ];
      td:isIdempotent false;
      td:isSafe false;
      td:name "switch";
    ] .
```
 - the agent tries to find something that has an action affordance of type onto:SwitchOnOffAffordance
 - however, a device that can be switched on or off is not necessarily emitting light (e.g., the heater)
 - the agent only looks for things of type onto:LightingDevice
 - no such information is available, but the agent may dereference the class URI onto:TPLinkLB130
 - this leads to something like this:
```
onto: a owl:Ontology;
  rdfs:comment "An ontology describing various types of connected devices and device categories."@en .
onto:LightingDevice a owl:Class;
  rdfs:comment "A device that can emit light."@en;
  rdfs:subClassOf td:Thing .
onto:SmartLightbulb a owl:Class;
  rdfs:comment "A light bulb that can be operated via network commands, such as HTTP requests."@en;
  rdfs:subClassOf onto:LightingDevice .
onto:TPLink130 a owl:Class;
  rdfs:label "A model of connected light bulb, manufactured by TP LINK Corporation."@en;
  rdfs:seeAlso <https://www.tp-link.com/us/home-networking/smart-bulb/lb130/>;
  rdfs:subClassOf onto:SmartLightbulb .
```
 - now we can infer that the thing is a light source, so the agent can switch it on

Lots of issues:
 - what if the description is not available from a beacon? how does the agent discover it?
 - what if another vocabulary is used? how to align the vocabulary used in the description to the concepts that the agent knows?
 - what if the light source cannot be activitated in the way the agent knows? maybe there must be a payload with a certain structure? maybe there is authentication?
 - how do we know that switching on a light source is illumating the place where the agent's owner is? what if we have a description of a whole building? maybe there is a dim flashlight and a bright lamp, both capable of illuminating the room to a certain degree?
 - what if the light source cannot be activated by network connection but can be switched on mechanically, by operating a robot or something else?
 - what about a multi-agent scenario: some agents have access to capabilities that can illuminate a room, others don't
 - what about rights? policies?
