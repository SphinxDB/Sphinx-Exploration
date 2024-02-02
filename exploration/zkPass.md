
# ZkPass
---
![ZkPass](https://miro.medium.com/v2/resize:fit:1400/0*rEP3jNq_iFcw64gJ.png "ZkPass")

## What is ZkPass briefly?

Zkpass is a privacy protocol for private data based on Multi-Party Computation (MPC), Zero-Knowledge Proofs (ZKP), and three-party Transport Layer Security (3P-TLS) to provide privacy-preserving data verification solutions. ZkPass's mission to empower users to validate their data without compromising their privacy. Main use cases of zkpass depends on verifying your real-world private data without revealing private details.


ZkPass's latest funding round was on Aug 03, 2023

August 3rd, 2023, New York, US, — zkPass, a privacy-preserving protocol for private data verification, has secured a $2.5 million seed round. The funding saw substantial participation from renowned investors, including Sequoia China, Binance Labs, OKX Ventures, dao5, SIG DT Investments, Inc., Leland Ventures, Cypher Capital, Blockchain Founders Fund, and others.

Founded Year: 2022

Location: Sydney, Australia

Company Stage: Seed

Total Funding: $2.5M

## Who created ZkPass?

There are two co-founder of ZkPass

Joshua Peng, Co-Founder at ZkPass:

[Joshua P Linkedin](https://www.linkedin.com/in/joshua-p-466504257/ "Joshua P Linkedin")

Education:
University of Missouri-Columbia

Doctor of Philosophy - PhD, Structural Engineering

Oca 2012 - Tem 2015



Bing J, Co-Founder at ZkPass:

[Bing J Linkedin](https://www.linkedin.com/in/zkbing/ "Bing J Linkedin")

Education:
南开大学南开大学

Master's degree, Software Engineering

Eyl 2007 - Haz 2010


南开大学南开大学

Bachelor's degree, Software Engineering

Eyl 2003 - Haz 2007



## Who are using ZkPass?

The provided use cases by the zkPass:

# ZkKYC


an decentralized authentication solution that verifies your legal identity without requiring file uploads or the over-disclosure of private information.

# Un­der­col­lat­er­al­ized defi lend­ing pro­to­col


a defi lending protocol combining on-chain and off-chain credit allows users to selectively verify their on-chain and off-chain reputations have access to lower collateralized borrowing opportunities, increasing capital efficiency.



# Health­care zk-data mar­ket­place


a private healthcare data marketplace that allows users to selectively disclose trusted healthcare data to earn rewards.


# De­cen­tral­ized job mar­ket­place


a decentralized freelance marketplace that allows users to secure remote work opportunities by privately disclosing some of their trusted data through zkpass. a defi lending protocol combining on-chain and off-chain credit allows users to selectively verify their on-chain and off-chain reputations have access.

# In­sur­ance claims


generate zero-knowledge proofs from private data during a web session and submit them to a smart contract for insurance policy eligibility verification, enabling automatic claim settlement without the need for manual review.



## Why should we use ZkPass?

## Advantages of using ZkPass


## Disadvantages of using ZkPass

## How much is it related with Sphinx?

## How does ZkPass work?

## How does it handle security and privacy concerns?
 
## Which protocols it uses and what is it for?
ZkPass built on with these core protocols: Three-Party TLS (3P-TLS), Multi-party Secure Computation (MPC), and Zero-Knowledge Proof (ZKP).

# MPC


Multi-party Computation (MPC) has its origins in the millionaire problem, which was proposed by Andrew Yao in 1982. MPC enables participants to collectively compute a function using their private inputs without revealing the inputs themselves. Even if one or more parties are compromised during the computation, MPC ensures the confidentiality of the participants' original secret data and guarantees the accuracy of the function's output.
Since the development of MPC theory, several specialized techniques have emerged, including Garbled Circuits (GC), Secret Sharing (SS), Homomorphic Encryption (HE), and Oblivious Transfer (OT). Each of these techniques addresses different aspects of privacy-preserving computation, offering unique security properties and performance characteristics.
The zkPass Protocol requires a significant number of bitwise operations. As a result, high-performance Oblivious Transfer Extension (OTE) and Garbled Circuits (GC) algorithms were chosen for implementation. These algorithms optimize the efficiency of secure computations while maintaining robust privacy guarantees, making them an ideal fit for the complex requirements of the zkPass Protocol. By utilizing these advanced MPC techniques, the zkPass Protocol can deliver a privacy-preserving, high-performance identity solution that meets the demands of the Web3 ecosystem.

![3P-TLS MPC](https://lh7-us.googleusercontent.com/ejD8G0zTtEepb4PWKdMtIT8KdMRLB3W-9IzAlMq03J-qPh4IcIQARaN4Aqt2uz48u3yGPNVpr5cWlZlgKmLI3qSrTIKcx4gF3R8AZrQhTLvfPa1vDTfOTW14kJ2bokozufPQUx6pmxDalfSpIEZmOA  "3P-TLS MPC")

This image shows How 3P-TLS & MPC Work on zkPass.

# 3P-TLS

In the 3P-TLS protocol, there are three key players: S, who serves as a trusted data source, P, the Prover/user, and V, the zkPass node. P and V collaborate as a client to establish secure communication with S through a series of stages.
The first stage involves a three-party handshake protocol. Here, P, V, and S collectively generate session keys. P and V each obtain a share of these keys. This is achieved using the Paillier encryption algorithm, which offers additive homomorphism. The pre-master key is divided into two parts, with P and V receiving one-half each, while S retains the complete pre-master key. Importantly, to prevent the client from forging fake websites, after the Client and Server exchange greetings, the Client will ask the Server to return the certificate. The subsequent key exchange phase also includes the server’s public key signature, which is signed by the private key of the certificate. This allows V within the Client to also obtain the certificate and signature for verification, ensuring trust in the data source.
In steps 6 and 7, P and V engage in MPC to compute the encryption key (enc_key) for data protection and the message authentication code key (mac_key) for data integrity. It’s essential to note that V only possesses a share of the mac_key and no enc_key. This ensures that V cannot access the user’s private information. In contrast, P holds a share of the mac_key, granting access to specific identity information without the ability to tamper with it. Any tampering can be detected by verifying message authenticity using the mac_key.
Steps 8 and 9 follow standard TLS protocol procedures for application data. In steps 10 to 12, P and V exchange keys in preparation for an upcoming phase involving zero-knowledge proofs.
At this point, the three-party TLS protocol concludes. The MPC algorithm of zkPass has undergone significant optimization in terms of communication time, hash functions for Garbler, Evaluator, and OT, as well as memory copying operations. This has resulted in an efficiency improvement of over threefold. Additionally, a new AES128 proof method has been adopted which has reduced the number of blocks by 300 times and improved Garbler/Evaluator execution time tenfold. Specifically, zkPass employs Silent OT for OT operations, effectively reducing offline network communication during OT generation. In terms of Garbled Circuits, zkPass utilizes Stacked GC which significantly reduces the size of Garbled Circuits thereby decreasing online communication and execution time. This overall optimization has substantially reduced the runtime of the entire MPC process.


![ZKP](https://lh7-us.googleusercontent.com/M9_rJi12xGu6Lnocwng2oyNjkrONofoiSX3Gxmqtn1hO0ZQSbSSxHTmBL9kACbd2xqS60ZZ2X4sPOpaKTq8jEIV0mnAb9dATFMyQKP8odmHDM6yguud4QUgq9USJMJihFhW5M9r8ZUcTvMgMGMKs7Q  "ZKP")

This image shows How interactive zero knowledge proofs Work on zkPass.

The final step of the zkPass protocol involves the client generating zero-knowledge proof, which the smart contract on the blockchain verifies. We employ a Hybrid Zero-Knowledge (ZK) approach that combines both interactive and non-interactive ZK protocols. 

# Interactive Zero-Knowledge (IZK):

We utilize a VOLE-based interactive Zero-Knowledge (ZK) protocol, which we refer to as VOLE-ZK 23. This protocol plays a crucial role in authentication, ensuring the data's origin from the precise data source and safeguarding it against tampering by clients. The VOLE-ZK 23 protocol can be described as a "commit and prove" framework. In this setup, both the Prover (P) and the Verifier (V) jointly generate numerous VOLE instances, each satisfying a linear formula denoted as "m = k + w * delta." P holds certain components of this formula as a commitment, with 'm' serving as the commitment, and 'w' can be converted into a witness after derandomization. 
On the other hand, V holds the remaining components ('k' and 'delta'). The objective is to prove and verify the satisfaction of a boolean circuit. P establishes a commitment for every gate based on the VOLE instance. Since the correlation between VOLE instances is linear, we can batch-check the results by summing up all commitments and confirming whether the final result still adheres to the correlation. This linearity is a key reason our solution is cost-effective, setting it apart from other high-degree polynomial solutions like SNARK. Consequently, P only needs to transmit two field elements (the sum of 'm' and the sum of 'w') to the Verifier. To protect sensitive information, a random linear combination can be created. V then validates the correlation using its VOLE parameters ('k' and 'delta').
There are five main constraints at this stage:
The vector x = (Q', R', mac_key_pv, b) represents the public signal, and w = (enc_key, token, Q, R) is the witness.

Dec(enc_key, Q') = Q, and Q = Query(token)

The first two constraints are related to the HTTP requests made to the trusted data source. The first constraint ensures that the request is encrypted using the encryption key. The second constraint specifies that the request must be generated using the user's access token, typically stored in cookies in most cases. These two constraints confirm that the user is using their personal data (such as a username and password) and is following a specific API defined in the template.

Dec(enc_key, R‘) = R

R' represents the response received from the trusted data source and is encrypted using the encryption key. Therefore, this constraint implies that the user must possess the encryption key, generated during a three-party handshake, to decrypt the response. This constraint serves to ensure that the user cannot create a counterfeit encryption key.

Verify(mac_key_pv, MAC, R) = 1

R stands for the decrypted response. It's crucial for the zkPass protocol to ensure that this response (R) remains unaltered by the user. To substantiate this, the constraint is applied. The additional MAC (Message Authentication Code) data attached to the end of R is generated using the MAC key. The verification process employs HMAC with the SHA256 hash function. This verification step serves as a safeguard against any unauthorized modifications to the response data by the user.

b = Assert(R)

The final constraint signifies that the data contained within R must adhere to specific conditions outlined in the template. For instance, if R is structured as a JSON object like {user: xxx, age: 30}, it necessitates that the "age" property must have a value greater than 18. In simpler terms, this constraint ensures that the data inside R complies with predetermined criteria.


## Resources

- [ZkPass](https://zkpass.org "ZkPass") Jan 2024
- [ZkPass/Docs](https://zkpass.gitbook.io/zkpass/ "ZkPass Docs") Jan 2024
- [ZkPass/WhitePaper](https://docsend.com/view/5wdg66beu7m95jf3 "ZkPass WhitePaper") Jan 2024
- [ZkPass Github](https://github.com/zkPassOfficial "ZkPass Github") Jan 2024
- [ZkPass Investments](https://medium.com/zkpass/zkpass-raised-a-2-5m-seed-round-funding-af6419d3b50f "ZkPass Investments") Jan 2024
- [ZkPass Company Details](https://tracxn.com/d/companies/zkpass/__t3yqnfdP0JVik7J5UYRBnn9nRg66gfl8B1ogIkKsbTU "ZkPass Company Details") Jan 2024

