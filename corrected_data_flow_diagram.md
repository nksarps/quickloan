# Corrected Data Flow Diagram

The corrected data flow diagram below addresses the key governance, compliance, and ethical gaps identified in QuickLoan’s original pipeline. Each numbered annotation explains the specific control added and why it is necessary for responsible data management.

- **Correction 1 – Step 1: User Mobile App** <br>
**Change Implemented:** Data Minimization Control <br>
**What Was Wrong:** The mobile application collected excessive personal data, including users’ entire contact lists, which is not necessary for assessing creditworthiness.  <br>
**Correction:** Restrict data collection strictly to essential loan-related information such as national ID, income details, repayment history, and phone number.  <br>
**Why It Is Necessary:** This aligns with the Data Minimization principle under Ghana’s Data Protection Act (Act 843) and significantly reduces privacy, security, and regulatory risk.<br>

- **Correction 2 – Between Step 2 & Step 3: API Gateway to Raw Data Database**  <br>
**Change Implemented:** Consent Management Layer  <br>
**What Was Wrong:** Personal data was transferred and stored without capturing explicit, informed user consent.  <br>
**Correction:**  
Introduce a Consent Management module that:  
- Displays clear purpose limitation statements  
- Requires explicit user agreement before submission  
- Logs timestamped consent records prior to data storage
<br>
**Why It Is Necessary:** This ensures lawful data processing under Act 843 and provides documented audit evidence of compliance. <br>

- **Correction 3 – Step 3: Raw Data Database**  <br>
**Change Implemented:** Data Classification & Retention Policy  <br>
**What Was Wrong:** There was no defined data classification level or retention period for stored loan applicant information.  <br>
**Correction:**  
- Classify all loan applicant data as Sensitive  
- Encrypt data at rest  
- Apply strict role-based access controls  
- Implement automatic deletion after a defined retention period (e.g., unsuccessful applications deleted after a specified number of months)
<br>
**Why It Is Necessary:** This prevents indefinite storage, reduces breach exposure, and ensures regulatory compliance with data protection requirements. <br>

- **Correction 4 – Step 7: Decision Service**  <br>
**Change Implemented:** Decision Logging & Explainability  <br>
**What Was Wrong:** Loan approval and rejection decisions were not logged, traceable, or explainable.  <br>
**Correction:**  
- Log every automated decision with standardized reason codes  
- Store feature importance or decision factors  
- Maintain audit trails for internal and regulatory review
<br>
**Why It Is Necessary:** Supports transparency, accountability, and fairness monitoring in automated decision-making systems. <br>
