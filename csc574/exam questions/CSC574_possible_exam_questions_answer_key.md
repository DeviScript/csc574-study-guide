# CSC/ECE 574 Possible Exam Questions — Answer Key

This answer key corresponds to the question bank in `CSC574_possible_exam_questions.md`.

## Important note about source grounding

The Fall 2026 CSC/ECE 574 exam guide explicitly identifies these Week 1 topics:

- security terminology, goals, and measurement challenges;
- security models;
- confidentiality, integrity, and availability;
- assets, participants, vulnerabilities, threats, attacks, defenses, TCB, and risk;
- common attacker types;
- **four attack archetypes**;
- **five defense archetypes**;
- trusted vs. trustworthy;
- creation of security models;
- the principle of adequate protection.

However, the uploaded Week 1 guide **does not provide the names or definitions of the four attack archetypes, five defense archetypes, or a detailed definition of adequate protection**. Where a question depends on those exact lecture-specific terms, this key says so rather than inventing terminology.

Many of the remaining answers use standard computer-security interpretations consistent with the concepts named in the guide.

---

# Task 1 — Quick Questions

## 1. What does CIA stand for in the CIA triad?

**Answer:** Confidentiality, Integrity, Availability.

## 2. Define confidentiality in one sentence.

**Answer:** Confidentiality means preventing unauthorized disclosure of information.

## 3. Define integrity in one sentence.

**Answer:** Integrity means preventing unauthorized or improper modification or destruction of information or system state.

## 4. Define availability in one sentence.

**Answer:** Availability means ensuring authorized users can access a system, service, or information when needed.

## 5. What is an asset in a security model?

**Answer:** An asset is something of value that the system is intended to protect.

Examples include data, credentials, money, hardware, services, or reputation.

## 6. What is a vulnerability?

**Answer:** A vulnerability is a weakness that can potentially be exploited to violate a security goal.

## 7. What is a threat?

**Answer:** A threat is a potential circumstance, actor, or event that could cause harm to an asset or violate a security goal.

## 8. What is an attack?

**Answer:** An attack is an actual attempt to exploit a vulnerability or otherwise violate a system's security.

## 9. What is a defense?

**Answer:** A defense is a mechanism, policy, or action intended to prevent, detect, limit, or recover from attacks.

## 10. What does TCB stand for?

**Answer:** Trusted Computing Base.

## 11. What is an adversary?

**Answer:** An adversary is an entity whose actions or goals may conflict with the security goals of the system.

## 12. What is a participant in a security model?

**Answer:** A participant is an entity that interacts with or plays a role in the system being modeled.

A participant does **not** have to be a human; it may also be software, hardware, an organization, or another system.

## 13. What is meant by trust in a security model?

**Answer:** Trust means that the security of the system depends on an entity behaving correctly or as expected.

## 14. What is the difference between a threat and an attack?

**Answer:** A threat is the **possibility or potential source of harm**, while an attack is an **actual attempt to cause that harm**.

## 15. What is the difference between a vulnerability and a threat?

**Answer:** A vulnerability is a weakness in a system; a threat is something that could exploit that weakness and cause harm.

## 16. What is the difference between trusted and trustworthy?

**Answer:** **Trusted** means the system's security depends on the component. **Trustworthy** means there is good reason to believe the component will behave correctly and securely.

A component can therefore be trusted without actually being trustworthy.

## 17. What is a security model?

**Answer:** A security model is a structured description of the relevant system, its assets and participants, its security goals, its adversaries/threats, and the assumptions or protections on which security depends.

**Source note:** The guide explicitly asks students to define a security model and asks which other models it consists of, but the uploaded document does not provide the instructor's exact preferred definition.

## 18. What other models/components make up a security model?

**Answer:** **Use the exact decomposition from your lecture notes.**

The uploaded guide asks this question but does not provide the answer or the instructor's exact terminology.

## 19. Does a participant in a security model have to be a human?

**Answer:** No. A participant can also be software, hardware, an external service, an organization, or another technical entity.

## 20. What is the principle of adequate protection?

