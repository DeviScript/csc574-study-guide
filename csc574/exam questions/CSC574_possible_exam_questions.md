# CSC/ECE 574 Possible Exam Questions

Based on:
- *2024 Human-Centered Security Midterm*
- *2024 Human-Centered Security Final*
- *CSC/ECE 574 Fall 2026 Exam Information & Learning Objectives*

The older Human-Centered Security exams are used primarily as a guide to the instructor's **question style and structure**, while the Fall 2026 CSC/ECE 574 guide is used for the **actual course topics and learning objectives**.

The exam guide indicates that likely questions will include:
- short written answers ranging from 1–2 words to 2–3 sentences;
- "Quick Questions" spanning multiple lecture areas;
- scenario-based application and analysis;
- concise comparisons and explanations;
- possible sketching or labeling of diagrams;
- higher-level tasks involving analysis, evaluation, and creation.

---

## Task 1 — Quick Questions

1. What does CIA stand for in the CIA triad?

2. Define confidentiality in one sentence.

3. Define integrity in one sentence.

4. Define availability in one sentence.

5. What is an asset in a security model?

6. What is a vulnerability?

7. What is a threat?

8. What is an attack?

9. What is a defense?

10. What does TCB stand for?

11. What is an adversary?

12. What is a participant in a security model?

13. What is meant by trust in a security model?

14. What is the difference between a threat and an attack?

15. What is the difference between a vulnerability and a threat?

16. What is the difference between trusted and trustworthy?

17. What is a security model?

18. What other models/components make up a security model?

19. Does a participant in a security model have to be a human? Explain briefly.

20. What is the principle of adequate protection?

---

## Task 2 — CIA Triad and Security Fundamentals

### Possible Question 21

For each scenario below, identify whether confidentiality, integrity, availability, or multiple CIA properties are primarily affected. Briefly justify each answer.

a. An attacker reads a company's private customer database.

b. Malware modifies students' grades in a university database.

c. A DDoS attack prevents users from accessing a banking website.

d. Ransomware encrypts all files stored on a company's servers.

e. An attacker both steals and modifies medical records.

### Possible Question 22

A company's payroll database is accidentally published on the public internet. Which security property has been violated? Explain in 1–2 sentences.

### Possible Question 23

An attacker changes the destination account number in an online bank transfer without preventing the transfer itself. Which component of the CIA triad is primarily violated? Why?

### Possible Question 24

A server is perfectly protected against unauthorized disclosure and modification but crashes every few minutes. Is the system secure according to the CIA model? Explain.

---

## Task 3 — Threats, Vulnerabilities, Attacks, and Defenses

### Possible Question 25

Consider this scenario:

> An employee uses the password `password123` for a company account. An attacker guesses the password and downloads confidential customer records.

Identify each of the following:

- Asset
- Vulnerability
- Threat/adversary
- Attack
- Security property affected
- One possible defense

### Possible Question 26

Is a broken window in a server room a threat, vulnerability, attack, or something else? Briefly explain your classification.

### Possible Question 27

Explain the relationship between a vulnerability, threat, and attack using one concrete example.

### Possible Question 28

A web application contains a SQL injection vulnerability, but nobody has attempted to exploit it. Has an attack occurred? Explain.

### Possible Question 29

A company fixes a software vulnerability immediately after discovering it. Does eliminating the vulnerability necessarily eliminate every threat to the system? Why or why not?

---

## Task 4 — Attack Archetypes

> Use the exact names and terminology for the attack archetypes from your course lecture notes.

### Possible Question 30

List and briefly define the four attack archetypes discussed in lecture.

### Possible Question 31

For each of the following scenarios, identify the most appropriate attack archetype and explain your choice.

a. An attacker silently copies confidential files.

b. An attacker changes entries in a database.

c. An attacker prevents legitimate users from accessing a service.

d. An attacker impersonates another user.

### Possible Question 32

Can a single attack belong to more than one attack archetype? Give an example and explain.

### Possible Question 33

An attacker gains access to a company's servers and deploys ransomware that encrypts its files, interrupting every service that depends on them. Which attack archetype or archetypes apply? Explain briefly.

---

## Task 5 — Defense Archetypes

