
# ZkPass
---
![ZkPass](https://miro.medium.com/v2/resize:fit:1400/0*rEP3jNq_iFcw64gJ.png "ZkPass")

# What is ZkPass briefly?

Zkpass is a privacy protocol for private data based on Multi-Party Computation (MPC), Zero-Knowledge Proofs (ZKP), and three-party Transport Layer Security (3P-TLS) to provide privacy-preserving data verification solutions. ZkPass's mission to empower users to validate their data without compromising their privacy. Main use cases of zkpass depends on verifying your real-world private data without revealing private details.


ZkPass's latest funding round was on Aug 03, 2023

August 3rd, 2023, New York, US, — zkPass, a privacy-preserving protocol for private data verification, has secured a $2.5 million seed round. The funding saw substantial participation from renowned investors, including Sequoia China, Binance Labs, OKX Ventures, dao5, SIG DT Investments, Inc., Leland Ventures, Cypher Capital, Blockchain Founders Fund, and others.

Founded Year: 2022

Location: Sydney, Australia

Company Stage: Seed

Total Funding: $2.5M<br><br>

# Who created ZkPass?

There are two co-founder of ZkPass

Joshua Peng, Co-Founder at ZkPass:<br>
[Joshua P Linkedin](https://www.linkedin.com/in/joshua-p-466504257/ "Joshua P Linkedin")<br>
Education:<br>
University of Missouri-Columbia<br>
Doctor of Philosophy - PhD, Structural Engineering<br>
Oca 2012 - Tem 2015<br><br>



Bing J, Co-Founder at ZkPass:<br>
[Bing J Linkedin](https://www.linkedin.com/in/zkbing/ "Bing J Linkedin")<br>
Education:<br>
南开大学南开大学<br>
Master's degree, Software Engineering<br>
Eyl 2007 - Haz 2010<br>


南开大学南开大学<br>
Bachelor's degree, Software Engineering<br>
Eyl 2003 - Haz 2007<br><br>


# Why should we use ZkPass?

The provided use cases by the zkPass:

### ZkKYC<br>
An decentralized authentication solution that verifies your legal identity without requiring file uploads or the over-disclosure of private information.<br><br>

### Un­der­col­lat­er­al­ized defi lend­ing pro­to­col<br>
A defi lending protocol combining on-chain and off-chain credit allows users to selectively verify their on-chain and off-chain reputations have access to lower collateralized borrowing opportunities, increasing capital efficiency.<br><br>



### Health­care zk-data mar­ket­place<br>
A private healthcare data marketplace that allows users to selectively disclose trusted healthcare data to earn rewards.<br><br>


### De­cen­tral­ized job mar­ket­place<br>
A decentralized freelance marketplace that allows users to secure remote work opportunities by privately disclosing some of their trusted data through zkpass. a defi lending protocol combining on-chain and off-chain credit allows users to selectively verify their on-chain and off-chain reputations have access.<br><br>

### In­sur­ance claims<br>
Generate zero-knowledge proofs from private data during a web session and submit them to a smart contract for insurance policy eligibility verification, enabling automatic claim settlement without the need for manual review.<br><br>

# How does ZkPass work?

Currently, in order to use zkpass, users need to download an extension called [ZkPass Transgate](https://chromewebstore.google.com/detail/zkpass-transgate/afkoofjocpbclhnldmmaphappihehpma?utm_source=ext_app_menu "ZkPass Transgate").

![ZkPass Dashboard](https://miro.medium.com/v2/resize:fit:1400/1*lDtRjHstbVnD3-2BIjgWuA.png  "ZkPass Dashboard")
ZkPass currently at pre-alpha stage. This image shows zkpass app dashboard.<br>
Templates show possible zkSBT's like having an instagram account over 100 followers.<br>
For this instance, there are 3 main steps for an user to proof his/her instagram account has over 100 followers and mint corresponding zero knowledge soul bound token:
1. User need to chose a field that want to Verify
    There are some trusted datasource offered in zkpass default template, user should chose and fill in the statement.<br> Moreover, ZkPass encourage users to apply more datasource and template by contributor programme.
2. Access to your datasource
    After Installing zkSBT tool kit, user will be asked to login his/her account to the specific website.
3. Verify & Mint zkSBT
    The field user would like to prove will be mint as a SBT by multi-party computing & zero-knowledge proof.<br><br>


# What is ZkPass Architecture?
![ZkPass Overall Architecture](https://2254424488-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FC2Jh1oquOpJPfwzD3x9L%2Fuploads%2FLMF0EDjIw8EJM71LSmnD%2FOverall%20Architecture%20-%20zkPass%20(1).png?alt=media&token=e78e6e3c-aa78-4de2-88bf-00e68ce5b6e5  "ZkPass Overall Architecture")

### Overall
zkPass primarily employs technologies such as Three-Party TLS (3P-TLS), Multi-party Secure Computation (MPC), and Zero-Knowledge Proof (ZKP). These technologies enable provers to convert any private data from HTTPS websites into zk proofs. At the same time, they ensure privacy protection and prevent data forgery by malicious users.<br><br>
### Data Layer 
This describes the various types of data sources that the zkPass Protocol is capable of handling, including public on-chain data and any off-chain private data secured by HTTPS. The zkPass Protocol then generates identity credentials by processing data according to the data persistence protocol and homomorphic encryption data lake standard.<br><br>
### Protocol Layer 
Contains the most important three sub-protocol modules implemented by zkPass Protocol, namely<br>
Oblivious TLS Protocol: implements an efficient 3-party TLS protocol, and supports both CBC and GCM block cipher modes;<br>
MPC Protocol: implements a data exchange protocol with low communication cost and encapsulates it as a component to provide external privacy computing services; <br>
ZKP Protocol: implements a memory-friendly zero-knowledge proof protocol, and provides two API methods to empower the Web3 privacy ecosystem.<br><br>

### Network Layer 
Contains the blockchain network that zkPass Protocol can support, and the main contract modules involved in the protocol, which are<br>
Task: task distribution smart contract;<br>
Template: support data source smart contracts;<br>
ZK-Verification: Zero-knowledge verification of smart contracts.<br><br>
### Identity Layer 
Authenticated users will end up with a series of sovereign data, including <br>
zkSBT: represents participation in certain types of identity authentication activities and ZK proof for privacy verification;<br>
typeSBT: represents a certain type of identity authentication activities participated in;<br> 
dateSBT: represents that the identity comes from a trusted data source; <br>
mainClaim: represents the main claim about the identity; <br>
queryClaim: represents the secondary claim included in mainClaim.<br><br>
### Product Layer 
The user's sovereign data represents various identities in the Web3 ecosystem, which can be applied across different Web3 and Web2 application scenarios.<br>
Integrating or building on top of the zkPass Protocol, zkPass Products with unique features will be developed to adapt to specific application scenarios.<br><br>

# How does it handle security and privacy concerns?
 As centralized organizations in the Web2 world predominantly hold sensitive private data, zkPass has reconstructed the standard TLS protocol. Combining trusted private data in Web2 and Web3 using leading MPC and ZKP technologies, zkPass provides a highly available private data layer for constructing DeSoc. This integrated solution offers a solid foundation for privacy protection.

### Reliability of Private Data Source
The reliability of the private data source is of utmost importance as it typically originates from centralized organizations such as government agencies, educational institutions, financial institutions, and other authorized entities that issue identification documents and records. These documents and records may include government-issued identification cards, diplomas, transcripts, bank account information, vehicle registration records, and more. To ensure the legitimacy of private data, zkPass verifies that it comes from trusted data sources that undergo a rigorous validation process.<br>
Furthermore, zkPass provides customizable and flexible templates designed for different users and business scenarios. These templates incorporate an audit mechanism that helps prevent malicious behavior by phishing websites, which aim to steal private data and undermine the reliability of the data source.<br>
### The Authenticity of Private Data
Ensuring the authenticity of private data is crucial, and zkPass employs advanced privacy computing techniques to achieve this. It leverages high-performance algorithms such as Oblivious Transfer (OT) and Garbled Circuit (GC) to implement secure Multi-Party Computation (MPC). This approach effectively prevents fraudulent behavior by customers attempting to tamper with their private data locally.<br>
During each round of identity verification, zkPass randomly assigns a group of zkPass Nodes, forming a client known as the zkPass Kit. The client accesses the trusted data source server using the standard Transport Layer Security (TLS) protocol, overseen by the zkPass Task Smart Contract. This ensures data security, as the zkPass Node only possesses the MacKey Share in the Session Key, which poses no threat to data security. In contrast, the zkPass Kit has the complete EncKey and the other half of the MacKey Share. This approach allows the zkPass Node to promptly detect and reject any fraudulent behavior if a client attempts to tamper with their private data locally.<br>
By utilizing advanced privacy computing techniques, zkPass ensures the authenticity of private data, making it a highly effective solution for protecting against identity fraud.<br>
### Privacy of Private Data
Privacy protection for private data is a top priority for zkPass. After a client's private data is committed, zkPass enables them to generate Zero-Knowledge Proofs (ZKPs) locally. This ensures that zkPass does not expose any privacy-related information. However, this process can be resource-intensive and slow, especially when the client's hardware resources are limited. To address these challenges, zkPass utilizes VOLE-based linear commitment and high-performance IZK algorithms.<br>
The interactive IZK algorithm eliminates the need for TrustSetup, allowing Provers and Verifiers to directly interact. It generates Vector Oblivious Linear Evaluation (VOLE) and commits to each gate using VOLE, resulting in improved processing efficiency. VOLE's linearity enables batch processing, allowing Provers and Verifiers to compute separately in their respective locations. The results can then be aggregated and verified, significantly enhancing computational efficiency.<br>
The advanced algorithms employed by zkPass ensure the secure and private handling of clients' private data, even with limited hardware resources. As a result, zkPass provides an effective solution for safeguarding sensitive private information, making it a critical tool for preventing identity theft and fraud.<br>
### Verifiability of Private Data
Verifiability is critical to identity data security, and zkPass offers a reliable solution. Once the customer's ZKP is generated, it can be uploaded to the blockchain, enabling anyone to verify their identity by simply calling the zkPass Verification Smartcontract.<br>
It is worth noting that this process only exposes the verification conditions and does not reveal any private information about the customer, such as whether they meet the access requirement of being over 18 years old. This feature is crucial for customers who want to keep their personal information private. For instance, they may send the ZKP directly to a specific program, enabling them to access the service while keeping their identity private.<br>
By providing this level of verifiability while maintaining customers' sensitive information private.<br>
### Private Data Diversity and Interoperability 
The zkPass protocol generates a zk-based Soul Bound Token (zkSBT) representing the client's unique data in a specific application scenario. The zkPass zkSBT adheres to the ERC-998 standard protocol, and other protocols do not require integration of this type. The SBT is structured as a Hash Tree, with leaves composed of various Claims originating from trusted data sources. zkPass validation occurs in two stages: the mClaim ZK proof verifies that the target field originates from a trusted data source and is within the mClaim Tree, while the qClaim ZK proof verifies that the target field is within the mClaim Tree and satisfies the logical assertion. Type representation includes tSBT (Type, e.g., "I am a car owner") and dSBT (Datasource, e.g., "Mercedes and BMW"). Through the tSBT, an auto alliance DAO can fully identify a car owner's identity and conduct subsequent derivative activities, demonstrating interoperability.<br><br>
The zkPass protocol supports diverse private data sources, ensuring individuals can securely and efficiently prove their private data in various scenarios. Additionally, the zkPass zkSBT structure, which conforms to the ERC-998 standard protocol, enables interoperability with other systems, facilitating the integration of identity data into various applications. Overall, zkPass provides a comprehensive and secure solution for private data verification in today's digital landscape.<br><br>


# Which protocols it uses and what is it for?
ZkPass built on with these core protocols: Three-Party TLS (3P-TLS), Multi-party Secure Computation (MPC), and Zero-Knowledge Proof (ZKP).

### MPC


Multi-party Computation (MPC) has its origins in the millionaire problem, which was proposed by Andrew Yao in 1982. MPC enables participants to collectively compute a function using their private inputs without revealing the inputs themselves. Even if one or more parties are compromised during the computation, MPC ensures the confidentiality of the participants' original secret data and guarantees the accuracy of the function's output.
Since the development of MPC theory, several specialized techniques have emerged, including Garbled Circuits (GC), Secret Sharing (SS), Homomorphic Encryption (HE), and Oblivious Transfer (OT). Each of these techniques addresses different aspects of privacy-preserving computation, offering unique security properties and performance characteristics.
The zkPass Protocol requires a significant number of bitwise operations. As a result, high-performance Oblivious Transfer Extension (OTE) and Garbled Circuits (GC) algorithms were chosen for implementation. These algorithms optimize the efficiency of secure computations while maintaining robust privacy guarantees, making them an ideal fit for the complex requirements of the zkPass Protocol. By utilizing these advanced MPC techniques, the zkPass Protocol can deliver a privacy-preserving, high-performance identity solution that meets the demands of the Web3 ecosystem.

![3P-TLS MPC](https://lh7-us.googleusercontent.com/ejD8G0zTtEepb4PWKdMtIT8KdMRLB3W-9IzAlMq03J-qPh4IcIQARaN4Aqt2uz48u3yGPNVpr5cWlZlgKmLI3qSrTIKcx4gF3R8AZrQhTLvfPa1vDTfOTW14kJ2bokozufPQUx6pmxDalfSpIEZmOA  "3P-TLS MPC")

This image shows How 3P-TLS & MPC Work on zkPass.

### 3P-TLS

In the 3P-TLS protocol, there are three key players: S, who serves as a trusted data source, P, the Prover/user, and V, the zkPass node. P and V collaborate as a client to establish secure communication with S through a series of stages.
The first stage involves a three-party handshake protocol. Here, P, V, and S collectively generate session keys. P and V each obtain a share of these keys. This is achieved using the Paillier encryption algorithm, which offers additive homomorphism. The pre-master key is divided into two parts, with P and V receiving one-half each, while S retains the complete pre-master key. Importantly, to prevent the client from forging fake websites, after the Client and Server exchange greetings, the Client will ask the Server to return the certificate. The subsequent key exchange phase also includes the server’s public key signature, which is signed by the private key of the certificate. This allows V within the Client to also obtain the certificate and signature for verification, ensuring trust in the data source.
In steps 6 and 7, P and V engage in MPC to compute the encryption key (enc_key) for data protection and the message authentication code key (mac_key) for data integrity. It’s essential to note that V only possesses a share of the mac_key and no enc_key. This ensures that V cannot access the user’s private information. In contrast, P holds a share of the mac_key, granting access to specific identity information without the ability to tamper with it. Any tampering can be detected by verifying message authenticity using the mac_key.
Steps 8 and 9 follow standard TLS protocol procedures for application data. In steps 10 to 12, P and V exchange keys in preparation for an upcoming phase involving zero-knowledge proofs.
At this point, the three-party TLS protocol concludes. The MPC algorithm of zkPass has undergone significant optimization in terms of communication time, hash functions for Garbler, Evaluator, and OT, as well as memory copying operations. This has resulted in an efficiency improvement of over threefold. Additionally, a new AES128 proof method has been adopted which has reduced the number of blocks by 300 times and improved Garbler/Evaluator execution time tenfold. Specifically, zkPass employs Silent OT for OT operations, effectively reducing offline network communication during OT generation. In terms of Garbled Circuits, zkPass utilizes Stacked GC which significantly reduces the size of Garbled Circuits thereby decreasing online communication and execution time. This overall optimization has substantially reduced the runtime of the entire MPC process.


![ZKP](https://lh7-us.googleusercontent.com/M9_rJi12xGu6Lnocwng2oyNjkrONofoiSX3Gxmqtn1hO0ZQSbSSxHTmBL9kACbd2xqS60ZZ2X4sPOpaKTq8jEIV0mnAb9dATFMyQKP8odmHDM6yguud4QUgq9USJMJihFhW5M9r8ZUcTvMgMGMKs7Q  "ZKP")

This image shows How interactive zero knowledge proofs Work on zkPass.

The final step of the zkPass protocol involves the client generating zero-knowledge proof, which the smart contract on the blockchain verifies. ZkPass employs a Hybrid Zero-Knowledge (ZK) approach that combines both interactive and non-interactive ZK protocols. 

### Interactive Zero-Knowledge (IZK):

ZkPass utilize a VOLE-based interactive Zero-Knowledge (ZK) protocol, which referred as VOLE-ZK 23. This protocol plays a crucial role in authentication, ensuring the data's origin from the precise data source and safeguarding it against tampering by clients. The VOLE-ZK 23 protocol can be described as a "commit and prove" framework. In this setup, both the Prover (P) and the Verifier (V) jointly generate numerous VOLE instances, each satisfying a linear formula denoted as "m = k + w * delta." P holds certain components of this formula as a commitment, with 'm' serving as the commitment, and 'w' can be converted into a witness after derandomization. 
On the other hand, V holds the remaining components ('k' and 'delta'). The objective is to prove and verify the satisfaction of a boolean circuit. P establishes a commitment for every gate based on the VOLE instance. Since the correlation between VOLE instances is linear, ZkPass can batch-check the results by summing up all commitments and confirming whether the final result still adheres to the correlation. This linearity is a key reason of ZkPass's solution is cost-effective, setting it apart from other high-degree polynomial solutions like SNARK. Consequently, P only needs to transmit two field elements (the sum of 'm' and the sum of 'w') to the Verifier. To protect sensitive information, a random linear combination can be created. V then validates the correlation using its VOLE parameters ('k' and 'delta').
There are five main constraints at this stage:
The vector x = (Q', R', mac_key_pv, b) represents the public signal, and w = (enc_key, token, Q, R) is the witness.

Dec(enc_key, Q') = Q, and Q = Query(token)

The first two constraints are related to the HTTP requests made to the trusted data source. The first constraint ensures that the request is encrypted using the encryption key. The second constraint specifies that the request must be generated using the user's access token, typically stored in cookies in most cases. These two constraints confirm that the user is using their personal data (such as a username and password) and is following a specific API defined in the template.

Dec(enc_key, R‘) = R

R' represents the response received from the trusted data source and is encrypted using the encryption key. Therefore, this constraint implies that the user must possess the encryption key, generated during a three-party handshake, to decrypt the response. This constraint serves to ensure that the user cannot create a counterfeit encryption key.

Verify(mac_key_pv, MAC, R) = 1

R stands for the decrypted response. It's crucial for the zkPass protocol to ensure that this response (R) remains unaltered by the user. To substantiate this, the constraint is applied. The additional MAC (Message Authentication Code) data attached to the end of R is generated using the MAC key. The verification process employs HMAC with the SHA256 hash function. This verification step serves as a safeguard against any unauthorized modifications to the response data by the user.

b = Assert(R)

The final constraint signifies that the data contained within R must adhere to specific conditions outlined in the template. For instance, if R is structured as a JSON object like {user: xxx, age: 30}, it necessitates that the "age" property must have a value greater than 18. In simpler terms, this constraint ensures that the data inside R complies with predetermined criteria.<br><br>


# Advantages of using ZkPass

- Privacy Protection: zkPass employs a combination of Multi-Party Computation (MPC), Zero-Knowledge Proofs (ZKP), and Three-Party Transport Layer Security (3P-TLS) to ensure that users can verify their data without revealing sensitive information. This robust privacy protection is crucial in an era where data breaches and privacy concerns are prevalent.

- Secure Data Verification: The use of advanced cryptographic techniques, including MPC and ZKP, ensures secure data verification. Users can prove the authenticity of their data without exposing the actual data itself, preventing unauthorized access and tampering.

- Diverse Use Cases: zkPass offers a range of use cases, such as decentralized authentication (ZkKYC), decentralized job marketplace, insurance claims processing, healthcare data marketplace, and undercollateralized DeFi lending. This versatility makes zkPass applicable in various industries and scenarios.

- Flexible Templates and Customization: zkPass provides users with templates and encourages the application of additional data sources through its contributor program. This flexibility allows users to adapt zkPass to their specific needs and scenarios.

- Reliability of Private Data Source: zkPass verifies the reliability of private data sources through a rigorous validation process. This helps ensure that the data used for verification comes from trusted and authorized entities, reducing the risk of using false or manipulated information.

- Verifiability of Private Data: zkPass enables users to verify their identity without revealing specific details. The zero-knowledge proofs can be uploaded to the blockchain, allowing anyone to verify the identity without exposing sensitive information.<br><br>

# Disadvantages of using ZkPass

- Complex Implementation: The use of advanced cryptographic protocols like MPC and ZKP can make zkPass complex to implement and understand. Users and developers may require a deep understanding of cryptography to effectively use and contribute to the protocol.

- Resource Intensiveness: Generating Zero-Knowledge Proofs (ZKPs) locally, as mentioned in the architecture, can be resource-intensive and slow, especially on hardware with limited capabilities. This could impact the user experience, particularly in scenarios with constrained computing resources.

- Dependency on Trusted Data Sources: The reliability of zkPass relies on the trustworthiness of the private data sources. If these sources are compromised or provide inaccurate information, it could undermine the effectiveness of zkPass in ensuring the authenticity of private data.

- Adoption Challenges: Adoption of zkPass may face challenges due to the need for users to download and use specific extensions (e.g., ZkPass Transgate). Achieving widespread adoption may require overcoming barriers related to user awareness and willingness to adopt new tools.

- Regulatory Considerations: The use of zkPass for identity verification and data processing may face regulatory challenges, especially in regions with stringent data privacy and security regulations. Ensuring compliance with these regulations is crucial for widespread acceptance.<br><br>

# How much is it related with Sphinx?

At Protocol Layer Sphinx and ZkPass uses TLS and ZKP in common. ZkPass uses a reconstructed version of TLS called 3P-TLS. 
ZkPass uses interactive ZK's


## Resources

- [ZkPass](https://zkpass.org "ZkPass") Jan 2024
- [ZkPass/Docs](https://zkpass.gitbook.io/zkpass/ "ZkPass Docs") Jan 2024
- [ZkPass/WhitePaper](https://docsend.com/view/5wdg66beu7m95jf3 "ZkPass WhitePaper") Jan 2024
- [ZkPass Github](https://github.com/zkPassOfficial "ZkPass Github") Jan 2024
- [ZkPass Investments](https://medium.com/zkpass/zkpass-raised-a-2-5m-seed-round-funding-af6419d3b50f "ZkPass Investments") Jan 2024
- [ZkPass Company Details](https://tracxn.com/d/companies/zkpass/__t3yqnfdP0JVik7J5UYRBnn9nRg66gfl8B1ogIkKsbTU "ZkPass Company Details") Jan 2024