**Answer:** At a high level, adequate protection means applying security protections that are appropriate to the value of the asset, the threats, and the expected cost or risk rather than simply maximizing security at any cost.

**Source note:** The guide names this principle but does not provide the exact lecture definition. Use the wording from your notes if your instructor gave a more precise formulation.

---

# Task 2 — CIA Triad and Security Fundamentals

## 21. Identify the CIA property or properties affected.

### a. An attacker reads a company's private customer database.

**Answer:** Confidentiality.

Unauthorized disclosure has occurred.

### b. Malware modifies students' grades.

**Answer:** Integrity.

The information has been changed without authorization.

### c. A DDoS attack prevents users from accessing a banking website.

**Answer:** Availability.

Legitimate users cannot access the service.

### d. Ransomware encrypts all files stored on a company's servers.

**Answer:** Primarily availability, and potentially integrity depending on how the course treats unauthorized modification.

The files are no longer usable by legitimate users. Because the data representation is also modified without authorization, integrity may also be relevant.

### e. An attacker both steals and modifies medical records.

**Answer:** Confidentiality and integrity.

The records were disclosed to an unauthorized party and modified without authorization.

## 22. Payroll database published publicly

**Answer:** Confidentiality has been violated because information intended to be restricted was disclosed to unauthorized people.

## 23. Destination account number changed in a bank transfer

**Answer:** Integrity.

The transaction data was modified without authorization.

## 24. Server crashes every few minutes

**Answer:** No. Even if confidentiality and integrity are protected, availability is still part of the CIA triad. A system that authorized users cannot reliably access fails an important security property.

---

# Task 3 — Threats, Vulnerabilities, Attacks, and Defenses

## 25. `password123` scenario

### Asset

The customer records, employee account, and/or credentials.

### Vulnerability

The weak and easily guessed password.

### Threat/adversary

The attacker attempting unauthorized access.

### Attack

Guessing the password and using the compromised account to access the records.

### Security property affected

Primarily confidentiality because customer records were disclosed without authorization.

### One possible defense

Use stronger authentication, such as stronger password requirements and/or multi-factor authentication.

## 26. Broken window in a server room

**Answer:** Most naturally, the broken window is a **vulnerability** because it creates a weakness that may allow unauthorized physical access.

A person who might use that opening to enter the server room would represent a threat/adversary; actually entering through it would be part of an attack.

## 27. Relationship between vulnerability, threat, and attack

**Answer:** A vulnerability is a weakness, a threat is something capable of exploiting the weakness, and an attack is the actual exploitation attempt.

**Example:** A weak password is a vulnerability. A credential thief is a threat/adversary. Guessing the password and logging in is the attack.

## 28. SQL injection vulnerability exists but nobody exploits it

**Answer:** No attack has necessarily occurred. The vulnerability exists, but an attack requires an actual attempt to exploit or violate the system's security.

## 29. Does eliminating one vulnerability eliminate every threat?

**Answer:** No. Fixing a vulnerability removes or reduces one avenue of attack, but other vulnerabilities, attack paths, or threats may remain.

---

# Task 4 — Attack Archetypes

## 30. List and define the four attack archetypes.

**Answer:** Use the exact four names and definitions from your lecture notes.

**Why this key does not fill them in:** The uploaded exam guide says students must know four attack archetypes, but it does not state their names or definitions.

## 31. Match scenarios to attack archetypes.

**Answer:** Use the instructor's four-archetype framework from lecture.

Conceptually:

- copying confidential files corresponds to unauthorized disclosure;
- changing database entries corresponds to unauthorized modification;
- preventing access corresponds to disruption/denial of service;
- impersonating another user corresponds to an identity/authentication-related attack.

Map those concepts to the **exact archetype names used in class**.

## 32. Can one attack belong to more than one attack archetype?

**Answer:** Yes, depending on the lecture taxonomy. A ransomware incident, for example, can involve unauthorized access/modification and disruption of availability.

Use the instructor's exact archetype labels in an exam answer.

## 33. Ransomware archetype(s)

