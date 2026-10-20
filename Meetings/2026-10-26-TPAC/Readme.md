# Autonomous Agents on the Web TPAC Meeting

## Logistics

- Location: Clayton Hotel Burlington Road, Dublin, Ireland and online
- Online link: https://www.w3.org/events/meetings/d5d8738b-a68b-41fa-81e0-87170a8de54b/

## The Web as a Platform for Agents (Oct. 26, 09:00–12:30 Dublin time)

Two 90-minute slots with a 30-minute coffee break in between.

### 09:00–10:30 — Meeting slot 1

- 5 min: Introduction to the WebAgents CG (Ege Korkan)
- 25 min: Placing the Web into the Agentic Web (Rem Collier)
  - Overview of what underlies the different approaches today, and to what extent the Web is used ([Summary Table](https://w3c-cg.github.io/webagents/TaskForces/Interoperability/Reports/report-interoperability.html#state-of-web-based-multi-agent-systems))
  - The Web as a Platform for Agents: Architectural design ideas from the Interop Report
    - Core tenet: hypermedia environments as a design space to support openness for agents on the Web
- 20 min: Web of Things (WoT) WG/CG: The WoT and the Agentic Web (Ege Korkan)
  - Initiatives related to Agentic AI based on W3C WoT recommendations
  - Outlook: Manageable affordances for AI Agents
- 40 min: Open discussion

#### Session details

Open discussion target: Agent-Environment interaction, tool discovery and use.

### 10:30–11:00 — Coffee break

### 11:00–12:30 — Meeting slot 2

- 10 min: Interaction Protocols: motivation for hypermedia and the potential conceptual shift towards using the Web as more than a transport layer (Andrei Ciortea)
- 20 min: AI Agent Protocol CG: Progress on Protocol, Whitepaper, Use Cases and Demo (Song Xu & Gaowei Chang)
- 20 min: Interaction-Oriented Standards for Multiagentic AI (Amit Chopra)
- 40 min: Open discussion (Moderator: Rem Collier)

#### Session details

**Title**

AI Agent Protocol CG: Progress on Protocol, Whitepaper, Use Cases and Demo

**Abstract**

We present the latest achievements from the AI Agent Protocol CG in the last six months, covering protocol design, whitepaper, practical use cases and live demo. Integration of Decentralized Identifiers (DID) and verifiable credentials into the protocol stack, which delivers a native trust layer. We discuss how APCG’s agent protocol design works align with and support WebAgents CG to advance the agentic Web.

**Speakers**

- Song Xu — APCG Co-chair; Director, China Mobile
- Gaowei Chang — APCG Co-chair; Founder, ANP Open-source Community

---

**Title**

Interaction-Oriented Standards for Multiagentic AI

**Abtract**

Agentic AI has led to a resurgence of interest in multiagent
interaction protocols. Several multiagent protocol specification and
standardization efforts are currently underway. Some, as exemplified
by A2A, address infrastructure for multiagent systems. Others,
exemplified by the Universal Commerce Protocol (UCP), address domains
involving autonomous principals.  Although guided by the right
motivations, protocols in these efforts suffer from several
limitations.

1. They are informally specified, which hinders verification and
correct implementation.
2. They are inflexible, which means they can't exploit the flexible
reasoning of LLMs.
3. They suffer from an inadequate conception of multiagent interaction.

My purpose in this talk is to surface foundational requirements for
multiagent interaction protocols.  To do this, I will draw upon
Interaction-Oriented Programming (IOP), a formal, declarative approach
that enables specifying flexible protocols, verifying them, and
implementing compliant agents.  Unlike traditional approaches, IOP is
motivated by interaction semantics, broadly, the idea that
interactions change the normative state of the world.  Thus, IOP can
provide a suitable basis for flexible and safe reasoning about actions
by LLM agents.

IOP is backed by running code and its languages (e.g., BSPL, Langshaw,
and Cupid) are amenable to standardization. In other words, an
IOP-based standard would be a metastandard that stakeholders in
various domains could apply to formalize interactions in their
specific domains.


**Speakers**

- Amit K. Chopra — Lancaster University

Amit Chopra is a Senior Lecturer at Lancaster University in the UK. He
holds a PhD in Computer Science (2008) from North Carolina State
University.

Amit is a co-founder of Interaction-Oriented Programming, an approach
that enables the development of decentralized multiagent systems and
that combines insights from software engineering, systems, and AI.
His research has been published in AI conferences such as AAMAS,
IJCAI, and AAAI and journals as AIJ, JAIR, and JAAMAS. Software
implementations of his work are available at https://gitlab.com/masr

Amit serves on the Board of Directors of the International Foundation
for Autonomous Agents and Multiagent Systems (IFAAMAS); on the
Steering Committee of the Engineering Multiagent Systems Workshop; and
on the Editorial Board of JAIR.  He also co-leads the W3C WebAgents
CG's newly-constituted task force on multiagent interactions.  Amit
has given several tutorials and invited talks.  His research has been
funded by the UKRI and the EU.

---

Open discussion target: Agent-to-Agent interaction on the Web and a roadmap for an Interaction Task Force.

## Scratchpad for Meeting Topics

Below is a list of topics that can be part of TPAC. We will move them to the sessions if they are confirmed.

- Presentation of the Interoperability Report. Possibly breakout
  - Update to TPAC25 breakout
  - Progress and what are new standards, aspects that we found out
- Interaction Protocols
  - Web and AI IG, joint breakout session? 
- Revisiting the work around manageable affordances
  - Everything here is for the joint session with WoT WG
  - Participating in the WoT Plugfest to show hands-on results
    - To Do: What are the scenarios to show there?
  - To Do: Summary of the use cases submitted and the topics below. A simple readme like a Manifesto to be sent before TPAC to the potential participants.
  - Topic 1: Going beyond synchronous user assistant flows
    - Showing a summary of the following:
      - https://emas-workshop.github.io/2026/papers/050_S-ORA_Situated_Reasoning_and_Asynchronous_Tool_Use_for_Langu.pdf
      - https://arxiv.org/abs/2602.11964
      - One more reference coming
    - Where the Agentic Systems are moving towards Manageable Affordances, how WoT can help.
- "Web Environments for Agentic AI”
  - Insight into Interoperability Report and mention of WoT
  - Relating existing approaches to it (if they don't already adopt it)
  - Pitching some plugfest scenarios for hands-on tests (WoT WG is doing a plugfest at the same time)
  - Interaction Protocols
  - What are potential contributions to "WoT Primer and Best Practices"
    - `WoT Primer and Best Practice: Document supporting developers in designing WoT‑based applications, including the combination of AI techniques and tooling (e.g, AI Agents and MCP)`
    - Informative Deliverable
    - https://w3c.github.io/wot/charters/wot-wg-2025-draft.html
    - What are the properties of a protocol needed to support agentic systems

## Breakout Session

Topic ideas:

- "What is the role of the Web in Agentic Web"
- Environment Design/Engineering, Representing the Environment, Symbolic AI, "Prompt Engineering to Context Engineering"
