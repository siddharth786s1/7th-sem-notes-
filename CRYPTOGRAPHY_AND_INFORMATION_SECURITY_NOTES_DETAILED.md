# Cryptography and Information Security Notes
## Detailed & Comprehensive
## B.Tech CSE & AIML — LNCT University
### VII Semester Syllabus

---

## 📚 TABLE OF CONTENTS

- [Unit I: Introduction to Information Security](#unit-i-introduction-to-information-security)
- [Unit II: Symmetric Key Cryptography](#unit-ii-symmetric-key-cryptography)
- [Unit III: Asymmetric Key Cryptography](#unit-iii-asymmetric-key-cryptography)
- [Unit IV: Message Authentication and Hash Functions](#unit-iv-message-authentication-and-hash-functions)
- [Unit V: Network Security and Applications](#unit-v-network-security-and-applications)

---

## 📖 UNIT I: INTRODUCTION TO INFORMATION SECURITY

### **1. What is Information Security?**

**Detailed Explanation:**

**Simple Definition:**
Information Security (InfoSec) is the practice of protecting information and information systems from unauthorized access, use, disclosure, disruption, modification, or destruction.

**Technical Definition:**
Information Security is a set of strategies, policies, processes, and technologies designed to protect the confidentiality, integrity, and availability of data (both digital and physical) throughout its entire lifecycle.

**Analogy:**
Think of information security like protecting your house:
- **Locks on doors** = Authentication (only authorized people enter)
- **Alarm system** = Intrusion detection
- **Safe for valuables** = Encryption (protect most important items)
- **Security camera** = Audit logs (record who did what)
- **Insurance** = Backup and recovery

**Why Information Security Matters:**

**Real-World Impact:**
```
1. Financial Losses:
   - IBM Report (2023): Average data breach costs $4.45 million
   - Ransomware attacks cost businesses $20 billion annually
   - Credit card fraud: $28 billion globally

2. Identity Theft:
   - 15 million Americans affected yearly
   - Average loss: $1,100 per victim
   - Takes 6 months to recover on average

3. Business Disruption:
   - Colonial Pipeline (2021): $4.4M ransom, gas shortage
   - NotPetya attack (2017): $10 billion in damages globally
   - Average downtime cost: $5,600 per minute

4. Reputation Damage:
   - Equifax breach (2017): 147M records, stock dropped 35%
   - Yahoo breach (2013): 3B accounts, sale price reduced $350M
   - Customer trust takes years to rebuild

5. Legal Consequences:
   - GDPR fines: up to €20M or 4% of annual revenue
   - British Airways: £20M fine for data breach
   - Marriott: £18.4M fine for security failure
```

---

### **2. The CIA Triad - Foundation of Information Security**

**Detailed Explanation:**

The CIA Triad is the fundamental model for information security, consisting of three core principles: **Confidentiality, Integrity, and Availability**.

---

#### **A) CONFIDENTIALITY**

**Definition:**
Confidentiality ensures that information is accessible only to those authorized to access it. It prevents unauthorized disclosure of sensitive data.

**Simple Analogy:**
Like a sealed letter - only the intended recipient should be able to read it.

**Key Concepts:**

**1. Data Classification:**
```
Classification Levels:

TOP SECRET / HIGHLY CONFIDENTIAL:
- Company financial records
- Trade secrets
- Strategic plans
- Customer payment information
Example: Apple's new iPhone design before launch

SECRET / CONFIDENTIAL:
- Employee salary information
- Internal audit reports
- Customer database
Example: Netflix user viewing history

INTERNAL USE:
- Company policies
- Internal memos
- Project documentation
Example: Employee handbook

PUBLIC:
- Marketing materials
- Press releases
- Public website content
Example: Company about us page
```

**2. Access Control Methods:**

**a) Physical Access Control:**
```
Examples:
🔐 Locks and keys (basic)
🏢 Security guards
💳 ID badges and card readers
👤 Biometric scanners (fingerprint, face, iris)
📹 Surveillance cameras
🚪 Mantrap doors (two-door system)

Real-World Example: Data Center
- First barrier: Perimeter fence
- Second barrier: Security checkpoint with ID verification
- Third barrier: Biometric scanner at server room
- Fourth barrier: Individual rack locks
- Fifth barrier: Hard drive encryption
```

**b) Logical/Technical Access Control:**
```
Examples:
🔑 Passwords and PINs
🎫 Access tokens
🔐 Encryption
🛡️ Firewalls
🔒 VPN (Virtual Private Network)
👥 Role-Based Access Control (RBAC)

Example: Banking System
User Role: Customer
- Can view: Own account balance
- Can do: Transfer money from own accounts
- Cannot do: View other customers' accounts

User Role: Bank Teller
- Can view: Customer account details
- Can do: Deposits, withdrawals
- Cannot do: Modify account ownership

User Role: Bank Manager
- Can view: All accounts, audit logs
- Can do: Approve large transactions
- Cannot do: Directly transfer money (needs approval)

User Role: System Administrator
- Can view: System logs, configurations
- Can do: Manage user access
- Cannot do: View customer account balances (separation of duties)
```

**3. Confidentiality Protection Methods:**

**Encryption:**
```
Definition: Converting readable data (plaintext) into unreadable format (ciphertext)

Example: Simple Substitution
Plaintext:  "HELLO WORLD"
Key:        Shift by 3
Ciphertext: "KHOOR ZRUOG"

Real-World Examples:
✅ HTTPS: Encrypts data between browser and website
✅ WhatsApp: End-to-end encryption of messages
✅ BitLocker: Encrypts entire hard drive
✅ VPN: Encrypts internet traffic
```

**Access Control Lists (ACL):**
```
Example: File Permissions

File: salary_report.xlsx
User: John (HR Manager)
  - Read: ✅ Yes
  - Write: ✅ Yes
  - Delete: ✅ Yes

User: Sarah (Employee)
  - Read: ❌ No
  - Write: ❌ No
  - Delete: ❌ No

User: Admin (IT)
  - Read: ✅ Yes (for backup)
  - Write: ❌ No
  - Delete: ❌ No
```

**4. Confidentiality Threats:**

**Threat 1: Unauthorized Access**
```
Scenario: Hacker breaks into company database

Attack Vector:
- SQL injection on login page
- Bypasses authentication
- Gains access to customer data

Prevention:
- Input validation
- Parameterized queries
- Web Application Firewall (WAF)
- Regular security testing
```

**Threat 2: Social Engineering**
```
Scenario: Phone Scam (Vishing)

Attack Flow:
1. Attacker calls employee: "Hi, this is IT support"
2. "We need to verify your password for security update"
3. Employee gives password (thinking it's legitimate)
4. Attacker uses password to access company systems

Prevention:
- Security awareness training
- Never ask for passwords over phone
- Callback verification procedures
- Multi-factor authentication (even if password stolen)
```

**Threat 3: Data Leakage**
```
Scenario: Employee accidentally emails confidential file

Incident:
- Employee preparing report
- Accidentally attaches wrong file (salary data)
- Sends to external partner
- Confidential information leaked

Prevention:
- Data Loss Prevention (DLP) software
- Email encryption
- Classification labels on documents
- Training on data handling
- Review before sending external emails
```

**Threat 4: Insider Threats**
```
Scenario: Disgruntled employee steals data

Incident:
- Employee being fired
- Before leaving, copies customer database to USB drive
- Sells data to competitors

Prevention:
- Immediate access revocation upon termination
- USB port controls (disable on sensitive systems)
- Monitoring and audit logs
- Exit interviews and asset return
- Non-disclosure agreements (NDA)
```

**5. Real-World Confidentiality Breaches:**

**Case Study 1: Equifax Data Breach (2017)**
```
What Happened:
- Hackers exploited unpatched vulnerability
- Accessed personal data of 147 million people
- Data included: SSN, birth dates, addresses, driver's licenses

How Confidentiality Was Broken:
- Unpatched Apache Struts vulnerability
- Weak segmentation (access to one system = access to all)
- Insufficient monitoring (breach undetected for 76 days)

Impact:
- $1.4 billion in costs
- CEO resigned
- Multiple lawsuits
- Congressional hearings

Lessons:
✅ Patch management critical
✅ Network segmentation
✅ Continuous monitoring
✅ Encrypt sensitive data at rest
```

**Case Study 2: Celebrity iCloud Photo Leak (2014)**
```
What Happened:
- Attackers used phishing and password guessing
- Accessed celebrities' iCloud accounts
- Leaked private photos

How Confidentiality Was Broken:
- Weak passwords
- No two-factor authentication
- Password reset questions too easy to guess
- Phishing emails not recognized

Impact:
- Privacy violations
- Emotional distress
- Legal actions
- Apple enhanced security

Lessons:
✅ Use strong, unique passwords
✅ Enable two-factor authentication
✅ Be cautious of phishing
✅ Understand cloud storage security
```

---

#### **B) INTEGRITY**

**Definition:**
Integrity ensures that information is accurate, complete, and has not been modified by unauthorized parties. It maintains the trustworthiness and reliability of data.

**Simple Analogy:**
Like a sealed envelope with a wax seal - you can tell if someone opened and tampered with the contents.

**Key Concepts:**

**1. Data Integrity vs. System Integrity:**

**Data Integrity:**
```
Definition: Data remains accurate and unaltered

Example: Bank Account Balance
Correct:  $1,000.00
Altered:  $10,000.00 (unauthorized modification)

Importance:
- Financial transactions must be accurate
- Medical records must be correct
- Legal documents must be unaltered
```

**System Integrity:**
```
Definition: System operates correctly without unauthorized modification

Example: Operating System
Normal:  Windows boots correctly
Compromised: Bootkit installed (modified boot process)

Importance:
- System behaves as expected
- No malicious code injected
- Configuration not tampered with
```

**2. Types of Integrity:**

**a) Physical Integrity:**
```
Definition: Protecting data from physical damage or environmental factors

Threats:
⚡ Power surges/outages
🌊 Floods, water damage
🔥 Fires
🌪️ Natural disasters
💥 Hardware failures

Protection:
✅ Uninterruptible Power Supply (UPS)
✅ Redundant power sources
✅ Climate control (temperature, humidity)
✅ Fire suppression systems
✅ Offsite backups
✅ RAID (Redundant Array of Independent Disks)

Example: Data Center Design
- Dual power feeds from different substations
- On-site diesel generators
- Raised floors (protection from flooding)
- Advanced fire suppression (FM-200 gas)
- Temperature/humidity monitoring
- Backup sites in different geographic locations
```

**b) Logical Integrity:**
```
Definition: Protecting data from unauthorized logical modification

Threats:
🦠 Malware (viruses, trojans)
👤 Unauthorized users
🐛 Software bugs
💾 Data corruption

Protection:
✅ Access controls
✅ Checksums and hash functions
✅ Digital signatures
✅ Version control
✅ Audit trails

Example: Software Update Process
1. Developer writes code
2. Code review (peer verification)
3. Automated testing
4. Generate checksum (SHA-256 hash)
5. Digitally sign with private key
6. Publish update with signature

User's computer:
1. Download update
2. Verify digital signature (ensures from legitimate source)
3. Calculate checksum (ensures not corrupted)
4. If both match, install
5. If not, reject update
```

**3. Integrity Protection Mechanisms:**

**Hash Functions:**
```
Definition: One-way function that converts data into fixed-size string

Properties:
1. Deterministic: Same input → Same output
2. Fast to compute
3. Avalanche effect: Small change in input → Completely different output
4. One-way: Cannot reverse hash to get original data
5. Collision-resistant: Hard to find two inputs with same hash

Example: SHA-256 Hash

Input: "Hello World"
SHA-256: a591a6d40bf420404a011733cfb7b190d62c65bf0bcda32b57b277d9ad9f146e

Input: "Hello World!" (added one character)
SHA-256: 7f83b1657ff1fc53b92dc18148a1d65dfc2d4b1fa3d677284addd200126d9069

Completely different! This is the avalanche effect.
```

**Real-World Use Cases:**

**Use Case 1: File Download Verification**
```
Scenario: Downloading Linux Ubuntu ISO

Website provides:
- File: ubuntu-22.04.iso (4GB)
- SHA-256: 84eed...a987c

Process:
1. Download file
2. Calculate SHA-256 on your computer
3. Compare with website's hash
4. If match → File not corrupted ✅
5. If different → Download again ❌

Why Important:
- Ensures download didn't get corrupted
- Ensures file wasn't tampered with in transit
- Protects against man-in-the-middle attacks
```

**Use Case 2: Password Storage**
```
Scenario: Website storing passwords

❌ WRONG WAY (Storing plain text):
Database:
User: john, Password: johnpass123
User: sarah, Password: sarah456

Problem: If database breached, all passwords exposed!

✅ CORRECT WAY (Storing hash):
Database:
User: john, Hash: 8f3d...92a1
User: sarah, Hash: 5c7e...44fb

Login Process:
1. User enters password: "johnpass123"
2. System hashes it: 8f3d...92a1
3. Compares with stored hash
4. If match → Login successful ✅
5. Original password never stored!

Even Better: Add Salt
User: john, Salt: x7k9, Hash: 2a1f...88cd

Salt = Random data added before hashing
- Two users with same password have different hashes
- Protects against rainbow table attacks
```

**Digital Signatures:**
```
Definition: Cryptographic technique to verify authenticity and integrity

How It Works:
1. Create document
2. Hash the document (SHA-256)
3. Encrypt hash with sender's private key = Digital Signature
4. Send document + signature

Verification:
1. Recipient calculates hash of document
2. Decrypts signature with sender's public key → Original hash
3. Compare both hashes
4. If match → Document authentic and unmodified ✅

Example: Email Signing

Sender (Alice):
- Writes email: "Transfer $1000 to Bob"
- Hash: a3f2...87d1
- Encrypt hash with Alice's private key
- Send email + signature

Recipient (Bob):
- Receives email
- Decrypts signature with Alice's public key → a3f2...87d1
- Calculates hash of received email → a3f2...87d1
- Hashes match → Verified ✅

If attacker modifies to "Transfer $10000 to Attacker":
- Hash becomes: 9d4e...23c8 (different!)
- Signature still decrypts to: a3f2...87d1
- Hashes don't match → Tampering detected! ❌
```

**Checksums:**
```
Definition: Simple error-detection code (less secure than hash)

Example: Credit Card Checksum (Luhn Algorithm)

Credit Card Number: 4532 1488 0343 6467
Last digit (7) is checksum

Calculation:
1. Starting from right, double every second digit
2. If result > 9, subtract 9
3. Sum all digits
4. If sum mod 10 = 0, valid ✅

Use Cases:
- ISBN numbers (books)
- Credit card validation
- Serial numbers
- Network packets (TCP checksum)
```

**4. Integrity Threats:**

**Threat 1: Man-in-the-Middle (MITM) Attack**
```
Scenario: Attacker intercepts and modifies communication

Attack Flow:
1. Alice wants to send message to Bob: "Transfer $100"
2. Message passes through attacker
3. Attacker modifies to: "Transfer $1000"
4. Bob receives modified message
5. Integrity violated!

Real-World Example: Public WiFi
- Connect to coffee shop WiFi
- Attacker controls the network
- You try to access bank.com
- Attacker intercepts and modifies transactions

Prevention:
✅ Use HTTPS (encrypted + integrity checked)
✅ VPN on public networks
✅ Digital signatures
✅ Certificate pinning
```

**Threat 2: SQL Injection**
```
Scenario: Attacker modifies database through input fields

Vulnerable Code:
query = "SELECT * FROM users WHERE username='" + userInput + "'"

Attack:
User input: admin' OR '1'='1
Resulting query: SELECT * FROM users WHERE username='admin' OR '1'='1'
Result: Returns all users! (Always true condition)

Worse Attack (Data Modification):
User input: '; DROP TABLE users; --
Resulting query: SELECT * FROM users WHERE username=''; DROP TABLE users; --'
Result: Entire users table deleted!

Prevention:
✅ Parameterized queries (prepared statements)
✅ Input validation
✅ Least privilege (database user has minimal permissions)
✅ Web Application Firewall (WAF)

Correct Code (Parameterized):
query = "SELECT * FROM users WHERE username=?"
execute(query, [userInput])
```

**Threat 3: Malware/Ransomware**
```
Scenario: Malicious software modifies or encrypts data

Ransomware Attack Flow:
1. User opens malicious email attachment
2. Ransomware executes
3. Encrypts all files on computer
4. Changes file extensions (.doc → .locked)
5. Displays ransom note: "Pay $500 in Bitcoin to decrypt"

Data Integrity Impact:
- Original files destroyed
- Data inaccessible
- Possible permanent loss

Famous Example: WannaCry (2017)
- Exploited Windows vulnerability
- Spread to 200,000 computers in 150 countries
- Encrypted files and demanded ransom
- Affected hospitals (UK NHS), causing surgery cancellations
- $4 billion in damages

Prevention:
✅ Regular backups (offline/offsite)
✅ Keep software updated (patches)
✅ Antivirus/Anti-malware
✅ Email filtering
✅ User training (don't open suspicious attachments)
✅ Network segmentation
✅ Application whitelisting
```

**Threat 4: Unauthorized Modification**
```
Scenario: Insider or attacker changes critical data

Example 1: Grade Manipulation
- Student hacks into school system
- Changes grades from C to A
- Integrity of academic records compromised

Example 2: Financial Fraud
- Employee with database access
- Transfers money to personal account
- Modifies audit logs to hide traces

Prevention:
✅ Access controls (least privilege)
✅ Audit trails (log all changes)
✅ Digital signatures (verify authenticity)
✅ Separation of duties (multiple approvals needed)
✅ Regular audits and reconciliation
```

**5. Real-World Integrity Violations:**

**Case Study 1: Stuxnet Worm (2010)**
```
What Happened:
- Sophisticated malware targeted Iranian nuclear facilities
- Modified PLC (Programmable Logic Controller) code
- Altered centrifuge speeds causing physical damage
- Masked modifications from operators (showed normal readings)

Integrity Impact:
- System integrity compromised (malicious code injected)
- Data integrity violated (false sensor readings)
- Physical integrity affected (equipment damaged)

How It Worked:
1. Infected via USB drives
2. Spread through network
3. Targeted specific Siemens SCADA systems
4. Modified control logic
5. Sent false feedback to operators

Lessons:
✅ Air-gapped networks not foolproof
✅ Supply chain security important
✅ Monitor for unauthorized changes
✅ Integrity checking on critical systems
```

**Case Study 2: Bangladesh Bank Heist (2016)**
```
What Happened:
- Hackers compromised SWIFT banking system
- Sent fraudulent transfer requests
- Attempted to steal $951 million
- Successfully stole $81 million

Integrity Violation:
- Modified legitimate transfer messages
- Altered bank records
- Manipulated audit logs

Attack Process:
1. Phishing email to bank employees
2. Installed malware
3. Observed transaction patterns
4. Crafted legitimate-looking transfers
5. Modified SWIFT software to hide transfers
6. Deleted evidence

Prevention Failures:
❌ No printer (transfer confirmations weren't printed)
❌ Weak network security
❌ Insufficient monitoring
❌ No integrity checking on SWIFT messages

Lessons:
✅ Multi-factor authentication on critical operations
✅ Transaction monitoring and anomaly detection
✅ Message integrity verification
✅ Network segmentation
✅ Regular security audits
```

---

#### **C) AVAILABILITY**

**Definition:**
Availability ensures that information and resources are accessible and usable by authorized users when needed. Systems must be reliable and maintain uptime.

**Simple Analogy:**
Like an ATM machine - it should be working 24/7 so you can withdraw money whenever you need it.

**Key Concepts:**

**1. Measuring Availability:**

**Uptime Percentages:**
```
Availability Level (Nines) | Uptime % | Downtime per Year
---------------------------|----------|-------------------
One nine (90%)             | 90%      | 36.5 days
Two nines (99%)            | 99%      | 3.65 days
Three nines (99.9%)        | 99.9%    | 8.76 hours
Four nines (99.99%)        | 99.99%   | 52.56 minutes
Five nines (99.999%)       | 99.999%  | 5.26 minutes
Six nines (99.9999%)       | 99.9999% | 31.5 seconds

Industry Standards:
🏥 Healthcare (critical systems): 99.999% (5 nines)
💰 Banking systems: 99.99% (4 nines)
🌐 E-commerce websites: 99.9% (3 nines)
📧 Email services: 99.9% (3 nines)

Example:
Amazon: Each minute of downtime costs ~$220,000
99% uptime = 3.65 days down = $1.16 billion lost!
This is why they invest heavily in availability
```

**2. Availability Requirements:**

**Business Impact Analysis:**
```
Critical Systems (Tier 1):
- Must be available 24/7/365
- Examples: Emergency services (911), air traffic control, hospital systems
- Cost of downtime: Life-threatening
- Required availability: 99.999%+

High Priority (Tier 2):
- Significant business impact
- Examples: E-commerce, banking, payment processing
- Cost of downtime: $100,000s per hour
- Required availability: 99.99%

Medium Priority (Tier 3):
- Moderate business impact
- Examples: Email, internal tools
- Cost of downtime: Productivity loss
- Required availability: 99.9%

Low Priority (Tier 4):
- Minimal business impact
- Examples: Training systems, archive systems
- Cost of downtime: Minor inconvenience
- Required availability: 99%
```

**3. Availability Threats:**

**Threat 1: Denial of Service (DoS) Attacks**
```
Definition: Attack that makes system unavailable to legitimate users

Types:

A) Volumetric Attacks (Overwhelming Traffic)
Example: UDP Flood
- Attacker sends massive UDP packets
- Consumes all bandwidth
- Legitimate users can't connect

Scale:
- Normal traffic: 1 Gbps
- Attack traffic: 1 Tbps (1000x more!)
- Server overwhelmed, crashes

B) Protocol Attacks (Exploiting Weaknesses)
Example: SYN Flood
How TCP connection works:
1. Client sends SYN (synchronize)
2. Server responds SYN-ACK
3. Client sends ACK (connection established)

Attack:
1. Attacker sends millions of SYN packets
2. Server waits for ACK (which never comes)
3. Server's connection table fills up
4. No resources for legitimate connections

C) Application Layer Attacks (Expensive Operations)
Example: Slowloris
- Open many connections to web server
- Send partial HTTP requests slowly
- Keep connections open indefinitely
- Server runs out of connection slots
- New legitimate requests rejected

Real-World Example: GitHub DDoS (2018)
- 1.35 Tbps attack (largest at the time)
- Used memcached amplification
- GitHub offline for 10 minutes
- Mitigated by Akamai DDoS protection

Prevention:
✅ DDoS protection services (Cloudflare, Akamai)
✅ Rate limiting
✅ Traffic filtering
✅ Redundant infrastructure
✅ Anycast network (distribute load)
✅ Web Application Firewall (WAF)
```

**Threat 2: Hardware Failures**
```
Common Failures:

Hard Drive Failure:
- Average lifespan: 3-5 years
- Failure rate: 2-4% per year
- Impact: Data loss, system downtime

Example Calculation:
- Data center with 10,000 drives
- 3% annual failure rate
- Expected failures per year: 300 drives
- If each failure causes 2 hours downtime...
- Without redundancy: Constant outages!

Prevention:
✅ RAID (Redundant Array of Independent Disks)
   - RAID 1: Mirroring (duplicate everything)
   - RAID 5: Striping with parity (can lose 1 drive)
   - RAID 10: Mirror + Stripe (high performance + redundancy)

✅ Hot Swappable Drives
   - Replace failed drive without powering down
   - RAID rebuilds data automatically

Power Supply Failure:
- MTBF (Mean Time Between Failures): 100,000 hours
- Impact: Immediate system shutdown

Prevention:
✅ Redundant power supplies (dual PSU)
✅ UPS (Uninterruptible Power Supply)
✅ Backup generators

Network Equipment Failure:
- Router/Switch failure
- Impact: Network connectivity lost

Prevention:
✅ Redundant network paths
✅ Hot standby equipment
✅ Automatic failover
```

**Threat 3: Natural Disasters**
```
Types and Impact:

Earthquakes:
- Can destroy data centers
- Example: Japan earthquake (2011) caused data center outages

Floods:
- Water damage to equipment
- Example: Thailand floods (2011) disrupted hard drive production

Fires:
- Complete equipment destruction
- Example: OVH data center fire (2021) destroyed servers

Power Outages:
- Grid failures
- Example: Texas power crisis (2021) affected data centers

Prevention Strategy: Geographic Redundancy

Example: Multi-Region Deployment
Primary Data Center: Mumbai
- Handles 100% of traffic normally
- Real-time replication to backup

Backup Data Center: Delhi
- On standby (warm backup)
- Can take over within minutes

Disaster Recovery Site: Bangalore
- Cold backup
- Can be activated within hours

Disaster Scenario:
1. Mumbai data center destroyed by disaster
2. Automatic failover to Delhi (5 minute switch)
3. Traffic routes to Delhi
4. Business continues with minimal disruption
5. Mumbai rebuilt over weeks/months
```

**Threat 4: Human Errors**
```
Common Mistakes:

Accidental Deletion:
Example: GitLab Incident (2017)
- System administrator accidentally deleted production database
- Intended to delete test database
- 300GB of production data lost
- 6 hours to restore from backups

Impact:
- Website offline for hours
- Recent data lost (5000 projects affected)
- Reputation damage

Prevention:
✅ Confirmation prompts for critical operations
✅ Regular, tested backups
✅ Version control
✅ Change management procedures
✅ "Trash" or soft delete (recoverable)

Misconfiguration:
Example: AWS S3 Bucket Misconfiguration
- Developer sets bucket to "public" accidentally
- Meant for internal use only
- Millions of records exposed

Impact:
- Data breach
- Privacy violations
- Compliance penalties

Prevention:
✅ Configuration management tools
✅ Automated security scanning
✅ Least privilege by default
✅ Peer review of changes
✅ Infrastructure as Code (version controlled configs)

Poor Capacity Planning:
Example: Website Launch
- Expected: 10,000 concurrent users
- Actual: 100,000 users (went viral)
- Servers overwhelmed
- Website crashes

Prevention:
✅ Load testing
✅ Auto-scaling (cloud)
✅ Capacity monitoring
✅ Performance baselines
```

**4. Availability Protection Strategies:**

**Strategy 1: Redundancy**
```
Definition: Having backup components that can take over if primary fails

Types:

A) Hardware Redundancy
- Redundant servers (active-active or active-passive)
- Redundant storage (RAID)
- Redundant network connections
- Redundant power sources

Example: Web Server Setup
Single Server (No Redundancy):
[Internet] → [Single Web Server] → [Database]
Problem: If web server fails, entire site down!

Load Balanced (With Redundancy):
                    ┌─→ [Web Server 1] ─┐
[Internet] → [Load Balancer] → [Web Server 2] → [Database Cluster]
                    └─→ [Web Server 3] ─┘

Benefits:
- If one server fails, others handle traffic
- Can maintain service during updates
- Distribute load (better performance)

B) Data Redundancy
- Multiple copies of data
- Replicated across locations
- RAID for local redundancy
- Geo-replication for disaster recovery

Example: Database Replication
Primary Database (Mumbai):
- Handles all writes
- Replicates to secondaries in real-time

Secondary Database 1 (Delhi):
- Read-only copy
- Can be promoted to primary if Mumbai fails

Secondary Database 2 (Bangalore):
- Read-only copy
- Backup for disaster recovery

Benefits:
- If primary fails, secondary promoted automatically
- Read queries distributed (better performance)
- Data safe even if one location destroyed

C) Network Redundancy
- Multiple internet connections (different ISPs)
- Redundant network paths
- Multiple data center locations

Example: Enterprise Network
                  ┌─→ ISP 1 (Fiber) ─┐
Office Network ───┤                   ├─→ Internet
                  └─→ ISP 2 (Cable) ─┘

Benefits:
- If one ISP down, traffic routes through other
- Can load balance across both
- Better reliability
```

**Strategy 2: Fault Tolerance**
```
Definition: System continues operating even when components fail

Techniques:

A) Graceful Degradation
- System continues with reduced functionality

Example: E-commerce Site
Normal Mode:
✅ Product browsing
✅ Search
✅ Recommendations
✅ Reviews
✅ Checkout
✅ Payment processing

When Recommendation Engine Fails:
✅ Product browsing (still works)
✅ Search (still works)
❌ Recommendations (disabled)
✅ Reviews (still works)
✅ Checkout (still works)
✅ Payment processing (still works)

Result: Site still functional, just less features
Better than complete outage!

B) Automatic Failover
- Automatically switch to backup when primary fails

Example: Database Cluster
Normal Operation:
Primary DB (Active) → Serves all requests
Standby DB (Passive) → Stays synchronized

Health Check Every 10 seconds:
Primary alive? ✅ Continue normal operation

Primary Failure Detected:
1. Standby detects primary down (missed 3 health checks)
2. Standby promotes itself to primary (30 seconds)
3. Applications automatically connect to new primary
4. Service continues (brief 30-second disruption)

C) Checkpointing and Recovery
- Save system state periodically
- Can resume from last checkpoint if crash

Example: Long-Running Process
Task: Process 1 million records (takes 10 hours)

Without Checkpoints:
- Process crashes at record 900,000 (after 9 hours)
- Must restart from beginning
- Another 10 hours wasted!

With Checkpoints (every 100,000 records):
- Process crashes at record 900,000
- Resume from checkpoint at 800,000
- Only lose 1 hour of work
- Complete in additional 2 hours
```

**Strategy 3: Regular Backups**
```
Backup Types:

A) Full Backup
- Complete copy of all data
- Pros: Simple, fast to restore
- Cons: Time-consuming, storage intensive

B) Incremental Backup
- Only data changed since last backup
- Pros: Fast, less storage
- Cons: Slower to restore (need all increments)

C) Differential Backup
- Data changed since last full backup
- Pros: Faster restore than incremental
- Cons: More storage than incremental

Backup Strategy Example (3-2-1 Rule):
3 = Three copies of data
  - 1 primary (live system)
  - 2 backups

2 = Two different media types
  - Disk (fast recovery)
  - Tape (long-term, cheaper)

1 = One offsite backup
  - Protected from local disasters
  - Cloud or remote data center

Backup Schedule Example:
Sunday:    Full backup (all data)
Monday:    Incremental (changes since Sunday)
Tuesday:   Incremental (changes since Monday)
Wednesday: Incremental (changes since Tuesday)
Thursday:  Incremental (changes since Wednesday)
Friday:    Incremental (changes since Thursday)
Saturday:  Incremental (changes since Friday)

Storage:
- Last 4 weeks: Onsite disk (fast recovery)
- Last 12 months: Offsite tape (compliance)
- Last 7 years: Cloud archive (long-term retention)

Recovery Scenarios:
Scenario 1: File deleted Tuesday afternoon
- Restore from Tuesday morning incremental
- Recovery time: 10 minutes

Scenario 2: Server crash Friday
- Restore from Sunday full backup
- Apply Monday-Thursday incrementals
- Recovery time: 2 hours

Scenario 3: Data center destroyed
- Restore from offsite backup
- Recovery time: 24 hours (includes shipping time)
```

**Strategy 4: Disaster Recovery Planning**
```
Components:

A) Recovery Time Objective (RTO)
- How long can business survive without system?

Examples:
Critical System (Hospital EHR): RTO = 15 minutes
Important System (Email): RTO = 4 hours
Standard System (Intranet): RTO = 24 hours

B) Recovery Point Objective (RPO)
- How much data loss is acceptable?

Examples:
Financial Transactions: RPO = 0 (no loss acceptable)
Customer Database: RPO = 1 hour
Training Videos: RPO = 24 hours

C) Disaster Recovery Plan (DRP)
1. Risk Assessment
   - Identify potential disasters
   - Assess likelihood and impact

2. Business Impact Analysis
   - Determine critical systems
   - Set RTO and RPO for each

3. Recovery Strategies
   - Backup sites
   - Data replication
   - Failover procedures

4. Plan Documentation
   - Step-by-step procedures
   - Contact information
   - Resource inventory

5. Testing and Training
   - Regular DR drills
   - Update plan based on results

Example DR Test:
Scenario: Primary data center fire

9:00 AM: Simulate disaster (turn off primary)
9:05 AM: Declare disaster (confirm outage)
9:10 AM: Activate DR plan
9:15 AM: Notify stakeholders
9:30 AM: Failover to secondary data center
10:00 AM: Systems back online
10:30 AM: Verify all services functional

Results:
✅ RTO met (1 hour target, actual 1 hour)
❌ Data loss: 15 minutes (RPO was 5 minutes)

Actions:
- Investigate RPO miss
- Improve replication frequency
- Document lessons learned
```

**5. Real-World Availability Incidents:**

**Case Study 1: AWS Outage (2017)**
```
What Happened:
- Amazon S3 (Simple Storage Service) outage
- Human error during routine maintenance
- Intended to remove small number of servers
- Typo in command removed critical servers
- Cascading failure affected entire US-EAST-1 region

Impact:
- Duration: 4 hours
- Affected services: Netflix, Quora, Slack, Trello, thousands more
- Estimated cost: $150 million

Why So Many Services Affected:
- Many companies rely on AWS
- S3 is fundamental storage service
- Single region failure impacted all dependent services

Availability Calculation:
- AWS promises 99.99% availability
- This outage: 4 hours ≈ 0.045% of year
- Still within SLA technically
- But massive impact

Lessons Learned:
❌ What Went Wrong:
- Human error (typo in command)
- Insufficient safeguards on critical commands
- Cascading failure (removing servers affected others)
- Single region dependency

✅ Improvements Made by AWS:
- Additional safeguards on operational tools
- Can't remove beyond certain capacity at once
- Improved monitoring and alerts
- Faster recovery procedures

✅ Lessons for Users:
- Multi-region deployment (don't rely on single region)
- Graceful degradation (some features vs. complete outage)
- Status page monitoring
- Disaster recovery planning
```

**Case Study 2: Fastly CDN Outage (2021)**
```
What Happened:
- Fastly (Content Delivery Network) outage
- Software bug triggered by customer configuration change
- Affected 85% of their network

Impact:
- Duration: 49 minutes
- Affected websites: Amazon, Reddit, Twitch, GitHub, CNN, NYTimes, UK Government
- Billions of users affected
- Estimated millions lost in e-commerce

Root Cause:
- Software bug in Fastly's system
- Specific customer configuration change triggered bug
- Bug caused servers to return errors
- CDN is critical infrastructure (many sites depend on it)

Availability Calculation:
49 minutes out of 525,960 minutes/year = 99.984% uptime
Still very high availability, but impact was massive

Why Single Point of Failure:
Many websites use CDN for:
- Faster content delivery (caching)
- DDoS protection
- Load balancing

When CDN down → Entire site down (even if origin servers fine)

Lessons:
✅ CDN redundancy (use multiple CDN providers)
✅ Ability to bypass CDN (direct to origin)
✅ Better testing of configuration changes
✅ Gradual rollout of changes (canary deployments)
```

**Case Study 3: Facebook Outage (2021)**
```
What Happened:
- Facebook, Instagram, WhatsApp, Messenger all down
- 6 hours offline
- Affected 3.5 billion users globally

Root Cause:
- BGP (Border Gateway Protocol) configuration error
- During routine maintenance, command removed BGP routes
- Routers stopped announcing Facebook's IP addresses
- Internet couldn't find Facebook (like removing from phone book)
- Made it worse: remote access also lost, couldn't fix remotely

Recovery Process:
- Engineers had to physically go to data centers
- Security protocols delayed entry (no remote auth working)
- Had to restore BGP configurations manually
- Took 6 hours to fully restore

Impact:
- Financial: $60 million in revenue lost
- Stock: Dropped 5%, Zuckerberg lost $6 billion net worth
- Social: Billions of users unable to communicate
- Business: Small businesses dependent on Facebook/Instagram suffered
- Emergency: Some relied on WhatsApp for emergency communications

Availability Calculation:
6 hours / 8760 hours per year = 99.93% availability
Below their internal target of 99.99%

Cascading Effects:
- Facebook's own communication tools (Workplace) also down
- Couldn't coordinate recovery internally
- Physical security systems affected (badge readers)
- Even internal engineers couldn't enter buildings easily!

Lessons:
✅ BGP configuration validation before deployment
✅ Out-of-band management (separate network for admin)
✅ Better change management procedures
✅ Physical access procedures for emergencies
✅ Communication plan when internal tools down
✅ Multi-channel redundancy
```

---

### **3. Additional Security Principles (Beyond CIA Triad)**

While the CIA Triad is fundamental, modern security includes additional principles:

#### **A) Authentication**

**Definition:**
Authentication is the process of verifying the identity of a user, device, or system. It answers the question: "Who are you?"

**Types of Authentication Factors:**

**1. Something You Know (Knowledge Factor)**
```
Examples:
- Passwords
- PIN codes
- Security questions
- Passphrases

Advantages:
✅ Easy to implement
✅ No special hardware needed
✅ Users familiar with concept

Disadvantages:
❌ Can be forgotten
❌ Can be guessed or cracked
❌ Can be shared
❌ Vulnerable to phishing

Password Guidelines (NIST 2023):
✅ DO: 
- Minimum 8 characters (longer is better)
- Allow all characters (spaces, symbols)
- Check against breach databases
- Use password managers

❌ DON'T:
- Force periodic changes (leads to weak passwords)
- Complex rules (P@ssw0rd! is actually weak)
- Security questions (answers often guessable)
```

**Example: Password Security Evolution**
```
2000s: "Use complex passwords"
Required: P@ssw0rd123!
Problem: Hard to remember, written down, reused

2010s: "Change passwords every 90 days"
Result: Users increment: P@ssw0rd1, P@ssw0rd2...
Problem: Predictable patterns, still weak

2020s: "Use long, unique, random passwords"
Recommended: correct-horse-battery-staple-mountain-river
Or: vK9$mN2#pL6@rT8&qW1!
Problem Solved: Stored in password manager, unique per site
```

**2. Something You Have (Possession Factor)**
```
Examples:
- Physical tokens (RSA SecurID)
- Smart cards
- Mobile phones (SMS, authenticator apps)
- Hardware keys (YubiKey)
- ATM/Credit cards

Advantages:
✅ Hard to duplicate
✅ Can be revoked if lost
✅ Provides additional security layer

Disadvantages:
❌ Can be lost or stolen
❌ Cost of hardware
❌ Need to carry device

Example: Hardware Token (YubiKey)
- USB security key
- Generates one-time codes
- Or uses FIDO2/WebAuthn standards
- Plug in and tap to authenticate
- Can't be phished (cryptographic proof)

Real-World Use:
Google: After requiring hardware keys for employees:
- Zero successful phishing attacks
- Previously: frequent credential compromise
```

**3. Something You Are (Inherence Factor)**
```
Biometric Authentication:

Fingerprint:
- Most common (smartphones, laptops)
- False Accept Rate: 1 in 50,000
- Fast, convenient

Facial Recognition:
- Used in: iPhone Face ID, Windows Hello
- 3D mapping (harder to fool than 2D photo)
- Works in various lighting
- False Accept Rate: 1 in 1,000,000 (Face ID)

Iris Scan:
- Very accurate
- Used in: High-security facilities, airports
- False Accept Rate: 1 in 1,200,000
- Expensive hardware required

Voice Recognition:
- Used in: Banking phone systems
- Analyzes voice patterns
- Can be fooled by recordings (improving)

Behavioral Biometrics:
- Typing rhythm (keystroke dynamics)
- Mouse movement patterns
- Gait (walking style)
- Touch patterns on phone

Advantages:
✅ Can't be forgotten
✅ Hard to transfer to someone else
✅ Convenient (don't need to remember/carry)

Disadvantages:
❌ Privacy concerns
❌ Can't be changed if compromised
❌ False positives/negatives
❌ Expensive hardware
❌ May not work for everyone (injuries, conditions)
```

**Multi-Factor Authentication (MFA/2FA):**
```
Definition: Using two or more different types of factors

Common Combinations:

Password + SMS Code:
1. Enter password (something you know)
2. Receive code via SMS (something you have - phone)
3. Enter code
4. Access granted ✅

Security Level: Medium
- SMS can be intercepted (SIM swapping)
- Better than password alone
- Not recommended for high-security

Password + Authenticator App:
1. Enter password
2. Open Google Authenticator / Authy
3. Enter 6-digit code (changes every 30 seconds)
4. Access granted ✅

Security Level: High
- TOTP (Time-based One-Time Password)
- Not vulnerable to SIM swapping
- Works offline

Password + Hardware Key:
1. Enter password
2. Insert YubiKey and tap
3. Access granted ✅

Security Level: Highest
- Physical device required
- Cryptographic proof
- Immune to phishing

Biometric + PIN (Phone Unlock):
1. Face ID / Fingerprint (something you are)
2. Fallback to PIN if biometric fails (something you know)

Real-World MFA Effectiveness:
Microsoft Study (2019):
- MFA blocks 99.9% of account compromise attacks
- Even simple SMS-based MFA is vastly better than none
- Hardware tokens: 100% effective against phishing
```

---

#### **B) Authorization (Access Control)**

**Definition:**
Authorization determines what an authenticated user is allowed to do. It answers: "What are you allowed to access?"

**Important Distinction:**
```
Authentication: Who you are (identity)
Authorization: What you can do (permissions)

Example:
Authentication: You prove you're employee #1234 (badge, password)
Authorization: As employee #1234, you can:
  ✅ Access general office areas
  ✅ View your own payroll
  ❌ Cannot access CEO's office
  ❌ Cannot view others' payroll
```

**Access Control Models:**

**1. Discretionary Access Control (DAC)**
```
Definition: Owner of resource controls access

Characteristics:
- Flexibility (owner decides)
- Used in: Windows, Linux file systems

Example: File Permissions
Owner: John creates document "project_plan.docx"
John can grant access:
- Sarah: Read and Write
- Mike: Read only
- Everyone else: No access

Advantages:
✅ Flexible
✅ Easy to understand
✅ Quick to set up

Disadvantages:
❌ Inconsistent security (different owners, different policies)
❌ Access can be granted to anyone
❌ Hard to audit across organization
❌ Permissions can proliferate uncontrolled

Linux/Unix DAC Example:
$ ls -l report.txt
-rw-r--r-- 1 john users 1024 Nov 7 15:30 report.txt

Permissions breakdown:
- (file type)
rw- (owner: john) - Read, Write
r-- (group: users) - Read only
r-- (others) - Read only

Change permissions:
$ chmod 600 report.txt
Now only john can read and write, nobody else can access
```

**2. Mandatory Access Control (MAC)**
```
Definition: System enforces access based on classification levels

Characteristics:
- Rigid, centralized control
- Used in: Military, government systems
- Classification-based

Example: Military Classification
Classifications (hierarchical):
- Top Secret
- Secret
- Confidential
- Unclassified

Users have clearances:
- Colonel Smith: Top Secret clearance
  ✅ Can access Top Secret, Secret, Confidential, Unclassified

- Captain Jones: Secret clearance
  ✅ Can access Secret, Confidential, Unclassified
  ❌ Cannot access Top Secret

- Private Brown: Confidential clearance
  ✅ Can access Confidential, Unclassified
  ❌ Cannot access Secret or Top Secret

Rules (Bell-LaPadula Model):
1. No Read Up: User can't read higher classification
   - Secret clearance can't read Top Secret docs

2. No Write Down: User can't write to lower classification
   - Prevents accidental leakage of classified info

Advantages:
✅ Strong security
✅ Prevents unauthorized disclosure
✅ Consistent across organization

Disadvantages:
❌ Inflexible
❌ Complex to implement
❌ Can hinder collaboration
❌ High administrative overhead
```

**3. Role-Based Access Control (RBAC)**
```
Definition: Access based on user's role in organization

Characteristics:
- Most common in enterprises
- Permissions assigned to roles, not individuals
- Scalable

Example: Hospital System
Roles:
- Doctor
- Nurse
- Pharmacist
- Patient
- Administrator

Permissions:

Doctor Role:
✅ View patient medical history
✅ Prescribe medications
✅ Order tests
✅ Write diagnoses
❌ Access billing information
❌ Modify user accounts

Nurse Role:
✅ View patient medical history
✅ Update vital signs
✅ Administer medications (prescribed by doctor)
❌ Prescribe new medications
❌ Access financial data

Pharmacist Role:
✅ View prescriptions
✅ Dispense medications
✅ Check drug interactions
❌ View complete medical history
❌ Prescribe medications

Patient Role:
✅ View own medical records
✅ Schedule appointments
✅ View bills
❌ View others' records
❌ Modify medical data

Administrator Role:
✅ Manage user accounts
✅ Assign roles
✅ Configure system settings
❌ View patient medical data (separation of duties)

Implementation:
User: Dr. Sarah Smith
Assigned Role: Doctor
Automatic Permissions: All doctor permissions apply

When Dr. Smith logs in:
- System checks her role
- Grants doctor permissions
- If promoted to Department Head, assign new role
- Gets additional permissions automatically

Advantages:
✅ Easy to manage (change role, not each user)
✅ Scalable (1000s of users, dozens of roles)
✅ Reduces errors (standardized permissions)
✅ Easier auditing
✅ Follows least privilege principle

Disadvantages:
❌ Role explosion (too many specific roles)
❌ Can be too rigid (special cases hard to handle)
❌ Initial setup complex
```

**4. Attribute-Based Access Control (ABAC)**
```
Definition: Access based on attributes of user, resource, and environment

Characteristics:
- Most flexible
- Complex to implement
- Dynamic, context-aware

Attributes:
User Attributes: Department, clearance level, location, time
Resource Attributes: Classification, owner, type, sensitivity
Environmental Attributes: Time of day, location, device, network

Example: Corporate Document Access

Policy: "Allow access to financial reports if:"
- User department = Finance OR Executive
- User clearance level >= Confidential
- Time = Business hours (9 AM - 6 PM)
- Access from = Corporate network OR VPN
- Device = Company-managed laptop

Scenario 1:
User: John (Finance dept, Confidential clearance)
Time: 2 PM (business hours)
Location: Office (corporate network)
Device: Company laptop
Result: ✅ Access Granted

Scenario 2:
User: John (same person)
Time: 11 PM (after hours)
Location: Home
Device: Personal phone
Result: ❌ Access Denied (outside business hours, wrong device)

Scenario 3:
User: Sarah (Marketing dept, Confidential clearance)
Time: 2 PM
Location: Office
Device: Company laptop
Result: ❌ Access Denied (wrong department)

Advantages:
✅ Very flexible
✅ Fine-grained control
✅ Context-aware (time, location)
✅ Easily adaptable to new requirements

Disadvantages:
❌ Complex to implement
❌ Hard to troubleshoot
❌ Performance overhead (evaluate many attributes)
❌ Difficult to audit
```

---

#### **C) Non-Repudiation**

**Definition:**
Non-repudiation ensures that a party cannot deny the authenticity of their signature on a document or sending a message. It provides proof of origin and delivery.

**Why It Matters:**
```
Scenario Without Non-Repudiation:
1. Alice sends email: "I agree to purchase 1000 units at $50 each"
2. Later, Alice claims: "I never sent that email"
3. No way to prove she sent it
4. Dispute arises

Scenario With Non-Repudiation:
1. Alice digitally signs email with her private key
2. Email sent with digital signature
3. Later, Alice claims: "I never sent that"
4. Digital signature proves she signed it (only her private key could create that signature)
5. Alice cannot deny sending it
```

**Implementation Methods:**

**1. Digital Signatures**
```
How It Works:

Signing Process:
1. Alice writes document
2. Hash document (SHA-256)
3. Encrypt hash with Alice's private key = Digital Signature
4. Send document + signature

Verification Process:
1. Bob receives document + signature
2. Decrypt signature with Alice's public key → Hash A
3. Calculate hash of received document → Hash B
4. If Hash A = Hash B:
   ✅ Document authentic (from Alice)
   ✅ Document unmodified
   ✅ Alice cannot deny sending it (only her key could create signature)

Real-World Example: Software Updates
When you download software:
- Developer signs it with their private key
- Your computer verifies signature with developer's public key
- If signature valid:
  ✅ Definitely from that developer
  ✅ Not tampered with
  ✅ Safe to install

Example: Windows updates signed by Microsoft
- Microsoft signs each update
- Windows verifies signature before installing
- Prevents malware disguised as updates
```

**2. Audit Logs**
```
Definition: Detailed records of all system activities

What to Log:
- Who: User ID, IP address
- What: Action performed
- When: Timestamp (precise to millisecond)
- Where: System/resource accessed
- How: Method used (API, GUI, command line)
- Result: Success or failure

Example Audit Log Entry:
{
  "timestamp": "2024-11-07T15:30:45.123Z",
  "user_id": "john.doe@company.com",
  "source_ip": "192.168.1.100",
  "action": "DELETE",
  "resource": "/financial/reports/Q3_2024.xlsx",
  "result": "SUCCESS",
  "details": "File moved to trash, recoverable for 30 days"
}

Use Cases:

Forensic Investigation:
- Data breach discovered
- Check audit logs to see:
  - When breach occurred
  - What data was accessed
  - Who accessed it (compromised account?)
  - How they accessed it (SQL injection?)

Compliance:
- GDPR requires logs of data access
- HIPAA requires tracking who viewed medical records
- SOX requires financial transaction audit trails

Non-Repudiation Example:
- Employee claims: "I didn't delete that important file"
- Audit log shows:
  Date: 2024-11-05 14:25:30
  User: employee_id_1234 (that employee)
  Action: DELETE
  File: important_project.docx
  IP: Employee's computer
- Employee cannot deny action

Best Practices:
✅ Log to separate, secure server (can't be modified)
✅ Encrypt logs
✅ Set up alerts for suspicious activities
✅ Regular log review
✅ Retain logs per compliance requirements (1-7 years)
❌ Don't log sensitive data (passwords, credit cards)
```

**3. Trusted Timestamps**
```
Definition: Cryptographic proof that data existed at specific time

How It Works:
1. Create document
2. Hash document
3. Send hash to Trusted Timestamp Authority (TSA)
4. TSA adds timestamp and signs with their private key
5. Timestamp certificate returned

Example Use Case: Patent Filing
- Inventor creates design document on Nov 1, 2024
- Gets trusted timestamp
- Later, someone else claims they invented it first
- Timestamp proves inventor had it on Nov 1
- Cannot be backdated or altered

Another Example: Legal Contracts
- Contract signed digitally on specific date
- Timestamp proves when it was signed
- Parties cannot claim it was signed earlier/later
```

**4. Blockchain for Non-Repudiation**
```
How Blockchain Helps:
- Immutable ledger (cannot be changed retroactively)
- Distributed (no single point of control)
- Timestamped (chronological order)
- Cryptographically secured

Example: Supply Chain Tracking
Product Journey:
1. Manufacturer records: "Produced 1000 units on Nov 1"
   - Recorded in blockchain
   - Cannot be changed later

2. Distributor records: "Received 1000 units on Nov 5"
   - New block added
   - Linked to previous block

3. Retailer records: "Received 1000 units on Nov 8"
   - New block added

If dispute arises:
- Complete, unalterable history available
- Timestamp for each transaction
- Each party's actions recorded
- Cannot deny their recorded actions

Real-World: IBM Food Trust (Walmart)
- Tracks food from farm to store
- If contamination found, trace back to source
- All parties' actions recorded
- Cannot deny handling contaminated product
```

---

#### **D) Accountability**

**Definition:**
Accountability ensures that actions can be traced back to specific individuals. Users are held responsible for their actions.

**How It's Achieved:**

**1. Unique User Accounts**
```
Principle: Each person has own account (no sharing)

❌ Wrong: Shared Accounts
Account: "admin"
Password: Shared among 5 IT staff

Problem:
- Malicious action occurs
- Which of 5 people did it?
- Cannot determine accountability

✅ Correct: Individual Accounts
Accounts: admin_john, admin_sarah, admin_mike...
Each with unique password

Benefits:
- Know exactly who performed each action
- Can revoke specific person's access
- Audit trail links to individual
- Accountability enforced
```

**2. Audit Trails**
```
Comprehensive logging of actions:

Example: Bank Teller System
Every action logged:

08:30:15 - teller_sarah - LOGIN - Success
08:45:22 - teller_sarah - VIEW_ACCOUNT - Account #12345
08:46:10 - teller_sarah - WITHDRAW - Account #12345 - $500
09:15:33 - teller_sarah - DEPOSIT - Account #67890 - $1000
17:30:00 - teller_sarah - LOGOUT

If discrepancy found:
- Review Sarah's audit trail
- See all her actions
- Hold her accountable if error/fraud
```

**3. Separation of Duties**
```
Principle: No single person has complete control

Example: Financial System
Action: Transfer $1 million

Split into steps:
1. Employee A: Initiates transfer
2. Manager B: Reviews and approves
3. System: Executes transfer
4. Auditor C: Reviews transaction

Benefits:
- Prevents single person fraud
- Requires collusion (multiple people)
- Clear accountability at each step

Real-World Example: Nuclear Missile Launch
- Two-person rule
- Both officers must turn keys simultaneously
- Neither can launch alone
- Accountability shared
```

---

### **4. Types of Security Threats**

Understanding threats is crucial for implementing appropriate defenses.

#### **A) Malware (Malicious Software)**

**Definition:**
Software designed to harm, exploit, or otherwise compromise systems.

**Types:**

**1. Viruses**
```
Definition: Malicious code that attaches to legitimate files and spreads when files are shared

Characteristics:
- Requires host program
- Spreads when host executed
- Can replicate itself

Famous Example: ILOVEYOU Virus (2000)

Attack Flow:
1. Sent as email attachment: "LOVE-LETTER-FOR-YOU.TXT.vbs"
2. Subject: "ILOVEYOU"
3. Victim opens attachment (thinking it's a love letter)
4. VBScript executes
5. Overwrites files (images, documents)
6. Sends itself to all contacts in address book
7. Spreads exponentially

Impact:
- 45 million PCs infected in 10 days
- $10 billion in damages
- Affected Pentagon, CIA, British Parliament

How It Spreads:
User A opens attachment → Virus executes → Sends to A's 100 contacts → Each opens it → Sends to their contacts → Geometric progression

Prevention:
✅ Don't open suspicious attachments
✅ Antivirus software
✅ Email filtering
✅ User education
✅ Disable macros in documents
```

**2. Worms**
```
Definition: Self-replicating malware that spreads automatically without user interaction

Characteristics:
- No host file needed (standalone program)
- Spreads through network vulnerabilities
- Can spread rapidly

Famous Example: WannaCry Ransomware Worm (2017)

Attack Flow:
1. Exploited Windows SMB vulnerability (EternalBlue)
2. Scanned network for vulnerable systems
3. Self-replicated to found systems
4. Encrypted files on infected systems
5. Demanded ransom ($300-$600 in Bitcoin)

Impact:
- 200,000+ computers in 150 countries
- NHS (UK healthcare) severely affected:
  - 19,000 appointments cancelled
  - Ambulances diverted
  - Operations postponed
- FedEx, Renault, Deutsche Bahn affected
- $4 billion in damages

Speed of Spread:
- Started May 12, 2017
- Within hours: Global epidemic
- Infected 200,000+ in 4 days

How It Spreads:
Computer A infected → Scans network → Finds vulnerable Computer B → Automatically infects B → B scans network → Finds C → Chain reaction

Prevention:
✅ Keep systems patched (WannaCry exploited known vulnerability with available patch)
✅ Network segmentation
✅ Firewall rules
✅ Disable unnecessary services (SMBv1)
✅ Backup data (offline)
```

**3. Trojan Horses**
```
Definition: Malware disguised as legitimate software

Characteristics:
- Does not self-replicate
- Tricks user into installing
- Creates backdoor for attacker

Example Scenario: Fake Antivirus

Attack Flow:
1. Pop-up appears: "Warning! Your computer is infected!"
2. "Download SuperAntivirus to clean your PC"
3. User downloads and installs
4. Actually installs malware
5. Steals passwords, credit cards
6. May display fake scan results
7. Demands payment to "remove viruses"

Types of Trojans:

A) Banking Trojans
- Captures banking credentials
- Example: Zeus Trojan
  - Infected 3.6 million PCs in US
  -