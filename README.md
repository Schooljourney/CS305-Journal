# CS305-Journal



Practices for Secure Software Report

 
Table of Contents
DOCUMENT REVISION HISTORY	3
CLIENT	3
INSTRUCTIONS	3
DEVELOPER	4
1. ALGORITHM CIPHER	4
2. CERTIFICATE GENERATION	4
3. DEPLOY CIPHER	4
4. SECURE COMMUNICATIONS	4
5. SECONDARY TESTING	4
6. FUNCTIONAL TESTING	4
7. SUMMARY	4
8. INDUSTRY STANDARD BEST PRACTICES	4

 
Document Revision History

Version	Date	Author	Comments
1.0
1.1	4-13-2025
4-14-2025	Kimberly Blackwood	Project started

Client

 

Instructions

Submit this completed practices for secure software report. Replace the bracketed text with the relevant information. You must document your process for writing secure communications and refactoring code that complies with software security testing protocols.

•	Respond to the steps outlined below and include your findings. 
•	Respond using your own words. You may also choose to include images or supporting materials. If you include them, make certain to insert them in all the relevant locations in the document.
•	Refer to the Project Two Guidelines and Rubric for more detailed instructions about each section of the template.
 
Developer
Kimberly Blackwood


1.	Algorithm Cipher

a. Provide a brief, high-level overview of the encryption algorithm cipher

After I reviewed  the scenario that was given, I decided that AES which is Advanced Encryption Standard because it is symmetric block cipher widely used for transmission and storage. It can provide a strong level of security.

b. Discuss the hash functions and bit levels of the cipher.

SHA-256 is the best algorithm for Artemis Financial. This is because it provides 256-bit hash value. Making it suitable for verifying the public key accuracy during client downloads (Oracle, 2013).

Hash functions and bit levels of the cipher are intended for password security, data integrity and the prevention of duplication by hackers. Artemis financial should use this recommendation because it has:
•	Tamper detection: Identifies unauthorized modifications to protected data.
•	Version control: Allows tracking different iterations of files.
•	Authentication: Proves data legitimacy and origin through certificate matching.
•	Efficiency: Compact hash fingerprints enable faster processing than encrypting entire files (S Detect, 2024).

c. Explain the use of random numbers, symmetric verses non-symmetric keys, and so on.

The use of random numbers, symmetric verses non-symmetric keys, and so on are very vital for Artemis Financial because, random numbers ensure the security of online transaction, generate unique IDs, and guarantee the integrity of the data (NIST 2025). Symmetric verses non- symmetric keys, symmetric encryption uses a  single key for both encryption and decryption. This makes it very efficient for encrypting large amounts of data. 
In symmetric key encryption the message is encrypted by using a key and the same key is used to decrypt the message which makes it easy to use but less secure. It also requires a safe method to transfer the key from one party to another.
•	It uses one key for both encryption and decryption.
•	Faster and more efficient for large amount of data.
•	Requires a secure method to share the key between sender and receiver.
•	Common algorithms include AES, DES, Blowfish.
•	It is used in file encryption, VPNs, and secure data storage.

Non-symmetric key encryption is one of the most common cryptographic methods that involve using a single key and its pendent, where one key is used to encrypt data and the second one is used to decrypt an encryption text. The second key is kept highly secret, while the first one which is called a public key can be freely distributed among the service users.
•	It uses two keys a public key for encryption and a private key for decryption.
•	More secure but slower than symmetric encryption.
•	No need to share the private key, reducing the risk of exposure.
•	Common algorithms include RSA, ECC.
•	It is used for digital signatures, SSL/TLS, and secure email communications (ResearchGate,2024).


d. Describe the history and current state of encryption algorithms. 

Looking back to how cryptography was used, early civilizations like the Egyptians were early adopters of them. The Egyptians had their hieroglyphics which was used for their texts. Hieroglyphics showed things such as how they lived their lives, their rules, and just about everything else. One of the ways that Egyptians used their cryptic hieroglyphics were by monks and they used “nonstandard hieroglyphics to keep anyone outside of their inner circle from understanding what was being communicated” (Levinsky, 2022). With this historical data we are aware that the encryption algorithm is not something new. Ancient civilizations used it in several aspects of their lives to keep outsiders at bae. We currently do the same by writing codes with special encryption to keep hackers away.
In our modern-day society encryption carries a heavy load. We use it to protect medical records, email messages, banking transaction and our national security. We can send data across public computer networks because it is unreadable to all but the sender and the intended receiver. Currently encryption tools rely on complex math problems that conventional computers find difficult or impossible to solve. The algorithms NIST has standardized are based on different math problems that would block both conventional and quantum computers (NIST 2025).


