# WebAgents CG: In-person Meeting @ECAI2025, Bologna Oct. 25, 2025

## Agenda

See [https://github.com/w3c-cg/webagents/tree/main/Meetings/2025-10-25-HyperAgents](https://github.com/w3c-cg/webagents/tree/main/Meetings/2025-10-25-HyperAgents)

   * 14:00 - 14:15 Welcome \& Agenda Setting
   * 14:15 - 15:30 Focused Discussion
   * 15:30 - 16:00 Coffee Break
   * 16:00 - 17:00 Demo / Hands-on session
   * 17:00 - 17:30 Wrap-up and Next Steps

## Participants

   * Andrei Ciortea (univ. St. Gallen, Switzerland)
   * Antoine Zimmermann (Mines Saint-Étienne, France)
   * Danai Vachtsevanou (univ. St. Gallen, Switzerland)
   * Habtom Gidey (TU Munich, Germany)
   * Gustavo Nardin (Mines Saint-Étienne, France -- online participant)
   * Jérémy Lemée (univ. St. Gallen, Switzerland)
   * Jonathan Rau (TU Berlin, Germany)
   * Maksim Ilin (Transport and Telecommunication Institute, Latvia)
   * Önder Gürkan (Norwegian Research Centre, Norway)
   * Rem Collier (univ. college Dublin, Ireland)
   * Simon Mayer (univ. St. Gallen, Switzerland)
   * Stephen Cranefield (univ. Otago, New Zealand -- after coffee break)
   * Terry Payne (univ. Liverpool, UK)

## Scribe:
    read.ai + Antoine Zimmermann + Jérémy Lemée

## Focused discussion

Architectural design. See the document at [https://deploy-preview-92--w3cwebagentscg.netlify.app/](https://deploy-preview-92--w3cwebagentscg.netlify.app/)

Discussions stayed some time on slide 8 of the presentation about Design Goals.

The notion of adaptability may be focused on the internal of agents while what must be the goal for the Web should be openness. But the definition given in the meeting of openness should be improved to cover openness of the environment beyond adding agents (the provided definition is: "the ability of introducing additional agents into the system in excess to the agents that comprise it initially", which only considers agents, and not other components of a MAS, such as artifacts).

   * Issue of what's in scope or not? We need to focus on the Web, not the internal of agents, or the offline parts of MAS. Simon proposes that a NFP can be in scope if it is applied at the system-level not at the agent level only. However, even among these properties, a choice needs to be made by the community to determine what is relevant for the report.
Discussion of Hewitt's requirements for open systems. Many of these properties are already enabled by the Web (e.g., negociation is covered by content negociation)


*AI stopped recording at 15:00 !!*


Discussions on what we put inside "openness" -> does it bring interoperability necessarily? does it bring evolvability? Or should we have interoperability and evolvability as desirable properties?


*AI started recording again at 15:13 !!*

Andrei mentions that the Web can be applied in a closed environment, even though the Web enables the construction of open systems.

Scalability makes sense at the environment level, less at the agent level, because each agent does not necessarily interact with many other agents, even if many agents are participating in the MAS and such a challenge would be at the agent level, not at the Web level.

Designing an adaptable agent is out of scope of the report. However, an agent pattern for interacting in hypermedia environments is in scope.

Agentic AI mirrors the separation of agents and environments with agents vs tools.

We summarise the NFPs that are in scope, in a slide.

Break from 15:50 until 16:15

Andrei proposes a test for introducing a NFP: if we can create a Web standard, or help with the standardization, then it is within scope.

Example discussed: WebSub could be a standard for situatedness so situatedness could be within scope (the concept is defined within the report but not included within the list of NFPs).

Discussion of the architectural patterns for situated MAS and presentation of an Yggdrasil demo to illustrate some concepts.

Conclusion: the goals were very ambitious and could not be fully achieved.
