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
In recent years, cyber threats have become more advanced and difficult to detect [1], [2]. Traditional security systems such as firewalls, intrusion detection systems (IDS), and antivirus programs mainly rely on static rules or known attack signatures. This makes them ineffective against zero-day attacks and adversarial behaviors that disguise themselves as normal network activity.
 Although artificial intelligence and machine learning have improved the detection accuracy of modern cybersecurity tools, these models usually lack causal reasoning. They can identify anomalies, but they do not explain why they occurred or how different factors are connected. Because of this, many analysts still find it difficult to trust AI-based alerts or use them for quick decision-making.
 In real-world environments, this limitation can lead to slower response times, higher false alarm rates, and missed detection of complex or multi-stage attacks. Therefore, there is a strong need for a causality-driven cybersecurity framework that can enhance existing systems by providing deeper understanding and explainable insights into the causes of suspicious behaviors. Such an approach can improve both the accuracy and interpretability of threat detection, making network defense more adaptive and reliable.


### 1.2 Project Motivation and Importance
Cybersecurity has become one of the most critical challenges facing organizations, governments, and individuals worldwide. Every year, cyberattacks grow in number and complexity, targeting sensitive data, financial systems, and critical infrastructures. Despite continuous improvements in security tools, attackers continue to exploit weaknesses in traditional detection methods and even manipulate machine learning models to evade detection.
 The motivation behind this project arises from the need to improve the reliability and transparency of threat detection systems. Most existing AI-based solutions behave like “black boxes,” producing alerts without explaining the reasoning behind them [2]. This limits the trust of security teams and slows down the response to potential threats.
 By integrating Causal Artificial Intelligence (Causal AI) into cybersecurity analysis, the project aims to build smarter and more explainable security mechanisms. Causal AI can help identify not only what happened in a network attack but also why it happened — allowing analysts to trace the root causes of malicious behavior. This understanding can enhance decision-making, reduce false positives, and strengthen overall cyber defense strategies.
 Ultimately, the importance of this project lies in its potential to bridge the gap between data-driven detection and human-understandable reasoning, providing a foundation for more adaptive, explainable, and trustworthy cybersecurity systems [2], [4].
As illustrated in Figure 1, the number of reported cyberattacks has significantly increased in recent years, highlighting the growing need for advanced and explainable cybersecurity systems.

Figure 1: Growth of reported cyberattacks in the U.S. from 2018 to 2024, showing a 144% increase and emphasizing the need for stronger cybersecurity frameworks [7].

### 1.3 Goals and Objectives  
The primary goal of this research is to enhance cybersecurity systems through the application of Causal AI and machine learning, focusing on understanding the underlying causes of security incidents rather than merely detecting correlations or anomalies [9][10]. This project seeks to apply causal inference techniques to analyze the relationships between network activities and potential threats, enabling a deeper understanding of how specific attacks emerge and propagate [11]. By developing explainable causal models and integrating them with machine learning methods, the research aims to provide transparency in cybersecurity decision-making, offering insights into why and how particular events occur [10][12]. Additionally, a hybrid causal framework will be designed, combining data from tools such as Wireshark with causal reasoning and machine learning approaches to support proactive threat prevention and early detection [14][15]. Ultimately, the research aspires to improve the reliability and interpretability of cybersecurity systems by leveraging cause–effect reasoning and intelligent learning models to guide more effective and targeted responses [9][11].

### 1.4 Solution  
Design a causal AI framework that learns from security data, identifies attack patterns, and explains the cause–effect relationships behind them.  

### 1.5 Research Scope  
The scope of this project is to create a causal-based machine learning framework that will improve cybersecurity systems by determining the root causes of security events instead of merely looking for trends or abnormalities. Using information from tools like Wireshark and Intrusion Detection Systems (IDS), the study uses causal inference techniques to examine connections between network behaviors and security alerts. The project aims to develop more transparent and explicable detection models that facilitate proactive threat prevention and early response by fusing machine learning and causal reasoning.
However, outside of the project's purview, the model solely relies on correlation and will only address specific network behaviors and attack patterns, not all potential forms of cyberattacks. Lastly,  The project does have certain limitations, though, such as limited access to real-world datasets, the possibility of missing values or data noise, and the challenge of simulating intricate and dynamic cyberattack patterns. Furthermore, because the majority of the experiments will be conducted using simulated or publicly accessible data, the framework might need a lot of processing power and might not generalize completely across various network environments.

---

## 2. Background  

