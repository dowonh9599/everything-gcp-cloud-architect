# Security

Security infrastructure that Google Cloud and Google services run on:

### Hardware infrastructure layer

**Custom-designed equipments by Google**

* server boards
* networking equipment
* chips, including a hardware security chip that's currently being deployed on both servers and peripheral.

**secure boot stack.**

variety of technologies to ensure that they are booting the correct software stack, such as:

* cryptographic signatures over the BIOS
* bootloader
* kernel
* base operating system image.

**premises security**

* designs and builds its own data centers, which incorporate multiple layers of physical security protections.
* Access to these data centers is limited to only a very small number of Google employees.

### Service deployment layer

**encryption of inter-service communication.**&#x20;

* Google’s infrastructure provides cryptographic privacy and integrity for remote procedure call (“RPC”) data on the network.
*   Google’s services communicate with each other using RPC calls.

    User identity layer.
* automatically encrypts all infrastructure RPC traffic that goes between data centers.&#x20;
* hardware cryptographic accelerators that will allow it to extend this default encryption to all infrastructure RPC traffic inside Google data centers.

**Google’s central identity service**

* intelligently challenges users for additional information based on risk factors (devise-wise and location-wise sign-in history)
* 2FA sign-in, including devices based on the Universal 2nd Factor (U2F) open standard.

### Storage services layer

**encryption at rest security feature**

* encryption using centrally managed keys is applied at the layer of storage services.
* hardware encryption support in hard drives and SSDs.

### **Internet communication layer**

* Google services that are being made available on the internet,&#x20;
  * follows best practices such as supporting perfect forward secrecy
  * register themselves with an infrastructure service called the Google Front End, which ensures that all TLS connections are ended using a public-private key pair and an X.509 certificate from a Certified Authority (CA).
  * The GFE protections against Denial of Service attacks.
  * Denial of Service (“DoS”) protection.&#x20;
  * The sheer scale of its infrastructure enables Google to simply absorb many DoS attacks.
  * multi-tier, multi-layer DoS protections that further reduce the risk of any DoS impact on a service running behind a GFE.

### Google's Operational security layer

**intrusion detection**.

* Rules and machine intelligence give Google’s operational security teams warnings of possible incidents.
* Google conducts Red Team exercises to measure and improve the effectiveness of its detection and response mechanisms.&#x20;

**reducing insider risk**

* Google aggressively limits and actively monitors the activities of employees who have been granted administrative access to the infrastructure.

**Employee U2F use**

* require use of U2F-compatible Security Keys to guard against phishing attacks against Google employees.

**Stringent software development practices**

* employs central source control and requires two-party review of new code
* provides its developers libraries that prevent them from introducing certain classes of security bugs.
* runs a Vulnerability Rewards Program where we pay anyone who is able to discover and inform us of bugs in our infrastructure or applications.