2.	Certificate Generation
Insert a screenshot below of the CER file.

 

 
3.	Deploy Cipher
Insert a screenshot below of the checksum verification.

 

4.	Secure Communications 
Insert a screenshot below of the web browser that shows a secure webpage.

 

 

 

5.Secondary Testing
Insert screenshots below of the refactored code executed without errors and the dependency-check report.

 


 

6.Functional Testing
Insert a screenshot below of the refactored code executed without errors.

 
 
 
 
 


 
Before Refactoring-
 



After Refactoring-
 
7..Summary
Discuss how the code has been refactored and complies with security testing protocols. In the summary of your practices for secure software report, be certain to address the following items:
a.Refer to the vulnerability assessment process flow diagram in the Supporting Materials section. Highlight the areas of security that you addressed by refactoring the code.
The areas of security that I addressed by refactoring the code are:
1. Cryptography- is important to secure sensitive data and transactions, while ensuring confidentiality. For Artemis financial when storing and receiving data this maintains customers trust and prevents fraud. Applying this will ensure that they comply to the Gramm Leach Billey Act. The Gramm-Leach-Bliley Act requires financial institutions – companies that offer consumers financial products or services like loans, financial or investment advice, or insurance – to explain their information-sharing practices to their customers and to safeguard sensitive data (Federal Trade Commission, 1999)
 2. Code error- testing for code error ensures that the system is robust especially with input validation. For Artemis Financial this prevents unauthorized users from having access to personal information. This will ensure that the code does what it is supposed to do by following the security measures. This is where I did checksum to detect errors that may have occurred during the code transmission.
3. Code quality- ensures the reliability, security, and stability of Artemis Financial system.  It manages errors and adheres to security code practices. I updated the dependencies in pom.xml. file and fixed crucial and high  vulnerabilities.
4. Client server- for Artemis financial I enforced HTTPs secured communication.  

5.	Added unique string: String data =
     "Hello Kimberly Blackwood!";
6.Implemented the SHA-256 algorithm using : MessageDigest digest = MessageDigest.getInstance("SHA-256");
7.Hex conversion for better readability using: String checksum = bytesToHex(hash);Edited the return method using HTML format: 
return "<p>data: " + data + "</p>" + 
"<p>Algorithm: SHA-256</p>" +
"<p>Checksum: " + checksum + "</p>";
8. I changed pom. Xml by adding the latest version of the different spring boot libraries. This reduced vulnerabilities and focused on eliminating the critical ones.
9. I did iteration to identify and mitigate vulnerabilities.
10. I verified that vulnerabilities were gone.

8.Industry Standard Best Practices: Explain how you applied industry standard best practices for secure coding to mitigate known security vulnerabilities. Be sure to address the following 
items:
a.Explain how you used industry standard best practices to maintain the software application’s existing security.
I used industry standards practices to maintain Artemis Financial software application security by conducting regular testing, updates, and implanting strong security measures such as: 
•	Encryption 
•	Access control,
•	Secure dependency management by using the checksum tool and following OWASP recommendation.  
•	Input validation
b. Explain the value of applying industry standard best practices for secure coding to the company’s overall well-being

Applying industry standard best practices for secure coding is essential for Artemis Financial overall well-being because it reduces vulnerabilities, minimize financial risk, and improves user’s trust. This will provide protection for sensitive data and makes the software more resilient and ensures the success of the company.
















References

Federal Trade commission.(1999) The Graham Leach Billey Act. https://www.ftc.gov/business-guidance/privacy-security/gramm-leach-bliley-act

Keyfactor. (2020). When To Use Symmetric Encryption Verses Non-Symmetric Encryptioonhttps://www.keyfactor.com/blog/symmetric-vs-asymmetric-encryption

Levinsky,J.(2022). Encryption The History and Implementation.https://soar.suny.edu/bitstream/handle/20.500.12648/12073/4418_Jacob_Levinsky.pdf?sequence=1&isAllowed=y

NIST.(2025). Numbers for Cryptography https://csrc.nist.gov/csrc/media/events/random-number-generation-workshop-2004/documents/developmenthistory.pdf

Oracle.(n.d) Standard Names for JDK Security Providers.Oracle.https://docs.oracle.com

ResearchGate.(2024).Comparing Symmetric and Asymetrix Key.https://www.researchgate.net/publication/354859313_A_Comparative_Study_on_Symmetric_and_Asymmetric_Key_Encryption_Techniques

Score Detect. (2024). Securing Digital Access with Cryptographic Hashinghttps://www.scoredetect.com




MODULE 8 JOURNAL
Kimberly Blackwood
SNHU
Cs305 Module 8 Journal
Professor Wayne Morris


