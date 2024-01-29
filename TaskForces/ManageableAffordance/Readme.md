# Manageable Affordances

**Moderators:** Ege Korkan, Andrei Ciortea

## Description

Action Affordances in hypermedia environments, as in the current W3C WoT specifications and Hydra, are rather simplistic, where a software agent sends a request and the entity exposing the affordance responds. 
It is unclear whether the response corresponds to the result of the (physical) action process or whether it is just an acknowledgment. 
Thus, it is needed to better describe the lifecycle of an action for software agents to better interact with environmental entities. 
Examples include the long-lasting dimming of a light, long-lasting movements such as robots and cameras (panning, tilting), or long-running actions that would require human curation.

Given that the hypermedia community is also represented in the WebAgents CG, the discussions would benefit from the various expert viewpoints in the CG.
This topic is relevant to the new WoT WG charter and the results of this TF may provide non-normative input to the standardization efforts.

## Activity

Suggested activities for this task force:
- reviewing the state-of-the-art; topics include:
  - the W3C WoT specifications for action affordances
  - affordance theory
  - architectures and programming paradigms for autonomous agents
- identifying and documenting current limitations and gaps
- proposing mechanisms for manageable action affordances

The TF will meet regularly every two weeks and will also interact asynchronously.

## Expected Outcome

A CG group report on manageable affordances.

## Related Resources

- Preliminary proposals on the WoT WG repository: https://github.com/w3c/wot-thing-description/tree/main/proposals (hypermedia-control 1, 2, and 3).
- Hydra: https://www.hydra-cg.com/

## Open Questions

- How does it effect the Consumer application? What is the committment of the Consumer?
- What happens if the underlying "regulation" changes during the runtime of the action? What if the "environment" changes, e.g. someone enters the working area of the robot while it is moving.
