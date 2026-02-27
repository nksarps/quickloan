# Summary of Review Process

In conducting this governance review of **QuickLoan’s data pipeline**, I applied **Data Lifecycle principles** to systematically examine each stage of data handling: collection, transmission, storage, preprocessing, decision-making, analytics, and third-party sharing. By mapping risks to specific lifecycle stages, I identified critical weaknesses such as:  

- Excessive data collection at onboarding  
- Absence of explicit consent before storage  
- Lack of classification and retention controls in the database  
- Insufficient validation during preprocessing  
- Missing transparency in automated decisions  

Viewing the system through the lifecycle lens made it easier to pinpoint where governance controls were absent or weak.  

I then applied **Data Classification principles** to determine the sensitivity level of the information processed. Loan applicant data includes financial details and personally identifiable information, which classifies it as **Sensitive data**. This classification immediately highlighted the need for stronger controls such as:  

- Encryption  
- Role-based access restrictions  
- Masking and anonymization  
- Defined retention schedules  

These measures help align QuickLoan’s processes with **Ghana’s Data Protection Act (Act 843)**.  

The proposed reporting metric, **Demographic Approval Rate Disparity (DARD)**, strengthens ethical and transparent governance by continuously measuring differences in loan approval rates across demographic groups. By monitoring and visualizing this metric regularly, QuickLoan can:  

- Proactively detect potential bias in its machine learning model  
- Demonstrate accountability to regulators  
- Ensure automated lending decisions remain fair, explainable, and compliant with data protection standards
