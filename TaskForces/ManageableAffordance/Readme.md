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

## Workflow

1. We get motivating scenarios via GitHub issues using an issue template. 
2. We extract the requirements together with the submitter using [the requirements template](./Requirements.md).
3. Identify the gaps in the standards (WoT, other W3C, other SDOs) and open specifications (e.g. Hydra, JSON-HAL)
4. (Optional) Propose a concrete mechanism to satisfy the gap. This can be some diagram that gives enough information to implement or can be a proof of concept implementation

Regarding the mechanical workflow:

1. Description and requirements are collected in the issue. The issue owner can edit and extend their first comment with further information. Click [here](https://github.com/w3c-cg/webagents/issues/new?assignees=&labels=scenario&projects=&template=scenario_manageable_affordances.md&title=%5BManageable+Affordances+TF%5D+Add+Scenario+Title) to create one.
2. Once there are enough requirements (see [the requirements template](./Requirements.md)), the moderators or the issue creator opens a Pull Request to <https://github.com/w3c-cg/webagents/tree/main/TaskForces/ManageableAffordance/Submissions> by copy-pasting their first comment contents in markdown. The file should be named `{issue number}-{title of the scenario}.md` to avoid name conflicts and track the submission back to the issue.
3. A wider group extends the submission with the gap analysis as a follow-up Pull Request. A conversation can happen in the Pull Request
4. Once the Pull Request is merged, the group turns it into a section in the report HTML document.

Once we have enough contributions to the HTML and it is reviewed, it can be published as a CG report.

## Related Resources

- Preliminary proposals on the WoT WG repository: https://github.com/w3c/wot-thing-description/tree/main/proposals (hypermedia-control 1, 2, and 3).
- Hydra: https://www.hydra-cg.com/

## Open Questions

- How does it effect the Consumer application? What is the committment of the Consumer?
- What happens if the underlying "regulation" changes during the runtime of the action? What if the "environment" changes, e.g. someone enters the working area of the robot while it is moving.
