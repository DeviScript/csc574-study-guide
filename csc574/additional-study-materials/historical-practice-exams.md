# Historical Practice Exams and Answers

> **Additional study material:** These are historical and sample questions from an external source. They are not instructor-provided course material and are not confirmed to be part of CSC 574 assessments.

> **Source:** User-provided `Extracted_Midterm_Questions_and_Answers_Updated.docx`.

_Compiled from the two attached PDFs_

Note: Source-provided answers are reproduced as closely as possible from the original files, including original wording, spelling, and apparent calculation errors. Answers supplied to fill blank or incomplete items are explicitly labeled "Answer (added)" or "Supplement (added)."

## Document 1 - Midterm Exam 1

## Q1 (4 Points)

**Question:** What are the three desired properties of cryptographic hash functions? (Just list them, no need to define)

> **Answer:** One wayness or Pre-image Resistance 2nd Pre-image resitance Collision resistnace

## Q2 (4 Points)

**Question:** If a good-quality hash of a message produces a 400-bit output, how many messages would you need to try at random to have at least a 50% chance of two messages generating the same hash output (i.e., a collision)?

> **Answer:** 399

## Q3 (4 Points)

**Question:** What critical functionality does the Diffie-Hellman protocol provide? That is, what do many protocol use Diffie-Hellman for?

> **Answer:** DH provide negotiate a secret over insecure media. DH Ephemeral key provide perfect Forward secrecy hence many protocol use it for data encryption during session.

## Q4 (4 Points)

**Question:** What valuable property is supported by digital signatures but not by HMACs?

> **Answer:** Digital signature provide non-repudiation by signing the message with private key however HMAC uses symetric key which can be evesdrop or compromised.

## Q5 (4 Points)

**Question:** Why is Encrypt-and-MAC (E&M) highly discouraged?

> **Answer:** E&M uses symetric encryption for encryption and MAC, if key is compromised/sniffed it is easy to decrypt data.

## Q6 (4 Points)

**Question:** Why does RSA blinding prevent timing attacks during decryption?

> **Answer:** Blinding is multiply the ciphertext by a random number before performing decryption, Attcker will not know what the bits of "c" are.

## Q7 (4 Points)

**Question:** What is the purpose of a nonce in a challenge-response protocol?

> **Answer:** To provide freshness and mitigate replay attacks.

## Q8 (4 Points)

**Question:** Why is secure authentication critical to the security of a system?

> **Answer:** Authentication establishes one's identity so they can obtain the set of rights.

## Q9 (4 Points)

**Question:** Where does TLS appear in the IP protocol stack?

> **Answer:** Inside Application layer

## Q10 (4 Points)

**Question:** What type of VPN configuration only protects network traffic to a specific set of destination IP addresses?

> **Answer:** IP sec VPN

## Q11 (4 Points)

**Question:** ARP spoofing is possible because the \_\_\_\_ response wins.

> **Answer:** Last

## Q12 (4 Points)

**Question:** Does a stateful firewall have more or less performance overhead than a stateless firewall? Why?

> **Answer:** a stateful firewall have more performance overhead than a stateless firewall because it has to keep track of establish connections and flags however Stateless FW inspect each packet at a time.

## Q13 (4 Points)

**Question:** Why are Layer-3 firewalls significantly less useful today than 20 years ago?

> **Answer:** More applications starts using port 80 or 443 to tunnel or encapsulate other applications which make it difficult for firewall to inspect real application.

## Q14 (4 Points)

**Question:** With respect to BGP security, is prefix hijacking more or less dangerous than sub-prefix hijacking? Why?

> **Answer:** Sub-prefix hijacking is more dangerous because it advertise more specific prefix than actual originator hence always wins for that particular prefix.

## Q15.1 (3 Points)

**Question:** Suppose someone gives you the RSA public key K+ = (e=5, n=35). What is the ciphertext for the plaintext message M=3, encrypted with the public key? Show your work.

> **Answer:** E({5,35},3) = 33

## Q15.2 (3 Points)

**Question:** What is the private key, K-, that corresponds with K+? Show your work.

> **Answer:** given n= 35 and e (pub key)= 5 n= pq assume p =5 and q=7 (prime numbers) phi(n)=phi(pq)+(p-1)(q-1)= 24 then : edmodphi(pq)=1 5\*d mod 24 =1 d=5 K- or privaye key is 5

## Q15.3 (1 Point)

**Question:** Assuming you can calculate an answer for Q15.2, why is RSA not broken?

> **Answer:** Because P and q are thrown aways after calculation and it is a large pseudo random generated prime. Brute forcing this will take a long time.

## Q16 (7 Points)

