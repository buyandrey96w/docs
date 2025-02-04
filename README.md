# Glossary and Guides

## Table of Contents
- [Glossary](#glossary)
  - [ASN](#asn)
  - [Assignment Request](#assignment-request)
  - [Business Account](#business-account)
  - [Certificate of Authorisation](#certificate-of-authorisation)
  - [CIDR](#cidr)
  - [LOA (Letter of Authorization)](#loa-letter-of-authorization)
  - [Minimal Lease Period](#minimal-lease-period)
  - [Minimal Order Period](#minimal-order-period)
  - [Minimal Split Size](#minimal-split-size)
  - [PandaDoc](#pandadoc)
  - [Prefix](#prefix)
  - [rDNS](#rdns)
  - [IP-Blocks](#ip-blocks)
  - [Stripe](#stripe)
  - [Stripe Connected Accounts](#stripe-connected-accounts)
  - [RIR (Regional Internet Registry)](#rir-regional-internet-registry)
  - [RIPE NCC](#ripe-ncc)
  - [RIPE Maintainer Attributes](#ripe-maintainer-attributes)
  - [ARIN Maintainer Attributes](#arin-maintainer-attributes)
  - [VAT](#vat)
  - [VAT Number](#vat-number)
- [Guides](#guides)
  - [Importing a Business Account](#importing-a-business-account)
  - [Editing a Business Account](#editing-a-business-account)
  - [Stripe Onboarding](#stripe-onboarding)
  - [Importing an IP-Block](#importing-an-ip-block)
  - [Assignment Request](#assignment-request-1)
  - [rDNS Request](#rdns-request)

## Glossary

### ASN
[ASN](#asn) stands for Autonomous System Number. It is a unique identifier assigned to an autonomous system (AS) in the Internet that participates in the Border Gateway Protocol (BGP). An autonomous system is a collection of connected Internet Protocol (IP) routing prefixes under the control of one or more network operators that has a single, clearly defined routing policy.

In practical terms, an [ASN](#asn) is used by routers in the Internet to exchange information about IP routing paths. Each AS has a unique [ASN](#asn), which is used to identify it to other ASes and to BGP routers in the Internet. This enables routers to determine the best path for traffic to take as it travels between different ASes and across the Internet.

ASNs are assigned by the Internet Assigned Numbers Authority (IANA) to regional Internet registries, which in turn allocate them to individual organizations or Internet Service Providers (ISPs) that operate autonomous systems.

### Assignment Request
The **Assignment Request** (AR) process is initiated by the Customer after successfully completing an order to rent an [IP-Block](#ip-blocks). Other participants in the process include the Supplier of the [IP-Block](#ip-blocks) (from whom the Customer placed the order) and the InterLIR Manager.

The outcome of the process is that the Customer can announce an [ASN](#asn) on the [IP-Block](#ip-blocks) using an **LOA** (Letter of Authorization) and utilize the rented block in accordance with the signed contract and the rules governing the use of the rented resource.

You can read the rental rules in the [General Terms and Conditions for the Use of the Internet Site interlir.com](https://interlir.com/terms-of-service/) section.

### Business Account

A Business Account (BA) is a representation of your organization on the InterLIR portal.

Without a BA, you can only view the marketplace. 

After adding BA, all other functions of the platform become available to you, such as renting blocks through the marketplace or renting out blocks, and much more.


### Certificate of Authorisation
The **Certificate of Authorisation** is a mandatory agreement signed by suppliers when importing an [IP-Block](#ip-blocks) onto the platform. This certificate signifies the supplier's consent for their [IP-Block](#ip-blocks) to be listed on the marketplace and rented out to other users in accordance with the platform's rules and policies.

When a supplier imports an [IP-Block](#ip-blocks), the certificate is sent to them via **PandaDoc**. By signing the document, the supplier confirms their agreement to the terms of usage, ensuring a transparent and secure process for all parties involved.

### CIDR
**[CIDR](#cidr) (Classless Inter-Domain Routing)** is a method for allocating and representing IP addresses and their associated routing. [CIDR](#cidr) uses the format `IP_address/prefix_length`, where:
- `IP_address` is the starting address of the range.
- `prefix_length` is the [prefix](#prefix), which specifies the number of bits used for the network portion of the address.

### LOA (Letter of Authorization) Description
The **Letter of Authorization (LOA)** is a formal document issued to a client after successfully completing the **Assignment Request** process. This document grants the client permission to announce an **[ASN](#asn) (Autonomous System Number)** for a specified **IP address range**.

The LOA serves as proof that the client has the right to broadcast and manage the assigned IP address range within a network. It is often required by data centers, internet service providers, and network operators to confirm that the client is authorized to use the specified resources.

The document typically includes the following details:
- Client's name and contact information  
- Assigned IP address range  
- [ASN](#asn) details  
- Authorization date and validity period  
- Issuing organization's contact information  

This document ensures proper routing and compliance within global network infrastructures, preventing unauthorized use of IP address space.

### Minimal Lease Period
The **minimal lease period** refers to the time during which the settings made by the **[IP-Block](#ip-blocks)** owner are stored in the **RIR** database, enabling the platform to use IPv4 addresses. The value can be selected from 14 to 60 months, with the option to extend the certificate in the future.

### Minimal Order Period
The [minimal order period](#minimal-order-period) refers to the minimum period (in months) during which an [IP-Block](#ip-blocks) can be rented. For example, if the minimal order period is set to 6, it means the [IP-Block](#ip-blocks) cannot be rented for less than 6 months. Additionally, the earliest possible date to cancel the subscription for the block will be after 6 months of rental.

### Minimal Split Size
The [minimal split size](#minimal-split-size) refers to the smallest [prefix](#prefix) into which an [IP-Block](#ip-blocks) can be divided for rental purposes.

For example:
1. **For a /24 block**:  
   Splitting a /24 block into smaller subnets (e.g., /25) for rental is not allowed since InterLIR supports blocks starting from a /24 mask.

2. **For a /20 block**:  
   The [minimal split size](#minimal-split-size) can be set to `/20`, `/21`, `/22`, `/23`, or `/24`.  
   - **If you choose `/20`**, the block will be listed on the marketplace as a single /20 block.  
   - **If you choose `/24`**, all sub-blocks within the /20 block will be available for rental as individual /24 blocks.

This flexibility allows providers to define how granularly their IP blocks can be rented while adhering to platform policies.

### PandaDoc
**PandaDoc** is an all-in-one document automation platform that enables businesses to create, send, and manage digital documents like contracts, proposals, and agreements. It streamlines the signing process with eSignatures and ensures documents are securely delivered and managed. Learn more: [PandaDoc](https://www.pandadoc.com/).

### Prefix
The [prefix](#prefix) represents the number of leading 1 bits in the [IP-Block](#ip-blocks) mask. It determines the width (in bits) of the **[IP-Block](#ip-blocks)**.

### [rDNS](#rdns)

**Reverse DNS ([rDNS](#rdns))** is the process of resolving an IP address to a domain name, the opposite of the standard DNS lookup. In a regular DNS query, a domain name is translated into an IP address. However, with [rDNS](#rdns), the system identifies which domain name is associated with a specific IP address.

[rDNS](#rdns) is primarily used for verification and security purposes. It helps validate the origin of emails to reduce spam by confirming that the sender's IP address matches a legitimate domain name. Many mail servers reject or flag emails from servers without proper [rDNS](#rdns) configuration.

[rDNS](#rdns) records are stored as **PTR (Pointer) records** in the DNS database. Unlike forward DNS, [rDNS](#rdns) queries use a special domain called `in-addr.arpa`, where the IP address is reversed and appended with this domain for lookup.

Setting up [rDNS](#rdns) requires administrative access to the DNS records of the IP address block. It is typically managed by the IP block owner or provider through cooperation with the relevant Regional Internet Registry (RIR), such as RIPE for Europe.

Although [rDNS](#rdns) is not essential for most internet services, it plays a key role in improving trust and reducing network abuse.

You can make a [rDNS Request](#rdns-request) to the leased [IP-Block](#ip-blocks) to connect rDNS.

### IP-Blocks
A contiguous range of IP addresses used for networking purposes. [IP-Blocks](#ip-blocks) on the platform can have the following statuses:

- **New**: The initial status when a block is added but not yet processed.  
- **Suspended**: Assigned when a manager rejects the block or penalizes it temporarily or permanently.  
- **Avail**: Indicates the block is successfully imported and available for listing. Blocks with partially rented sub-blocks also retain this status.  
- **Expired**: Shows the block's authorization certificate has expired. Renewal moves the block back to "Avail".  
- **Occupied**: Assigned when the block is fully leased by clients.

you can rent out your IP-Block by going through the [IP-Block importing process](#importing-an-ip-block)
### Stripe
A payment processing platform enabling businesses to accept online payments and manage transactions. Learn more: [Stripe](https://stripe.com/).

### Stripe Connected Accounts
Accounts connected to a primary **[Stripe](#stripe)** platform account, allowing businesses to manage payments for multiple users.

### RIR (Regional Internet Registry)
Organizations responsible for managing and registering internet resources (e.g., IP addresses and [ASNs](#asn)). Examples: ARIN, RIPE NCC, APNIC.

### RIPE NCC
The **Réseaux IP Européens Network Coordination Centre** manages IP resources in Europe, the Middle East, and Central Asia. RIPE NCC provides tools, databases, and support for managing internet infrastructure.

### RIPE Maintainer Attributes
- **MNT-BY**: Specifies who manages an object in the RIPE database.  
- **MNT-DOMAIN**: Manages domain objects (e.g., DNS records).  
- **MNT-ROUTE**: Manages route objects linking an [IP-Block](#ip-blocks) to an [ASN](#asn).  
- **MNT-LOW**: Defines who can manage sub-blocks of a primary IP prefix.
- **mnt-domains**: Specifies the maintainer responsible for managing domain records associated with the resource.
- **mnt-routes**: Specifies the maintainer responsible for managing routing records related to the resource.
- **org**: The organization to which the resource is allocated or assigned.
- **admin-c**: The administrative contact responsible for organizational decisions and resource management.
- **tech-c**: The technical contact responsible for the technical operations and management of the resource.
- **descr**: A brief description of the resource, such as its purpose or name.

### ARIN Maintainer Attributes
- **ORG Handle**: A unique identifier for an organization in the ARIN database, used to associate related resources ([IP-Blocks](#ip-blocks), [ASN](#asn), and contacts).
- **Descr**: A brief textual description indicating the name or purpose of the resource (e.g., network or organization).

### VAT
**Value Added Tax (VAT)** is applied to services or goods. VAT requirements depend on the supplier and client locations and whether a VAT number is provided.

### VAT Number
A required field for EU organizations when creating a [Business Account](#business-account). Verify VAT numbers at [VIES VAT Validation](https://ec.europa.eu/taxation_customs/vies/).

---
---
---
---
---

## Guides

### Importing a [Business Account](#business-account)

Users can follow these steps to create a [Business Account](#business-account)

---

1. **Accessing the [Business Account](#business-account) Creation Page**  
   The user navigates to the page for creating a [Business Account](#business-account).

---

2. **Entering Customer Information**  
   The user provides the following details:  
   - **First Name**  
   - **Last Name**  
   - **Email**  
   - **Email for Duplicating Notifications** *(optional)*  
   - **Email for Abuse Notifications** *(optional)*  
   - **Country**  
   - **Phone**

---

3. **Entering [Business Account](#business-account) Information**  
   The user enters the following business details:  
   - **Company Name**  
   - **Company Number**  
   - **VAT Number** *(optional for all except organizations from EU countries, where it is mandatory)*  
   - **Website** *(optional)*  
   - **Industry**  
   - **Phone** *(optional)*

---

4. **Providing Billing Address**  
   The user specifies the billing address, including:  
   - **Address Line**  
   - **Zip Code**  
   - **State**  
   - **City**

---

5. **Uploading Documents**  
   If all required fields are completed correctly, the user proceeds to the document upload step.  
   - The user uploads documents in the required format.  
   - If the document is valid, the user submits a request for BA creation.

---

6. **Manager Review**  
   An **InterLIR Manager** receives a notification about the new BA creation request.  
   - The manager reviews the request.  
   - If everything is in order, the request is approved.  
   - If there are issues, the request is rejected, and the manager asks the user to make corrections.

---

Completion: Once the user receives approval for the BA creation, the process is complete.

---

### Editing a [Business Account](#business-account)  
If the user needs to make changes to the [Business Account](#business-account) later, they must follow a similar process to edit the BA as outlined in the creation steps.

---

### Stripe Onboarding

**[Stripe Onboarding](#stripe-onboarding)** is a mandatory process to verify your identity and business details through Stripe’s KYC (Know Your Customer) requirements. Completing this process allows you to receive payments for renting out [IP-Blocks](#ip-blocks) to clients via the marketplace.

#### Why is [Stripe](#stripe) Onboarding Necessary?
1. Ensures compliance with financial regulations and anti-fraud standards.  
2. Enables transactions, allowing you to list [IP-Blocks](#ip-blocks) for lease and receive payments.  
3. Facilitates subscription-based billing with clients.

#### Required Details for [Stripe](#stripe) Onboarding:
- **Personal Information**: Full Name, Address, and Contact Information.  
- **Business Information**: Organization Name, Registration Details (e.g., Tax ID, VAT Number), and Business Address.  
- **Banking Information**: Bank Account Number for receiving payouts.

---

The onboarding process begins when you initiate the first **[IP-Block](#ip-blocks) import**. You will receive a link to start the **[Stripe](#stripe)** setup process in the second step of the first **[IP-Block](#ip-blocks) import**. Fill out all required forms with accurate information. After verification by **[Stripe](#stripe)**, you will be able to start receiving payments.

[Stripe](#stripe) onboarding is done once and does not need to be repeated. Subsequent imports bypass this step. By default, the connected account type is **custom**, allowing full platform functionality.  

Suppliers who prefer a **standard** [Stripe Connected Account](#stripe-connected-accounts) can request this from InterLIR support. With a standard account:  
- Suppliers handle fund withdrawals personally.  
- Some platform functionality becomes unavailable.

---

### Importing an [IP-Block](#ip-blocks)

Suppliers with an approved [Business Account](#business-account) can import [IP-Blocks](#ip-blocks) by following these steps:

1. **Initial Step: Entering [CIDR](#cidr) and Selecting RIR**  
   Enter the [CIDR](#cidr) of the [IP-Block](#ip-blocks) (address and [prefix](#prefix)) and select the appropriate **[Regional Internet Registry (RIR)](#rir-regional-internet-registry)**.

2. **Onboarding (if required)**  
   Complete the [Stripe](#stripe) onboarding process if it hasn't been done previously.

3. **Setting Parameters**  
   Configure the following:  
   - [Min Split Size](#minimal-split-size): Minimum block subdivision size.  [1]
   - **Pricing**: Prices for the block and its sub-blocks.  
   - **Leasing Period**: Duration for which the block is listed (14–60 months).  
   - **[rDNS](#rdns) Delegation**: Allow reverse DNS delegation if needed.  
   - **Minimum Lease Period**: Shortest rental period.

4. **Manager Approval**  
   Submit the block for approval by an InterLIR manager.  
   - **Approved**: The supplier is notified and can proceed.  
   - **Rejected**: The manager provides feedback for corrections.

5. **Review and Agreement**  
   After approval, the supplier reviews and updates block parameters if necessary.

6. **Signing the Contract**  
   Sign the **Certificate of Authorisation** via **PandaDoc** (sent to the supplier’s email).

7. **Completion**  
   - Assign [MNT attributes](#ripe-maintainer-attributes) in **RIPE NCC** if applicable.  
   - The block is ready for leasing with the **Avail** status.

---

This process ensures proper configuration and approval of [IP-Blocks](#ip-blocks), making them available for rental on the InterLIR platform.

---

### Assignment Request

#### **Step 1: Complete the [IP-Block](#ip-blocks) Order**  
- The Customer places an order to rent an [IP-Block](#ip-blocks).  
- After the order is successfully completed, the Customer receives a contract and the ability to submit an Assignment Request (AR).

---

#### **Step 2: Access the AR Flow**  
- The Customer navigates to the Assignment Request flow page.  
- The Customer selects the [IP-Block](#ip-blocks) from the block selector.  
- Based on the [RIR](#rir-regional-internet-registry) of the selected block(s), the set of fields that the Customer can fill out will vary.

---

#### **Step 3: Fill Out the AR Fields**  
Depending on the [RIR](#rir-regional-internet-registry), the fields available for input are as follows:

1. **If blocks are from [RIPE NCC](#ripe-ncc):**  
   - [ASN](#asn) (required)  
   - [Mnt domains](#ripe-maintainer-attributes) (optional)  
   - [Mnt routes](#ripe-maintainer-attributes) (optional)
   - [Org](#ripe-maintainer-attributes) (optional)
   - [admin-c](#ripe-maintainer-attributes) (optional) 
   - [Tech-c](#ripe-maintainer-attributes) (optional)  
   - [Descr](#ripe-maintainer-attributes) (optional)

2. **If blocks are from [RIR](#rir-regional-internet-registry) APNIC, LACNIC, or AFRNIC:**  
   - [ASN](#asn) (required)  
   - [ORG Handle](#arin-maintainer-attributes) (optional)   
   - [Descr](#arin-maintainer-attributes) (optional) 

3. **If blocks are from [RIR](#rir-regional-internet-registry) is ARIN:**  
   - [ASN](#asn) (required)  
   - [ORG Handle](#arin-maintainer-attributes) (optional)   
   - [Descr](#arin-maintainer-attributes) (optional) 

4. **If multiple blocks from different [RIRs](#rir-regional-internet-registry) are selected:**  
   - [ASN](#asn) (required)  
   - [Mnt domains](#ripe-maintainer-attributes) (optional)  
   - [Mnt routes](#ripe-maintainer-attributes) (optional)
   - [Org](#ripe-maintainer-attributes) (optional)
   - [admin-c](#ripe-maintainer-attributes) (optional) 
   - [Tech-c](#ripe-maintainer-attributes) (optional)  
   - [Descr](#ripe-maintainer-attributes) (optional)
   - [ORG Handle](#arin-maintainer-attributes) (optional)  

5. **If multiple blocks from ARIN and APNIC, LACNIC, or AFRNIC are selected:**  
   - [ASN](#asn) (required)  
   - [Org](#ripe-maintainer-attributes) (optional)
   - [ORG Handle](#arin-maintainer-attributes) (optional)  
   - [Descr](#arin-maintainer-attributes) (optional)

---

#### **Step 4: Submit the Assignment Request**  
- After selecting and filling out the required fields for the block(s), the Customer submits the Assignment Request.  

---

#### **Step 5: Request Review by InterLIR Manager**  
- The InterLIR Manager receives a notification about the request.  
- The Manager opens the request, reviews it, and performs any necessary actions with the [RIR](#rir-regional-internet-registry).  
- The Manager can either approve or reject the request:
  - **If approved:** The process continues to the next step.
  - **If rejected:** The Customer is notified and must make corrections before resubmitting the request.

---

#### **Step 6: Supplier Configures RPKI/ROA & Routes**  
- Upon approval, the Supplier receives a notification to configure RPKI/ROA & routes in their [RIR](#rir-regional-internet-registry) for the blocks listed in the request.  
- The Supplier performs the configuration and confirms completion on the InterLIR portal.

---

#### **Step 7: Manager Verifies Configuration**  
- The InterLIR Manager receives a notification that the configuration has been completed.  
- The Manager verifies that the required RPKI/ROA & routes are present in the [RIR](#rir-regional-internet-registry):
  - **If confirmed:** The assignment is marked as complete, and the Customer can now use the rented block.
  - **If not confirmed:** The Manager periodically rechecks until the configuration is complete and then confirms.

---

#### **Step 8: Assignment Request Completion or Cancellation**  
The Assignment Request can be completed or canceled under the following scenarios:

1. **Manual Deletion by the Customer:**  
   - The Customer manually submits a deletion request.  
   - The Supplier is notified to remove objects created in the [RIR](#rir-regional-internet-registry) during the assignment process.  
   - The Supplier removes the objects and confirms the action on the portal.  
   - The InterLIR Manager also removes associated objects in the [RIR](#rir-regional-internet-registry), and the request is marked as canceled.

2. **Subscription Termination:**  
   - If the Customer's subscription for the rented block ends, the process of object removal is similar to the manual deletion process.  
   - The Supplier and InterLIR Manager remove objects from the [RIR](#rir-regional-internet-registry), and the request is marked as canceled.

### rDNS Request

After successfully being assigned an IP block, the customer can submit an [rDNS](#rdns) request if [rDNS](#rdns) setup was enabled at the time of assignment. If this feature is unavailable, the customer cannot send an [rDNS](#rdns) request.

**Process steps:**

1. **Check [rDNS](#rdns) setup availability:**  
   Ensure that [rDNS](#rdns) setup is enabled for your [IP-Block](#ip-blocks).

2. **Fill out the form:**  
   Open the [rDNS](#rdns) request form and complete all required fields. The `nservers` fields are mandatory.  
   - You can add multiple `nservers` fields as needed.

3. **Submit the request:**  
   Click "Submit." The request will be processed as follows:  
   - If the block belongs to the RIPE RIR, the InterLIR manager will handle the configuration.  
   - If the block belongs to another RIR, the supplier will perform the setup.

4. **Confirmation or rejection:**  
   - If successful, the customer will receive a confirmation, and [rDNS](#rdns) will be active on their [IP address range](#ip-blocks).  
   - If rejected, the manager or supplier will provide an explanation. The customer can correct the issue and resubmit the request.

5. **Canceling [rDNS](#rdns):**  
   - [rDNS](#rdns) is automatically canceled if the customer terminates the [IP-Block](#ip-blocks) subscription. The manager or supplier removes the objects from the [RIR](#rir-regional-internet-registry) and confirms the action.  
   - The customer can also manually cancel [rDNS](#rdns) through the management form.