1.Briefly summarize your client, Artemis Financial, and its software requirements. Who was the client? What issue did the company want you to address?
Artemis Financial is a consulting company that develops individualized financial plans for its customers. The financial plans include savings, retirement, investments, and insurance. Artemis Financial wants to modernize its operations. As a crucial part of the success of its custom software, the company also wants to use the latest and most effective software security, to protect sensitive client data.
Artemis Financial has a RESTful web application programming interface (API). The 
company is seeking Global Rain, my employer for their expertise on how to protect the organization from external threats. Threats such as unauthorized access and data breaches. 
The requirements include implementing the most recent security best practices while ensuring compliance to cyber security practice and support  secure communication through their digital infer structure.

2.What did you do well when you found your client’s software security vulnerabilities? Why is it important to code securely? What value does software security add to a company’s overall well-being?
When I found my clients software security vulnerabilities, I interpreted the results from the manual review and static testing report. I identified the steps to mitigate the security vulnerabilities for Artemis Financials’ software application. I implemented encryption methods in the java code, I updated all the outdated  dependencies to eliminate code vulnerabilities by updating the JAVA version  and remove hardcoding credentials to reduce the risk of unauthorized access. It is important to code securely because it prevents potential vulnerabilities that can expose data or cause harm within the system.  And introduce financial losses to the company.

What value does software security add to a company’s overall well-being?
For a company’s overall well -being software security adds value because it protects the company’s reputation, customers trust and financial security. With a strong software security companies can  prevent leak of sensitive information and theft.
3.Which part of the vulnerability assessment was challenging or helpful to you?
 Filtering false positive was very helpful to me because it : 
•	Focus on real security issues, instead of wasting time on non-critical vulnerabilities.
•	Enable better management of resources, by directing efforts towards real threats.
•	Increase accuracy in assessment, getting clear picture of the actual vulnerabilities.
•	Improve efficiency of the security scanning process, this reduces the time, and efforts spend on investigating and resolving the false alarms.
•	Allows developers to focus on real security risk.


4.How did you increase layers of security? In the future, what would you use to assess vulnerabilities and decide which mitigation techniques to use?
I increased the layers of security by adding:
Collision resistance- this  refers to a desired property of cryptographic hash functions where it is difficult to find two different input values that result in the same hash value output. This makes it infeasible for attackers to find inputs that collide or match the same hash. SHA-256 is designed to be highly collision resistant. It will prevent hackers from inputting information into their system.  It is supported by JAVA security, which means it utilizes the security framework and tools provided by the JAVA platform to ensure the security of the application. As a result, in it will provide developers and administrators tools 

Checksum -which is crucial to ensure the integrity of the files being downloaded. 

Cipher-  AES which is Advanced Encryption Standard because it is a symmetric block
cipher widely used for transmission and storage. It can provide a strong level of security.
Implement an SSL certificate.

In the future I would identify potential weakness in the code and filter out all the false positives  to assess vulnerabilities and decide which mitigation techniques to use. I would also use multifactor authentication, this will reduce unauthorized access, protect against phishing, and  ransomware attacks  while ensuring  compliance with governmental regulations/


5.How did you make certain the code and software application were functional and secure? After refactoring the code, how did you check to see whether you introduced new vulnerabilities?
To make certain the code and software application were functional and secure I conducted  several test runs. I conducted frequent test with checksum tool generating a report and looking at the dependency and CVE report and removed the vulnerabilities. After I refactored a code, I did another review of  dependency check. After refactoring the code,  I ran test very often to  check to see whether I introduced new vulnerabilities,
To make sure there were no errors I tested it code and updated the libraries. I update the code to meet the requirement by adding the checksum .I ran status tool and looked at the security aspects. I did it by iteration to suppress false positives.
6.What resources, tools, or coding practices did you use that might be helpful in future assignments or tasks?
There are several resources that I used that will be helpful in the future. These include having the  ability to create an HTML report in Eclipse where I used a plug-in into the pom xml file that shows all the dependencies and the NIST website. I used encryption coding practice such as collision resistance and  I also utilized  peer review with  professional JAVA developers.
7.Employers sometimes ask for examples of work that you have successfully completed to show your skills, knowledge, and experience. What might you show future employers from this assignment?

I would show my future employer the Vulnerability Report. In this assignment my ability to follow the current OWASP dependency check tutorial to  intergrade the Maven dependency check plug-in into the pom.xml file was shown. This assignment  shows how I ran the dependency check to document the known vulnerabilities in the HTML file. I was able to create a suppression.xml file and revise the code in my software application’s pom.xml file. I was also able to  make revision to change the configuration settings of the dependency check in Maven and pointed it  to the suppression.xml file. 


![image](https://github.com/user-attachments/assets/7396b51c-5e0e-4f99-8063-3d4e4df80629)




