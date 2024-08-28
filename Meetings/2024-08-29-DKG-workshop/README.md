# Autonomous Web Agents as Knowledge Graphs prosumers

An in-person meeting will take place on the 29th of August, 2024 in Dublin, at the same location as the EUMAS conference.
This event is organised as part of the activities of the COST Action CA19134 on [Distributed Knowledge Graphs](https://cost-dkg.eu/).

## Summary

Software agents that must interact with an open set of web resources must have machine-processable descriptions of said resources. Moreover, if they want to collaborate between them or with people online, they need to provide knowledge about themselves or about what they want, do, what they are capable of, etc. Therefore, autonomous agents should be providers and consumers of knowledge graphs distributed on the Web. This workshop should aim at discussing the design of KGs that describe actionable web resources, as well as agents, their communication interfaces, and possibly multi agent societies with their norms and rules. The workshop will also include demonstrations of implemented systems of Web agents.

## Agenda

| Time (Irish Summer Time) | Activity                                                                       |
|--------------------------|--------------------------------------------------------------------------------|
|   9:00 - 9:10            | Intro                                                                          |
|   9:10 - 10:00           | keynote: Alessandro Ricci                                                      |
|  10:00 - 10:30           | break                                                                          |
|  10:30 - 12:30           | presentations (input for a knowledge model for web agents)                     |
|  12:30 - 14:00           | Lunch                                                                          |
|  14:00 - 15:00           | demos                                                                          |
|  15:00 - 15:30           | break                                                                          |
|  15:30 - 17:30           | work on a use case: what do we need in terms of KGs to implement the use case? |
|  17:30 - 17:45           | wrap up                                                                        |

## Keynote

**Speaker:** Alessandro Ricci, Università di Bologna, Italy

**Title:** From Mirror Worlds to the Web of Digital Twins

**Summary:** In recent years, digital twins have been pervading different application domains -- from manufacturing to healthcare -- as an approach for virtualising different kinds of physical entities (things, products, machines).  The dominant view developed in the literature is being about the virtualisation of individual physical assets, in a closed-system perspective. In this talk, I will give an account of another, broader perspective - called Web of Digital Twins (WoDT) -- in which the digital twin paradigm is exploited for the pervasive softwarisation of possibly large-scale interrelated physical realities. A WoDT can be conceived as an open, distributed and dynamic ecosystem of connected digital twins, functioning as an interoperable service-oriented layer  for applications running on top, especially smart applications and multiagent systems. The WoDT idea is rooted on Gelernter's seminal work on Mirror Worlds and adopts (Distributed) Knowledge Graphs as reference approach to define an explict distributed semantic layer that agents can exploit at runtime.

## Presentations

All participants can submit a short position statement by issuing a pull request that adds a file to the directory "[Statements](https://github.com/w3c-cg/webagents/tree/main/Meetings/2024-08-29-DKG-workshop/Statements)". Additionally, everyone on site will be invited to present themselves and tell others about their interest in this workshop, or how they will contribute.

## Demos

Depending on how may tools we will have this session may be shortened to allow more time for the working session at the end.

## Use case

In order to have a concrete use case to work on during the workshop, we will focus on a very simple scenario that can be complexified easily to extend coverage.

We assume there is an autonomous vacuum cleaner that wants to clean a home every day. The occupants of the house should not have to setup a specific cleaning schedule, but the vacuum cleaner should take advantage of knowledge on the Web and possibly other agents to infer when the occupants should not be disturbed.

As a baseline, we assume the vacuum cleaner knows an entry point to a knowledge graph about the home and graphs about the occupants.

The occupants have calendars semantically describing their current and future activities (e.g., an occupant is at home and have a videoconference between 10 and 11 am).

The house may have a smart mattress that can be queried to know if a person lies on the bed. Occupants may have smart wristbands that detect sleep.
The house may be associated with a "do-not-disturb" agent that can inform other agents when to not disturb. The do-not-disturb agent may be aware of the occupants' calendars or even directly interact with the occupants to ask them if they can tolerate noise.

Other agents may exist to proactively trigger cleaning, or provide more knowledge that implies a do-not-disturb situation.

Our goal is to describe what knowledge graphs should be made available, and how, in order for the vacuum cleaner to operate without prior knowledge of the home, occupants, devices and other agents. However, some assumptions will have to be made and encoded in the vacuum cleaner agent, such as knowledge of the vocabularies.

## Expected output

Some contributions that we can envisioned: list of existing ontologies that can be used for the scenario; additional ontology requirements; draft of ontologies; architecture for the publication and sharing of knowledge; additional requirements, rules, norms, etc to make the overall system more robust and generic.

## Attendance-type

In-person.

## Date

29th of August, 2024.

## Where

University College Dublin, Ireland. [School of Computer Science](https://www.openstreetmap.org/way/23653391#map=18/53.308973/-6.223916), room B1.06, first floor. There will be signposts.

## Funding

COST is providing financial support for the event, and only people who have been formally invited can get reimbursement for their expenses. If you think you can contribute and would like to be invited, please fill in the [registration form](https://framaforms.org/participation-to-cost-action-dkg-meeting-on-web-agents-1712069231) and make sure you have an [e-Cost](https://e-services.cost.eu/) account (you can create one for free).
