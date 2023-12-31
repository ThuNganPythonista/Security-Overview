# Security-Overview

**Detailed Report on Web Security**

**I. Introduction:**
In the era of Industry 4.0, digital transformation is a prevailing trend. Applications, especially websites, are experiencing explosive growth to meet societal needs. Web security is a crucial aspect of managing and maintaining a website, ensuring its safety from data and system attacks.

Websites are often targeted for various purposes:

- **Data theft:** Stealing user information and sensitive data from the system.
  
- **Ransom:** Threatening and demanding payment to prevent an attack.
  
- **Showcasing skills:** Demonstrating hacking capabilities and techniques.
  
- **Sabotage:** Inflicting harm and causing losses in various aspects to the victim.
  
- **Satisfying curiosity:** Exploring and understanding system intricacies.
  
- **Damaging reputation:** Causing reputational damage to a company in front of customers.
  
- **Setting the stage for future attacks:** Preparing for subsequent attacks.

**II. Commonly Targeted Services:**
1. **SMTP Servers (Port 250):** Vulnerability in Sendmail's address parser, allowing attacks to control the application.
  
2. **RPC Servers (Port 111 & Others)**
  
3. **NetBIOS Shares (Ports 135, 139, 445):** Vulnerabilities exploited by worms like Blaster and Sasser.
  
4. **FTP Servers (Port 20, 21):** Security vulnerabilities in wuftpd.
  
5. **SSH Servers (Port 22):** Security vulnerabilities in OpenSSH and PAM.
  
6. **Web servers (Port 80, 443):** Chunked encoding vulnerability in Apache.

These services often become targets for network attacks due to security vulnerabilities that can be exploited for system control and intrusion.

**IV. Web Server Attack Steps:**
1. **Scan active ports**
  
2. **Banner Grabbing:** Obtain server configuration information, probe weaknesses on ports.
  
3. **Learn server configuration:** Check server configuration for Windows, Unix, using TCP fingerprinting.
  
4. **Probe weaknesses on ports:** Default file configurations, buffer overflow, check insecure applications.
  
- **Utilize attack means:** Use available attack code from the internet or build custom code.

**V. Common Web Application Security Vulnerabilities:**
1. **Unvalidated Parameters:**
   - **Description:** Attackers can alter any component of an HTTP request before sending it. Examples: URL, Cookies, Form fields, Headers, Hidden fields.
   - **Mitigation:** Firewalls, tainting, and code reviews.

2. **Broken Access Control:**
   - **Description:** Inconsistently defined and applied access controls in the system, allowing attackers unauthorized access.
   - **Mitigation:** Code reviews, non-programmatic controls through application configuration, access verification through centralized containers.

3. **Broken Account/Session Management:**
   - **Description:** Authentication-related vulnerabilities, e.g., using only passwords for authentication, easily guessable accounts, lack of encryption for important data.
   - **Mitigation:** Use strong passwords, avoid default accounts, encrypt protection for crucial files.

4. **Cross-Site Scripting (XSS):**
   - **Description:** Attackers use trusted applications/companies to distribute malicious code to end-users, hiding the malicious code.
   - **Mitigation:** Common user issue. Allow only safe input. Confirm input data does not contain special characters or strings (e.g., <, >, (,), #, &, commonly used in HTML and JS).

5. **Buffer Overflows:**
   - **Description:** Security vulnerability occurring when a program writes more data than allocated for a specific memory area, usually a buffer. Can have serious consequences, including program flow control or even system control.
   - **Mitigation:** Monitor patches, report bugs. Review code before approval. Limit application rights during runtime. Use secure languages like Java.

6. **Command Injection:**
   - **Description:** Attack type allowing users to inject malicious code into form or URL variables (system commands, SQL, interpreted commands).
   - **Mitigation:** Label all input data for control (Tainting). Prevent system call commands. Limit application rights during runtime.

7. **Error Handling Problems:**
   - **Description:** Vulnerability when developers inadvertently reveal information that aids attackers in targeting applications.
   - **Mitigation:** Describe issues and cope, such as changing default error pages.

8. **Insecure Use Of Cryptography:**
   - **Description:** Storing data unsafely, e.g., storing credit card information, passwords, without encryption. Poor choice of encryption algorithms (or self-built).
   - **Mitigation:** Careful use of public cryptography.

9. **Remote Administration Flaws:**
   - **Description:** Issues related to remote system or application administration. A security hole that can be exploited for remote system intrusion, often through remote administration tools or interfaces.
   - **Mitigation:** Avoid combining admin interfaces with servers. Control user accounts. Restrict IPs.

10. **Web and App Server Misconfiguration:**
    - **Description:** Related to the choice between using "work out of the box" and "use only what you need" principles.
    - **Mitigation:** Create and use enhanced guidelines. Turn off all unused services.

**VI. Security Principles:**
Despite the various attack methods developed and deployed, avoiding these attacks only requires adherence to the following basic principles:

1. **Turn off unnecessary services:** Fundamental

 principle to reduce attack risk.
  
2. **Regularly patch systems:** Maintain and update systems to prevent new vulnerabilities.
  
3. **Do not trust input data:** Verify and authenticate input data to prevent attacks.
  
4. **Search for logical errors:** Analyze applications to find logical errors and correct them.
  
5. **Provide only necessary information:** Limit information scope to reduce attack risk.
  
6. **Hide critical information:** Use encryption and access controls to protect crucial information.