**Answer:** Use the exact attack archetype names from lecture.

At a conceptual level, ransomware that encrypts files and interrupts services clearly includes an availability/disruption component and may also involve unauthorized modification.

---

# Task 5 — Defense Archetypes

## 34. List three of the five defense archetypes.

**Answer:** Use the exact five defense-archetype names and definitions from your lecture notes.

The uploaded guide confirms that five archetypes were discussed but does not provide their names.

## 35. Two defense archetypes against phishing

**Answer:** Use two different defense categories from the lecture taxonomy.

Possible concrete mechanisms could include:

- phishing-resistant multi-factor authentication;
- filtering or blocking known malicious messages/sites;
- user-facing warnings or training;
- detection and incident-response mechanisms.

On the exam, map the mechanisms to the exact defense-archetype names used in class.

## 36. Repeated unauthorized login attempts

**Answer:** Two reasonable concrete defenses are:

1. **Stronger authentication**, such as MFA, which makes a stolen or guessed password insufficient.
2. **Rate limiting / lockout / detection**, which slows or detects repeated attempts.

Again, categorize these using the exact defense-archetype terminology from lecture.

## 37. Why use multiple defense archetypes?

**Answer:** Different defenses address different stages or forms of attack. Layering defenses reduces reliance on a single mechanism and can limit damage if one defense fails.

## 38. Select the most appropriate defense archetype

**Answer:** There is no single universal answer without a scenario. A strong response should:

1. identify the relevant attack or security goal;
2. name the lecture's corresponding defense archetype;
3. explain how the defense reduces the attacker's ability to succeed.

---

# Task 6 — Trusted vs. Trustworthy

## 39. Trusted vs. trustworthy

**Answer:** A component is **trusted** when system security depends on it. A component is **trustworthy** when there is justified confidence that it will behave correctly.

## 40. Can something be trusted without being trustworthy?

**Answer:** Yes.

For example, a poorly designed operating system may still be trusted because the system's security depends on it, even if there is little reason to believe it is secure.

## 41. Can something be trustworthy without being trusted?

**Answer:** Yes.

A highly reliable component may be trustworthy but not security-critical. If the system's security does not depend on it, it need not be trusted in that security model.

## 42. ATM operating system

**Answer:** It is likely **trusted** because the ATM's security depends on it correctly controlling components such as the display, keypad, card reader, transaction logic, and communication.

Whether it is **trustworthy** depends on the evidence that it actually behaves correctly and securely. "Trusted" alone does not prove "trustworthy."

## 43. Why minimize trusted functionality?

**Answer:** Every trusted component is something whose failure or compromise can undermine system security. A smaller trusted base generally reduces the amount of security-critical code or functionality that must be correct.

## 44. One trusted ATM component

**Example answer:** The ATM's transaction software or operating system.

If it is malicious or compromised, it could capture PINs, alter withdrawal amounts, misreport transactions, or expose account information.

---

# Task 7 — Trusted Computing Base

## 45. What does TCB stand for and what is its role?

**Answer:** Trusted Computing Base.

The TCB is the collection of components whose correct operation is relied upon to enforce the system's security properties.

## 46. Why should the TCB be small?

**Answer:** A smaller TCB reduces the amount of security-critical functionality that must be trusted, analyzed, implemented correctly, and protected from compromise.

## 47. Which components might be in the TCB?

Possible answer:

- operating system kernel;
- authentication service;
- access-control mechanism.

A calculator probably would not belong in the TCB unless system security somehow depends on it. Whether the web browser belongs depends on the specific security model and system goals.

## 48. Does every program belong to the TCB?

**Answer:** No. Only components whose correct behavior is necessary for the relevant security guarantees need to be part of the TCB.

---

# Task 8 — Building a Security Model

## 49. ATM security model

A concise answer could include:

### Assets
- cash;
- account balances;
- PINs and credentials;
- transaction records;
- customer financial information.

### Participants
- customer;
- ATM;
- bank backend;
- network/payment infrastructure;
- maintenance staff.

