# TLS Notary
---

![TLS Notary](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT-Sg3rZyhgMiVaVT_mkfNRfjcv6PiGZIHpHg&usqp=CAU "TLS Notary")

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





## Resources

- [TLS Notary](https://tlsnotary.org/ "TLS Notary") Feb 2024
- [TLS Notary/Docs](https://docs.tlsnotary.org/intro.html "TLS Notary Docs") Feb 2024