**Question:** EBay wants to create a system where customers (a) commit to bids on items and (b) do so at a particular time t_i. Assume they provide a system where each customer (Bob in this example) uses a shared key (k_bob) to commit to a bid D. Bob provides E(k_bob, "Bob") to EBay as this commitment. Identify at least 3 problems with this scheme, i.e., why does it not provide the desired properties?

> **Answer:** 1. Kbob is shared key there is no way to authenticate if it comes from Bob. 2. message "Bob" is in clear text there in MITM can change it to Alice. No integrity. 3. No non-repudiation here, Bob can deny later point that he made this commitment.

## Q17.1 (2 Points)

**Question:** Prof. Pedantic recently developed a new network intrusion detection system called The Classier Classifier. What is the name we give to the table-like layout shown in Table 1?

> **Answer:** Confusion Matrix

## Q17.2 (2 Points)

**Question:** What is the True Positive Rate (TPR), True Negative Rate (TNR), False Positive Rate (FPR), and False Negative Rate (FNR) of The Classier Classifier? Assume that a "true positive" is when The Classier Classifier correctly detects a malicious packet as malicious. Hint: no need to perform a calculation, simply write the correct value from Table 1.

> **Answer:** TPR: 1-FNR= Tp/FN+TP= 99/1+99  
> TNR: 1-FPR= TN/FP+TN=97/3+97  
> FPR: FP/FP+TN= 3/3+97  
> FNR: FN/FN+TP= 1/1+99

## Q17.3 (6 Points)

**Question:** Suppose that someone is foolish enough to deploy Prof. Pedantic's system. When The Classier Classifier raises an alarm that it has detected attack traffic, what is the probability that it is correct? That is, what is the true alarm rate, Pr(M\|A). Show your work. State all equations before filling in values. Failure to state equations will result in points deducted.

> **Answer:** True Alarm rate is - Pr(M\|A) = Pr(A\|M) · Pr(M)/Pr(A\|M) · Pr(M) + Pr(A\|!M) · Pr(!M)  
> base rate is 0.0001

**Supplement (added):** Pr(M\|A) = \[Pr(A\|M)Pr(M)\] / \[Pr(A\|M)Pr(M) + Pr(A\|!M)Pr(!M)\] = (0.99×0.0001) / \[(0.99×0.0001) + (0.03×0.9999)\] ≈ 0.003289, or about 0.329%.

## Q18.1 (2 Points)

**Question:** iface=WAN, s_ip=172.16.0.233, s_port=43223, d_ip=10.0.1.15, d_port=443, proto=TCP

> **Answer:** 1.c

## Q18.2 (2 Points)

**Question:** iface=WAN, s_ip=172.16.0.33, s_port=2435, d_ip=10.0.0.150, d_port=53, proto=UDP

> **Answer:** 1.d

## Q18.3 (2 Points)

**Question:** iface=WAN, s_ip=172.16.0.33, s_port=14223, d_ip=10.0.0.24, d_port=22, proto=TCP

> **Answer:** 1.e

## Q18.4 (2 Points)

**Question:** iface=LAN, s_ip=10.0.0.26, s_port=53224, d_ip=8.8.8.8, d_port=53, proto=UDP

> **Answer:** 2.f

## Q18.5 (2 Points)

**Question:** iface=LAN, s_ip=10.0.2.182, s_port=53224, d_ip=172.16.0.43, d_port=25, proto=TCP

> **Answer:** 2.e

## Q19.1 (3 Points)

**Question:** The identifier field in DNS requests and responses is 16 bits long. Edward can inject 4096 forged DNS responses per second, and the correct response arrives in 0.25 seconds. What is the probability that Edward will be able to poison a particular request? Assume the requested hostname is not locally cached and source port randomization is not used.

> **Answer:** Edward rate is 2^10/sec but it takes only 0.25sec for correct response so he can sent 25% of 4094 response in that time that is 2^10. Probability of successful attack is then = 2^10/2^16 = 1/64 = 1.5%

## Q19.2 (3 Points)

**Question:** Now assume that the DNS server is updated to use source port randomization. The DNS server is configured to select from 2^11 different source ports. What is the updated probability that Edward will be able to poison a particular request?

> **Answer:** Attcker response rate remains same 2^10 in 0.25 sec. however wiht port randomnization attack success proability = 2^10/2^16\*2^11 =1/2^17 = 00076%

## Q19.3 (4 Points)

**Question:** If Edward is unsuccessful in the previous two attacks, he must wait until the TTL on the cached DNS information expires. To overcome this limitation, Edward uses the Kaminsky attack. What is the expected number of hours it will take Edward to be successful? Assume the source port randomization as in Q19.2. Hint: the expected value for a geometrically distributed random variable X is 1/p.