### 2.1 Cybersecurity Threats Overview  
Cybersecurity threats have become increasingly diverse and sophisticated, targeting not only large organizations but also governments, small businesses, and individuals. These threats exploit vulnerabilities in networks, software, and human behavior to gain unauthorized access, steal data, or disrupt normal operations. Common types of cyber threats include malware, phishing, ransomware, denial-of-service (DoS/DDoS) attacks, and zero-day exploits. Malware can infiltrate systems and damage or steal data, while phishing attacks deceive users into revealing sensitive information. Ransomware encrypts victims’ files and demands payment, and DoS attacks overload systems to make services unavailable. Zero-day exploits, on the other hand, take advantage of unknown vulnerabilities before patches are released, making them extremely dangerous.
 In recent years, the rise of advanced persistent threats (APTs) has posed even greater risks, involving long-term, targeted attacks often backed by organized cybercrime or state actors. These threats are difficult to detect because they use stealthy techniques and evolve continuously.
 Modern cybersecurity strategies therefore emphasize defense in depth — applying multiple layers of protection across the network, application, and data levels. This multi-layered approach is designed to detect, contain, and mitigate attacks at various stages of their lifecycle. Understanding these threats is essential for designing intelligent and adaptive defense systems that can respond to the evolving nature of cyberattacks.  

### 2.2 Introduction to Causal Inference and Causal AI  
In the context of cybersecurity, Causal AI provides a powerful framework for moving beyond traditional correlation-based analytics. While conventional AI models detect patterns or anomalies, they often fail to explain why an event occurred — such as the root cause of a breach or the chain of actions leading to a cyberattack. By leveraging causal inference, Causal AI can model cause-and-effect relationships within complex security systems, enabling more proactive defenses, better threat attribution, and smarter automated responses [9][10]. Instead of simply reacting to suspicious activity, systems powered by Causal AI can predict potential attack paths, identify underlying vulnerabilities, and propose interventions that directly address the causes rather than the symptoms [11].  

### 2.3 Tools and Technologies Overview  
The project utilizes a combination of tools and technologies to develop, test, and deploy causal cybersecurity models. Python serves as the primary programming language due to its extensive libraries and flexibility for data analysis and modeling [12]. DoWhy and CausalNex are employed to perform causal inference and construct causal graphs, enabling the identification of cause–effect relationships within network events [13]. Wireshark is used for capturing and analyzing network traffic, providing real-world data for testing causal models [14]. Finally, AWS (Amazon Web Services) offers a scalable cloud environment for data storage, computation, and deployment of the developed models, ensuring efficient and secure experimentation [15].

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

 3.3.1 Overview
 
In recent years, researchers have started combining Causal Artificial Intelligence (Causal AI) with cybersecurity to make detection systems more explainable and proactive. Traditional AI and ML-based systems can identify suspicious patterns, but they often fail to explain why the attack occurred or what factors led to it [9], [10]. This lack of transparency makes it difficult for analysts to trust AI-based alerts or improve system rules.
Causal AI, on the other hand, focuses on understanding the cause-and-effect relationships within network data. By identifying how different events lead to attacks, it helps in explaining the reasons behind alerts, predicting future threats, and improving defense decisions [9], [12]. Several research projects, including work by the Alan Turing Institute, highlighted that causal reasoning can connect attacker behaviors and system responses in a logical sequence, allowing faster threat attribution and more explainable detection [9].  



3.3.2 Causal Modeling in Cybersecurity

Causal modeling provides a framework for understanding how one factor influences another in a cyber environment. Unlike correlation-based approaches that only show patterns, causal analysis identifies which actions directly lead to a threat [7].
 One study applied causal modeling to the VERIS Community Database (VCDB), which contains real-world breach incidents [7]. The authors analyzed six types of attacks (such as hacking, misuse, and malware) to measure their causal impact on two outcomes: the number of records lost and the time it took to detect the breach. Figure 4 presents the causal model developed by Lin and Banitaan [7], which was constructed using data from the VCDB dataset. The model shows how different attack categories — including malware, hacking, physical, and misuse — influence the discovery time and the resulting records lost. This visualization highlights how causal modeling helps in identifying the key relationships between attack types and breach consequences.





Figure 4: Causal model of cybersecurity incidents showing the relationships between attack types, discovery time, and data loss. Adapted from Lin and Banitaan (2020) [7].
Their results showed that hacking had the strongest causal effect on record loss, while misuse and physical attacks increased detection time. This study proved that causal analysis can reveal the most harmful attack factors, which is useful for prioritizing defense strategies.
 For this project, the same concept can be used but focused on network alerts (IDS data) instead of general breach outcomes — identifying which network behaviors are the main causes of an alert.


