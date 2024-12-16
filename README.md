# aml
Resources for eID use in a UK AML process


“eID for AML”

An open standard electronic ID for KYC/AML:
A reference implementation for the UK

25th September 2024

AML
AML is complex:
FATF global recommendations
UK 25 regulators
Process diagram
 

Legal
•	Proceeds of Crime Act 2002; 
•	Anti-terrorism, Crime and Security Act 2001; 
•	The Money Laundering, Terrorist Financing (Amendment) (EU Exit) Regulations 2020 (ML Regulations); 
•	Counter Terrorism Act 2008; 
•	The Criminal Finances Act; and Systems and Controls (SYSC) Rules of the FCA Handbook

ID standards
There are many open standards for electronic/digital identity, including those from the Open Identity Foundation and W3C (see Appendix A for a list of standards, their use cases and adoption).

Implementing ID standards
There are essentially five levels of information, from high level to low detail, that enable service providers to build electronic identification services, and for firms in scope of AML to adopt digital services (‘electronic identification’) that help them become compliant, and for providers to build standards-based solutions:

1)	International recommendations – FATF
2)	National legislation – the UK Money Laundering Regulations (MLRs)
3)	Guidance – JMLSG, LSAG, CCAB, HMRC, FCA, (for ID, GPG44/45)
4)	Standards – 	for ID; OIDC, DIDs/VCs, mDLs
for governance/KYC; ISO29115, OIDC IDA
5)	Reference implementation of standards (this material “eID for AML”)

DSIT have published the DIATF, with 50 providers of ID&V (not all for AML use cases).
DIATF github repository (A Treharn) – data model for UK IDs

Examples of implementations of open standards for ID are:
•	EUDI wallet in github
•	Open Wallet Foundation

Benefits of an open standard implementation:
•	Open collaboration to define a model that works for the broadest use cases
•	Encourages adoption of best practice by the market
•	Open competition, from which the most effective services evolve
•	Interoperability with other solutions / countries
•	Easy common approach to integration for customers
•	No vendor lock-in to proprietary solutions for customers
•	No commercial fees; encourages adoption
•	Extensibility to connect to other capabilities / processes

Aims of “eID for AML”:
•	Collate existing guidance and standards, from which an authorised CAB can certify vendors that they meet the guidance (e.g. ACCS).
•	Establish a reference implementation for the provision of electronic ID data into an AML process, using open standards.
•	Gather input from DIATF IDPs to agree a common approach and best practice.
•	Gain buy-in from guidance authorities (HMRC, FCA, JMLSG, LSAG, CCAB etc.) and recognition in guidance as an industry-accepted process.
•	Accelerate adoption of electronic ID by firms in scope of AML

Scope of implementation
•	Electronic ID only?
•	CDD?
o	Source of funds
o	Source of wealth
o	Purpose of account / service
o	Record keeping
 
•	Risk assessment?
•	EDD?
•	AML?
o	PEPs (how to measure scope / effectiveness? Which lists?)
o	Sanctions (how to measure scope / effectiveness? Which lists?)
	OpenSanctions
o	Adverse media
o	Ongoing KYC
o	Transaction monitoring
o	Fraud screening
o	SARs

Where does ID end and risk assessment, AML decision start?
What should an open standard implementation cover?
Best to componentise it, do ID first?

Governing body
Which entity is best placed to govern, publish and maintain the reference implementation:
•	DSIT – OfDIA
•	FCA
•	DBT / Smart Data Forum
•	Input - CFIT – defining a ‘company ID’
 
International recommendations – FATF 
UK national legislation – MLRs

The MLRs cover the requirements for Customer Due Diligence (CDD), which is a key part of Anti-Money Laundering (AML) processes (AKA Know Your Customer (KYC)).
Part 3, Chapter 1, Regulation 28: Customer due diligence measures
(2) The relevant person must—
(a) identify the customer unless the identity of that customer is known to, and has been verified by, the relevant person;
(b) verify the customer's identity unless the customer's identity has already been verified by the relevant person; and
(c) assess, and where appropriate obtain information on, the purpose and intended nature of the business relationship or occasional transaction.

Part 3, Chapter 1, Regulation 28: Customer due diligence measures
(18) For the purposes of this regulation—
(a) except in paragraph (10), “verify” means verify on the basis of documents or information in either case obtained from a reliable source which is independent of the person whose identity is being verified;
(19) For the purposes of this regulation, information may be regarded as obtained from a reliable source which is independent of the person whose identity is being verified where—
(a) it is obtained by means of an electronic identification process, including by using electronic identification means or by using a trust service (within the meanings of those terms in Regulation (EU) No 910/2014 of the European Parliament and of the Council of 23rd July 2014 on electronic identification and trust services for electronic transactions in the internal market); and
(b) that process is secure from fraud and misuse and capable of providing [assurance that the person claiming a particular identity is in fact the person with that identity, to a degree that is necessary for effectively managing and mitigating any risks of money laundering and terrorist financing].] 

 
JMLSG guidance