> **Answer (added):** With source-port randomization, one request has success probability p = 2^-17. A Kaminsky attack can force a fresh uncached lookup each time, so the expected number of attempts is 1/p = 2^17 = 131,072. At 0.25 seconds per attempt, the expected time is 131,072 × 0.25 = 32,768 seconds ≈ 9.1 hours.

## Document 2 - CSC/ECE574 Spring 2019 Midterm Exam - Solutions

**Source note:** "Obviously answers will not be verbatim to what is shown below, but should make similar points in your own words."

## 1(a) (8 points (question total))

**Question:** For encryption of simple text, the homework should have convinced you that permutation ciphers are tougher to break than substitution ciphers. Why (one or two sentence answer)?

> **Answer:** The fairly predictable (far from random) frequencies of letters make breaking simple substitution ciphers easy to break. There are not such easy to use clues about how to reverse engineer an arbitrary permutation (optional: although letter n-gram frequencies can help).

## 1(b)

**Question:** A one-time pad provides perfect encryption strength. Are there any drawbacks (one or two sentence answer)?

> **Answer:** 1. Can only use the pad (which is like a key) one time, and 2. the pad must be the same length as the message being encrypted.

## 2(a) (8 points (question total))

**Question:** With CBC, will plaintext blocks that are equal produce the same ciphertext output blocks when encrypted (one or two sentence answer), and why or why not?

> **Answer:** No, they will not produce the same ciphertext, because the message is first XOR’ed with the ciphertext block immediately preceding (i.e., the output depends on block position).

## 2(b)

**Question:** If ciphertext block C2 is manipulated by an attacker before decryption, with CBC which output plaintext blocks will be affected?

> **Answer:** M2 and M3 only.

## 3 (5 points)

**Question:** Which of the 4 steps in a round of AES encryption most thoroughly “diffuses” the bits of the partially-encrypted block?

> **Answer:** MixColumn by far diffuses bits across the entire block.

## 4 (6 points)

**Question:** Let p = 23 and q = 13 be two primes. Explain how you would generate an RSA public / private keypair (and indicate which is public and which is private). You don’t need to do any arithmetic - just write expressions with the proper values.

> **Answer:** n = p \* q = 23 \* 13. The totient function of n, φ(n) = (p−1) \* (q−1) = 22 \* 12. Choose a value e which is relatively prime to φ(n); the public key = \<e, n\>. Let d be the multiplicative inverse of e mod φ(n); the private key is \<d, n\>.

## 5 (8 points)

**Question:** Suppose values for p = 73 and g = 5 have been selected, and two parties A and B have selected secret random numbers of 12 and 35, respectively. For Diffie-Hellman key exchange, explain what messages they exchange, and how they compute the value of the shared secret.

> **Answer:** A sends p = 73 and g = 5 to B. A generates random number S_A \< (73−1), B generates random number S_B \< (73−1). A computes T_A = 5^S_A mod 73, and B computes T_B = 5^S_B mod 73. A sends T_A to B, B sends T_B to A. A computes T_B^S_A mod 73, B computes T_A^S_B mod 73.

## 6(a) (6 points (question total))

**Question:** How are the public keys of roots of trust verified, since there is no certificate authority “above” them (one or two sentence answer)?

> **Answer:** The public keys of roots of trust, like certificates of authority, are hard-coded in the keystore of the OS and/or the browser, by the vendor.

## 6(b)

**Question:** What is a major advantage of an OCSP vs a CRL (one or two sentence answer)?

> **Answer:** OCSP does not require downloading lengthy certificate revokation lists periodically (and can give completely up to the minute answers about certificate status).

## 7(a) (8 points (question total))

**Question:** Computing a residue is proposed as a MAC solution. Does this have the right properties for a MAC, and if not, what property(ies) is(are) violated?

> **Answer:** The residue has properties 1, 2, and 3 of the hash function requirements.

## 7(b)

**Question:** Are there any other drawbacks to using this as a MAC?

> **Answer:** There is a major cost to using the residue; the entire message has to be encrypted, which is computationally slower/more expensive than hashing.

## 7(c)

**Question:** Is it subject to the extension attack, and if so, how (one sentence answer)?

> **Answer:** No. Given message P consisting of blocks P1...Pn, if only ciphertext block output Cn (i.e. the residue) is known, it is computationally infeasible to find a plaintext block Pn+1 for which the ciphertext block Cn+1 = Cn. (However, if you assumed all ciphertext blocks are known, including Cn−1, there is an easy extension attack - I’ll accept that answer, and “No” to the first question, if you state that assumption.)

