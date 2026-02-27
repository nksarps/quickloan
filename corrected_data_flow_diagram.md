# Corrected Data Flow Diagram

The corrected data flow diagram below addresses the key governance, compliance, and ethical gaps identified in QuickLoan’s original pipeline. Each numbered annotation explains the specific control added and why it is necessary for responsible data management.

- **Correction 1 – Step 1: User Mobile App**  
**Change Implemented:** Data Minimization Control  
**What Was Wrong:** The mobile application collected excessive personal data, including users’ entire contact lists, which is not necessary for assessing creditworthiness.  
**Correction:** Restrict data collection strictly to essential loan-related information such as national ID, income details, repayment history, and phone number.  
**Why It Is Necessary:** This aligns with the Data Minimization principle under Ghana’s Data Protection Act (Act 843) and significantly reduces privacy, security, and regulatory risk.

- **Correction 2 – Between Step 2 & Step 3: API Gateway to Raw Data Database**  
**Change Implemented:** Consent Management Layer  
**What Was Wrong:** Personal data was transferred and stored without capturing explicit, informed user consent.  
**Correction:**  
Introduce a Consent Management module that:  
- Displays clear purpose limitation statements  
- Requires explicit user agreement before submission  
- Logs timestamped consent records prior to data storage  
**Why It Is Necessary:** This ensures lawful data processing under Act 843 and provides documented audit evidence of compliance.

- **Correction 3 – Step 3: Raw Data Database**  
**Change Implemented:** Data Classification & Retention Policy  
**What Was Wrong:** There was no defined data classification level or retention period for stored loan applicant information.  
**Correction:**  
- Classify all loan applicant data as Sensitive  
- Encrypt data at rest  
- Apply strict role-based access controls  
- Implement automatic deletion after a defined retention period (e.g., unsuccessful applications deleted after a specified number of months)  
**Why It Is Necessary:** This prevents indefinite storage, reduces breach exposure, and ensures regulatory compliance with data protection requirements.

- **Correction 4 – Step 7: Decision Service**  
**Change Implemented:** Decision Logging & Explainability  
**What Was Wrong:** Loan approval and rejection decisions were not logged, traceable, or explainable.  
**Correction:**  
- Log every automated decision with standardized reason codes  
- Store feature importance or decision factors  
- Maintain audit trails for internal and regulatory review  
**Why It Is Necessary:** Supports transparency, accountability, and fairness monitoring in automated decision-making systems.
