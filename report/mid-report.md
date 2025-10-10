# 🧩 Mid Report – Cyber Defense Through Causal Attack Analysis  

**King Saud University**  
**College of Computer and Information Sciences**  
**Computer Science Department**  

---

## 🧑‍💻 Project Title
**Cyber Defense Through Causal Attack Analysis**  
**CSC 496 – Midterm Report**

**Prepared by:**  
- Saleh Alomair  
- Abdulaziz Alqahtani  
- Fares Alansi  
- Mousa Tairi  

**Supervised by:**  
**Dr. Maher Alhossaini**  

*Software project for the degree of Bachelor’s in Computer Science*  
*First Semester 1447/1448 – Fall 2025*  

---

## 📝 Acknowledgements  

On behalf of our team, we would like to thank everyone who supported us in our graduation project.  
Our sincere appreciation goes to **Dr. Maher Alhossaini** for his guidance and encouragement throughout this work.  
We are also grateful to **King Saud University** for giving us the opportunity to complete this project, and to all our professors who have shared their knowledge with us and helped us during our studies.  

---

## 🇬🇧 English Abstract  

Cybersecurity continues to face growing challenges as cyberattacks become more advanced, organized, and complex.  
Traditional defense methods usually respond only after an attack has already taken place, which leaves systems exposed and unprepared.  

This project aims to apply **causal analysis** together with **machine learning** to better understand the factors behind cyberattacks and provide a smarter, proactive defense.  
By building a **causal network**, the system will demonstrate how elements such as system vulnerabilities, user behavior, and attack patterns are connected and contribute to breaches.  

The project integrates **predictive models** that analyze historical attack data to anticipate possible threats.  
These models recognize trends, generate early warnings, and allow organizations to strengthen defenses before attacks occur.  

The expected outcome is an improved proactive defense capability, deeper understanding of attack origins, and stronger protection for digital infrastructures.  
Overall, the project emphasizes the shift from reaction to prevention.  

---

## 🇸🇦 Arabic Abstract  

يواجه الأمن السيبراني في العصر الرقمي تحديات متزايدة مع تطور الهجمات الإلكترونية من حيث التعقيد والتنظيم والأساليب المستخدمة.  
وغالبًا ما تعتمد الأنظمة الدفاعية التقليدية على ردود الأفعال بعد وقوع الهجوم، مما يجعل البنى التحتية عرضة للاختراق وضعيفة أمام التهديدات المتقدمة.  

يهدف هذا المشروع إلى الاستفادة من **التحليل السببي** بالتكامل مع **تقنيات التعلم الآلي** من أجل فهم العوامل الكامنة وراء الهجمات الإلكترونية وتقديم أسلوب أكثر فاعلية للتعامل معها بشكل استباقي.  

يعتمد النظام المقترح على بناء **شبكة سببية** توضّح كيفية ارتباط العناصر المختلفة مثل الثغرات التقنية، وسلوك المستخدمين، وأنماط المهاجمين، وكيفية مساهمتها في وقوع الاختراقات.  
ويساعد هذا النهج على الكشف عن العلاقات الخفية بين العوامل المسببة للهجمات، بدلاً من الاكتفاء بملاحظة الأعراض الظاهرة فقط.  

كما سيتم دمج **نماذج تنبؤية** تعتمد على تحليل البيانات التاريخية للهجمات من أجل التعرف على الأنماط المتكررة والتنبؤ بالتهديدات المستقبلية المحتملة قبل حدوثها.  

---

## 📘 Table of Contents  

