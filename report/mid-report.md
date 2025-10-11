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
## 3. Literature Review


### 3.1 Existing Cybersecurity Solutions  

Today’s cyber threats are more advanced, so organizations use several layers of protection to stop and detect attacks.  
Common tools include **firewalls**, **intrusion detection systems (IDS)**, **antivirus or anti-malware programs**, and newer **AI-based security tools**.  
Each one has a different job: firewalls and antivirus software block known threats at the network or host level, while IDS watch for unusual activities that could mean an intrusion, even if it’s a new or hidden attack [1].  
Modern security practices focus on combining these tools into a **multi-layered system** that works together to provide stronger and more complete protection [2].  

As illustrated in *Figure 1*, cybersecurity defenses are typically organized in multiple layers,  
each addressing different types of threats and vulnerabilities.  

*(Figure 1 – The seven layers of cybersecurity defense)*
 

---
### 3.1.1 Firewall Systems  

Firewalls are one of the oldest and most fundamental defense mechanisms in network security.  
They act as barriers controlling the flow of network traffic based on predefined security rules [3].  
Traditional firewall types include **packet-filtering**, **stateful inspection**, and **proxy firewalls**,  
while **next-generation firewalls (NGFWs)** add capabilities like **deep packet inspection** and **application awareness** [3].  

These enhancements allow NGFWs to identify and block more sophisticated malicious traffic at the network perimeter,  
although they also introduce greater complexity in configuration and maintenance [4].  

Overall, firewalls serve as a **first line of defense**, preventing unauthorized access and segmenting network traffic to contain potential intrusions.

---

### 3.1.2 Intrusion Detection and Prevention Systems (IDS / IPS)  

Intrusion Detection Systems monitor network or host activities to identify signs of malicious behavior that bypass preventive defenses.  
Unlike firewalls or anti-virus (which primarily block known threats via static rules or matching signature),  
IDS can detect anomalous or suspicious patterns that may indicate previously unknown attacks [1].  

Classic IDS approaches include **signature-based detection** (matching known attack patterns) and **anomaly-based detection** (flagging deviations from normal behavior).  
Modern IDS solutions increasingly incorporate **AI and machine learning** to enhance their capabilities – enabling the identification of complex attack behaviors and improving detection accuracy beyond manual methods [5][6].  

These **AI-integrated IDS** have shown promising results in catching attacks more efficiently,  
though challenges remain in managing false alarms (false positives) and detecting zero-day exploits that lack any known signature [5].  

In practice, **Intrusion Detection and Prevention Systems (IDPS)** are often deployed to not only alert on intrusions  
but also automatically block or contain suspicious activities in real time.  

As illustrated in *Figure 2*, IDS is typically deployed for monitoring and alerting,  
while IPS takes proactive action to block or prevent attacks.  

*(Figure 2 – Comparison between Intrusion Detection System (IDS) and Intrusion Prevention System (IPS) within a network)*

---

### 3.1.3 Antivirus and Anti-Malware Solutions  

**Antivirus software (anti-malware solutions)** is designed to detect and remove malicious software on endpoints, primarily using **signature-based detection** of known malware.  
This traditional approach is effective for known threats but struggles against new, polymorphic, or fileless malware that can evade signature matching [4].  

As a result, modern endpoint protection has evolved toward **heuristic** and **behavior-based detection techniques**, often aided by **machine learning**,  
to recognize malware based on malicious behaviors or anomalies rather than static signatures [4].  

For example, many organizations now use **Endpoint Detection and Response (EDR)** tools, which extend traditional antivirus by continuously monitoring system activities  
and can heuristically detect advanced threats (including fileless attacks) that would bypass signature-only defenses [5].  
These advances help improve the detection of zero-day malware and reduce reliance on frequent signature updates,  
making anti-malware defenses more adaptive against evolving threats.  

The antivirus detection process generally follows a structured sequence that involves scanning incoming files,  
comparing them against known threat indicators, and performing behavioral checks to determine whether the file is safe or malicious,  
as illustrated in *Figure 3*.  