### Adversaries
- thief;
- fraudster;
- malicious insider;
- malware operator.

### Trust assumptions
- the ATM hardware/software correctly handles PINs and transactions;
- communication with the bank is authentic and protected;
- the bank backend correctly validates transactions.

### Vulnerabilities
- exposed keypad;
- compromised software;
- insecure communications;
- physical tampering.

### Threats
- credential theft;
- cash theft;
- transaction manipulation;
- service disruption.

### Attacks
- shoulder surfing;
- skimming;
- malware;
- physical tampering.

### Defenses
- tamper-resistant hardware;
- protected PIN entry;
- secure authenticated communication;
- monitoring;
- transaction limits;
- appropriate authentication.

## 50. Online banking security model

### Assets
- account balances;
- credentials;
- transaction data;
- customer personal information.

### Participants
- customer;
- bank;
- banking application;
- authentication service.

### Adversary
An attacker attempting account takeover or fraud.

### Trust assumption
The bank's authentication and transaction-processing systems behave correctly.

### Threat
Credential theft, transaction manipulation, service disruption, or unauthorized disclosure.

## 51. University course-management system

### Assets
Grades, assignments, student information, course materials, credentials.

### Participants
Students, instructors, administrators, authentication service, learning-management platform.

### Threats
Unauthorized grade changes, account compromise, data disclosure, service disruption.

## 52. Smart door lock

Potential trusted components include:

- lock controller;
- authentication mechanism;
- credential storage;
- firmware;
- communication path if unlocking can be performed remotely.

If one of these components can unlock the door or authorize access, the system's security may depend on it.

## 53. Password manager

**Example trust assumption:** The password manager correctly protects its encrypted vault and master-secret handling.

If that assumption fails, compromise of the manager could expose many or all stored credentials at once.

---

# Task 9 — ATM / Shoulder Surfing

## 54. Rearranging the numeric keypad

**Answer:** It may make memorized finger-position observation harder, but it can also confuse users, slow transactions, create accessibility/usability problems, and may not stop an attacker who can directly observe the keys being pressed.

Therefore it may offer limited security benefit at a meaningful usability cost.

## 55. What threat is being addressed?

**Answer:** PIN theft through shoulder surfing or visual observation.

## 56. Better defense against shoulder surfing

Possible answer:

Use a physical privacy shield around the keypad and encourage users to cover their hand while entering the PIN.

This reduces an observer's visibility without changing the familiar numeric layout.

## 57. Security vs. usability

**Answer:** A rearranged keypad may make observation-based PIN theft harder, but users are accustomed to a standard layout. Changing it can increase errors, slow entry, frustrate users, and create accessibility problems.

---

# Task 10 — Principle of Adequate Protection

## 58. Define adequate protection.

**Answer:** Adequate protection means choosing security safeguards that are proportionate to the assets, risks, threats, and costs involved.

**Source caution:** Use the instructor's exact definition if it differs from this wording.

## 59. Why isn't maximum possible security always adequate protection?

**Answer:** Security mechanisms have costs, including money, performance, complexity, and usability. Protection should be sufficient for the risk rather than needlessly imposing every possible control.

## 60. Blog with password + token + biometric + physical ID

**Answer:** Probably not, assuming the asset and risk are relatively low. The controls appear disproportionate to the value and likely threat level, and they impose excessive usability and operational costs.

The key reasoning is proportionality.

## 61. Asset value and attack cost

**Answer:** Higher-value assets and higher expected losses generally justify stronger or more expensive protections. Defenses should be selected so their costs and burdens are reasonable relative to the risk being reduced.

---

# Task 11 — Larger Scenarios

## 62. Hospital ransomware

### Primary asset
Patient records and the systems/services that clinicians need to access them.

### Adversary
The ransomware operator or attacker.

### CIA properties affected
- **Availability:** clinicians cannot access records.
- **Integrity:** files have been modified/encrypted without authorization.

Confidentiality may also be affected if the ransomware campaign steals data before encryption, but that is not stated in the scenario.

### Attack archetypes
Use the exact lecture terms. Conceptually, the attack includes disruption/denial of availability and unauthorized modification.

