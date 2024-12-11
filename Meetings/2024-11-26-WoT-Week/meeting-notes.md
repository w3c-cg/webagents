# WebAgents CG: WoT Week 2024 (Nov. 26, 2024)

## Agenda
   * Welcome \& Review of CG Activity
   * Updates \& Feedback from the PlugFest
   * Open Discussion
       * Challenges \& Opportunities
       * Interoperability Task Force
   * Conclusions and Next Steps


## Participants
   * Andrei Ciortea
   * Andrei Olaru
   * Julian Padget
   * Ege Korkan
   * Danai Vachtsevanou
   * Simon Mayer

**Scribe**: Danai Vachtsevanou

## Meeting Notes

EK: Nobody is using TDs as RDF. Most consumers usually consume TD documents as JSON documents.

AC: I am already starting to take notes because this is interesting. So, Jeremy's and Rem's participation to the PlugFest is highlight a need that is perhaps more specific to the WebAgents CG: using TD documents as RDF documents. This makes sense for us, because we typically think of programming agents at the knowledge level.

[Andrei's Slides](https://github.com/w3c-cg/webagents/tree/main/Meetings/2024-11-26-WoT-Week/) (provide an overview of the WebAgents CG Charter, among others)

Ideas for discussion:
   * suggestion to organize an event at ECAI 2025 (next autumn) in Bologna
   * Curating online materials to promote the work of the CG (e.g., tutorials)
   * Define use cases that me be also relevant to the [Linked Web Storage WG]([https://www.w3.org/groups/wg/lws/)](https://www.w3.org/groups/wg/lws/))

Updates from WoT Week

Jeremy: 
   *  We are trying to resolve some discrepancies between the W3C WoT TD spec and the wot-td-java library 
       * JSON-LD context seems to be wrong in the security schemes. 
   *   Ganesh points out that TDs could be used more broadly, going beyond using it as a JSON-LD document   
       * People are not importing new ontologies to the TD.

Simon: We should avoid hardcoding against TDs. This leads to collapsing semantics and ignoring hypermedia. 

Andrei:
   * We could contribute ideas for motivating the use of additional vocabularies in TDs as part of KGs
   * We could contribute ideas for motivating the use of autonomous clients

Ege: Indeed, the application logic commonly remains static in WoT applications.  If you don't care about consumer applications, you do not care more ontologies. Another direction that is not explored is a TD having a dynamic set of affordnces, e.g., acquiring new affordances, or considering that some affordances are not always allowed. This would require the application logic to be updated so that the consumer can deal with such dynamics. In Siemens, we commonly represent the affordances of fixed-function devices in TDs. 

Andrei: How often do we need to replace fixed-function devices to motivate the update of TDs

Ege: This is a real UC that we have. Sometimes we cannot replace a device with one of the same time (e.g., due to constraints on the protocol use), so a device of a different type is being used. There is one demo from Siemens, where the affordances of a Thing [EGE, PLEASE CORRECT THIS SENTENCE] change based on rules injected at run time (e.g., measuring a temperature is now being computed based on the presence of humans in the room). 

Ege: We do store TDs in RDF, but I'm not sure how many people actually implement logic on RDF.

Ege: There had been a proposal of extending the scripting API so that affordances can be selected/used based on their semantic type (instead of only their name). The proposal was not liked a lot (see issue: [Semantic ConsumedThing part of Scripting API · Issue #527 · w3c/wot-scripting-api · GitHub](github.com/w3c/wot-scripting-api/issues/527))

Rem: [Rem, feel free to provide here your feedback for the 1st day of the WoT week] It was not easy to relate the TDs to the physical world. Some contextual information in TDs could help in this. For example, Ganesh was using the BRICK ontology. 

Ege: How to tell where a device is being located, e.g., to accommodate people with visual impairment (for instance, with a "beep" affordance).

Andrei: Should we enlarge the scope of the use cases to motivate the use of RDF?

Rem: Let's focus on a particular use case, and examine its challenges, e.g., in building automation. 

Simon: We already had several use case TFs in the past, the goal is indeed "large", so how do we approach this?

Rem: Gather use ideas from this event here, or gather use cases from publications in WoT

Simon: What I learnt from the IntelIoT project is that people considered TDs as API descriptions which could be integrated at the end of the project, so no one had looked at it until the end of the project. Maybe a survey about WoT use cases could be useful. 

Andrei: Maybe a community group report could be used. 

Simon: It would be interested to show what on WoT has been done in research, what has not been adopted by industry, and why. 

Julian: I've seen use case collections in the context of Distributed Ledgers. There the collection was use full to see the commonalities between the cases. However, this requires a large number of use cases, which may not be possible here. I can look at collections that I have seen in different contexts to provide input. 

Andrei O.: I think the use cases aspect is very important, and it is a good discussion to have. 

Andrei: I think Rem's proposal to build towards the Interoperability TF might help to make things more hands-on and more applied. 
