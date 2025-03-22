### **HR Chatbot for Leave Management**
To streamline the leave management process by providing instant responses to leave-related queries, automating leave requests and approvals, and maintaining a centralized database of leave records.

* * * * *

#### **Components Involved:**
1. **Power Virtual Agents:(Starter prompts, Knowledge, Topics, Channels)** To create the chatbot interface.
2. **Power Automate:(Cloud flows, Dataverse connectors, Email connectors)** To automate workflows and integrate with other systems.
3. **Dataverse:(Tables)** To store and manage data.
4. **Power Apps:(AppHeader, AppFooter, Chatbot, Azure Text to speech, Azure Speech-to-text)** UI interface to get leave history, available balance and Power Virtual Agent for user interaction to understand leave policies, raising leave request. 
5. **Power Pages(Data forms, Chatbot):** UI interface with interactive Virtual Agent for user interaction to understand leave policies, raising leave request.
6. **Azure App Service:** To access Dataverse tables via Dataverse Web API and deploy that service in Azure App Service. 

* * * * *

#### **Flow - Add Knowledge to Agent** 
![Image](https://github.com/user-attachments/assets/ba2a9fb5-8d30-4e0e-8a51-62d877386963)

* * * * *

#### **Flow - User search query from Agent**
![Image](https://github.com/user-attachments/assets/dd141b86-468b-450f-ada3-954d99740bfc)

* * * * *

#### **Architecture Diagram:**
![Image](https://github.com/user-attachments/assets/73b343b4-769c-4b85-bf81-14683faadf30)

* * * * *

#### **Flow 1: User search leave policy related queries to HRBot Agent via Power Apps(Leave Assistant System - Canvas App)**

1.  **Power Apps:** User access **Leave Assistant System - Canvas App**, search some query to understand leave policy. Example - **What are the leave policies?**
2.  **Power Virtual Agent:** Checkes **Starter Prompts** and **Topics**, provide search result based on knowldge is boosted with Agent.
3.  **Power Virtual Agent:** Provides all possible related results and link to the document. 

* * * * *

#### **Flow 2: User raise a leave request using HRBot Agent via Power Pages(Leave Assistant System)**

1.   **Power Pages:** User navigates to Leave Policy page, search the query like **Need to apply leave.**
2.   **Power Virtual Agent:** Checkes **Starter Prompts** and **Topics**, triggers Topic flow. Collected all related information to raise the leave request and validates it.
3.   **Power Automate:**
   
	- Reads user input from Agent and store it local variables. 
	- Add an entry in Dataverse Table. 
	- Trigger an email for the leave submission.
	- Send return message to Agent.
5.  **Power Virtual Agent:** Receive the status message from Power Automate flow. 
6.  **Power Apps:** User will get an confirmation message for Power Agent. 

* * * * *

#### **Flow 3: User raise a leave request using HRBot Agent via Power Apps(Leave Assistant System - Canvas)**

1.   **Power Apps:** User navigates to Leave History. 
2.   **Dataverse:** Fetch the leave history and provide the results with basic operations like search, reload and filter. 
3.   **Power Apps:** User navigates to Leave Balance.
4.   **Dataverse:** Fetch the leave balance details.

* * * * *

#### ** Demo **
**Power Virtual Agent:**
https://copilotstudio.microsoft.com/environments/f3a9c683-e734-e79f-b715-3a1c30dfa6db/bots/crd77_leaveAssistant/webchat?__version__=2

**Power Page:**
https://employeeleavemanagement-e626.powerappsportals.com/leave-policy/

**Power Apps - Canvas:**
https://apps.powerapps.com/play/e/f3a9c683-e734-e79f-b715-3a1c30dfa6db/a/3cd8d331-f3fc-4c23-8757-8679cd02dbdc?tenantId=dabd0981-3847-4c61-99f7-8d1958b2eec2&hint=763e1264-cb03-4f9b-9e45-031c7d5e635a&sourcetime=1742617706622

**Azure Portal:**
https://portal.azure.com/#@basavakumarrmoutlook.onmicrosoft.com/resource/subscriptions/2276e794-3271-4193-bcf6-dbb25c698499/resourceGroups/DAI-Team3/providers/Microsoft.Web/sites/EmployeeService/appServices

**Azure App Service:**
https://employeeservice-a6csfubhhsgpgcht.canadacentral-01.azurewebsites.net/swagger/index.html













 