Regulation 28(19)
5.3.52 Before using an organisation for digital identities, electronic or digital identity verification, or trust services, firms should be satisfied that information supplied by the provider is considered to be sufficiently extensive, reliable, accurate, independent of the customer, and capable of providing an appropriate level of assurance that the person claiming a particular identity is in fact that person. This judgment may be assisted by considering whether the provider meets the following criteria: 
➢ it is recognised, through registration with the Information Commissioner’s Office (or national equivalent for EEA/EU registered organisations), to store personal data; 
➢ it is accredited or certified to offer the identity verification service through a governmental or industry process that involves meeting minimum published standards; 
➢ it uses a range of multiple, positive information sources, including other activity history where appropriate, that can be called upon to link an applicant to both current and previous circumstances; 
➢ it accesses negative information sources, such as databases relating to identity fraud and deceased persons; 
➢ it accesses a wide range of alert data sources; 
➢ its published standards, or those of the scheme under which it is accredited or certified, require its verified data or information to be kept up to date, or maintained within defined periods of re- verification; 
➢ arrangements exist whereby the identity provider’s continuing compliance with the minimum published standards is assessed; and 
➢ it has transparent processes that enable the firm to know what checks were carried out, what the results of these checks were, and what they mean in terms of how much certainty they give as to the identity of the subject. 
➢ it keeps sufficient records of information used to provide its services.
5.3.53 In addition, an organisation should have processes that allow the enquirer to capture and store the information they used to verify an identity, and/or return a level of assurance that can be stored by the enquirer as evidence of the organisations’ verification processes.

Regulation 28(19)
5.3.52 eID should be sufficiently extensive, reliable, accurate, independent of the customer, right level of assurance
The provider should:

JMSLG requirement	OneID evidence
be registered with ICO	ICO registration 
be certified to a government process to published standards	DIATF certification, GPG44/45 standards

use multiple, positive information sources, including activity history	Bank account, CRA, Activity History
use negative information sources, such as identity fraud and deceased persons	Fraud data integration
access a wide range of alert data sources	CRAs, Fraud, DIATF fraud alerts
have published standards that require information to be kept up to date	DIATF
have continuing compliance with published standards	DIATF certification/surveillance audit/recertification
have transparent processes on checks carried out, results, and certainty as to identity of the subject	DIATF, OIDC Identity Assurance open standards, GPG Medium/High LoC
keep records	DIATF record keeping
5.3.53 allow the enquirer to capture and store identity information and LoA	RP record keeping, GPG Medium/High LoC
  
LSAG guidance

https://www.sra.org.uk/globalassets/documents/solicitors/firm-based-authorisation/lsag-aml-guidance.pdf?version=496f8e

LSAG Section 6.14.3 provides definitions of electronic IDs (and trust services) that are enabled for use in MLRs.

6.14.3 Electronic verification

As technology has developed, use of electronic identification and verification (EID&V) tools have become more common. While you can never outsource your ultimate responsibility, EID&V tools can be useful in protecting your practice. R28 sets out minimum requirements for EID&V processes to be regarded as reliable sources in applying CDD. 

Test for whether you are able to use an EID&V tool 

Meeting the definitions in the (R2014/910/EU of the European Parliament and of the Council of 23rd July 2014) as below

Electronic identification - means the process of using person identification data in electronic form uniquely representing either a natural or legal person, or a natural person representing a legal person

Trust service - means an electronic service normally provided for remuneration which consists of:
(a) the creation, verification, and validation of electronic signatures, electronic seals or electronic time stamps, electronic registered delivery services and certificates related to those services;
(b) the creation, verification and validation of certificates for website authentication; or (c) the preservation of electronic signatures, seals or certificates related to those services 

-and being secure from fraud, misuse and capable of providing an appropriate level of assurance that the person claiming a particular identity is in fact the person with that identity, to a degree that is necessary for effectively managing and mitigating any risks of money laundering and terrorist financing.

There is further information available on this in Section 7.

7.3 Electronic Verification

Legal practices may wish to make use of technology, particularly electronic identification and verification (EID&V) tools in order to help fulfil their obligations under the Regulations. Use of EID&V tools may be helpful in that they: 
•	can improve efficiency in customer identification and verification at on-boarding;
•	allow the undertaking of checks that may be resource intensive to be done more efficiently;
•	can be applied on a consistent basis from client to client; and 
•	can support ongoing due diligence and scrutiny of transactions throughout the course of the business relationship via automated monitoring of client/transaction features as set against red flags or risk factors. 

