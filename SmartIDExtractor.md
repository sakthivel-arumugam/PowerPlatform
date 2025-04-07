### **SmartIDExtractor**
SmartIDExtractor is a Power Apps-based solution that utilizes AI Builder’s Custom Document Processing model to automatically extract essential base information (e.g., First Name, Last Name, POB, DOB, Nationality, etc.) from uploaded ID cards.

* * * * *

#### **Components Involved:**
1. **Power Apps (Canvas App)** – User interface for uploading ID cards.
2. **AI Builder (Custom Model)** – Trained to extract relevant fields from ID card documents.
3. **Power Automate (Instant Flow, Dataverse connectors)** – For integrating dataverse for storing extracted data.
4. **Dataverse** – Backend for storing extracted data.
* * * * *

#### **Architecture Diagram:**
![image](https://github.com/user-attachments/assets/97fec73e-06d2-4d25-95a2-9312413b4708)

* * * * *

#### **Flow - upload ID document and get the extractions using AI Builder Document Processing Model**
![image](https://github.com/user-attachments/assets/90e2e71a-6124-4fe3-bb4c-09f466ffe0f3)

* * * * *

**Reference Links:**
https://learn.microsoft.com/en-us/ai-builder/form-processing-model-overview
https://learn.microsoft.com/en-us/ai-builder/prompt-modelsettings#temperature

* * * * *

#### **Demo Links ** 

**Power Apps - Canvas:** [https://apps.powerapps.com/play/e/f3a9c683-e734-e79f-b715-3a1c30dfa6db/a/3cd8d331-f3fc-4c23-8757-8679cd02dbdc?tenantId=dabd0981-3847-4c61-99f7-8d1958b2eec2&hint=763e1264-cb03-4f9b-9e45-031c7d5e635a&sourcetime=1742617706622](https://apps.powerapps.com/play/e/f3a9c683-e734-e79f-b715-3a1c30dfa6db/a/08b2e122-e1bd-42d9-9e4d-350f56026635?tenantId=dabd0981-3847-4c61-99f7-8d1958b2eec2&hint=b11c26eb-58d3-48e1-9b74-9984aa06a135&sourcetime=1743851191953&source=portal)

**AI Builder - Document Processing Model**
https://make.powerapps.com/environment/f3a9c683-e734-e79f-b715-3a1c30dfa6db/aibuilder/models/68d37abc-3527-4c13-8ef1-e7faf03ffd24

**Power Automate - Instant Flow**
https://make.powerapps.com/e/f3a9c683-e734-e79f-b715-3a1c30dfa6db/canvas/?action=edit&app-id=%2Fproviders%2FMicrosoft.PowerApps%2Fapps%2F08b2e122-e1bd-42d9-9e4d-350f56026635


