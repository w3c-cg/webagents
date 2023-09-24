# TPAC 2023: WebAgents CG and WoT CG/WG Joint Meeting

## Proposed Agenda
- Introduction to the W3C Web of Things [Link to slides](https://github.com/w3c-cg/webagents/blob/main/Meetings/2023-09-11-TPAC/Presentations/TPAC2023-WebAgents-WoT-Discussion_Points-Korkan.pdf)
- Introduction to the WebAgents CG [Link to slides](https://github.com/w3c-cg/webagents/blob/main/Meetings/2023-09-11-TPAC/Presentations/TPAC2023-joint-meeting-WebAgents-WoT.pdf)
- Open Discussion

## Participants
- Andrei Ciortea
- Luca Barbato
- Michael McCool
- Antoine Zimmermann
- Simon Mayer
- Alessandro Ricci
- Ege Korkan
- Nicoletta Fornara
- Julian Padget
- Stephen Cranefield
- Samuele Burattini
- Jérémy Lemée
- Danai Vachtsevanou
- Kudzai Manditereza
- Rem Collier
- Robert Winkler
- Tomoaki Mizushima
- Justus Fries
- Jan Romann
- Christian Glomb
- Zoltan Kis
- Justus Fries
- Wout Slabbinck
- Cristiano Aguzzi
- Mahda Noura
- ...


**Scribe:** (collaborative notes)

## Meeting Notes

11:36:50 From Michael McCool To Everyone:
	would be good to set the stage first with WebAgents?
    
11:37:22 From Michael McCool To Everyone:
	I for one am wondering how Agents relate to IoT
    
11:38:04 From Michael McCool To Everyone:
	although maybe this was discussed in an earlier session...
    
11:39:12 From Andrei Ciortea To Everyone:
	Hi Michael! Indeed, we already discussed a bit on this point in the previous session — but we will reiterate when we introduce the WebAgents CG.
    
11:40:59 From Michael McCool To Everyone:
	ok, sorry I missed the earlier session, then.
    
11:44:39 From Michael McCool To Everyone:
	To be clear, I'm one of the WoT co-chairs, I just don't want to lose people who came for agents :)
    
11:48:02 From Michael McCool To Everyone:
	please mention use cases and requirements document
    
11:48:11 From Andrei Ciortea To Everyone:
	Reacted to "please mention use c..." with 👍
    
11:49:43 From Jérémy Lemée To Everyone:
	Replying to "To be clear, I'm one..."
	Many members (I don't want to speak for everyone though) of the webagents community group have experience with the Web of Things so I don't think this should be a problem.
    
11:59:48 From Michael McCool To Everyone:
	would like to comment on the "function" concept
    
12:01:58 From Simon Mayer (University of St.Gallen) To Everyone:
	Agents driving Tractors (by TTTech) and handling Robots (by Siemens):  https://www.ifaamas.org/Proceedings/aamas2023/pdfs/p2499.pdf (this is an architecture publication, now it's implemented)
    
12:03:38 From Ege Korkan To Everyone:
	Breakout sessions on Wednesday that are relevant to WoT:
- Home Assistant Dialogue: https://www.w3.org/2023/09/TPAC/breakouts.html#b-c13a3ae8-979c-4157-9c74-b28aba314878
- Schema Languages: https://www.w3.org/2023/09/TPAC/breakouts.html#b-b8617206-4c2b-4355-80da-fcf4eb628d1a 
- Web-based Digital Twins for Smart Cities: https://www.w3.org/2023/09/TPAC/breakouts.html#b-36a66bc5-7515-41a1-b7a8-625d4dadb338

12:04:01 From Michael McCool To Everyone:
	however... there are hooks for such things, e.g. WoT TDs are JSON-LD documents and support semantic extensions.  So what we would want is a standardized way to annotate the semantics of actions.  A related topic is accessibility, i.e. does an action result in a real-world visible/audible UI element?
    
12:04:56 From Zoltan Kis, Intel, WoT To Everyone:
	Reacted to "however... there a..." with 👍
    
12:05:12 From Samuele Burattini To Everyone:
	Reacted to "however... there are..." with 👍
    
12:05:42 From Michael McCool To Everyone:
	s/action or event/ -> in general, how does the network API described by the TD related to the external environment?
    
12:11:00 From Michael McCool To Everyone:
	regarding devices "carrying" TDs: self-description is one pattern.  however things being described by "others" is also possible
    
12:11:48 From Antoine Zimmermann To Everyone:
	I'm wondering: what do the WoT people think about using WoT TDs to describe non physical things, like a web service or a web platform?
    
12:13:00 From Michael McCool To Everyone:
	Replying to "I'm wondering: what ..."
	It is explicitly allowed.  We can describe "things" without network APIs, and we can also describe "virtual things" that may have a network API but not be "physical" (e.g. they might be a network service).
    
12:14:01 From Michael McCool To Everyone:
	Replying to "I'm wondering: what ..."
	however, I should say that while semantic annotations to describe these things can be used, we have not defined any.  It was considered out of scope in our last (and current) charter.  But the hooks are there.
    
12:16:05 From Alessandro Ricci To Everyone:
	Thanks a lot @Michael McCool for the feedbacks and links. From an agent point of view, a description of a “function” (purpose) of a thing could be even more abstract wrt to how I can use that thing. That is: I could reason and understand that a thing could be useful for me before learning how to use it through its affordances..  This is what happens for human agents with human artifacts.
    
12:16:47 From Robert Winkler To Everyone:
	Replying to "I'm wondering: what ..."
	As an example, in the Smart Home domain, we model a Weather Service or a virtual Alarm System with WoT and it is working fine.
    
12:16:56 From Michael McCool To Everyone:
	suggestion: for Agents to have a good foundation, need to start with clear use cases and requirements before diving into trying to standardize anything... need to find the "gaps" where standards are needed, first!
    
12:17:24 From Zoltan Kis - Intel To Everyone:
	Reacted to "As an example, in ..." with 👍
    
12:17:40 From Andrei Ciortea To Everyone:
	Reacted to "regarding devices "c..." with 👍
    
12:20:38 From Robert Winkler To Everyone:
	Replying to "Thanks a lot @Michae..."
	In the Smart Home domain we added a "purpose" extension to the WoT TD which we use for a higher level (more abstract) description of the device. For example a LightBulb or Lightstrip fulfill the same purpose "Lighting", even if they might provide different properties/actions/events
    
12:20:49 From Michael McCool To Everyone:
	Replying to "Thanks a lot @Michae..."
	OK, that kind of information can also be associated with a Thing via "links" which can carry relations as well.   We have looked at the existing IANA relations to see which ones are relevant.  We could do even more with RDF semantics.
    
12:21:22 From Alessandro Ricci To Everyone:
	Replying to "Thanks a lot @Michae..."
	THX!
    
12:23:09 From Michael McCool To Everyone:
	Replying to "Thanks a lot @Michae..."
	regarding "higher level" descriptions: another thing we have discussed and would be useful would be "adapters".   How can I describe, for example, stateful vs. non-stateful lights and how could I unify APIs that use different color spaces?  Could have a service with a standardized abstract interface that maps to multiple concrete lights...
    
12:23:43 From Samuele Burattini To Everyone:
	Reacted to "regarding "higher le..." with 👍
    
12:23:49 From Michael McCool To Everyone:
	Replying to "Thanks a lot @Michae..."
	the above scenario is not hypothetical, lights are surprisingly complex and a good test case
    
12:24:27 From Michael McCool To Everyone:
	Replying to "Thanks a lot @Michae..."
	there is also the relation between lights and entities in the real world they provide illumination for

12:29:03 From Michael McCool To Everyone:
	the mention of fading reminded me of another topic: the representation of time.  There is an IEEE PG looking at spatial-*temporal* intervals, queries, etc. which is relevant.

12:29:49 From Michael McCool To Everyone:
	Note: we want to avoid reinventing things.  It's important to connect to existing standards where they exist

12:30:57 From Zoltan Kis - Intel To Everyone:
	(Note: chairs, please make sure to save this side chat for the record and eventually include in the meeting minutes as well? Thanks.)

12:35:00 From Michael McCool To Everyone:
	(IEEE P2874)

12:35:51 From Michael McCool To Everyone:
	(also regarding spatial data, has been ongoing discussion with Spatial Data on the Web IG, who also collaborate externally with OGS)

12:39:13 From Simon Mayer (University of St.Gallen) To Everyone:
	Signifiers for Web Agents: https://dl.acm.org/doi/10.5555/3545946.3598763

12:39:22 From Andrei Ciortea To Everyone:
	The FIPA standards I mentioned:
- FIPA Abstract Architecture: http://fipa.org/specs/fipa00001/SC00001L.html
- FIPA Agent Management Specification (incl. the FIPA Agent Identifier Description): http://fipa.org/specs/fipa00023/SC00023K.html

12:41:30 From Michael McCool To Everyone:
	Signifier paper also seems to be on ArXiv...

12:41:59 From Michael McCool To Everyone:
	Replying to "Signifier paper also..."
	https://arxiv.org/pdf/2302.06970.pdf

12:45:37 From Julian Padget To Everyone:
	+1 Fabien. Affordance is concept that has a range of meanings and usages

12:48:01 From Robert Winkler To Everyone:
	What I miss in WoT is something like in HATEOS. The actions a device provides can be dependent on the state of the device. How does a Client know based on a TD which actions can be used when a device is in a given state. For example, when a song is running on a soundsystem, you can pause or stop it, but when no song is running, you have to pick a song and start it. 
	Isn't this also important for autonomous agents which need to know the possible next steps to be invoked to reach the final state?

12:48:41 From Simon Mayer (University of St.Gallen) To Everyone:
	Robert, this is precisely what we have been working towards in that paper :-)

12:49:06 From Robert Winkler To Everyone:
	Perfekt 🙂

12:49:13 From Simon Mayer (University of St.Gallen) To Everyone:
	"Affordances" that emerge as a function of the current context (i.e., the agent-environment situation and the agent's abilities)

12:49:14 From Michael McCool To Everyone:
	Replying to "What I miss in WoT i..."
	Agree.  In short, what are the preconditions for an action to be valid?

12:50:44 From Robert Winkler To Everyone:
	Reacted to "Agree.  In short, wh..." with 👍

12:50:49 From Samuele Burattini To Everyone:
	Reacted to "Agree.  In short, wh..." with 👍

12:51:00 From Michael McCool To Everyone:
	Regarding mangeable actions, the "jobs" aspect is related to the management of dynamic resources, which is a RESTful thing - but means the "API" is not "static" - URL entry points can be created and destroyed.

12:51:45 From Robert Winkler To Everyone:
	Replying to "What I miss in WoT i..."
	Or what propertes are effected by an action. For example, setting the lamp to a color could also implicity power on a light and thus mutate multiple properties.

12:52:25 From Michael McCool To Everyone:
	Another not-quite-related topics is dynamic TDs.  Are TDs changing over time, or fixed?   Fixed makes life easier, but some information (e.g. geospatial location) may or may not be changing over time.

12:52:58 From Ege Korkan To Everyone:
	https://github.com/w3c/wot-thing-description/tree/main/proposals

12:53:36 From Samuele Burattini To Everyone:
	Replying to "Another not-quite-re..."
	To that regard, what's the feeling of achieving dynamic exposure of valid affordances with a changing TD?

12:53:38 From Robert Winkler To Everyone:
	Long Running actions: Enable Guest Wifi on a Router and get notified when it is turned on. How does the client know that it needs to listen for an event after calling an action :D

12:55:01 From Robert Winkler To Everyone:
	Reacted to "Another not-quite-re..." with 👍

12:55:04 From Michael McCool To Everyone:
	Replying to "Long Running actions..."
	Exactly.  So the event can return information... and that could include an indication that an event will be forthcomings, URLs to manage event subscriptions, URLS to poll status, etc.

12:55:34 From Michael McCool To Everyone:
	Replying to "Long Running actions..."
	sorry, I meant "the action can..."

12:55:45 From Robert Winkler To Everyone:
	Replying to "Another not-quite-re..."
	In the Smart Home domain TD can change over time, because some devices are modular and can be extended at runtime. For example Weather Stations.

12:56:01 From Ege Korkan To Everyone:
	Reacted to "Another not-quite-re..." with 👍

12:56:31 From Jérémy Lemée To Everyone:
	Replying to "What I miss in WoT i..."
	In our conception of signifiers developed in the paper, we develop the concept of "signifier exposure" that enables a signifier to be shown to an Agent only when certain conditions are met, such as the affordance is available for example. This exposure can be implemented by comparing the current state of the environment with metadata integrated with a signifier, indicating when it is valid. By using signifiers, we can enable HATEOAS for the Web of Things. One additional benefit for agents is that signifiers could be explicitly linked to a potential goal, thus helping the Agent decides whether to use or not the affordance described by the signifier.
    
12:56:55 From Robert Winkler To Everyone:
	Replying to "Another not-quite-re..."
	So it's not only the state like a location which can change over the time, but also the capabilities of a device.
    
12:57:00 From Michael McCool To Everyone:
	Replying to "Another not-quite-re..."
	There is a question of *how* dynamic.  Occasional updates are one thing, when do updates become so frequent they should be managed with affordances instead?  There is also an issue of privacy: we may want to limit access to some information
    
12:57:27 From Simon Mayer (University of St.Gallen) To Everyone:
	Replying to "Another not-quite-re..."
	We argued that interaction affordances in TDs should not just (typically)be able to change over time but that they in Addition should sometimes be hidden, sometimes be emphasized, sometimes be shown in a different way, ...
    
12:58:37 From Samuele Burattini To Everyone:
	Reacted to "There is a question ..." with 👍

12:59:29 From Julian Padget To Everyone:
	the conditions affecting an action could be maintained externally to the Thing, if desirable, as a policy (which is norms by another name)

13:01:10 From Michael McCool To Everyone:
	"data" vs. "metadata": imo metadata should be information that changes relatively slowly.

13:01:48 From Michael McCool To Everyone:
	so... templates for resources, but not the dynamic resources themselves

13:03:49 From Michael McCool To Everyone:
	regarding semantics development, I think development of ontologies should wait until a clear set of requirements and purpose is defined, otherwise it would be an endless job

13:04:08 From Robert Winkler To Everyone:
	Thank you for the interesting meeting!