## 8(a) (8 points (question total))

**Question:** Suppose passwords are 80 bits long and a salt is 4 bits long. What does adding salt to the hash of the password improve, and by how much does it improve it?

> **Answer:** Since for each password there may be any of 2^4 = 16 possible salt values, if you wish to pre-compute and store all hashed concatenations of possible passwords with possible salts, 16 times more computation and storage is required.

## 8(b)

**Question:** Does repeated hashing of a password (without salt) before storage have the same benefit as hashing, and why or why not?

> **Answer:** It is not the same benefit; x times more computation (if x is the number of times the password is hashed) is required to check a possible password value, but only the same amount of storage is required to store pre-computed values (there is only one possible result per password).

## 9(a) (8 points (question total))

**Question:** It is said a reflection attack is possible for the following protocol. Explain the attack (one or two sentences).

> **Answer:** In channel 1 from an imposter connecting to Bob, the value of Bob’s nonce in message 2 can be used as the value of the Imposter’s nonce in message 1 of a second channel opened to Bob. Bob’s answer in message 2 of this second channel can be used as the Imposter’s response in message 3 of the first channel.

## 9(b)

**Question:** The following is an attempt to accomplish 2-way authentication, and negotiate a session key. Are there any problems with this protocol, and if so, what, and how can it be fixed (one sentence answer)?

> **Answer:** The protocol does authenticate Bob and Alice to each other, but there is no secret (basis for a session key) that is not known to others; better if Bob responds to Alice with {R_Alice}\_Alice.

## 10(a) (6 points (question total))

**Question:** Does Bob authenticate to Alice in the Needham-Schroeder protocol, and if so, how?

> **Answer:** Yes. In order for Bob to respond to Alice’s challenge in message 3, he must possess K_Bob−KDC to decrypt the ticket.

## 10(b)

**Question:** Does Bob authenticate to Alice in the Otway-Rees protocol, and if so, how?

> **Answer:** Yes, Bob authenticates to Alice in that the last message contains something “recognizable”, which could only be correct if K_AB is decrypted from the ticket sent to Bob, which only he can decrypt (using K_Bob−KDC).

## 11 (5 points)

**Question:** In Kerberos, why does the server issue a ticket-granting ticket + a service-granting ticket, i.e., why are there two tickets instead of one, as in the Needham-Schroeder protocol (one or two sentence answer)?

> **Answer:** Because Kerberos decouples the activity of authenticating to the KDC from the act of requesting services from a server (i.e., one authentication can be used for multiple requests to servers).

## 12 (5 points)

**Question:** What is the single most important difference between IPsec and TLS, and why does it matter (one or two sentence answer)?

> **Answer:** IPsec is on top of IP but below the transport layer, which it means it can be used by any networked application, without modification of that application. TLS is on top of the transport layer, which means it can only be used by applications that are aware of the fact they are running on top of TLS.

## 13(a) (8 points (question total))

**Question:** The client and server in TLS both send nonces (timestamps+random number) to each other. Why are these useful (one or two sentence answer)?

> **Answer:** Both nonces are used to compute the master secret, which means both parties contribute to the randomness of the resulting key.

## 13(b)

**Question:** Both Diffie-Hellman and public key crypto can be used for key negotiation. What is a major advantage of using Diffie-Hellman vs. public key for this purpose (one or two sentence answer)?

> **Answer:** Diffie-Hellman does not need to assume the availability of a public key infrastructure (optional: and does not require that either party know the identity of the other).

## 14(a) (6 points (question total))

**Question:** What advantages does ESP tunnel mode have over ESP transport mode, if any?

> **Answer:** ESP tunnel mode encrypts (and optionally authenticates) the original (inner) IP header, which transport mode does not. This is useful for private (anonymous) communication.

## 14(b)

**Question:** What is a traffic selector in IPsec?

> **Answer:** A traffic selector specifies what traffic a SA (security association) should be applied to (optional: usually consist of source and destination IP address, type of transport, and source and destination port numbers).

## 15(a) (6 points (question total))

**Question:** What is a DDoS reflection attack, and why is it a problem (1-2 sentence answer)?

> **Answer:** A reflection attack uses IP source address spoofing to have a response from a non-malicious server directed to a victim address. It is a problem because it is a way to generate lots of traffic to the victim, without revealing who the source of the attack is.

## 15(b)

**Question:** What are 3 practical defenses against DDoS (phrase or sentence for each)?