3.3.3 Causal Defense Optimization and Simulation

Another important work was presented by Spillard and Dhir (2022), who developed a simulation-based approach using Dynamic Causal Bayesian Optimization (DCBO) [8]. They combined causal reasoning with reinforcement learning to create an intelligent agent that can automatically defend a network under attack. The model was tested in the Yawning Titan simulator and showed that causal reasoning helps the system decide the best defensive action at the right time.
 For example, the model could evaluate possible actions such as blocking a port or isolating a host and predict how each action would affect the success of the attack. The results showed that causal-based decisions reduced attack impact compared to traditional methods [8].
 This approach supports the idea of integrating causal analysis not only to detect threats but also to guide intrusion prevention (IPS) decisions, which aligns with the future goal of this project.


3.3.4 Explainable IDS using Causal AI

Recent research has also explored using causal inference directly inside Intrusion Detection Systems (IDS). A study published in 2025 proposed an explainable IDS framework that uses Structural Causal Models (SCM) to link network behavior and alerts [10]. The system could explain why an alert was triggered by identifying which network variables caused it — for example, unusual packet size or abnormal communication frequency.
 This method improved both accuracy and trust: the system achieved high detection performance while also providing human-understandable explanations for each alert [10]. The study also showed that causal analysis helps reduce false positives, because it distinguishes between events that are truly related to attacks and those that just look suspicious.
 This kind of explainable IDS directly supports the goals of our project — combining detection accuracy with clear reasoning and interpretation.


3.3.5 Challenges and Limitations

Although current research shows promising results, there are still challenges when applying causal AI to cybersecurity. Many studies were tested only in controlled or simulated environments, so results may not generalize to real-world networks [7], [8].
 Another limitation is the data bias. For example, the VCDB dataset used in [7] includes only organizations that were already attacked, which limits the diversity of data and can affect causal accuracy. Also, building a causal model requires expert knowledge to correctly define relationships between variables, and missing one important factor can change the results.
 In practical systems, integrating causal models in real-time detection tools may also face computational challenges. However, as tools like DoWhy and CausalNex improve [13], applying these models in cybersecurity environments becomes more feasible.



3.3.6 Summary

The reviewed studies demonstrate that integrating causal reasoning into cybersecurity can make threat detection systems smarter, more interpretable, and proactive.
- The study on data breaches [7] proved that causal analysis can reveal which attack types cause the most serious outcomes.
- The DCBO framework [8] showed that causal decision-making can improve active defense responses.
-Research on explainable IDS [10] demonstrated that causal AI can make alert interpretation clearer and reduce false positives.
 Together, these works confirm that combining causal inference with traditional AI provides a deeper understanding of threats and helps analysts take faster, more informed actions.
 This project builds on these findings by integrating causal inference with network-based IDS data. The goal is to identify the real causes behind alerts and simulate how preventive actions (IPS layer) can stop attacks before they spread.
 By linking detection and prevention through causal reasoning, the system can move from reactive defense to explainable and proactive cybersecurity [7].


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

[9] Turing Institute, “Causal Inference for Improved Cybersecurity Threat Detection,” 2024. [Online]. Available:
https://www.turing.ac.uk/research/research-projects/causal-inference-improved-cybersecurity-threat-detection

[10] ScienceDirect, “Explainable Causal AI in Cybersecurity,” 2025. [Online]. Available:
https://www.sciencedirect.com/science/article/abs/pii/S2542660525001027

[11] A. G. Lee, “Causal AI: Current State of the Art and Future Directions,” Medium, 2024. [Online]. Available:
https://medium.com/@alexglee/causal-ai-current-state-of-the-art-future-directions-c17ad57ff879

[12] Cybersecurity Tribe, “Unlocking the Benefits of Causal AI in Cybersecurity,” 2024. [Online]. Available:
https://www.cybersecuritytribe.com/articles/unlocking-the-benefits-of-causal-ai-in-cybersecurity

[13] Microsoft, DoWhy Documentation. [Online]. Available:
https://microsoft.github.io/dowhy/

[14] Wireshark Foundation, Wireshark Official Documentation. [Online]. Available:
https://www.wireshark.org/docs/

[15] Amazon Web Services (AWS), AWS Official Website. [Online]. Available:
https://aws.amazon.com/






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
