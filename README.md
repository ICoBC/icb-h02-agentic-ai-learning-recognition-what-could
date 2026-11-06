<!--
author:   ICoBC - International Council on Badges and Credentials
email:    info@icobc.net
version:  1.0.0
language: en
narrator: UK English Female
comment:  A workshop course in which learners analyse how AI agents request, hold and present credentials, assess the risks, and design controls that keep proof of achievement separate from authorisation to act.
@style
:root { --icobc-navy:#02375B; --icobc-orange:#F78222; --icobc-cyan:#5DCAE7; --icobc-lime:#B1CF37; --icobc-mist:#F1F5F8; --icobc-line:#D8E2E9; --icobc-muted:#4F6576; }
body { font-family: "Open Sans", Arial, sans-serif; }
h1, h2, h3, h4 { color: var(--icobc-navy); }
a { color: var(--icobc-navy); }
table th { background: var(--icobc-mist); color: var(--icobc-navy); }
blockquote { border-left: 4px solid var(--icobc-orange); background: var(--icobc-mist); padding: 8px 16px; }
@end
-->

# Agentic AI in Learning and Recognition: What Could Go Wrong

*Agents that request, hold and present credentials, and the controls they need.*

## About this course

**Course ID:** ICB-H02
**Framework alignment:** ICoBC Credentialing Skills Framework (ICSF), skill AIRC "Trustworthy AI in recognition", VRITE pillar Trustworthiness, level L4 "Assure", stage A "Ability".

**Who this course is for**

- L&D and corporate academy leads
- HR and learning technology owners
- Programme and micro-credential leads
- Education IT and credential operations staff
- Professional bodies and sector associations
- Standards and wallet community members

**What you will practise**

At level L4 you govern AI use in assessment and skills inference, assess regulatory classification and design oversight and delegation controls for agents. In this course you practise these skills on realistic cases in a controlled setting. You work on paper, with scenarios and templates. You do not need any live system.

**Learning outcomes**

1. Describe how AI agents can request, hold, present or act on credentials.
2. Analyse risk scenarios: fabricated credentials, persistent agent access, identity spoofing, actions beyond the mandate.
3. Design controls: holder binding, delegated and time-limited authority, audit trails, human approval.
4. Separate proof of achievement from authorisation to act.

**Workload**

The workshop has 4 hours of notional learning. This file covers the self-paced part. Live or workshop elements appear as facilitator notes.

**Prerequisite:** ICB-F07 AI Literacy for Recognition Work.

**How it is assessed**

You complete four modules with practice activities and short quizzes. The quizzes give you feedback and do not count towards the badge. The assessed task is a risk and control analysis for one agent scenario. A person marks it with the rubric in the section "Assessment and badge". There is also a final knowledge check for self-testing.

**Badge**

"Agentic AI in Learning and Recognition: What Could Go Wrong (Ability, L4)", alignment code ICSF-AIRC-L4-A. The badge evidence is your risk and control analysis. Completing the course shows that you have practised these tasks in a controlled setting. It does not prove competency in a job.

| Outcome | Module | How it is assessed |
|---|---|---|
| 1. Describe how AI agents can request, hold, present or act on credentials | Agents and credentials | Module quiz; the scenario description in the risk and control analysis |
| 2. Analyse risk scenarios | Risk scenarios | Module quiz; the risk analysis part of the assessed task |
| 3. Design controls | Controls | Module quiz; the control design part of the assessed task |
| 4. Separate proof of achievement from authorisation to act | Accountability | Module quiz; the separation statement in the assessed task |

> **Status as of November 2026; check before publishing.** Standards and rules for agent identity and delegation are still forming. This course teaches reasoning that holds as the details change. Where a fact may change, the text says so.

---

## Agents and credentials

### What an AI agent is in this course

In this course, an **AI agent** is a software system that pursues a goal on behalf of a person or organisation. It chooses its own steps, uses tools, and can act without a person approving each step. A chatbot that only answers questions is not the focus. A system that books a course, collects a certificate and submits it to an employer is.

Agentic AI in learning and recognition is the theme of the 6th ICoBC Symposium on 1 December 2026. Identity and delegation standards for agents are still forming. This means you cannot rely on a settled rulebook. You need to reason from first principles about who is acting, for whom, and with what permission.

### Four things an agent can do with a credential

A digital credential is a signed statement about a person, such as a degree, a badge or a licence. An agent can relate to credentials in four ways.

1. **Request.** The agent asks an issuer or a service for a credential on behalf of a person. Example: it applies for a course completion record after the learner finishes.
2. **Hold.** The agent keeps credentials in a store it controls. Example: an assistant that manages a learner's collection.
3. **Present.** The agent shows a credential to a verifier. Example: it submits a certificate to an employer's application portal.
4. **Act on.** The agent uses a credential to trigger a decision or an action. Example: it uses a safety certificate to book a place on a site or to unlock access to a system.

The fourth item matters most for risk. When an agent acts on a credential, a statement about the past turns into a permission in the present.

### The people and parties around the agent

Every agent scenario has at least these parties:

- the **holder**, the person the credential is about
- the **principal**, the person or organisation the agent acts for (often the holder, sometimes an employer or a provider)
- the **agent** itself, and whoever operates it
- the **issuer** of the credential
- the **verifier** who receives and checks it

Name each party before you analyse anything. Many failures begin when two roles are blurred, for example when the operator of an agent is treated as if it were the holder.

### The graphic: an agent acting for a person

The graphic shows the basic pattern used through the course. A person grants an agent a permission with a clear scope and an end time. The agent then presents a credential to a verifier. The permission is separate from the credential.

<svg viewBox="0 0 800 450" width="100%" role="img" xmlns="http://www.w3.org/2000/svg">
  <title>An agent acting for a person with a scoped, time-limited permission</title>
  <desc>A person on the left grants a delegation to an AI agent in the centre. The delegation has a scope and an end time. The agent presents a credential from an issuer to a verifier on the right. The credential and the delegation are shown as two separate items.</desc>
  <rect x="0" y="0" width="800" height="450" fill="#F1F5F8"/>
  <rect x="30" y="150" width="170" height="110" rx="6" fill="#02375B" stroke="#02375B" stroke-width="2"/>
  <text x="115" y="195" font-family="Open Sans, Arial, sans-serif" font-size="16" fill="#FFFFFF" text-anchor="middle">Person</text>
  <text x="115" y="220" font-family="Open Sans, Arial, sans-serif" font-size="14" fill="#FFFFFF" text-anchor="middle">holder and principal</text>
  <rect x="315" y="150" width="170" height="110" rx="6" fill="#FFFFFF" stroke="#02375B" stroke-width="2"/>
  <text x="400" y="195" font-family="Open Sans, Arial, sans-serif" font-size="16" fill="#02375B" text-anchor="middle">AI agent</text>
  <text x="400" y="220" font-family="Open Sans, Arial, sans-serif" font-size="14" fill="#4F6576" text-anchor="middle">acts on request</text>
  <rect x="600" y="150" width="170" height="110" rx="6" fill="#F78222" stroke="#02375B" stroke-width="2"/>
  <text x="685" y="195" font-family="Open Sans, Arial, sans-serif" font-size="16" fill="#02375B" text-anchor="middle">Verifier</text>
  <text x="685" y="220" font-family="Open Sans, Arial, sans-serif" font-size="14" fill="#02375B" text-anchor="middle">employer or service</text>
  <line x1="200" y1="205" x2="313" y2="205" stroke="#02375B" stroke-width="2"/>
  <polygon points="313,205 303,199 303,211" fill="#02375B"/>
  <line x1="485" y1="205" x2="598" y2="205" stroke="#02375B" stroke-width="2"/>
  <polygon points="598,205 588,199 588,211" fill="#02375B"/>
  <rect x="205" y="60" width="205" height="70" rx="6" fill="#B1CF37" stroke="#02375B" stroke-width="2"/>
  <text x="307" y="88" font-family="Open Sans, Arial, sans-serif" font-size="14" fill="#02375B" text-anchor="middle">Delegation</text>
  <text x="307" y="110" font-family="Open Sans, Arial, sans-serif" font-size="14" fill="#02375B" text-anchor="middle">scope + end time</text>
  <rect x="430" y="300" width="200" height="70" rx="6" fill="#5DCAE7" stroke="#02375B" stroke-width="2"/>
  <text x="530" y="328" font-family="Open Sans, Arial, sans-serif" font-size="14" fill="#02375B" text-anchor="middle">Credential</text>
  <text x="530" y="350" font-family="Open Sans, Arial, sans-serif" font-size="14" fill="#02375B" text-anchor="middle">issued by a provider</text>
  <line x1="530" y1="300" x2="530" y2="263" stroke="#02375B" stroke-width="2" stroke-dasharray="6 4"/>
  <text x="115" y="320" font-family="Open Sans, Arial, sans-serif" font-size="14" fill="#4F6576" text-anchor="middle">Grants permission</text>
  <text x="400" y="420" font-family="Open Sans, Arial, sans-serif" font-size="14" fill="#4F6576" text-anchor="middle">The delegation and the credential are two different things.</text>
</svg>

### Where the standards stand

The W3C Verifiable Credentials Data Model 2.0 is a W3C Recommendation since 2025 [Established]. It describes how credentials are structured, issued and verified. Related specifications for status lists and securing mechanisms continue to evolve. The data model tells a verifier whether a credential is genuine and who issued it. It does not, on its own, tell a verifier whether the party presenting it may act for the holder. That gap is the subject of this course.

The EUDI Wallet under eIDAS 2.0 is [Emerging]. Member States must offer at least one wallet by 24 December 2026. Germany plans its state wallet ('d-you') for 2 January 2027 with basic functions first. Regulated private sectors must accept the wallet about one year after issuance starts. Readiness varies widely between Member States. Wallets are where many agent questions will land, because a wallet holds credentials and presents them. Do not assume that a wallet will let an agent act in your country or sector yet. <!-- VERIFY: current Member State and German wallet timetable before publishing -->

**Worked example: The academy assistant**

*Context: corporate academy.* A corporate academy at a mid-sized manufacturer offers a safety-awareness course. The L&D lead, Mira, lets an assistant agent manage onboarding for new staff. The agent enrols each employee, collects their completion badge from the academy's issuing service and presents it to the facilities system to book site access.

Mapping the four relationships:

- **Request:** the agent asks the issuing service for the completion badge once the employee finishes.
- **Hold:** the agent stores the badge in the academy's learning system on the employee's behalf.
- **Present:** the agent shows the badge to the facilities system.
- **Act on:** the facilities system uses the presented badge to book site access.

Mapping the parties: the employee is the holder. The employer is the principal. The agent's operator is the learning technology team. The academy is the issuer. The facilities system is the verifier. Mira notes that the employer is the principal here, not the employee, and records this because it affects who can withdraw the permission.

**Practice activity: Map an agent to the four actions**

*Context: university.* A university programme lead, Tomas, tests an agent that helps students collect micro-credentials from three course providers and submit them to the credit recognition office.

1. List the five parties in this scenario (holder, principal, agent operator, issuer, verifier). Name one real role for each.
2. For each of the four actions (request, hold, present, act on), write one sentence describing what the agent does.
3. Mark the single point where a statement about the past turns into a permission in the present.

Compare your answer with the sample in the facilitator notes.

<details><summary>Facilitator notes</summary>

Allow 15 minutes. Participants work in pairs and then compare in plenary. A sample answer: holder is the student; principal is the student; agent operator is the university's IT service; issuers are the three providers; verifier is the credit recognition office. The turning point is the moment the recognition office grants credit because the agent presented the micro-credential. Ask groups where they placed the principal, since some will say the university. The answer depends on who instructs the agent, and the debate is useful. Remind participants that roles can differ between organisations and that clear naming is the skill being practised.

</details>

**Question 1.** Which action turns a statement about the past into a permission in the present?

[( )] The agent requests a credential from an issuer.
[( )] The agent stores a credential in a collection.
[( )] The agent presents a credential to a verifier without any decision following.
[(X)] The agent acts on a credential, for example to unlock access.
[[?]] Think about what changes in the world after the credential is used.
****
Acting on a credential means a decision or action follows from it. Requesting, holding and presenting are earlier steps. The risk grows at the point where the credential triggers something.
****

**Question 2.** In the academy example, who is the principal?

[( )] The employee, because the badge is about them.
[(X)] The employer, because it instructs the agent to run onboarding.
[( )] The issuing service, because it creates the badge.
[( )] The facilities system, because it uses the badge.
[[?]] The principal is the party the agent acts for.
****
The holder (the employee) is the subject of the credential. The principal (here the employer) is the party the agent acts for. They can be the same person or different parties, and the difference matters when permission has to be withdrawn.
****

**Question 3.** What does the W3C Verifiable Credentials Data Model 2.0 tell a verifier on its own?

[( )] Whether the presenting agent may act for the holder.
[(X)] How a credential is structured, issued and verified.
[( )] Whether the holder is competent in the job.
[( )] Which wallet each Member State must offer.
[[?]] The model concerns the credential, not the permission to present it.
****
The data model describes credential structure and verification. Authority to act for the holder is a separate question that needs its own controls, which later modules cover.
****

**Question 4.** Which statement about the EUDI Wallet is consistent with the status notes in this course?

[( )] Every Member State already has a fully working wallet that accepts agents.
[( )] Regulated private sectors must accept the wallet from 1 January 2026.
[(X)] Readiness varies widely between Member States, so agent use cannot be assumed.
[( )] The German state wallet is planned for 2024 with all functions.
[[?]] Look for the statement that is cautious about readiness.
****
Member States must offer at least one wallet by 24 December 2026, and readiness varies widely. Germany plans its wallet for 2 January 2027 with basic functions first. Check current dates before relying on them.
****

---

## Risk scenarios

### Why scenarios

Risk analysis in this course works through short scenarios. Each scenario has a trigger, a path and a harm. You describe what happens, who is affected and what would have stopped it. This module covers four risk scenarios. Every one of them involves an agent that is trusted a little more than it should be.

### Scenario 1: Fabricated credentials

An agent can produce text, images and files that look like credentials. A system built to generate documents may be asked to prepare an application, and a careless or dishonest instruction can lead it to invent a certificate or a transcript. Generative tools can also fill gaps by guessing, for example by adding a qualification that "should" be there.

Harm: a verifier accepts a fake, an employer hires on false grounds, and honest holders lose trust.

Key question: can the verifier check that a credential was signed by the issuer it names, and that it has not been revoked? A genuine verifiable credential supports that check. A PDF or an image does not.

### Scenario 2: Persistent agent access

A person gives an agent access for one task. The access is never withdrawn. Months later the agent still holds tokens, copies of credentials or a standing permission. If the agent is compromised, sold, reconfigured or simply left running, it can keep acting long after the person has forgotten the grant.

Harm: unneeded data stays exposed, and actions take place under an old permission that no one would approve today.

Key question: when does the permission end, and what removes the agent's copies?

### Scenario 3: Identity spoofing

A party pretends to be the holder, the agent, the issuer or the verifier. An attacker may present a real credential that belongs to someone else, because the credential itself is valid. Or an attacker may set up a fake agent that claims to represent a holder. In the other direction, a fake verifier may collect credentials from agents that do not check who is asking.

Harm: a valid credential is used by the wrong person, or personal data goes to the wrong party.

Key question: how does the verifier know the presenter is the holder or someone authorised by the holder? How does the agent know the verifier is genuine?

### Scenario 4: Actions beyond the mandate

The agent was asked to do one thing and does more. It was allowed to present a credential to confirm training and instead shares the full record. It was asked to apply for one course and enrols the learner in five. It uses a credential to open a door that no one meant it to open. Agents choose their own steps, so a vague instruction leaves room for steps the principal never imagined.

Harm: unwanted commitments, costs, data sharing and decisions that the principal must still answer for.

Key question: what exactly was the agent allowed to do, and what stops it from doing more?

### The graphic: four risk scenarios

<svg viewBox="0 0 800 450" width="100%" role="img" xmlns="http://www.w3.org/2000/svg">
  <title>Four risk scenarios for agents and credentials</title>
  <desc>Four labelled boxes in a two by two grid. Fabricated credentials, persistent agent access, identity spoofing and actions beyond the mandate. Each box names the question to ask. A navy circle with three open arcs in the centre stands for recognition and trust.</desc>
  <rect x="0" y="0" width="800" height="450" fill="#FFFFFF"/>
  <rect x="30" y="30" width="330" height="170" rx="6" fill="#F1F5F8" stroke="#02375B" stroke-width="2"/>
  <text x="50" y="62" font-family="Open Sans, Arial, sans-serif" font-size="16" fill="#02375B">1. Fabricated credentials</text>
  <text x="50" y="95" font-family="Open Sans, Arial, sans-serif" font-size="14" fill="#4F6576">Question: can the verifier check</text>
  <text x="50" y="117" font-family="Open Sans, Arial, sans-serif" font-size="14" fill="#4F6576">the issuer's signature and status?</text>
  <rect x="440" y="30" width="330" height="170" rx="6" fill="#F1F5F8" stroke="#02375B" stroke-width="2"/>
  <text x="460" y="62" font-family="Open Sans, Arial, sans-serif" font-size="16" fill="#02375B">2. Persistent agent access</text>
  <text x="460" y="95" font-family="Open Sans, Arial, sans-serif" font-size="14" fill="#4F6576">Question: when does the permission</text>
  <text x="460" y="117" font-family="Open Sans, Arial, sans-serif" font-size="14" fill="#4F6576">end and what is removed?</text>
  <rect x="30" y="250" width="330" height="170" rx="6" fill="#F1F5F8" stroke="#02375B" stroke-width="2"/>
  <text x="50" y="282" font-family="Open Sans, Arial, sans-serif" font-size="16" fill="#02375B">3. Identity spoofing</text>
  <text x="50" y="315" font-family="Open Sans, Arial, sans-serif" font-size="14" fill="#4F6576">Question: is the presenter the holder</text>
  <text x="50" y="337" font-family="Open Sans, Arial, sans-serif" font-size="14" fill="#4F6576">or authorised by the holder?</text>
  <rect x="440" y="250" width="330" height="170" rx="6" fill="#F1F5F8" stroke="#02375B" stroke-width="2"/>
  <text x="460" y="282" font-family="Open Sans, Arial, sans-serif" font-size="16" fill="#02375B">4. Actions beyond the mandate</text>
  <text x="460" y="315" font-family="Open Sans, Arial, sans-serif" font-size="14" fill="#4F6576">Question: what exactly was the agent</text>
  <text x="460" y="337" font-family="Open Sans, Arial, sans-serif" font-size="14" fill="#4F6576">allowed to do?</text>
  <circle cx="400" cy="225" r="34" fill="#02375B"/>
  <path d="M 372 205 A 34 34 0 0 1 428 205" fill="none" stroke="#B1CF37" stroke-width="2" transform="translate(0,-14)"/>
  <path d="M 440 215 A 40 40 0 0 1 440 237" fill="none" stroke="#F78222" stroke-width="2"/>
  <path d="M 366 240 A 40 40 0 0 0 380 258" fill="none" stroke="#5DCAE7" stroke-width="2" transform="translate(-2,0)"/>
</svg>

### A simple way to write a scenario

Use four lines for each scenario you analyse:

- **Trigger:** what starts it
- **Path:** the steps from trigger to harm
- **Harm:** who is affected and how
- **Stop point:** the earliest point where a control would have stopped it

The stop point is the bridge to the next module. A good analysis ends with a place where a control belongs.

**Worked example: The leftover access at the training provider**

*Context: university, college or training provider.* A training provider runs an evening programme. Its programme lead, Aisha, allowed a student's assistant agent to collect a completion certificate once. The agent kept a standing token with the provider's student portal. Eight months later the student changed jobs and stopped using the assistant. The assistant service was later taken over by another operator who reconfigured it.

- **Trigger:** a one-time grant with no end date.
- **Path:** the token stays valid, the agent service changes hands, the new operator's system still holds the token and can read the student's records.
- **Harm:** the student's study records are exposed to a party the student never chose.
- **Stop point:** the grant should have ended when the certificate was collected. A time limit or an end-of-task revocation would have stopped it. A review of active agent permissions would have found it later.

Aisha also notes a second stop point: the portal could have shown the student a list of active agent permissions.

**Practice activity: Analyse a scenario from the HR department**

*Context: HR department.* An HR team, led by Jonas, uses an agent to check that contractors hold a valid first-aid certificate before they start on site. The agent receives certificates from contractors' own assistants and records "valid" in the HR system. One contractor's assistant sends a certificate that belongs to a colleague of the same name.

1. Which of the four scenarios does this match best? Could more than one apply?
2. Write the four-line analysis: trigger, path, harm, stop point.
3. Name one question the agent should have asked before recording "valid".

<details><summary>Facilitator notes</summary>

Allow 20 minutes. This case is mainly identity spoofing (a valid credential presented by the wrong person), but participants may also point to actions beyond the mandate if the agent was only meant to check validity and not to update HR records. Accept both if the reasoning is clear. The central point is that a genuine signature proves who issued the credential, not who is presenting it. A good stop point is a check that links the credential to the contractor, which Module 3 calls holder binding. Collect two or three stop points on a flipchart for use in Module 3.

</details>

**Question 1.** A generative tool adds a qualification to an application because it "should" be there. Which scenario is this?

[(X)] Fabricated credentials
[( )] Persistent agent access
[( )] Identity spoofing
[( )] Actions beyond the mandate
[[?]] The credential did not exist before the agent produced it.
****
The agent invented content that looks like a credential. A verifier that can check the issuer's signature and status would reject it.
****

**Question 2.** A one-time grant is never withdrawn and the agent service changes hands. Which scenario is this?

[( )] Fabricated credentials
[(X)] Persistent agent access
[( )] Identity spoofing
[( )] Actions beyond the mandate
[[?]] The problem is how long the permission lasts.
****
The permission outlived the task. The stop point is an end time or a revocation at the end of the task.
****

**Question 3.** An agent presents a real, valid certificate that belongs to someone else. What does this show?

[( )] The certificate was fabricated.
[( )] The issuer's signature must be wrong.
[(X)] A valid credential can still be presented by the wrong party.
[( )] The agent exceeded its mandate by definition.
[[?]] Ask what a valid signature does and does not prove.
****
A valid signature shows who issued the credential. It does not show that the presenter is the holder. Linking presenter and holder is a separate control.
****

**Question 4.** An agent allowed to confirm training shares the learner's full record. Which scenario is this?

[( )] Fabricated credentials
[( )] Persistent agent access
[( )] Identity spoofing
[(X)] Actions beyond the mandate
[[?]] The agent did more than it was asked.
****
The agent stepped outside what it was allowed to do. A narrow scope, such as "confirm completion only", would have limited the action.
****

**Question 5.** What is the "stop point" in a scenario analysis?

[( )] The moment the harm is discovered.
[(X)] The earliest point where a control would have stopped the harm.
[( )] The point where the agent finishes its task.
[( )] The point where the issuer revokes the credential.
[[?]] It points forward to controls.
****
The stop point is the earliest place where a control belongs. It leads directly to control design.
****

---

## Controls

### From risk to control

Each risk scenario has stop points. A **control** is a rule, check or technical feature placed at a stop point. This module covers four controls: holder binding, delegated and time-limited authority, audit trails and human approval. No single control is enough. They work in layers.

### Holder binding

**Holder binding** links a credential to the person it was issued to, so that a verifier can tell the presenter is the holder or someone the holder has authorised. A credential about a person can be presented by anyone who holds a copy unless something ties the presentation to the holder. Binding can use a key held by the holder, a wallet that proves control, or a check against an identity record. The detail depends on the system and on the standards in use, which are still forming for agents.

For an agent, there are two questions: is the holder behind this presentation, and has the holder authorised this agent? Holder binding answers the first. Delegation answers the second.

Controls to consider:

- The verifier asks for proof of control, not only a copy.
- The credential carries the holder's identifier and the verifier checks it against the presenter.
- High-value credentials are never accepted from an agent without a second check.

### Delegated and time-limited authority

**Delegation** is the holder or principal giving an agent permission to act. A good delegation has these parts:

- **Who:** the named agent and its operator
- **For whom:** the holder or principal
- **What:** the allowed actions, for example "present the completion badge for course X to verifier Y"
- **Limits:** what is excluded, for example "no sharing of other records"
- **Until when:** an end time or an end event, such as "when the badge has been presented once"
- **Revocation:** how the holder or principal can withdraw it, and how fast it takes effect

The graphic in Module 1 showed delegation as a separate item from the credential. Make the delegation narrow. A narrow scope lowers the harm from actions beyond the mandate. A short life lowers the harm from persistent access.

Standards for expressing agent delegation are still forming. Where a standard is not available, record the delegation in a clear internal policy and keep it machine-checkable where you can. <!-- VERIFY: any named standards for agent delegation before adding references -->

### Audit trails

An **audit trail** is a record of what an agent did: which credential it requested, held or presented, to whom, when, under which delegation, and with what result. It lets a person answer "who did what, and was it allowed?" after the event.

A useful audit trail:

- links every action to a delegation
- records the human who granted or approved it
- cannot be altered by the agent itself
- is kept for a stated period and protected as personal data
- can be read by the holder

Keep the record to what you need. An audit trail that copies full credentials into a log creates a new store of personal data.

### Human approval

**Human approval** means a person confirms before the agent acts. You do not need it for every step. Use it where the action is hard to undo, has legal or financial effect, shares sensitive data or falls outside the usual pattern.

A simple test: would the principal want to know before this happens? If yes, ask. Design the request so that the person sees what will happen in plain words, not a code. An approval that nobody reads protects nobody. If approvals arrive too often, people click through them, so keep them for the moments that matter.

### Controls in layers

<svg viewBox="0 0 800 450" width="100%" role="img" xmlns="http://www.w3.org/2000/svg">
  <title>Four layered controls around an agent action</title>
  <desc>Four labelled layers from left to right that an agent request passes: holder binding, delegated and time-limited authority, human approval, and audit trail. Each layer shows the question it answers. The final layer records the result.</desc>
  <rect x="0" y="0" width="800" height="450" fill="#F1F5F8"/>
  <rect x="20" y="130" width="170" height="190" rx="6" fill="#FFFFFF" stroke="#02375B" stroke-width="2"/>
  <text x="105" y="165" font-family="Open Sans, Arial, sans-serif" font-size="16" fill="#02375B" text-anchor="middle">Holder binding</text>
  <text x="105" y="200" font-family="Open Sans, Arial, sans-serif" font-size="14" fill="#4F6576" text-anchor="middle">Is the presenter</text>
  <text x="105" y="222" font-family="Open Sans, Arial, sans-serif" font-size="14" fill="#4F6576" text-anchor="middle">tied to the holder?</text>
  <rect x="215" y="130" width="170" height="190" rx="6" fill="#B1CF37" stroke="#02375B" stroke-width="2"/>
  <text x="300" y="158" font-family="Open Sans, Arial, sans-serif" font-size="16" fill="#02375B" text-anchor="middle">Delegation</text>
  <text x="300" y="180" font-family="Open Sans, Arial, sans-serif" font-size="14" fill="#02375B" text-anchor="middle">scoped and</text>
  <text x="300" y="202" font-family="Open Sans, Arial, sans-serif" font-size="14" fill="#02375B" text-anchor="middle">time-limited</text>
  <text x="300" y="240" font-family="Open Sans, Arial, sans-serif" font-size="14" fill="#02375B" text-anchor="middle">Is the agent</text>
  <text x="300" y="262" font-family="Open Sans, Arial, sans-serif" font-size="14" fill="#02375B" text-anchor="middle">allowed this?</text>
  <rect x="410" y="130" width="170" height="190" rx="6" fill="#F78222" stroke="#02375B" stroke-width="2"/>
  <text x="495" y="165" font-family="Open Sans, Arial, sans-serif" font-size="16" fill="#02375B" text-anchor="middle">Human approval</text>
  <text x="495" y="200" font-family="Open Sans, Arial, sans-serif" font-size="14" fill="#02375B" text-anchor="middle">Would the principal</text>
  <text x="495" y="222" font-family="Open Sans, Arial, sans-serif" font-size="14" fill="#02375B" text-anchor="middle">want to know first?</text>
  <rect x="605" y="130" width="170" height="190" rx="6" fill="#5DCAE7" stroke="#02375B" stroke-width="2"/>
  <text x="690" y="165" font-family="Open Sans, Arial, sans-serif" font-size="16" fill="#02375B" text-anchor="middle">Audit trail</text>
  <text x="690" y="200" font-family="Open Sans, Arial, sans-serif" font-size="14" fill="#02375B" text-anchor="middle">Who did what,</text>
  <text x="690" y="222" font-family="Open Sans, Arial, sans-serif" font-size="14" fill="#02375B" text-anchor="middle">under which grant?</text>
  <line x1="190" y1="225" x2="213" y2="225" stroke="#02375B" stroke-width="2"/>
  <line x1="385" y1="225" x2="408" y2="225" stroke="#02375B" stroke-width="2"/>
  <line x1="580" y1="225" x2="603" y2="225" stroke="#02375B" stroke-width="2"/>
  <text x="400" y="80" font-family="Open Sans, Arial, sans-serif" font-size="16" fill="#02375B" text-anchor="middle">Agent request moves through four controls</text>
  <text x="400" y="390" font-family="Open Sans, Arial, sans-serif" font-size="14" fill="#4F6576" text-anchor="middle">Each layer answers a different question. No layer replaces another.</text>
</svg>

**Worked example: Controls for the site access agent**

*Context: corporate academy.* Back to the academy assistant from Module 1. The facilities system accepts a safety badge to book site access. The L&D lead, Mira, and the facilities owner, Pedro, design controls for the agent that presents the badge.

- **Holder binding:** the facilities system asks the presenter to prove control of the holder's key. A copy of the badge alone is not accepted.
- **Delegation:** the employee, through the onboarding policy, grants the agent: present the safety badge for course S-1 to the facilities system, for site bookings only, valid for 14 days, ends after the first booking is made, revocable by the employee or the employer at any time.
- **Human approval:** bookings for restricted areas need approval from the site manager. Ordinary bookings do not.
- **Audit trail:** the facilities system logs each booking with the delegation reference, the agent identifier and the approver where there was one. Employees can see their own entries.

Pedro asks what the controls cost in effort. Mira answers that the delegation template is written once and reused, and that the approval applies only to restricted areas, so volume stays low.

**Practice activity: Design controls for a university case**

*Context: university.* A university registry, led by Ines, allows a student's agent to submit a transcript extract and a language certificate to a partner university for an exchange application. The deadline is in three weeks. The student's agent also has access to the full transcript.

1. Write a delegation for the agent with who, for whom, what, limits, until when and revocation.
2. Decide where human approval is needed and where it is not. Give one reason for each.
3. Describe the holder binding you would ask the partner university to check.
4. List four fields you would record in the audit trail.

<details><summary>Facilitator notes</summary>

Allow 25 minutes. Give participants a blank delegation template with the six parts as rows. A strong answer limits the scope to the transcript extract and the language certificate, excludes the rest of the transcript, ends the permission on submission or at the deadline plus a short margin, and allows revocation by the student. Human approval is sensible before submission, because an application has lasting effect. It is not needed for intermediate steps such as preparing the file. Ask each group to name the weakest part of their design. Remind them that legal questions about data protection are for the university's data protection officer, and that this activity is about design reasoning.

</details>

**Question 1.** What does holder binding link?

[( )] The agent to its operator.
[(X)] The credential to the person it was issued to, as seen at presentation.
[( )] The issuer to the verifier.
[( )] The audit trail to the wallet.
[[?]] It answers whether the presenter is tied to the holder.
****
Holder binding lets a verifier check that the presenter is the holder or has been authorised by the holder. Without it, a copy of a valid credential can be presented by anyone.
****

**Question 2.** Which delegation is best designed?

[( )] "Manage my credentials."
[( )] "Act for me until I say otherwise."
[(X)] "Present my completion badge for course X to verifier Y, once, within 14 days, revocable by me."
[( )] "Present any credential needed to any verifier."
[[?]] Look for who, what, limits, end and revocation.
****
The best delegation names the action, the verifier, the limit, the end and the right to revoke. The others are open-ended and invite actions beyond the mandate and persistent access.
****

**Question 3.** What is a good use of human approval?

[( )] Every internal step the agent takes, so that nothing is missed.
[(X)] Actions that are hard to undo, have lasting effect or share sensitive data.
[( )] Only actions that the agent itself flags as risky.
[( )] Never, because it slows the agent down.
[[?]] Think about where a person's attention is worth most.
****
Approval is most useful for hard-to-reverse or sensitive actions. Asking for every step leads people to click through without reading. The agent should not be the only judge of what is risky.
****

**Question 4.** Which audit trail is best?

[( )] A log that copies the full credential for every action.
[( )] A log the agent can edit to correct mistakes.
[(X)] A log linking each action to a delegation, the agent and any approver, readable by the holder.
[( )] No log, to reduce personal data.
[[?]] Useful, protected and limited to what is needed.
****
A good audit trail links actions to their authority and can be read by the holder. It should be protected from the agent and should not duplicate more personal data than necessary.
****

**Question 5.** Which control best reduces persistent agent access?

[( )] Holder binding
[(X)] A time limit or end event on the delegation, with revocation
[( )] A longer audit retention period
[( )] A more detailed credential schema
[[?]] Which control sets an end to the permission?
****
A delegation with an end time or event, and a way to revoke it, directly limits how long an agent can act. The other controls help in other ways but do not end the permission.
****

---

## Accountability

### Proof of achievement and authorisation to act

A credential is **proof of achievement**. It says that a person completed a course, passed an assessment or holds a licence. It is evidence about the past.

**Authorisation to act** is permission to do something now. It says that a party may book a room, sign a form, enrol someone or open a door.

These two things are different. A person can hold a safety badge and still not be allowed on site this week. An agent can hold a valid badge and still not be allowed to present it. A verifier that treats the credential as permission, or treats an agent's possession of a credential as permission to act for the holder, has merged two questions into one.

Keep them apart in design:

- Ask of the credential: is it genuine, current and issued by a suitable issuer?
- Ask of the authority: who gave this party permission, for what, until when?
- Ask of the decision: does the achievement meet the rule, and is the party allowed to act on it?

A badge also does not prove that a person is competent in a job. It records what the issuer assessed under the issuer's criteria. Decisions that rely on it need their own rules.

### Who is accountable

When an agent acts, a person or organisation must still answer for it. Accountability does not move to the agent. For each action, you should be able to name:

- the **principal**, who gave the instruction
- the **operator**, who runs the agent and its technical controls
- the **verifier** or **issuer** whose decision relied on the agent's action
- the **owner of the control**, who maintains delegation rules, approvals and audit logs

Write these roles down before deployment. In many organisations the question "who is responsible when the agent gets it wrong?" has no clear answer until something goes wrong. Your task at level L4 is to make sure the answer exists before.

### Regulatory classification

Part of governing AI use is asking which rules apply. AI used in assessment, in access to education or in decisions about people at work may fall into regulated categories in some jurisdictions. Whether a given agent does depends on its purpose, its effect on people and the applicable law. Do not decide this alone. Involve legal, data protection and compliance colleagues, and record the outcome of the assessment and the reasons. <!-- VERIFY: applicable regulation and risk categories for the learner's jurisdiction before publishing -->

For credential agents, useful questions are:

- Does the agent influence a decision about a person's access, hiring, progression or recognition?
- Does it infer skills from data and present the result as a credential-like claim?
- Does it process personal data, and under which legal basis?
- Which person can review and overturn what the agent did?

### Overseeing in practice

Oversight is a routine, not an event. A simple rhythm:

- **Before launch:** write the scenario analysis, delegation template and approval rules. Get sign-off from the owner of the control.
- **In operation:** sample the audit trail, review active delegations, check that approvals are being read.
- **After an incident:** trace the action through the audit trail, find the stop point that failed, change the control and tell affected people.
- **On a schedule:** re-run the risk analysis when the agent, the verifier or the standards change. Standards for agents are still forming, so expect to revisit.

### The graphic: separating proof from permission

<svg viewBox="0 0 800 450" width="100%" role="img" xmlns="http://www.w3.org/2000/svg">
  <title>Proof of achievement and authorisation to act are separate questions</title>
  <desc>Two columns. The left column, proof of achievement, is about the past and is answered by the credential and its issuer. The right column, authorisation to act, is about the present and is answered by a delegation or a rule. A decision box below combines both answers and names an accountable person.</desc>
  <rect x="0" y="0" width="800" height="450" fill="#FFFFFF"/>
  <rect x="40" y="40" width="340" height="190" rx="6" fill="#5DCAE7" stroke="#02375B" stroke-width="2"/>
  <text x="210" y="75" font-family="Open Sans, Arial, sans-serif" font-size="16" fill="#02375B" text-anchor="middle">Proof of achievement</text>
  <text x="210" y="110" font-family="Open Sans, Arial, sans-serif" font-size="14" fill="#02375B" text-anchor="middle">About the past</text>
  <text x="210" y="140" font-family="Open Sans, Arial, sans-serif" font-size="14" fill="#02375B" text-anchor="middle">Genuine, current, suitable issuer</text>
  <text x="210" y="170" font-family="Open Sans, Arial, sans-serif" font-size="14" fill="#02375B" text-anchor="middle">Answered by the credential</text>
  <rect x="420" y="40" width="340" height="190" rx="6" fill="#B1CF37" stroke="#02375B" stroke-width="2"/>
  <text x="590" y="75" font-family="Open Sans, Arial, sans-serif" font-size="16" fill="#02375B" text-anchor="middle">Authorisation to act</text>
  <text x="590" y="110" font-family="Open Sans, Arial, sans-serif" font-size="14" fill="#02375B" text-anchor="middle">About the present</text>
  <text x="590" y="140" font-family="Open Sans, Arial, sans-serif" font-size="14" fill="#02375B" text-anchor="middle">Who, what, until when</text>
  <text x="590" y="170" font-family="Open Sans, Arial, sans-serif" font-size="14" fill="#02375B" text-anchor="middle">Answered by a delegation or rule</text>
  <line x1="210" y1="230" x2="210" y2="290" stroke="#02375B" stroke-width="2"/>
  <line x1="590" y1="230" x2="590" y2="290" stroke="#02375B" stroke-width="2"/>
  <line x1="210" y1="290" x2="590" y2="290" stroke="#02375B" stroke-width="2"/>
  <line x1="400" y1="290" x2="400" y2="310" stroke="#02375B" stroke-width="2"/>
  <rect x="220" y="310" width="360" height="100" rx="6" fill="#02375B" stroke="#02375B" stroke-width="2"/>
  <text x="400" y="348" font-family="Open Sans, Arial, sans-serif" font-size="16" fill="#FFFFFF" text-anchor="middle">Decision by a named person</text>
  <text x="400" y="378" font-family="Open Sans, Arial, sans-serif" font-size="14" fill="#FFFFFF" text-anchor="middle">Both answers are needed</text>
</svg>

**Worked example: The recognition decision at a college**

*Context: university, college or training provider.* A college offers credit for prior learning. A student's agent submits a professional micro-credential to the recognition office. The officer, Sara, reviews it.

- **Proof of achievement:** Sara checks that the micro-credential is genuine, not revoked and from an issuer the college accepts for this subject. These checks pass.
- **Authorisation to act:** Sara checks the delegation. The student authorised the agent to submit this micro-credential, once, until 30 days from the grant. The submission is inside the window and the scope.
- **Decision:** Sara decides whether the micro-credential meets the college's credit rule for the module. She records her name, the date, the delegation reference and her reasoning. The agent's presentation did not decide anything. Sara did.

Sara notes that if the delegation had expired, she would pause the case and ask the student to confirm, even though the micro-credential itself was valid.

**Practice activity: Separate proof from permission in an HR case**

*Context: HR department.* An HR system lets an agent apply on a manager's behalf for a restricted-access training programme. The agent holds the manager's leadership badge and presents it. The programme owner accepts the badge and enrols the manager. Later it turns out that the manager had not asked for the programme and the agent had been told "find development options".

1. State what the badge proves and what it does not prove.
2. State which authorisation was missing.
3. Name the accountable principal, operator and decision maker.
4. Write one change to the process so that proof and permission are checked separately.

<details><summary>Facilitator notes</summary>

Allow 20 minutes. Expected answers: the badge proves that the manager completed the leadership programme under the issuer's criteria. It does not prove that the manager wanted this enrolment or that the agent was allowed to enrol. The missing authorisation is a scoped delegation naming the programme, or a human approval from the manager before enrolment. The principal is the manager (or HR, if HR instructed the agent; discuss which). The operator is the learning technology owner. The decision maker is the programme owner who accepted the application. A good change is a required approval step by the manager before any enrolment. Use the discussion to show how an open instruction such as "find development options" leads to actions beyond the mandate.

</details>

**Question 1.** Which statement separates proof from permission correctly?

[( )] A valid credential gives its presenter permission to act.
[( )] An agent holding a credential may act for the holder.
[(X)] A credential shows what was achieved. Permission to act comes from a delegation or rule.
[( )] A badge proves competency in a job.
[[?]] One concerns the past, the other the present.
****
A credential is evidence about the past. Authorisation to act is granted separately, with a scope and an end. A badge records what the issuer assessed. It does not prove job competency.
****

**Question 2.** When an agent's action leads to a harmful decision, who is accountable?

[( )] The agent, because it acted.
[(X)] Named people and organisations: the principal, operator, decision maker and control owner.
[( )] Nobody, because agents act on their own.
[( )] Only the issuer of the credential.
[[?]] Accountability stays with people and organisations.
****
Responsibility does not pass to the agent. Name the principal, operator, decision maker and control owner in advance so that the answer exists before an incident.
****

**Question 3.** What is the best first step when assessing whether an agent falls under regulation?

[( )] Assume it does not apply because the agent only presents credentials.
[( )] Rely on the vendor's claim.
[(X)] Describe its purpose and effect on people, then involve legal, data protection and compliance colleagues.
[( )] Wait for a complaint.
[[?]] The assessment starts from purpose and effect.
****
Classification depends on what the agent does and how it affects people, under the law that applies. Specialist colleagues should take part, and the outcome and reasons should be recorded.
****

**Question 4.** In the college example, who made the recognition decision?

[( )] The student's agent.
[( )] The issuer of the micro-credential.
[(X)] The recognition officer, who recorded the reasoning and the delegation reference.
[( )] The wallet.
[[?]] A person weighed both answers.
****
The agent presented the credential. The officer checked proof and authority and made the decision, and recorded it. This keeps accountability with a named person.
****

---

## Assessment and badge

### The assessed task: Risk and control analysis for one agent scenario

You produce a written risk and control analysis for one agent scenario. A person assesses it using the rubric below. Nothing in this file grades your work.

**Choose a scenario.** Use one of the two below, or use a scenario from your own organisation with the facilitator's agreement. Remove personal data and confidential details.

*Option A: Corporate academy or HR department.* An HR team lets an agent maintain each employee's skills record. The agent collects certificates from external providers, stores them in the employee's profile, and presents them to line managers and to the project staffing tool, which uses them to assign people to projects with qualification requirements.

*Option B: University, college or training provider.* A provider lets students' assistant agents request micro-credentials, hold them in a wallet, and present them for credit recognition and for placements with partner employers. The provider's own agent also issues completion records at the end of each course.

**What to submit (about 1,000 to 1,500 words, plus any diagrams or tables you choose):**

1. **Scenario description.** Name the parties (holder, principal, operator, issuer, verifier). Describe how the agent requests, holds, presents and acts on credentials. State what the agent is allowed to do. (Outcome 1)
2. **Risk analysis.** Analyse the four risks: fabricated credentials, persistent agent access, identity spoofing, actions beyond the mandate. For each, give trigger, path, harm and stop point. Say which risks matter most in your scenario and why. (Outcome 2)
3. **Control design.** Design holder binding, delegated and time-limited authority, audit trail and human approval. Include a completed delegation with who, for whom, what, limits, until when and revocation. Link each control to a stop point. (Outcome 3)
4. **Separation statement.** Explain what the credentials in your scenario prove, what authorisation the agent needs, who grants it and who decides. Name the accountable people. Note any regulatory classification question you would raise and with whom. (Outcome 4)
5. **Open points.** List what you could not verify and what you would check, including any standards or wallet readiness that may change. <!-- VERIFY: ensure learners date their open points against current standards status -->

<details><summary>Facilitator notes</summary>

Plan 45 to 60 minutes of workshop time for the task, with the remainder of the submission completed afterwards within the period you set. Run a short peer review in pairs: each reader checks that the stop points in section 2 are matched by controls in section 3. Assessors use the rubric below and record a level per criterion with short comments. Make sure assessors apply the same standard, for example with a calibration round on one sample analysis. Remind learners that the analysis is a practice task in a controlled setting and that completing it does not prove job competency.

</details>

### Rubric

| Criterion | Not yet met | Met | Strongly met |
|---|---|---|---|
| Scenario description (Outcome 1) | Parties missing or confused; agent actions unclear | All parties named; requesting, holding, presenting and acting on credentials described correctly | Parties, flows and the scope of the agent's mandate are precise; points of risk are already visible |
| Risk analysis (Outcome 2) | Fewer than four risks, or no stop points | All four risks analysed with trigger, path, harm and stop point | Risks are specific to the scenario, ranked with reasons, and stop points are the earliest realistic ones |
| Control design (Outcome 3) | Controls are generic or missing; no usable delegation | All four controls designed; delegation has all six parts; controls linked to stop points | Controls are layered, proportionate and practical; trade-offs (effort, approval volume, data in logs) are discussed |
| Proof and authorisation (Outcome 4) | Credential treated as permission, or accountability unclear | Proof and permission separated; accountable people named; classification question raised | Separation is applied to each decision in the scenario; oversight routine and review triggers are described |
| Clarity and honesty | Hard to follow; unsupported claims | Clear structure; claims limited to what is known; open points listed | Concise and well organised; uncertainty about standards stated and dated |

### Pass rule

To earn the badge, you need a rating of "Met" or "Strongly met" on all five criteria. If a criterion is "Not yet met", you may revise and resubmit once within the period set by the facilitator. The assessor records the decision and a short justification.

### Evidence submitted for the badge

- Your risk and control analysis (the document described above)
- The completed delegation template
- The assessor's rubric record

The badge is "Agentic AI in Learning and Recognition: What Could Go Wrong (Ability, L4)", alignment code ICSF-AIRC-L4-A. It records that you practised these tasks on a realistic case in a controlled setting. It does not prove competency in a job.

### Final knowledge check

This check supports your preparation. It does not replace the assessed task.

**Question 1.** Which list names the four ways an agent can relate to a credential in this course?

[( )] Issue, revoke, verify, archive
[(X)] Request, hold, present, act on
[( )] Create, copy, send, delete
[( )] Enrol, assess, certify, publish
[[?]] These are the four relationships from Module 1.
****
The four relationships are request, hold, present and act on. Acting on a credential carries the highest risk because a decision or action follows from it.
****

**Question 2.** An agent is asked to apply for one course and enrols the learner in five. Which scenario is this?

[( )] Fabricated credentials
[( )] Persistent agent access
[( )] Identity spoofing
[(X)] Actions beyond the mandate
[[?]] The agent did more than was allowed.
****
The agent went beyond its mandate. A delegation naming the single course and a human approval for enrolment would have limited the action.
****

**Question 3.** A verifier accepts a PDF of a certificate that looks genuine. Which weakness does this show?

[(X)] The verifier cannot check the issuer's signature or the status of a PDF.
[( )] The agent held the PDF for too long.
[( )] The holder lacked a delegation.
[( )] The audit trail was too detailed.
[[?]] What can a verifier check on an image or PDF?
****
A PDF or image offers no signed, checkable statement. A verifiable credential lets the verifier check the issuer and the status. This is the main defence against fabricated credentials.
****

**Question 4.** A real, valid credential is presented by someone who is not its holder. Which control addresses this most directly?

[( )] A longer audit trail
[( )] A time limit on the delegation
[(X)] Holder binding
[( )] A broader scope for the agent
[[?]] Link the presentation to the holder.
****
Holder binding ties the presentation to the person the credential was issued to, or to someone the holder has authorised. A valid signature alone does not prove who is presenting.
****

**Question 5.** Which delegation limits both actions beyond the mandate and persistent access?

[( )] "Handle my learning records for as long as needed."
[( )] "Present any of my credentials to any employer."
[(X)] "Present my badge for course X to employer Y, once, within 14 days, revocable by me."
[( )] "Act for me in all recognition matters this year."
[[?]] Look for a narrow action and an end.
****
A narrow action and a clear end limit what the agent can do and how long it can do it. The revocation right gives the holder a way to withdraw it.
****

**Question 6.** When is human approval most useful?

[( )] For every step, so that no risk remains.
[( )] Only after an incident.
[(X)] For actions that are hard to undo, have lasting effect or share sensitive data.
[( )] When the agent is uncertain, and only then.
[[?]] Think about reversibility and sensitivity.
****
Approval protects best where the effect is lasting or sensitive. Too many approvals lead to click-through, and relying only on the agent to flag risk leaves a gap.
****

**Question 7.** What should a good audit trail allow?

[( )] The agent to correct its own entries.
[( )] Full copies of every credential to be stored in the log.
[(X)] People to see which action was taken under which delegation, by whom and with what result.
[( )] Only the operator to see it.
[[?]] It answers "who did what, and was it allowed?"
****
An audit trail links each action to its authority and result, and the holder should be able to read it. The agent must not be able to alter it, and it should not hold more personal data than needed.
****

**Question 8.** What is the difference between proof of achievement and authorisation to act?

[( )] They are the same when the credential is genuine.
[(X)] Proof is evidence about the past from the credential. Authorisation is permission for the present, granted by a delegation or rule.
[( )] Proof is granted by the agent. Authorisation is issued by the verifier.
[( )] Authorisation is a type of credential.
[[?]] One looks back, the other looks at what may happen now.
****
A credential says what was achieved. Permission to act must come from a separate delegation or rule, with a scope and an end.
****

**Question 9.** After an agent's action leads to harm, who answers for it?

[( )] The agent
[( )] Nobody, if the action was automated
[(X)] Named people and organisations, such as the principal, the operator, the decision maker and the control owner
[( )] Only the holder of the credential
[[?]] Accountability stays with people and organisations.
****
Accountability does not move to the agent. Name the roles in advance so that the answer is clear before an incident happens.
****

**Question 10.** Which statement about the status of wallets and standards is consistent with this course?

[( )] Agent delegation standards are settled and the same everywhere.
[( )] The EUDI Wallet is available in every Member State with full functions today.
[(X)] Identity and delegation standards for agents are still forming, and wallet readiness varies widely, so dated checks are needed.
[( )] The W3C Verifiable Credentials Data Model 2.0 covers agent delegation completely.
[[?]] Look for the answer that expects change.
****
Standards for agents are still forming, and Member States are at different stages with wallets. Treat any statement of status as dated and check it before relying on it.
****

---

## Sources and further reading

**Status as of November 2026; check before publishing.** The status of agent identity and delegation standards, EUDI Wallet timetables and related specifications can change quickly. <!-- VERIFY: all dates and status statements below before publishing -->

- W3C, *Verifiable Credentials Data Model v2.0*, W3C Recommendation. Published by the World Wide Web Consortium at w3.org. Search for the title on the W3C website for the current text and for related specifications on status lists and securing mechanisms.
- European Union, Regulation (EU) 2024/1183 amending Regulation (EU) No 910/2014 as regards establishing the European Digital Identity Framework (commonly called eIDAS 2.0), published in the Official Journal of the European Union and available on EUR-Lex. <!-- VERIFY: regulation number and citation before publishing -->
- European Commission, pages on the European Digital Identity Wallet and its implementation, available on the Commission's digital strategy website. Check the current timetable and Member State status there.
- ICoBC, *Credentialing Skills Framework (ICSF)*, International Council on Badges and Credentials, Berlin. Available from ICoBC at icobc.net.
- ICoBC, course ICB-F07 *AI Literacy for Recognition Work*, the prerequisite for this course, available in the ICoBC Kursbibliothek.
- ICoBC, programme and materials of the 6th ICoBC Symposium (1 December 2026), on agentic AI in learning and recognition. Check icobc.net for the current programme.
