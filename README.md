# SOC Spear Phishing Investigation

## Project Overview

In this project, I investigated a suspected spear phishing email to determine whether it was malicious and posed a risk to the organisation.

The investigation focused on analysing the email content, headers, sender information, and any embedded links or attachments. The goal was to identify indicators of compromise (IOCs) and confirm whether the email was a targeted phishing attempt.

I reconstructed the attack scenario, validated suspicious elements, and documented the findings along with recommended response actions.

This project reflects a real SOC workflow for email-based threat investigation, including detection, analysis, validation, and incident response.

---

## SOC Workflow

1. Suspicious email reported by user  
2. Analysed email content for phishing indicators  
3. Reviewed email headers to identify the true source  
4. Investigated sender address and domain reputation  
5. Examined links or attachments for malicious intent  
6. Correlated findings to identify indicators of compromise  
7. Assessed risk and likelihood of targeted attack  
8. Documented findings and recommended response actions  

---

## Investigation Focus

The investigation focused on identifying common spear phishing indicators, including:

- Use of **urgent or deceptive language**  
- Mismatch between sender name and actual email address  
- Suspicious or spoofed domains  
- Malicious or shortened URLs  
- Unexpected attachments  
- Signs of impersonation or targeting  

---

## Attack Timeline

- A suspicious email was received by the user  
- The email appeared to come from a trusted or known source  
- Analysis revealed inconsistencies in the sender details  
- Suspicious links or content were identified within the email  
- Further investigation confirmed indicators of phishing activity  

---

## Analysis

The email displayed multiple characteristics of spear phishing.

Spear phishing attacks are typically targeted and designed to appear legitimate by mimicking trusted sources. The presence of mismatched sender details, suspicious links, and deceptive messaging suggests an attempt to trick the user into taking an action such as clicking a link or providing sensitive information.

These indicators strongly suggest that the email was crafted with malicious intent.

---

## Conclusion

This email is classified as **malicious** and consistent with a spear phishing attempt targeting the user.

---

## Impact Assessment

If successful, this attack could have resulted in:

- Credential theft  
- Unauthorised account access  
- Malware infection via malicious links or attachments  
- Data exposure or further compromise  

---

## Response Actions

- Block or quarantine the phishing email  
- Report the sender domain and IP address  
- Alert other users about the phishing attempt  
- Block malicious URLs at the network level  
- Conduct user awareness training  
- Monitor for similar phishing campaigns  

---

## MITRE ATT&CK Mapping

- **Tactic:** Initial Access  
- **Technique:** T1566 – Phishing  

---

## Limitations

- Limited visibility into full email infrastructure  
- No access to full attachment or payload analysis  
- Additional threat intelligence sources would improve validation  

---

## Skills Demonstrated

- Email threat analysis  
- Phishing detection and investigation  
- Header and sender analysis  
- Identification of malicious indicators  
- Incident reporting and response planning  

---

## Data Source

The dataset used in this project was simulated to represent realistic phishing email scenarios for SOC investigation practice.