### Defenses
Possible examples:
- protected and tested backups;
- segmentation;
- patching;
- least privilege;
- endpoint detection;
- strong authentication.

Use lecture defense-archetype labels where required.

## 63. Stolen laptop

### Threat
A thief or unauthorized person gaining access to the laptop/data.

### Vulnerability
Possible vulnerabilities include lack of full-disk encryption, weak authentication, or leaving the device unattended.

### Security property at risk
Primarily confidentiality.

### Defenses
- full-disk encryption;
- strong authentication;
- remote wipe;
- minimizing locally stored sensitive data.

## 64. Malicious database administrator

**Answer:** Both can be appropriate.

The administrator is a **participant** because they legitimately interact with the system. Once acting against the security goals, the administrator is also an **adversary** in the security model.

## 65. Compromised update server

**Answer:** A critical trust assumption failed: users/systems relied on the update infrastructure to distribute authentic, authorized software.

If the trusted update system is compromised, malicious code may be delivered through a mechanism that users normally trust.

## 66. University authentication server

**Answer:** The authentication server may be part of the TCB because many services rely on it to correctly establish user identities.

If compromised, an attacker may impersonate users or gain unauthorized access across multiple services.

---

# Task 12 — Evaluate a Proposed Defense

## 67. Disable USB ports

**Answer:** This can reduce one path for unauthorized data removal and may reduce some removable-media malware risks.

However, it does not stop exfiltration through email, cloud storage, network connections, screenshots, or other channels, and it may interfere with legitimate work. It is therefore only one layer of defense.

## 68. Require a new password every day

**Answer:** Not necessarily.

Extremely frequent password changes may impose substantial usability costs and can encourage predictable or weak password choices. Under the principle of adequate protection, a control should provide a meaningful security benefit proportional to its cost and burden.

## 69. All controls at the network perimeter

**Answer:** Perimeter controls may not stop insider threats, attacks originating from compromised internal systems, malicious authorized users, or attacks that pass through allowed network traffic.

Security often requires protection at multiple layers.

## 70. Defense A vs. Defense B

**Answer:** If both provide comparable security, Defense B is generally preferable because it achieves the security objective with less usability cost.

A complete answer should still consider deployment cost, reliability, side effects, and whether the two defenses genuinely reduce risk to the same degree.

---

# Task 13 — Diagram / Sketch Questions

## 71. Simple security model diagram

One acceptable conceptual sketch:

```text
             threatens / attacks
[Adversary] ----------------------> [Asset]
                                        ^
                                        |
                                   protected by
                                        |
                                   [Defense]

[Participant] ---- interacts with ---- [System]

[Vulnerability] = weakness that may enable the attack
```

Label the components according to the specific scenario given on the exam.

## 72. Threat, vulnerability, attack, defense

A simple relationship:

```text
Threat / Adversary
        |
        | exploits
        v
  Vulnerability
        |
        | enables
        v
      Attack
        |
        | harms
        v
      Asset

Defense -> prevents, detects, limits, or helps recover from the attack
```

## 73. ATM and TCB

A possible sketch:

```text
        Customer
           |
           v
     +-------------+
     |     ATM     |
     |-------------|
     | Keypad      |
     | Card Reader |
     | Display     |
     | OS/Firmware |
     | ATM App     |
     +-------------+
           |
     authenticated /
     protected link
           |
           v
     +-------------+
     | Bank Backend|
     +-------------+
```

Likely TCB candidates include the components whose correct behavior is necessary to protect credentials and correctly authorize transactions, such as the ATM software/firmware, authentication logic, and relevant bank-side security mechanisms.

---

# Realistic 30-Point Practice Exam — Answer Key

## Task 1 — Quick Questions — 6 points

### a. What does TCB stand for?

**Trusted Computing Base.**

### b. Define integrity.

**Integrity is protection against unauthorized or improper modification or destruction of information or system state.**

### c. What is a vulnerability?

**A weakness that can potentially be exploited to violate a security goal.**