> Use the exact names and terminology for the defense archetypes from your course lecture notes.

### Possible Question 34

List three of the five defense archetypes discussed in lecture and briefly define each.

### Possible Question 35

For a phishing attack against employee credentials, identify two possible defense archetypes and describe how each could be implemented.

### Possible Question 36

Scenario:

> An organization is experiencing repeated unauthorized login attempts against employee accounts.

Provide two defenses from different defense archetypes. For each, explain how it changes the attacker's ability to compromise an account.

### Possible Question 37

Why might applying multiple defense archetypes be preferable to relying on a single security mechanism?

### Possible Question 38

Given an attack scenario, select the most appropriate defense archetype and justify your choice.

---

## Task 6 — Trusted vs. Trustworthy

### Possible Question 39

Explain the difference between "trusted" and "trustworthy."

### Possible Question 40

Can something be trusted without being trustworthy? Give an example.

### Possible Question 41

Can something be trustworthy without being trusted by a particular system? Explain.

### Possible Question 42

Scenario:

> You withdraw money from an ATM. The ATM's operating system controls the keypad, display, card reader, and communication with the bank.

Is the operating system trusted, trustworthy, both, or neither? Explain your answer.

### Possible Question 43

Why is minimizing the amount of trusted functionality in a system generally desirable?

### Possible Question 44

Identify one component of an ATM that must be trusted for the system's security and explain what could happen if that component were malicious.

---

## Task 7 — Trusted Computing Base

### Possible Question 45

What does TCB stand for, and what is its role in a secure system?

### Possible Question 46

Why is it desirable for a Trusted Computing Base to be small?

### Possible Question 47

Scenario:

> A system contains an operating system kernel, web browser, calculator application, authentication service, and access-control mechanism.

Which components might belong to the TCB? Explain your reasoning.

### Possible Question 48

Does every program running on a computer necessarily belong to its TCB? Why or why not?

---

## Task 8 — Building a Security Model

### Possible Question 49

Scenario:

> Consider an ATM located outside a convenience store.

Develop a basic security model for the ATM. Identify:

- important assets;
- participants;
- adversaries;
- trust assumptions;
- potential vulnerabilities;
- major threats;
- likely attacks;
- possible defenses.

### Possible Question 50

Create a security model for an online banking application. Identify at least two assets, two participants, one adversary, one trust assumption, and one threat.

### Possible Question 51

Create a security model for a university course-management system such as Moodle or Canvas. Identify the major assets, participants, and threats.

### Possible Question 52

Create a security model for a smart door lock. Who or what must be trusted for the system to provide adequate security?

### Possible Question 53

Create a security model for a password manager. Identify one important trust assumption and describe what happens if that assumption fails.

---

## Task 9 — ATM / Shoulder-Surfing Scenario

### Possible Question 54

An ATM provider rearranges the numeric keypad to make shoulder surfing more difficult. Is this an effective security defense? Discuss one benefit and one drawback.

### Possible Question 55

What security threat is the ATM provider attempting to address by changing the keypad layout?

### Possible Question 56

Propose a better defense against shoulder surfing and explain why it would be preferable to rearranging the keypad.

### Possible Question 57

How could rearranging an ATM keypad improve security while simultaneously harming usability?

---

## Task 10 — Principle of Adequate Protection

### Possible Question 58

Define the principle of adequate protection.

### Possible Question 59

Why does "maximum possible security" not necessarily represent adequate protection?

### Possible Question 60

Scenario:

> A small personal blog requires users to authenticate using a password, hardware token, biometric scan, and physical ID verification every time they leave a comment.

Does this system demonstrate adequate protection? Explain why or why not.

### Possible Question 61

How should the value of an asset and the cost of an attack influence the amount of protection applied to the asset?

---

## Task 11 — Larger Scenario Questions

### Possible Question 62 — Ransomware

A hospital's computers are infected with ransomware. Patient records become encrypted and doctors cannot access them.

Identify:

1. the primary asset;
2. the adversary;
3. at least two CIA properties affected;
4. the attack archetype(s);
5. two possible defenses.

### Possible Question 63 — Stolen Laptop

