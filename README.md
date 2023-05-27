# Data analysis report
## Task
I was given a list of univeristy course codes and names. 

The list contained many duplicates

My task was to collect the following information for each course:
- If it was thought in the fall 2023 semester
- If it was thought in the campus of Gjøvik, in Norway
- If it was thought in english
- What was the study level of the course (bachelor, master, etc)

## Data sources

<details>
  <summary>Uncleaned course list</summary>

|#| Courses |
|--| ------ |
| 1 | IMT4123 - System Security |
| 2 | MT4113 - Introduction to Cyber and Information Security Technology |
| 3 | IMT4114 - Introduction to Digital Forensics |
| 4 | IMT4887 - Specialisation in Web Technology |
| 5 | NFUT0030 - Norwegian for foreigners, online short course |
| 6 | TØL4018 – Renewable Energy Technology  |
| 7 | TØL4023 – Energy system analysis project course |
| 8 | TØL4012 – Sustainability Assessment    |
| 9 | TØL4014 – Sustainable Manufacturing Systems |
| 10 | IDG2003 - Back-end web development |
| 11 | IMT4889 - Specialisation in Decentralised Technologies |
| 12 | PROG2007 - Mobile Programming |
| 13 | TTM4165 - Digital Economics |
| 14 | IMT4887 - Specialisation in Web Technology |
| 15 | IIKG2001 - Software Security |
| 16 | IIKG3005 - Infrastructure as Code |
| 17 | TPD4156 Design 7- Service Design |
| 18 | IMT4312 Quantitative Methods and Use of Eyetrackers |
| 19 | IMT4316 Information Architecture |
| 20 | IMT4316 Information Architecture |
| 21 | IMT4898 Specialisation in Interaction Design |
| 22 | IMT4309 Usability and Human Factors in Interaction Design  |
| 23 | IDG4112 Research by Design and Tangible Interaction |
| 24 | TPD4156 Design 7 - Service Design |
| 25 | IMT4392 - Deep Learning for Visual Computing |
| 26 | IDIG4002 - Computer Graphics Fundamentals and Applications |
| 27 | PROG2002 - Graphics Programming |
| 28 | IMT4895 - Specialisation in Colour Imaging |
| 29 | IMT4304 : Cross-media Color Reproduction |
| 30 | IMT4884 : Colour management  |
| 31 | SMF1212 : Project management |
| 32 | SMF3084F : Organizational Behavior |
| 33 | NFUT0030 : Norwegian for foreigners, online short course |
| 34 | IMT3603 - Game Programming |
| 35 | PROG2002 - Graphics  Programming |
| 36 | IIK3100 - Ethical Hacking and Penetration Testing |
| 37 | NFUT0060 - Norwegian for foreigners, short course |
| 38 | IMT3603 - Game Programming |
| 39 | PROG2007 - Mobile Programming |
| 40 | PROG2053 - Web Technologies |
| 41 | NFUT0030 - Norwegian for foreigners, online short course |
| 42 | IDIG4002 - Computer Graphics Fundamentals and Applications  |
| 43 | IMT3603 - Game Programming |
| 44 | PROG2002 - Graphics Programming |
| 45 | NFUT0030 - Norwegian for foreigners, online short course |
| 46 | FENG2020 - Energy system analysis |
| 47 | FENG2022 - Bioenergy |
| 48 | TEK2002 - EcoDesign |
| 49 | TØL4018 - Renewable Energy Technology |
| 50 | TØL4015 - Project work |
| 51 | TØL4082 - Project Work for Exchange Students |
| 52 | PROG2007 Mobile Programming |
| 53 | IMT4316 Information Architecture |
| 54 | IDG2012 Web Accessibility, Usability and Ethics |
| 55 | PROG2053 Web Technologies |
| 56 | IDG2009 - Communication |
| 57 | IDG1006 - Physical Prototyping |
| 58 | IDG1362 - Introduction to User-Centered Design |
| 59 | IDG1100 - Web Fundamentals |
| 60 | Intrusion Detection in Physical and Virtual Networks (IMT4204) |
| 61 | Advanced Ethical Hacking - Information Security, Specialization Course (TTM4536) |
| 62 | Norwegian for foreigners, online short course - Campus Ålesund og Campus Gjøvik (NFUT0031) |
| 63 | IMT4392 Deep Learning for Visual Computing |
| 64 | IDIG4002 Computer Graphics Fundamentals and Applications |
| 65 | IDIG4321 Introduction to Color Image Processing |
| 66 | IMT4884 Advanced Colour Management |
| 67 | IIK3100 – Ethical Hacking and Penetration Testing |
| 68 | IIK1001 – Cyber security and computer networks  |
| 69 | PROG2053 – WWW technologies  |
| 70 | IMT3104 – Artificial Intelligence  |
| 71 | IIKG2001 - Software Security |
| 72 | NFUT0030 – Norwegian for foreigners |
| 73 | TPD4156 Design 7- Service Design |
| 74 | IMT4312 Quantitative Methods and Use of Eyetrackers |
| 75 | IMT4316 Information Architecture |
| 76 | TPD4156 Design 7- Service Design |
| 77 | IMT4312 Quantitative Methods and Use of Eyetrackers |
| 78 | IMT4316 Information Architecture |
| 79 | IMT4304 : Cross-Media Color Reproduction |
| 80 | SMF1200 : Introduction to Logistics Management |
| 81 | TØL4014 : Sustainable Manufacturing Systems |
| 82 | NFUT0031 : Norwegian for foreigners, online short course - Campus Ålesund og Campus Gjøvik |
| 83 | PROG2007 - Mobile Programming |
| 84 | IMT3603 - Game Programming |
| 85 | IIK3100 - Ethical Hacking and Penetration Testing |
| 86 | Praksis |
| 87 | IIKG1001 - Cybersecurity and computer networks |
| 88 | IDG2004 - Information Structures and Database Systems  |
| 89 | PROG2007 - Mobile Programming |
| 90 | IIK3100 - Ethical Hacking and Penetration Testing |
| 91 | NFUT0030 - Norwegian for foreigners, online short course |
| 92 | IMT4204 - Intrusion Detection in Physical and Virtual Networks |
| 93 | IIKG2001 - Software Security |
| 94 | IMT4123 - System Security |
| 95 | TTM4536 - Advanced Ethical Hacking  - Information Security, Specialization Course |
| 96 | IIKG3005 - Infrastructure as Code |
| 97 | IMT4113 - Introduction to Cyber and Information Security Technology |
| 98 | IMT4203 - Critical Infrastructure Security |
| 99 | IMT4115 - Introduction to Information Security Management |
| 100 | TPD4156 Design 7- Service Design |
| 101 | IMT4312 Quantitative Methods and Use of Eyetrackers |
| 102 | IMT4316 Information Architecture |
| 103 | IMT4392 Deep Learning for visual computing |
| 104 | IDIG4002 Computer Graphics Fundamentals and Applications |
| 105 | IMT4305 Image Processing and Analysis |
| 106 | IMT4895 Specialising in Colour Imaging |
| 107 | IMT4392 - Deep Learning for Visual Computing |
| 108 | IDIG4002 - Computer Graphics Fundamentals and Applications |
| 109 | IMT4895 - Specialisation in Colour Imaging |
| 110 | PROG2002 - Graphics Programming |
| 111 | PROG2007 - Mobile Programming |
| 112 | IMT3603 - Game Programming |
| 113 | IMT4134 - Specialisation in Software Engingeering |
| 114 | IMT4887 - Specialisation in Web Technology |
| 115 | TPD4156 Design 7- Service Design |
| 116 | IMT4312 Quantitative Methods and Use of Eyetrackers |
| 117 | IMT4316 Information Architecture |
| 118 | IDG1362 - Introduction to User-Centered Design |
| 119 | IDG1292 - Web Coding |
| 120 | IDG2012 - Web Accessibility, Usability and Ethics |
| 121 | IDIG4002 - Computer Graphics Fundamentals and Applications |
| 122 | IMT4884 Advanced Colour Management |
| 123 | IMT4890: Specialisation in Video Processing  |
| 124 | IMT4135: Introduction to Research on Colour and Visual Computing  |
| 125 | IMT4217 - Introduction to Data Privacy |
| 126 | IMT4114 - Introduction to Digital Forensics |
| 127 | IIK500 - Digital Law and Business |
| 128 | IIKG6503 - Introduction to Information Security Management |
| 129 | IMT4114 - Introduction to Digital Forensics |
| 130 | IMT4204 Intrusion Detection in Physical and Virtual Networks |
| 131 | IIKG2001 - Software Security |
| 132 | NFUT0031 - Norwegian for foreigners, online short course |
| 133 | TØL4018 – Renewable Energy Technology  |
| 134 | TØL4023 – Energy system analysis project course |
| 135 | TØL4012 – Sustainability Assessment    |
| 136 | TØL4014 – Sustainable Manufacturing Systems |
| 137 | PROG2002 - Graphics Programming |
| 138 | IMT3603 - Game Programming |
| 139 | IDG1362 - Introduction to User-Centered Design |
| 140 | NFUT0030 - Norwegian for foreigners, online short course |
  
</details>

The course information at the following URL:
www.ntnu.edu/studies/courses/<strong>[course code]</strong>/2023#tab=omEmnet</div>

## Data cleaning
1. Removed the term "praksis" (which means internship)
2. Manually converted # 60 61 and 62 to a format similar to the other entries
3. Extracted course codes with the "text to column" wizard. The separator was the space characters
4. Kept the course codes
5. Trimmed the coures codes
6. Removed duplicates
7. Used concat function to turn the course codes in the following format for scraping :

  |#| Courses |
  |--| ------ |
  | 1 | "IMT4123", |
  | 2 | "MT4113",|
  | ... | ... |
  
8. Scraped the relevant course information with the program in this repository
9. In the course of scraping, the following correcitons to the data were made: 

- course codes "MT4113" were replaced by "IMT4113"
- course codes "IIK1001" were replaced by "IIKG1001"
- the course codes "IMT3104" were replaced by code "PROG2051" because the website mentioned that "PROG2051" was now replacing "IMT3104"
- the course codes "IIK500" were replaced by code "IIK5000"

Because every failed http request was manually checked, along with scrapes that returned "Info not available" values