*(Figure 3 – Flow chart illustrating the antivirus detection process from initial file scanning to behavioral analysis for identifying and classifying malware)*  

---

In addition to the detection workflow shown in Figure 3, *Table 1* summarizes and compares the main malware detection methods used in modern antivirus systems.  

| **Detection Method** | **Description**                                                     | **Strengths**                                          | **Limitations** |
|----------------------|-----------------                                                    |----------------                                        |-----------------|
| **Signature-based** | Matches files against known malware signatures stored in a database. | Very accurate for known threats; fast and lightweight. | Ineffective against new or polymorphic malware; requires frequent updates. |
| **Heuristic-based** | Analyzes code structure and logic to detect suspicious or modified patterns. | Can detect unknown or slightly altered malware variants. | May generate false positives; less precise than signature-based methods. |
| **Behavior-based** | Monitors real-time actions and system behavior to identify malicious activity. | Detects zero-day and fileless attacks; adaptive against evolving threats. | Higher resource usage; possible false alarms from benign activity. |

*(Table 1 – Comparison of malware detection techniques in antivirus systems)*

---

### 3.1.4 AI-Based Cybersecurity Techniques  

In recent years, **artificial intelligence (AI)** and **machine learning (ML)** have become key parts of modern cybersecurity.  
AI-based security tools can quickly analyze large amounts of data — such as network traffic, system logs, and user activity —  
to detect complex attack patterns and subtle unusual behaviors in real time.  
This makes them faster and more flexible than traditional systems that rely only on fixed rules [6].  

By continuously learning from new data, **AI-based systems** adapt to previously unseen attack techniques,  
enhancing detection of advanced threats like **zero-day exploits, botnets, and insider attacks** that traditional tools often miss [6].  

However, one of the main challenges in using AI for cybersecurity is ensuring its decisions are **explainable**.  
Security analysts need to understand *why* the AI flagged something as a threat, not just accept it blindly.  
This idea, called **Explainable AI (XAI)**, helps build more trust and makes it easier to verify and improve the system’s behavior.  

For example, **machine learning models** are now used in intrusion detection and malware classification,  
where they have demonstrated higher accuracy in identifying malicious activity with fewer false alarms  
compared to manual or signature-based methods [6].  

Using AI adds significant power to cybersecurity defenses — it helps **automate threat hunting**,  
**accelerate incident response**, and allows organizations to take a more **proactive and scalable approach**  
against constantly changing cyber threats.  

In future systems, **combining AI detection with causal reasoning** could make security tools not only detect attacks,  
but also explain *why* they happened and *how* to prevent them more effectively.  

Integrating these intelligent systems alongside classical tools (**firewalls**, **IDS**, **antivirus**)  
in a layered security framework provides a more **resilient security posture** [2],  
as each layer compensates for others’ blind spots and adapts to dynamic attack behaviors.

---

### 3.2 Existing Applications of Causal AI  
Discuss how causal inference has been applied in non-security contexts (healthcare, economics, social science) and its potential adaptation for cybersecurity.  

### 3.3 Cybersecurity + Causal AI Projects  

 3.3.1  About the Causal Model Applied in Cybersecurity:

         Cybersecurity is a very important field that has many roles, including detecting any suspicious activities, like unauthorized access and ransomware, etc. It is great to make progress in a field like Cybersecurity because of its importance in our current world; without any security, with any vulnerability will be exploited, causing loss of data and large financial and as mentioned above, Cybersecurity is one of the applications causal model, which aims at causal analysis in cyber-attacks such as phishing and data breaches, and so on … rather than aiming at association factors, which provides smart analysis and prediction for incoming attacks that helps the security team to response and counter attacks at early stages or before they occur rather than waiting occur attacks to deal with it which leads increasing of opportunity in counter attack.     


3.3.2  Previous Paper Related to the Causal Model Applied in Cybersecurity :

        We searched a few papers related to our project in order to understand the topic very well and compare them with our work .

3.3.2.1   Application of Causal Modeling in Cybersecurity paper :   



3.3.2.1.1  Introduction to this paper :

