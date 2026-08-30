# CSC 574 Exams Guide Answers

These answers correspond only to the instructor-provided prompts in the Exams Guide. Use the course terminology from Lecture 02.

## Explain definitions of security

- **Harrison, Ruzzo, and Ullman:** security prevents access by unauthorized users.
- **Garfinkel and Spafford:** a computer is secure when you can depend on its software to behave as expected.
- **Course definition:** a system is secure if it maintains well-specified properties despite the actions of well-specified adversaries. A complete claim identifies the participant, conditions, and time period.

## Define adversary, trust, threat, and security models

- **Adversary:** anybody attempting to circumvent security infrastructure. State what the adversary can access, observe, modify, or control.
- **Trust:** the degree to which an entity is expected to behave in the system.
- **Threat model:** a description of relevant threats, adversaries, capabilities, and assumptions.
- **Trust model:** a description of who is trusted to do what in a particular environment.
- **Security model:** the combination of a trust model and a threat model that addresses perceived risks.

### What is a security model?

A security model identifies the assets and properties that must be protected; participants and trust assumptions; adversaries and capabilities; vulnerabilities and threats; and the defenses that preserve the required properties.

### Which models make up a security model?

$$\text{Trust model} + \text{Threat model} = \text{Security model}$$

## Define CIA, system vocabulary, and risk

- **Confidentiality:** prevent unauthorized disclosure of information.
- **Integrity:** prevent unauthorized modification of data, software, configuration, or behavior.
- **Availability:** preserve authorized access to information or services.
- **Asset:** something worth protecting, such as data, money, systems, access, or reputation.
- **Participant:** an expected system entity or viewpoint. It is not limited to people; computers, agents, servers, clients, organizations, and hosts can be participants.
- **Vulnerability:** a flaw or condition that exposes a system to harm.
- **Threat:** a possible danger that may exploit a vulnerability.
- **Attack:** an attempt to exploit a vulnerability.
- **Defense:** a control or countermeasure that reduces the potential or impact of an attack.
- **TCB:** Trusted Computing Base, the components critical to system security.
- **Risk:** expected concern from likelihood, vulnerability, and impact.

$$R = T \times V \times C$$

Or, when probability is combined:

$$R = P \times C$$

### Broken server-room window

The broken window is a **vulnerability** because it is a weakness or condition that exposes the system. An intruder is a possible **threat**; entering through the window is an **attack**.

## Identify attacker, attack, and defense archetypes

- **Common adversaries:** curious or clueless users, script kiddies, people with an axe to grind, organized criminals, competitors, and governments or nation-state actors.
- **Attack archetypes:** interception (unauthorized access), modification (unauthorized change), fabrication (creation of a false object, file, or message), and interruption (an asset is lost, unavailable, or unusable).
- **Defense archetypes:** prevention (block an attack or close a vulnerability), deterrence (make an attack harder or less attractive), deflection (make this target less desirable), detection (identify an attack and respond), and recovery (restore after an attack or failure).

### Ransomware archetypes

Ransomware that encrypts files is **modification** because the files are changed, and **interruption** because normal access to the files and dependent services is blocked.

## Differentiate trusted and trustworthy

- **Trusted:** a component whose failure can break the security policy; system security depends on it.
- **Trustworthy:** a component that has reason or assurance to be expected to behave correctly under stated conditions.

The ATM operating system is **trusted** because the ATM depends on it for security-critical work. It is not automatically **trustworthy**; that requires evidence that it will behave correctly.

## Create and articulate a security model

For the Glenwood Avenue ATM, identify:

- **Assets and properties:** PINs, account information, transaction records, balances, cash, software, and authorized access; protect confidentiality, integrity, availability, and atomic withdrawals.
- **Participants and trust:** customers, the bank, the ATM, payment networks, and maintenance staff. Customers trust the bank not to leak data and to return correct account information.
- **TCB:** the operating system, firmware and boot chain, transaction software, cryptographic keys, hardware protections, and bank authorization service.
- **Adversaries and capabilities:** thieves, skimmer operators, technically skilled attackers, fraudsters with stolen credentials, malicious insiders, and environmental events.
- **Vulnerabilities, threats, and attacks:** exposed keypad entry, skimming hardware, insecure configuration, unpatched software, weak physical protection, and service outages can enable credential theft, fraudulent withdrawals, transaction modification, or service interruption.
- **Defenses:** card-and-PIN authentication, PIN attempt limits and card lockout, encryption, access controls, anti-skimming checks, tamper-resistant enclosure, transaction limits, logging, monitoring, secure updates, network authentication, backup power, and recovery procedures.

### Upside-down ATM keypad scenario

Changing the keypad layout may slightly deter casual shoulder surfing, but it also harms usability and determined observers can learn the layout. Better controls include physical PIN shields, privacy-aware ATM placement, camera and tamper monitoring, anti-skimming inspections, transaction alerts, and strong fraud detection.

## Define the principle of adequate protection

Protect assets to a degree consistent with their value. More protection is not automatically better because controls cost money, performance, usability, time, and complexity. A defense is justified when its cost is lower than the expected loss it prevents.