Electronic verification methods are becoming increasingly more secure and sophisticated and may in fact be lower risk than traditional means in some circumstances. They can be used both at client on-boarding stage and as a tool for ongoing monitoring and the reapplication of CDD. 

7.5 Tiered Services

Many digital ID providers will provide a tiered service, allowing practices to subscribe to varying levels of verification which should be utilised in proportion to the level of risk presented by any given client/matter. Greater technical reliability should be employed for higher risk ML/TF situations, and conversely, lower risk ML/TF situations may permit use of systems with lower levels of assurance for the purposes of simplified due diligence. When making this determination, you may also consider whether the provider: 
•	can link an applicant to both current and previous circumstances using a range of positive information sources; 
•	accesses negative information sources, such as databases on identity fraud and deceased persons; 
•	accesses live databases of politically exposed persons and individuals/entities subject to sanctions (see Section 6); 
•	accesses more than one relevant data source; 
•	has transparent processes enabling you to know what checks are carried out, the results of the checks, and how much certainty they give on the identity of the subject; and 
•	allows you to capture and store the information used to verify an identity 

7.6 Digital ID Certifications

FATF Guidance recommends providers of EID&V seek assurance testing and certification by the government, an approved expert body, or another internationally reputable expert body.

 
CCAB guidance

https://www.ccab.org.uk/wp-content/uploads/2023/08/AMLGAS-update-June-2023-APPROVED.pdf

5.1.9 The identification phase requires the gathering of information about a client’s identity and the purpose of the intended business relationship. Appropriate identification information for an individual would include full name, date of birth and residential address. This can be collected from a range of sources, including the client.

5.4.13 Client verification means to verify on the basis of documents or information obtained from a reliable source which is independent of the person whose identity is being verified.

Use of electronic data
5.4.17 Businesses may choose to use electronic identification processes either on their own or in conjunction with other paper-based evidence, on a risk-based approach. A number of subscription services, many of them online, give access to identity-related information. A broad variety of electronic verification systems exist, including those drawing on multiple sources, those relying on the self-capture of documentation using an interactive application and those that provide credentials which confirm a third party has validated the ID. 

5.4.18 Before using any electronic service, firms should ensure they understand the basis of the systems they use and question whether the information is reliable, comprehensive and accurate. The process should be secure from fraud and misuse and capable of providing an appropriate level of assurance that the person claiming a particular identity is in fact the person with that identity, to a degree that is necessary for effectively managing and mitigating any risks of money laundering and terrorist financing. Consider the following: 
•	Does the system draw on multiple sources? A single source (e.g. the electoral register) is not usually sufficient unless there are additional controls to validate the information. A system that combines negative and positive data sources is generally more robust. 
•	Are the sources checked and reviewed regularly? Systems that do not update their data regularly are generally more prone to inaccuracy. 
•	Are there control mechanisms to ensure data quality and reliability? Systems should have built-in data integrity checks which, ideally, are sufficiently transparent to prove their effectiveness. 
•	Is the information accessible? It should be possible to either download and store search results in electronic form or print a hard copy that contains all the details required (name of provider, original source, date, etc.). 
•	Does the system provide adequate evidence that the client is who they claim to be? Consideration should be given as to whether the evidence provided by the system has been obtained from an official source, e.g. the certificate of incorporation from the official company registry or a passport.

This part suggests eID is at the bottom of the ‘hierarchy’!
Need to fix this perception, e.g. need legal equivalence of eID

9.3 APPENDIX B: CLIENT VERIFICATION Documentation purporting to offer evidence of identity may emanate from a number of sources. These documents differ in their integrity, reliability and independence. Some are issued after due diligence on an individual’s identity has been undertaken; others are issued on request, without any such checks being carried out. There is a broad hierarchy of documents: • Certain documents issued by government departments and agencies, or by a court; then • Certain documents issued by other public sector bodies or local authorities; then • Certain documents issued by regulated firms in the financial services sector; then • Those issued by other firms subject to the 2017 Regulations, or to equivalent legislation; then • Those issued by other organisations, including providers of electronic identification services

B.1.3 For information obtained from an electronic identification process to be regarded as reliable, the process must be secure from fraud and misuse and capable of providing an appropriate level of assurance that the person claiming a particular identity is in fact the person with that identity. 

B.1.4 The following is a suggested non-exhaustive list of sources of evidence for individuals: 
• Valid passport; 
• Valid photo card driving licence; 
• National Identity card (non-UK nationals); 
• Identity card issued by the Electoral Office for Northern Ireland; 
• A check provided via an electronic identification process that meets the criteria to be relied upon.