### d. Trusted vs. trustworthy?

**Trusted means security depends on it; trustworthy means there is justified confidence that it behaves correctly.**

### e. Name one attack archetype.

**Use one of the exact four archetype names from your lecture notes.**

### f. Principle of adequate protection?

**Use security protections proportional to the assets and risks rather than simply maximizing security regardless of cost.**

---

## Task 2 — Security Concepts — 4 points

### a. Threat vs. attack

A threat is the potential source or possibility of harm; an attack is an actual attempt to cause that harm.

Example: a password thief is a threat, while actually guessing a user's password and logging in is an attack.

### b. Why can a participant be non-human?

Security models include all relevant entities that interact with the system. Software, hardware, external services, organizations, and automated agents can therefore be participants.

---

## Task 3 — Attack & Defense Analysis — 6 points

### a. Two security properties

**Availability:** customers cannot access services that depend on the encrypted files.

**Integrity:** the attacker has modified/encrypted files without authorization.

### b. Attack archetypes

Use the exact lecture terminology. Conceptually, the ransomware includes service disruption and unauthorized modification.

### c. One defense

**Example:** Tested offline or otherwise protected backups.

They allow the organization to restore affected data and services without relying on the attacker's decryption mechanism.

Other defensible answers are possible if explained correctly.

---

## Task 4 — Trust and TCB — 6 points

### a. ATM operating system

The operating system is **trusted** if the ATM's security depends on it functioning correctly.

Whether it is trustworthy depends on whether there is good reason to believe it actually behaves securely.

### b. Two possible TCB components

Examples:
- ATM operating system/firmware;
- authentication or transaction-authorization logic.

Depending on the system boundary, bank-side authorization components may also be part of the relevant TCB.

### c. Consequence of compromise

A compromised trusted component could steal PINs, manipulate transactions, authorize fraudulent withdrawals, disclose account information, or otherwise defeat the ATM's security guarantees.

---

## Task 5 — Security Model — 4 points

### Asset
Customer account funds or transaction information.

### Participant
Customer.

### Adversary
An attacker attempting account takeover or fraudulent transactions.

### Trust assumption
The bank's authentication and transaction-processing systems correctly authenticate users and execute authorized transactions.

Other well-justified answers are valid.

---

## Task 6 — Evaluate a Defense — 4 points

### a. Rearranged ATM keypad

It might modestly hinder an observer who relies on memorized key locations, but it can confuse users and does not prevent direct observation of the PIN.

Therefore its security benefit may be small compared with its usability cost.

### b. Better solution

A physical privacy shield around the keypad is a strong alternative because it directly reduces visibility of the user's hand while preserving the familiar keypad layout.

---

# High-Priority Facts to Memorize

You should be able to answer these almost instantly:

- **CIA:** Confidentiality, Integrity, Availability.
- **Asset:** Something valuable that should be protected.
- **Vulnerability:** A weakness.
- **Threat:** Potential source/circumstance of harm.
- **Attack:** Actual attempt to violate security.
- **Defense:** Mechanism or action that mitigates attacks.
- **Trusted:** Security depends on it.
- **Trustworthy:** Deserves confidence that it behaves correctly.
- **TCB:** Trusted Computing Base.
- **Participant:** Any relevant interacting entity, not necessarily a human.
- **Security model:** Structured representation of the system, its security goals, relevant entities, assumptions, threats, and protections.
- **Adequate protection:** Protection proportionate to risk and asset value.

Also memorize from your lecture notes:

- the **exact four attack archetype names and definitions**;
- the **exact five defense archetype names and definitions**;
- the instructor's exact decomposition/definition of a **security model**;
- the instructor's precise wording for **adequate protection**, if given.

---

# Best Way to Practice

For every course concept, be able to do four things:

1. **Define it** in one sentence.
2. **Recognize it** in a short scenario.
3. **Apply it** to a new system.
4. **Justify your answer** in one or two sentences.

That preparation style closely matches the exam format described in the Fall 2026 guide and the concise, scenario-heavy structure used in the supplied 2024 exams.
