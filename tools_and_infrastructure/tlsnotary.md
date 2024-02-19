

![TLS Notary align="left"](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT-Sg3rZyhgMiVaVT_mkfNRfjcv6PiGZIHpHg&usqp=CAU "TLS Notary")

# TLS Notary
---
<br>
# What is TLS Notary briefly?

Data Provenance without Compromising Privacy, That is Why!
The Internet currently lacks effective, privacy-preserving Data Provenance. TLS, also known as the "s" in "https" 🔐 to the general public, ensures that data can be securely communicated between a server and a user. But how can this user credibly share this data with another user or server without compromising security, privacy, and control?

Enter TLSNotary: a protocol enabling users to export data securely from any website. Using Zero Knowledge Proof (ZKP) technology, this data can be selectively shared with others in a cryptographically verifiable manner.

TLSNotary makes data truly portable and allows a user, the Prover, to share it with another party, the Verifier, as they see fit.

# How Does the TLSNotary Protocol Work?
The TLSNotary protocol consists of 3 steps:

- The Prover requests data from a Server over TLS while cooperating with the Verifier in secure and privacy-preserving multi-party computation (MPC).<br>
- The Prover selectively discloses the data to the Verifier.<br>
- The Verifier verifies the data.<br>

![TLS Notary ](https://docs.tlsnotary.org/diagrams/overview_prover_verifier.svg "TLS Notary ")

① Multi-party TLS Request<br>
TLSNotary works by adding a third party, a Verifier, to the usual TLS connection between the Prover and a Server. This Verifier is not "a man in the middle". Instead, the Verifier participates in a secure multi-party computation (MPC) to jointly operate the TLS connection without seeing the data in plain text. By participating in the MPC, the Verifier can validate the authenticity of the data the Prover received from the Server.<br>

The TLSNotary protocol is transparent to the Server. From the Server's perspective, the Prover's connection is a standard TLS connection.<br>

② Selective Disclosure<br>
The TLSNotary protocol enables the Prover to selectively prove the authenticity of arbitrary parts of the data to a Verifier. In this selective disclosure phase, the Prover can redact sensitive information from the data prior to sharing it with the Verifier.<br>

This capability can be paired with Zero-Knowledge Proofs to prove properties of the redacted data without revealing the data itself.<br>

③ Data Verification<br>
The Verifier now validates the proof received from the Prover. The data origin can be verified by inspecting the Server certificate through trusted certificate authorities (CAs). The Verifier can now make assertions about the non-redacted content of the transcript.<br>

# TLS verification with a general-purpose Notary
Since the validation of the TLS traffic neither reveals anything about the plaintext of the TLS session nor about the Server, it is possible to outsource the MPC-TLS verification ① to a general-purpose TLS verifier, which we term a Notary. This Notary can sign (aka notarize) ② the data, making it portable. The Prover can then take this signed data and selectively disclose ③ sections to an application-specific Verifier, who then verifies the data ④.


![TLS Notary  ](https://docs.tlsnotary.org/diagrams/overview_notary.svg "TLS Notary  ")


In this setup, the Notary cryptographically signs commitments to the data and the server's identity. The Prover can store this signed data, redact it, and share it with any Verifier as they see fit, making the signed data both reusable and portable.<br><br>

Verifiers will only accept the signed data if they trust the Notary. A data Verifier can also require signed data from multiple Notaries to rule out collusion between the Prover and a Notary.<br><br>

# What Can TLSNotary Do?
TLSNotary can be used for various purposes. For example, you can use TLSNotary to prove that:<br><br>

- you have access to an account on a web platform
- a website showed specific content on a certain date
- you have private information about yourself (address, birth date, health, etc.)
- you have received a money transfer using your online banking account without revealing your login credentials or sensitive financial information
- you received a private message from someone
- you purchased an item online
- you were blocked from using an app
- you earned professional certificates<br>
While TLSNotary can notarize publicly available data, it does not solve the "oracle problem". For this use case, existing oracle solutions are more suitable.<br><br>

# What TLS version does TLSNotary support?
TLSNotary currently supports TLS 1.2. TLS 1.3 support will be added in 2024.<br><br>

# Who is behind TLSNotary?
TLSNotary is developed by the Privacy and Scaling Exploration (PSE) research lab of the Ethereum Foundation. The PSE team is committed to conceptualizing and testing use cases for cryptographic primitives.<br><br>

TLSNotary is not a new project; in fact, it has been around for more than a decade.<br><br>

In 2022, TLSNotary was rebuilt from the ground up in Rust incorporating state-of-the-art cryptographic protocols.<br>This renewed version of the TLSNotary protocol offers enhanced security, privacy, and performance.<br><br>

Older versions of TLSNotary, including PageSigner, have been archived due to a security vulnerability<br>

# Advantages of using TLSNotary

- Data Provenance with Privacy: TLS Notary allows users to prove the authenticity of data without compromising privacy. It enables selective disclosure of information, preserving user privacy while still providing cryptographic proof of data origin.

- Secure Multi-Party Computation (MPC): By employing MPC techniques, TLS Notary ensures that neither the Verifier nor the Prover can see the plaintext data during transmission, maintaining the integrity of the process.

- Selective Disclosure: Users have control over which parts of the data they disclose to the Verifier, allowing them to redact sensitive information while still proving the authenticity of the remaining data.

# Disadvantages of using TLSNotary

- Dependence on Trust: Verifiers must trust the Notary to accept the signed data. If there are concerns about the integrity or trustworthiness of the Notary, it could undermine the reliability of the verification process.

- Complexity: Implementing TLS Notary may introduce complexity into systems and applications, particularly in integrating with existing infrastructure and ensuring proper handling of cryptographic operations.

- Limited TLS Version Support: As of the provided information, TLS Notary supports TLS 1.2, with plans to add support for TLS 1.3 in the future. This limitation may restrict its compatibility with systems that rely on newer TLS versions.

- Not Suitable for All Use Cases: While TLS Notary is versatile, it may not be suitable for every use case, particularly those requiring real-time or continuous verification of data authenticity.

Overall, TLS Notary offers a promising solution for privacy-preserving data provenance, but careful consideration of its implementation and suitability for specific use cases is essential.


## Resources

- [TLS Notary](https://tlsnotary.org/ "TLS Notary") Feb 2024
- [TLS Notary/Docs](https://docs.tlsnotary.org/intro.html "TLS Notary Docs") Feb 2024