1. [Introduction](#1-introduction)  
2. [Background](#2-background)  
3. [Literature Review](#3-literature-review)  
4. [Summary](#4-summary)  
5. [References](#5-references)  

---

## 1. Introduction  

### 1.1 Problem Statement  
Traditional cybersecurity defenses are reactive, leaving systems exposed and unprepared for sophisticated and evolving attacks.  
This project addresses that gap by integrating causal reasoning with AI-driven analysis to enhance proactive detection and response.  

### 1.2 Goals and Objectives  
- Apply causal analysis to cybersecurity systems.  
- Integrate machine learning to improve detection accuracy.  
- Build explainable models that reveal *why* attacks occur.  
- Develop a hybrid approach for prevention and early detection.  

### 1.3 Solution  
Design a causal AI framework that learns from security data, identifies attack patterns, and explains the cause–effect relationships behind them.  

### 1.4 Research Scope  
The project focuses on combining causal AI with IDS/IPS systems for academic and experimental use.  

---

## 2. Background  

### 2.1 Cybersecurity Threats Overview  
Overview of key network threats, attack vectors, and vulnerabilities that modern organizations face.  

### 2.2 Introduction to Causal Inference and Causal AI  
Causal AI uses cause–effect reasoning to understand *why* phenomena occur, not just *what* occurs, allowing more intelligent security responses.  

### 2.3 Tools and Technologies Overview  
Python, DoWhy, CausalNex, Wireshark, and AWS are used to develop and test causal security models.  

### 2.4 Risk Assessment and Governance (RAG)  
Integration of risk evaluation and mitigation within AI-driven security decision-making.  

### 2.5 Governance and Compliance  
Ensuring the model follows data protection and ethical AI standards.  

---

### 3.1 Existing Cybersecurity Solutions  

Today’s cyber threats are more advanced, so organizations use several layers of protection to stop and detect attacks.  
Common tools include firewalls, intrusion detection systems (IDS), antivirus or anti-malware programs, and newer AI-based security tools.  
Each one has a different job: firewalls and antivirus software block known threats at the network or host level,  
while IDS watch for unusual activities that could mean an intrusion — even if it’s a new or hidden attack [1].  
Modern security practices focus on combining these tools into a **multi-layered system** that works together to provide stronger and more complete protection [2].  

As illustrated in *Figure 1*, cybersecurity defenses are typically organized in multiple layers,  
each addressing different types of threats and vulnerabilities.  

*(Figure 1 – The seven layers of cybersecurity defense)*  

---

### 3.1.1 Firewall Systems  

Firewalls are one of the oldest and most fundamental defense mechanisms in network security.  
They act as barriers controlling the flow of network traffic based on predefined security rules [3].  

Traditional firewall types include:  

- **Packet-filtering firewalls** – check packets individually against rule sets.  
- **Stateful-inspection firewalls** – track connection states to make context-aware decisions.  
- **Proxy firewalls** – act as intermediaries between users and external servers.  

Next-Generation Firewalls (NGFWs) extend these functions by adding **deep-packet inspection** and **application awareness** [3].  
These enhancements allow NGFWs to identify and block more sophisticated malicious traffic at the network perimeter,  
although they also introduce greater complexity in configuration and maintenance [4].  

Overall, firewalls serve as the **first line of defense**, preventing unauthorized access and segmenting network traffic to contain potential intrusions.  

---

### 3.1.2 Intrusion Detection and Prevention Systems (IDS / IPS)  

Intrusion Detection Systems monitor network or host activities to identify signs of malicious behavior that bypass preventive defenses.  
Unlike firewalls or anti-virus (which primarily block known threats via static rules or signatures),  
IDS can detect anomalous or suspicious patterns that may indicate previously unknown attacks [1].  

**Classic IDS approaches:**  

- **Signature-based detection** – matches known attack patterns.  
- **Anomaly-based detection** – flags deviations from normal behavior.  

Modern IDS solutions increasingly incorporate **AI and machine learning** to enhance their capabilities [5][6].  
These AI-integrated IDS identify complex attack behaviors and improve detection accuracy beyond manual methods.  
Challenges remain in managing **false positives** and detecting **zero-day exploits** that lack known signatures [5].  

In practice, **Intrusion Detection and Prevention Systems (IDPS)** are often deployed together,  
where IDS provides monitoring and alerting, and IPS automatically blocks or contains suspicious activity in real time.  

*(Figure 2 – Comparison between IDS and IPS within a network)*  

---

### 3.1.3 Antivirus and Anti-Malware Solutions  

Antivirus software (or anti-malware solutions) is designed to detect and remove malicious software on endpoints,  
primarily using **signature-based detection** of known malware.  
This traditional approach is effective for known threats but struggles against new, polymorphic, or fileless malware  
that can evade signature matching [4].  

Modern endpoint protection has evolved toward **heuristic** and **behavior-based detection**,  
often aided by **machine learning**, to recognize malware based on malicious behaviors or anomalies rather than static signatures [4].  

For example, many organizations now use **Endpoint Detection and Response (EDR)** tools,  
which extend traditional antivirus by continuously monitoring system activities  
and heuristically detecting advanced threats (including fileless attacks) that would bypass signature-only defenses [5].  

These advances improve detection of zero-day malware and reduce reliance on frequent signature updates,  
making anti-malware defenses more adaptive against evolving threats.  

The antivirus detection process generally follows a structured sequence that involves  
scanning incoming files, comparing them against known threat indicators,  
and performing behavioral checks to determine whether the file is safe or malicious.  

*(Figure 3 – Flow chart illustrating the antivirus detection process)*  

#### Table 1 – Comparison of Malware Detection Techniques  

| Detection Method     | Description                                                       | Strengths                                              | Limitations |
|------------------    |-------------                                                        |------------                                            |--------------                                                              |
| **Signature-based** | Matches files against known malware signatures stored in a database. | Very accurate for known threats; fast and lightweight. | Ineffective against new or polymorphic malware; requires frequent updates. |
| **Heuristic-based** | Analyzes code structure and logic to detect suspicious or modified patterns. | Can detect unknown or slightly altered malware variants. | May generate false positives; less precise than signature-based. |
| **Behavior-based** | Monitors real-time actions and system behavior to identify malicious activity. | Detects zero-day and fileless attacks; adaptive against evolving threats. | Higher resource usage; possible false alarms from benign activity. |

---

### 3.1.4 AI-Based Cybersecurity Techniques  

In recent years, **artificial intelligence (AI)** and **machine learning (ML)**  
have become integral to modern cybersecurity.  

AI-driven tools can rapidly analyze large volumes of data — network traffic, system logs, user behavior —  
to detect complex attack patterns and subtle anomalies in real time.  
This makes them faster and more adaptive than purely rule-based systems [6].  

By continuously learning from new data, AI-based systems adapt to previously unseen attack techniques,  
enhancing detection of advanced threats such as zero-day exploits, botnets, and insider attacks [6].  

One of the main challenges in applying AI to cybersecurity is ensuring **explainability**.  
Security analysts need to understand *why* the AI flagged something as a threat,  
not just accept it blindly.  This principle, known as **Explainable AI (XAI)**,  
builds trust and allows verification and improvement of system behavior.  

Machine-learning models are now widely used in intrusion detection and malware classification,  
demonstrating higher accuracy and fewer false alarms compared to manual or signature-based methods [6].  

Integrating AI adds substantial value to cybersecurity operations —  
it automates threat hunting, accelerates incident response,  
and supports proactive, scalable defenses against evolving attacks.  

In future systems, **combining AI detection with causal reasoning**  
could produce tools that not only detect attacks but also explain why they happened and how to prevent them more effectively.  

Integrating these intelligent systems alongside classical tools  
(firewalls, IDS, antivirus) within a layered-security framework  
provides a more resilient posture [2]; each layer compensates for others’ blind spots  
and collectively adapts to dynamic attack behaviors.  


---

### 3.2 Existing Applications of Causal AI  
Discuss how causal inference has been applied in non-security contexts (healthcare, economics, social science) and its potential adaptation for cybersecurity.  

### 3.3 Cybersecurity + Causal AI Projects  
Review emerging research integrating causal AI with threat detection and anomaly analysis.  

### 3.4 Summary and Gaps in Current Research  
Identify what current systems lack and how your approach fills the gap.  

### 3.5 Conclusion  
Summarize how causal AI enhances security intelligence and proactive defense.  

---

## 4. Summary  
This mid-term report summarized project motivation, objectives, and literature review, highlighting causal AI’s potential for improving cybersecurity.  

---

## 5. References  

1. L. Diana et al., *Overview on Intrusion Detection Systems for Computer Networking Security*, **Computers**, 14(3):87, 2025.  
2. T. Sowmya & E.A. Mary Anita, *A comprehensive review of AI-based intrusion detection system*, **Measurement: Sensors**, 28(4):100827, 2023.  
3. *Firewalls, Intrusion Detection/Prevention, Encryption, and Multi-Factor Authentication in Cybersecurity Solutions*, ResearchGate, 2024.  
4. J. Ferdous et al., *A Survey on ML Techniques for Multi-Platform Malware Detection*, **Sensors**, 25(4):1153, 2025.  
5. HIMSS, *Healthcare Cybersecurity Survey 2020*, HIMSS.org, 2020.  
6. O. Alzubi et al., *Advancing cybersecurity: a comprehensive review of AI-driven detection techniques*, **Journal of Big Data**, 11(1), 2024.  

---

## 👥 Team Members  
- **Saleh Alomair** — *Team Leader *  
- **Abdulaziz Alqahtani** —   
- **Fares Alansi** —  
- **Mousa Tairi** — 

---

### 🧑‍🏫 Supervised by
**Dr. Maher Alhossaini**  
King Saud University – Computer Engineering Department

---

> *Mid Report – King Saud University, Computer Engineering Department (2025)*
