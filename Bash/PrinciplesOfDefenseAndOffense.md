# Principles of DEFENSE and OFFENSE

## Cybersecurity  [5 principles] 

- Confidentiality
- Integrity 
- Availability
- Non-Repudiation
- Authentication 

### Confidentiality 
Information has *confidentiality* if it can be accessed and read only by authorized users. Violating confidentiality is often the goal of many cyberattacks. <u> To violate confidentiality attackers may intercept the information while in transit (such as an insecure WiFi connection or the internet), or they may bypass security controls on a system to steal the information while at rest. </u>

Information commonly targeted by attackers includes personal communication (e-mail, text messages), pictures, trade secret, payment information (credit/debit card numbers), personal identifiers (social security numbers), and sensitive government and military information.

Encryption and access control are typical mechanisms used to protect confidentiality. 

### Integrity 
Information has *integrity* if it can be modified only by authorized users. Integrity should be verifiable, meaning it should be easy to determine if information has been modified by an unauthorized third party.

Integrity can be violated while information is in transit or at rest, and that violation can be accidental or intentional. Accidental incidents include incorrect data entry, hardware failure, and effects from solar radiation. Intentional incidents include unauthorized modification of a file, database, or network packet.

Cryptographic hashing is often used to verify integrity of information.

### Availability
Information is considered *available* if it can be accessed when and where it is needed. Access to information should also be timely and convenient for the user.

Attacks against availability are becoming increasingly popular among nation-states and hacktivists, as they have an immediate and visible effect. Accidental incidents include loss of power, hardware failure, or software failure. Intentional acts include distributed denial-of-service (DDoS) attacks and ransomware attacks. 

Redundancy, data and power backups, and failover sites are typical used to maintain high availability rates.

### Nonrepudation 
*Nonrepudation* links an entity (user,program,etc.) to actions taken by that entity. For example, a person's signature on a legal contract can be used to prove that the person agreed to the terms of the contract. It is difficult for the person who signed the contract to later deny or repudiate doing so because the evidence of the signature exists.
Common methods to ensure nonrepudiation include user authentication, digit signatures, and system logging.

### Authentication 
*Authentication* deals with positively identifying and verifying the identity of a user. This is a critical component to ensuring that only authorized users can be access or modify information. Authentication mechanisms are one of the most targeted aspects of information systems, as the success of the other four principles is often dependent upon it. 

Common mechanisms used for authentication include usernames and passwords, electronic key cards, and biometrics



## The Attack Life Cycle 