> **Answer:** There are a number of possible answers here, both from the lecture and other sources. Any 3 reasonable answers are acceptable, including:  
> • Prevent IP address spoofing  
> • Use the services of a security provider or CDN to remove suspicious (attack) traffic  
> • Have lots of replicated services (so, increase the amount of available resources)  
> • Adopt standards and/or regulations that make it harder / more unlikely that IoT devices can be used for DDoS.  
> • etc.

## Document 3 - CSC574 Sample Exam Questions (Spring 2021)

**Source note:** The attached sample contains questions but no answer key. The answers below are supplied to fill those blanks and are labeled accordingly. The original numbering jumps from 4 to 15; questions 5-14 are not present in the attachment.

## 1

**Question:** Name a cryptosystem that offers provable guarantees, irrespective of computational abilities of an attacker. That is, it provides unconditional or probabilistic security.

**Answer (added):** One-time pad (Vernam cipher), when used with a truly random key as long as the message and never reused.

## 2

**Question:** What is the central difference between IPsec tunnel and transport modes?

**Answer (added):** Transport mode protects the IP payload while leaving the original IP header exposed. Tunnel mode encapsulates and protects the entire original IP packet inside a new IP packet, including the original header.

## 3

**Question:** Cipher modes such as CBC make use of an IV. What is an IV and why is it useful?

**Answer (added):** An IV (initialization vector) is a per-encryption input used with the key to initialize the cipher mode. It prevents identical plaintexts encrypted under the same key from deterministically producing identical ciphertext patterns; for CBC, the IV should be unpredictable and normally unique.

## 4

**Question:** Does a system that requires both a fingerprint and a retinal scan use 2-factor authentication? Why or why not?

**Answer (added):** No. Both are biometric credentials—“something you are”—so they are two checks from the same authentication factor, not two different factors.

## 15

**Question:** Explain the function of a salt. How are these implemented? How do they improve password resistance to offline attacks?

**Answer (added):** A salt is a random, unique value generated for each password and stored alongside the password hash; the system computes a password hash/KDF over the password together with the salt. The salt does not need to be secret.

Salts defeat precomputed rainbow tables and prevent equal passwords from having equal stored hashes. In an offline attack, an attacker must redo the password-guessing computation separately for each salt/account instead of reusing one precomputed table across many users.

## 16

**Question:** Explain how two neighboring ASes can leverage IP’s TTL field to verify BGP messages from one another (that is, that a BGP message actually originated from the neighbor AS). Recall that the maximum TTL is 255, and the TTL is decremented each time a packet traverses through a router.

**Answer (added):** Use the BGP TTL security mechanism (GTSM): each neighbor sends BGP packets with TTL = 255, and a directly connected peer accepts them only if the received TTL is 254 (or within a configured high-TTL threshold). A remotely spoofed packet must cross additional routers, so its TTL will be lower and it can be rejected.

## 17

**Question:** A is a terrestrial base communicating with satellites B and C. A broadcasts the first message; B and C each reply to A. The protocol must privately deliver d1 to B and d2 to C, let B/C prove receipt, and bind the paired data items so each satellite can later demonstrate which other item was paired with its own. A and B share k_AB, A and C share k_AC, and A, B, and C share k_ABC. The original message includes a nonce.

**Answer (added):** One valid construction is to use authenticated encryption (AE) under the pairwise keys and HMAC commitments under the opposite pairwise key. Let N be a fresh nonce, T_B = HMAC(k_AC, N \|\| d2), and T_C = HMAC(k_AB, N \|\| d1). Then:

> A → (B,C): N, AE(k_AB, d1 \|\| N \|\| T_B), AE(k_AC, d2 \|\| N \|\| T_C)
>
> B → A: HMAC(k_AB, "received" \|\| N \|\| d1 \|\| T_B)
>
> C → A: HMAC(k_AC, "received" \|\| N \|\| d2 \|\| T_C)

**Why this meets the goals:** (a) only A and B know k_AB, so d1 is confidential and integrity-protected for B; (b) only A and C know k_AC, so d2 is confidential and integrity-protected for C; (c) B’s HMAC proves to A that B possessed k_AB and recovered the fresh d1 tied to N, without sending d1 in the clear; (d) C’s HMAC provides the analogous proof for d2; (e) B retains T_B, a commitment to the specific N,d2 pair that B cannot open because it does not know k_AC, and can later present it to A; (f) C similarly retains T_C, which binds the corresponding N,d1 pair without revealing d1. The fresh nonce N prevents old protocol runs from being replayed as a new run.

**Note:** The shared k_ABC is not required by this construction. Using it to encrypt either d1 or d2 would violate the confidentiality goals because both B and C know k_ABC; it could instead be used only for a group-authentication field if the protocol required one.
