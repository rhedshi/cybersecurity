# Facebook Cybersecurity University

* [Sign Up](https://fbcodepath.splashthat.com/)
* [Course](https://courses.codepath.com/courses/cybersecurity_university/pages/bootcamp_structure)

## Pre-work

* [Course Overview](https://courses.codepath.com/snippets/cybersecurity_university/course_overview)
* [Course Policy](https://courses.codepath.com/snippets/cybersecurity_university/policies)
* [Course Pre-work](https://courses.codepath.com/snippets/cybersecurity_university/prework)
* [Submitting Pre-work](https://courses.codepath.com/snippets/cybersecurity_university/submitting_prework)

## Description

The Cybersecurity course focuses on teaching students the fundamentals of security with the aim of providing a foundational level of knowledge matched with offensive and defensive skills developed through hands-on experience. Students will learn the basics of cybersecurity and common vulnerabilities and attacks, receiving hands-on practice in both exploitation techniques and strategies for protecting and hardening applications. Developed in partnership with Facebook, the course introduces a wide range of topics via a combination of sessions, videos, projects, and labs, giving students both a thorough grounding in the details of cybersecurity and an introduction to the broader landscape of information security.

## Course Structure

This is a 12-week exploration of Cybersecurity focused on offensive attacks and penetration testing. The overall structure and components of this course are as follows:

**CodePath course curriculum share a common structure:**

- **Weekly Lab** (120 mins) - We will hold a weekly lab session in-person where we will focus on a few topics to explore in more depth together through an interactive session.
- **Weekly Capture the Flag (CTF)** - For the first 5 weeks of the course, students will apply the concepts practiced in the lab in Capture the Flag competitions.

## Requirements

Students should...
- have introductory knowledge of:
  - engineering and programming
  - web applications and web development
  - middleware such as web servers and databases
- be pursuing a course of study related to computer science that includes:
  - fundamental CS concepts such as data structures and algorithms
  - hands-on programming/scripting experience
  - application development and design
- be able to fulfill the attendance and work submission requirements outlined in Course Policies
- be able to dedicate 10-15 hours to the course outside of class sessions for 12 weeks

## Course Policies

As experienced programmers, you would be more than capable of leveraging the extensive online resources available to learn aspects of Cybersecurity on your own. The core value that we’re providing in this course is a framework for highly accelerated learning combining accountability, mentorship, focused curriculum, and peer collaboration on hands-on projects. For this reason, we have incredibly high expectations of all students participating in this course and will hold everyone accountable to the strict attendance and assignment submission policies.

#### Attendance
- **Attendance is required to all in-person sessions**
- **Excused Absences:** Maximum of 2 per semester
   - Excused absences must be requested in advance through the CodePath Course Portal
- **Unexcused Absences:** None allowed
   - An unexcused absence is defined as an absence where an excused absence was not requested prior to the missed class.
- **Consequences for absences beyond the maximum allowed:** In the event that a student has more than the maximum allowed excused absences or an unexcused absence, the student will no longer be able to participate in the course. If the course is being taken for credit and the absence occurs beyond the drop date, the student will receive a failing grade for the class. They will still be able to audit the course as an observer, but won't take part in the final project and have access to the support channels and grading.

#### Assignment Submission
- **Assignment Submission:** Assignments must have all required user stories complete and be submitted by the posted deadline.
- **Late Work Policy:** Students may request one additional day to complete and submit one assignment per semester.
- **Consequences for incomplete or missing assignments:** In the event that a student has more than the maximum allowed late assignments, misses an assignment all together or submits and incomplete assignment after having already used their one allotted late submission, the student will no longer be able to participate in the course. If the course is being taken for credit and the absence occurs beyond the drop date, the student will receive a failing grade for the class.
#### Assignment Submission
- **Assignment Submission:** Assignments must have all required user stories complete and be submitted by the posted deadline.
- **Late Work Policy:** Students may request one additional day to complete and submit one assignment per semester.
- **Consequences for incomplete or missing assignments:** In the event that a student has more than the maximum allowed late assignments, misses an assignment all together or submits and incomplete assignment after having already used their one allotted late submission, the student will no longer be able to participate in the course. If the course is being taken for credit and the absence occurs beyond the drop date, the student will receive a failing grade for the class.

## Course Resources

During this course, students should be aware of the following pages and resources:

- [Security Guides](http://guides.codepath.com/websecurity) - This includes a series of references to reinforce key concepts and topics
- [Submitting Assignments](https://courses.codepath.com/courses/cybersecurity_university/pages/submitting_assignments) - Guide for how to submit each of the required projects via Github and raising an issue.

Reviewing each of these sections ensures that you will get the most out of this course. 

## Course Content

### Week 1 - Data Exposures

Reading:
* Security Introduction
* Castles and Heist Films
* Fundamental Security Principles
* Request methods and headers
* Attack: URL Manipulation
* Attack: Insecure Direct Object Reference

Lab:
* Hands on with URL Manipulation and IDOR

### Week 2 - Sanitizing Input

Reading:
* Attack: SQL Injection (SQLI)
* Validating input
* Sanitizing incoming data
* Attack: File Upload Abuse
* Attack: Remote Code Execution

Lab:
* Hands on with SQLI and RCE exploits

Assignment:
* Capture The Flag (CTF): SQLI and RCE exploits

### Week 3 - Sanitizing Output

Reading:
* Attack: Cross-Site Scripting (XSS)
* Sanitizing outgoing data
* Attack: Clickjacking

Lab:
* Hands on with XSS and clickjacking exploits

Assignment:
* Capture The Flag (CTF): XSS and clickjacking exploits

### Week 4 - Cookie and Session Based Attacks

Reading:
* Attack: Faked Requests
* Cookies and Sessions
* Attack: Cookie Theft and Manipulation
* Attack: Cross-Site Request Forgery (CSRF)
* Attack: Session Hijacking
* Attack: Session Fixation

Lab:
* Hands on with CSRF exploits
* Learn design pattern for implementing CSRF tokens
* Hands on with Session Hijacking and Session Fixation exploits

Assignment:
* Capture The Flag (CTF): CSRF exploits

### Week 5 - Encryption

Reading:
* Encryption
* Attack: Brute Force Attack
* Attack: Dictionary Attack

Lab:
* Identify and exploit weak cryptographic protection
* Identify and exploit poorly-implemented crypto
* Using PGP / GPG

Assignment:
* Capture The Flag (CTF): Identify and exploit weak cryptographic protection and poorly-implemented crypto

### Week 6 - User Authentication

Reading:
* User Authentication
* Strong Passwords
* Password Managers
* Multi-Factor Authentication
* Attack: Username Enumeration
* Attack: Credential Theft
* Phishing
* Data breaches
* Attack: Privilege Escalation

Lab:
* Login page vulnerabilities and exploits
* Password reset vulnerabilities and exploits
* Hash cracking with `hashcat`

### Week 7 - White Hat, Black Hat

Reading:
* Attack: Footprinting, Enumeration, and Fingerprinting
* Code Reading and Analysis

Lab:
* Understanding VMs and containers
* Setting up WordPress in a VM/container
* Setting up Kali in a VM/container
* Using `wpscan` to discover and recreate known WP issues

Assignment:
* Research vulnerabilities in older WP versions
* Recreate exploits using Kali and other tools
* Documenting research and submitting proof of work

### Week 8 - Better Tools, Better Targets

Lab:
* Using Metasploit to attack WP
* Using Meterpreter and reverse shells
* Using `sqlmap`

### Week 9 - NetSec

Reading:
* Netsec Crash Course
* Firewalls
* Intrusion Detection Systems
* Risk Assessment
* Penetration Testing
* Threat Monitoring
* Incident Response

Lab:
* Basic networking tools
* Basic packet analysis
* Installing and using Wireshark
* Malware traffic analysis
* WiFi Cracking

Assignment:
* Build a Honeypot
* Intrusion Detection

### Week 10 - Social Engineering

Reading:
* Social Engineering Strategies
* Case Studies
* Attack: Social Engineering - Pretexting
* Attack: Social Engineering - Baiting
* Attack: Social Engineering - Phishing
* Attack: Social Engineering - Quid Pro Quo
* Attack: Social Engineering - Tailgating
* Insider Threats, Contractors

Lab:
* Using Social Engineering Toolkit
* Phishing via email
* Fake Login page
* Simulated Phishing Exercise

### Weeks 11 & 12 - Capture The Flag
* Mutli-week, multi-team CTF competition
* Live web targets at various difficulties
* Student-supplied targets
* Quiz questions


## Support Channels:

- **Facebook Groups**
   - CodePath @ [YourUniversity] Facebook Group: Best place to get info related to logistics at your specific university campus.
   - All University CodePath Web Security Facebook Group: Leverage the entire CodePath University community by instantly reaching out to over 500 students at more than 20 universities going through the same program at the same time!
- **[support.codepath.com](http://support.codepath.com)** <img src=http://i.imgur.com/NhG6t19.png title="Question Mark" width=20>
   - Browse our ever expanding FAQ based on topic or search by keyword
   - Send us a message 📬     
