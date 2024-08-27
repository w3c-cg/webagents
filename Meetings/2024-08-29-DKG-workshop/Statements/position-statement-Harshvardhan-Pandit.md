# Legal Barriers to Autonomous Agents on the Web

_Autonomous Agents_, can be defined as software that operates independent from,
but on behalf of, entities to perform specific tasks, make decisions, and
interact with humans and other agents. They represent a great degree of
advancement and innovation by opening up myriad possibilities for creating
interactive and reactive systems that can achieve more with less inputs and
time spent directly by humans as users. While recent advances in artificial
intelligence areas such as machine learning - especially large language models
(LLMs), enable advanced use of data analysis and a new level of synthetic media
generation, their use in autonomous agents is still uncertain in terms of legal
interpretations.

In addition to considering the technical challenges of implementing autonomous
agents, the legal aspects of developing, deploying, and using them must also be
considered. In this position statement, I illustrate the current state of
challenges as they relate to the known laws and why we need to develop
autonomous agents with a 'compliance-by-design' approach. I conclude with the
need to identify specific measures that autonomous agents will need to be
legally compliant, and how currently such approaches do not exist. Thus
establishing the need to undertake relevant research to develop them.

The GDPR establishes specific requirements for the use of personal data. Where
autonomous agents utilise personal data, which is quite likely when they act on
behalf of an individual (whether in personal or professional capacity) or are
interacting with individuals (e.g. as users), they will be subject to the GDPR.
This means the application of obligations such as transparency requirements
(e.g. privacy notices), accountability processes (e.g. maintaining a record of
activities), and data transfer restrictions (e.g. to third countries outside
EU/EEA) will need to be considered. Other than these, the appropriate legal
basis would need to be identified and implemented - such as asking for consent
where relevant, or creating appropriate service provision/consumption contracts
for the use of autonomous agents. Which depends on the kind of personal data
involved - for example health is a 'special category' which has specific
obligations to ensure it is not misused and is carefully handled.

In order to understand these obligations, it is imperative to first understand
who will have the role and responsibilities of a 'data controller' - the entity
under GDPR that 'determines the means and purposes' of processing. As recent
court judgements have highlighted, entities that define how a technology
functions can also become data controllers in certain circumstances. This means
that not only will the deployers of autonomous agents be responsible for them,
but that the developers would also share some responsibility, for example in
cases where the developers restrict the use of agents in specific ways to
require data be shared back to them - such as for product improvements.

The GDPR also requires specific rights to be provided to the data subjects,
which include the right to explanation for automated decision making.
Considering that autonomous agents are by decision an automated process and in
many cases would be making decisions on behalf of someone, it may be necessary
to have the capability to explain how the agent arrived at a particular
decision. The GDPR also requires provision of other rights - such as right of
access where information must be provided to the data subject regarding which
entities are processing the data and for what purposes, and where and how the
data has been shared with other entities. 

Regarding risk management, GDPR requires implementing appropriate technical and
organisational measures to safeguard the use of personal data from misuse,
breaches, corruption, and other risk sources. It also requires assessing and
conducting a 'Data Protection Impact Assessment' (DPIA) which will assess the
risks to the rights and freedoms of the individual - in this case the one the
agent is acting on behalf of or on.

All of the above means automated agents would need to be developed with the
capability to keep records of their interactions and to have the ability to act
in a manner that not only facilitates ensuring the autonomous agent is GDPR
compliant, but also to assist their users in ensuring the GDPR compliance of
the web agents and service providers they interact with. For example, if using
the agent with an external service requires some specific personal data, the
agent must be capable of assessing the validity of this request and have the
ability to exercise legal processes - such as to exercise the right of access
to ensure data is being processed as stipulated by the agent, or to conduct a
DPIA to ensure there are not risks in the use of the agent, or to request a
copy of provided data under the right to data portability.

While we have _some_ means to express this information and use it with semantic
web technologies, this is not sufficient. Standards such as [Open Digital
Rights Language (ODRL)](https://www.w3.org/TR/odrl-vocab/) exist to express
legal agreements - but by themselves they cannot be effectively used as there
is no canonical method for implementation where ODRL policies can be declared
or checked for compliance. There is also no consistency for how to represent
use-cases using ODRL - which leads to fragmented approaches and
non-interoperable data policies. The lack of practically required concepts is
addressed by the use of the [Data Privacy Vocabulary
(DPV)](https://w3id.org/dpv) and other domain specific vocabularies. However,
without their widespread use and a development of 'best practices' and common
tooling, an ecosystem based on them cannot emerge.

Finally, there is the topic of consent. Under EU laws, consent cannot be
'automated' in the sense of an autonomous agent taking the decision to provide
consent. However, no such barriers exist for the utilisation of agents to form
'contracts' - which are legally enforceable agreements. This means that we
should focus on the utilisation of contracts as much as possible to enable
agents rather than relying on consent - which is human-centric and requires
constant intervention from humans to give or withdraw it. Contract also provide
the ability to negotiate and insert reciprocal clauses whereby the agent agrees
to perform certain actions only if the other agent or human also agrees to
perform specific actions. This provides power to create agents that will only
act under the correct conditions and cannot be taken advantage of.

In conclusion, this position statement is an argument to increase the awareness
of current legal issues that must be resolved for an effective ecosystem
utilising autonomous agents to emerge. Here, the use of 'effective' refers to
the state where such agents are not limited to academic research or hobbyist
activities, but are instead adopted by commercial and non-commercial entities
and become 'mainstream'. For such an ecosystem to emerge, there must be
technical capability in tandem with legal clarity so that each entity is
assured of its duty and rights, and there is due law and procedure for cases
where there is potential misuse or discrimination. 

With the advancement of the AI Act from a proposal to law, the use of
autonomous agents will also become subject to laws specific to the use of AI
technologies. These include conducting risk assessments, fundamental rights
impact assessments, and certifying products before they can be used within the
EU. The AI Act also designates certain uses as 'high-risk', where use of AI
carries a higher level of obligations. Development and use of autonomous agents
in such cases would be subject to the AI Act, and similar to the argument made
regarding the GDPR, the agents should also consider a compliance-by-design
approach with the AI Act from the onset rather than passing on this
responsibility to the end-user entities.