The researchers of this paper explained how to apply the causal model in cybersecurity and tried to understand why cyber-attacks happened, and spot the difference between Statistical analysis and Causal analysis. The statistical analysis predicts the outcome based on correlation and doesn't care about causality. The objective of this paper is to rate the risk of data breaches in cybersecurity and to determine the relationship between the data. They used a VERIS Community Database (VCDB), " which is an open-sourced database consisting of a real log for attacks that occurred" as the main source data to build up a causal model.  

3.3.2.1.2 Findings of this paper
They used six types of attacks (Social, Physical, Misuse, Malware, Hacking, Error) from a (VCDB) to test them in terms of (Time Discovery and Record Lost).

Figure 7  shows the causal estimates of the six cybersecurity actions (Social, Physical, Misuse, Malware, Hacking, and Error) on the outcome variable Records Lost.
 Each bar in the figure represents the estimated causal effect of that specific action on the number of records lost during a data breach.
As you can see, Hacking has the highest positive causal estimate, indicating that it is the most significant impact that causes data loss among all attack types. Unlike the remaining actions (Social, Physical, Misuse, Malware, and Error) show a weak impact for Records lost.

By using refuters that verify the accuracy of the model, such as a " random common cause" which means adding a random variable to the model to check whether the result is the same or different, and there is another type called a "Placebo" which replaces a random variable with a causal variable to check if it gives the same result or not, and finally "Data Subset" rather than taking the whole dataset we take a part of it and test the model again to check accuracy of model, same thing applied to another for Discovery Time.





Figure 6 shows the causal estimates of six different cyberattack actions (Social, Physical, Misuse, Malware, Hacking, and Error) on the outcome variable Discovery Time.
From the results, Physical, Misuse, and Hacking actions demonstrate positive causal estimates, indicating that these types of attacks are associated with longer discovery times.
Unlike Social and Error actions show negative causal estimates, meaning these incidents are typically discovered more quickly.
In general, the figure indicates that certain attack types—especially Hacking and Misuse have a stronger causal impact for late detection, whereas the others can be detected easily . 

      3.3.2.1.3 Limitations of this paper:

- The dataset is biased and was taken from the VERIS Community Database (VCDB), which only contains records of organizations that have already experienced data breaches, so the dataset lacks examples of companies that have not been breached, introducing a bias.


- The study focuses on one field ( healthcare ) the findings may not be generalized to other fields; in other words, we don't know if the outcomes will be applied to other organizations.




  3.3.2.2 Developing Optimal Causal Cyber-Defence Agents via Cyber Security Simulation paper : 

3.3.2.2.1 Introduction to this paper :  
This paper explained how to use causal AI to protect the system from electronic attacks in an efficient way. The researchers said that the attacks became more sophisticated compared to cyber-defense, so they suggested using two ways to enhance the cyber-defense response: First, Reinforcement Learning which the machine learns new attacks based on its history (Experiment), and second, Causal AI, which aims to figure out why the attack occurred, so they focused more on the second method to help them know the relations between events, and this paper present DCBO (Dynamic Causal Bayesian Optimization) which is an algorithm that finds the best intervention at any moment on the network. Finally, the experiments are done by using Yawning Titan, which is a simulator developed in the U.K. Government to simulate attacks and defenses in a real environment.  

3.3.2.2.2 Findings of this paper : 



This Figure shows the performance of three optimization methods, DCBO (Dynamic Causal Bayesian Optimization), CBO (Causal Bayesian Optimization), and BO (Bayesian Optimization) applied to the Yawning Titan (YT) cyber defense simulator. The x-axis represents the cumulative cost of interventions, whereas the y-axis represents the expected outcome or performance of the intervention, and the shaded areas indicate one standard deviation around the mean, while the black dotted line shows the true optimal response value. As seen in this figure, DCBO and CBO are more effective than BO in enhancing decisions of cyber-defense, because the DCBO and CBO focus on causality, which makes taking decisions faster, unlike the BO just focuses on improving performance.  


3.3.2.2.3 Limitation of this paper : 