An employee's company laptop containing confidential files is stolen from their car.

Identify one relevant threat, one vulnerability, one security property at risk, and two possible defenses.

### Possible Question 64 — Malicious Administrator

A database administrator is authorized to access customer information but secretly copies the information and sells it.

Is the administrator a participant, adversary, or both within an appropriate security model? Explain.

### Possible Question 65 — Software Update

Users automatically trust software updates signed by a company's update server. An attacker compromises that server and distributes malicious updates.

Identify the important trust assumption that failed and explain the resulting security consequences.

### Possible Question 66 — Authentication Server

A university relies on one authentication server for every campus service.

Explain why the authentication server might be part of the university's TCB and identify one security consequence if it is compromised.

---

## Task 12 — Evaluate a Proposed Defense

### Possible Question 67

A company disables USB ports on every employee computer to prevent data theft. Evaluate this defense. What attack does it address, and what limitations does it have?

### Possible Question 68

A bank requires users to change their password every day. Does this necessarily make the system more secure? Explain your reasoning using the principle of adequate protection.

### Possible Question 69

An organization places all of its security controls at the network perimeter. Explain one reason this may provide insufficient protection.

### Possible Question 70

Two proposed defenses provide similar security, but Defense A greatly reduces system usability while Defense B has little effect on users. Which would you recommend and why?

---

## Task 13 — Diagram / Sketch Questions

### Possible Question 71

Sketch a simple security model showing an asset, participant, adversary, threat/attack, and defense. Label each component.

### Possible Question 72

Draw or label a diagram showing the relationship among threat, vulnerability, attack, and defense.

### Possible Question 73

Sketch the security-relevant components of an ATM and identify which components would belong to its TCB.

---

# Realistic 30-Point Practice Exam

## Task 1 — Quick Questions — 6 points

**1 point each. Answer in 1 word–1 sentence.**

a. What does TCB stand for?

b. Define integrity.

c. What is a vulnerability?

d. What is the difference between trusted and trustworthy?

e. Name one attack archetype.

f. What is the principle of adequate protection?

---

## Task 2 — Security Concepts — 4 points

### a. (2 points)

Explain the difference between a threat and an attack. Give one example.

### b. (2 points)

Explain why a participant in a security model does not necessarily have to be a human.

---

## Task 3 — Attack & Defense Analysis — 6 points

> An attacker compromises a company's server and installs ransomware. The ransomware encrypts important files and prevents customers from accessing the company's services.

### a. (2 points)

Identify and explain two security properties affected.

### b. (2 points)

Identify the relevant attack archetype(s).

### c. (2 points)

Provide one appropriate defense and briefly explain how it mitigates the attack.

---

## Task 4 — Trust and TCB — 6 points

> Consider an ATM used to withdraw money from a bank account.

### a. (2 points)

Explain whether the ATM operating system is trusted, trustworthy, or both.

### b. (2 points)

Identify two components that could belong to the ATM's TCB.

### c. (2 points)

Explain what could happen if one of those trusted components were compromised.

---

## Task 5 — Security Model — 4 points

> Consider an online banking website.

Identify:

- one asset;
- one participant;
- one adversary;
- one trust assumption.

Briefly explain each choice.

---

## Task 6 — Evaluate a Defense — 4 points

> An ATM provider rearranges its number pads to make shoulder surfing more difficult.

### a. (2 points)

Evaluate whether this is a good defense.

### b. (2 points)

Propose a better solution and explain why it would be preferable.

---

# Suggested Study Priorities

1. CIA triad.
2. Asset / participant / adversary / vulnerability / threat / attack / defense.
3. Trusted vs. trustworthy.
4. Trusted Computing Base (TCB).
5. Four attack archetypes.
6. Five defense archetypes.
7. Building a security model from a scenario.
8. Principle of adequate protection.
9. Recognizing concepts inside unfamiliar scenarios.
10. Evaluating whether a proposed defense is sensible.

For every major course concept, practice being able to:

- **define it;**
- **recognize it in a scenario;**
- **apply it;**
- **briefly justify why it applies.**

That pattern closely matches the structure emphasized in the Fall 2026 exam guide and the style used in the supplied 2024 exams.