- The experiments are done by the Yawning Titan Simulator to avoid realistic risks, so the results could not reflect all possible problems on a real Network.
 
 
- Constructing a DAG (Directed Acyclic Graph) in a real Network isn't easy, because not the same as the Yawning Titan Simulator; everything is visible, unlike, real Network, it might be a new attack appeared .









  

### 3.4 Summary and Gaps in Current Research  
Identify what current systems lack and how your approach fills the gap.  

### 3.5 Conclusion  
Summarize how causal AI enhances security intelligence and proactive defense.  

---

## 4. Summary  
This mid-term report summarized project motivation, objectives, and literature review, highlighting causal AI’s potential for improving cybersecurity.  

---

## References  

[1] L. Diana, *et al.*, “Overview on Intrusion Detection Systems for Computer Networking Security,”  
*Computers*, vol. 14, no. 3, p. 87, 2025.  

[2] T. Sowmya and E. A. Mary Anita, “A comprehensive review of AI-based intrusion detection system,”  
*Measurement: Sensors*, vol. 28, no. 4, p. 100827, 2023.  

[3] *FIREWALLS, INTRUSION DETECTION/PREVENTION, ENCRYPTION, AND MULTI-FACTOR AUTHENTICATION IN CYBERSECURITY SOLUTIONS*,  
*ResearchGate*, 2024. [Online]. Available:  
[https://www.researchgate.net/publication/382596527_FIREWALLS_INTRUSION_DETECTIONPREVENTION_ENCRYPTION_AND_MULTI-FACTOR_AUTHENTICATION_IN_CYBERSECURITY_SOLUTIONS](https://www.researchgate.net/publication/382596527_FIREWALLS_INTRUSION_DETECTIONPREVENTION_ENCRYPTION_AND_MULTI-FACTOR_AUTHENTICATION_IN_CYBERSECURITY_SOLUTIONS)  

[4] J. Ferdous, *et al.*, “A Survey on ML Techniques for Multi-Platform Malware Detection: Securing PC, Mobile Devices, IoT, and Cloud Environments,”  
*Sensors*, vol. 25, no. 4, p. 1153, 2025.  

[5] HIMSS, “Healthcare Cybersecurity Survey 2020,”  
*HIMSS.org*, 2020. [Online]. Available:  
[https://www.himss.org/sites/hde/files/media/file/2020/11/16/2020_himss_cybersecurity_survey_final.pdf](https://www.himss.org/sites/hde/files/media/file/2020/11/16/2020_himss_cybersecurity_survey_final.pdf)  

[6] O. Alzubi, *et al.*, “Advancing cybersecurity: a comprehensive review of AI-driven detection techniques,”  
*Journal of Big Data*, vol. 11, no. 1, 2024. [Online]. Available:  
[https://journalofbigdata.springeropen.com/articles/10.1186/s40537-024-00957-y](https://journalofbigdata.springeropen.com/articles/10.1186/s40537-024-00957-y)

[7] Lin, S., & Banitaan, S. (2020). Application of Causal Modeling in Cybersecurity. Advances in Science, Technology and Engineering Systems Journal (ASTESJ), 5(3), 372–379. https://www.scu.edu/media/school-of-engineering/pdfs/faculty-and-staff/faculty-pages/ASTESJ_050349.pdf

[8] Spillard, S., & Dhir, N. (2022). Optimal Causal Cyber-Defence Agents. In Proceedings of the 39th International Conference on Machine Learning (ICML 2022), Workshop on Machine Learning for Cybersecurity (ML4Cyber) (PMLR162). Baltimore, Maryland, USA. Retrieved from https://arxiv.org/pdf/2207.12355.pdf






---

## 👥 Team Members  
- **Saleh Alomair** — *Team Leader *  
- **Abdulaziz Alqahtani** —   
- **Fares Alansi** —  
- **Mousa Tairi** — 

---

### 🧑‍🏫 Supervised by
**Dr. Maher Alhossaini**  
King Saud University – Department of Computer Science
---

> *Mid Report – King Saud University, Department of Computer Science (2025)*
