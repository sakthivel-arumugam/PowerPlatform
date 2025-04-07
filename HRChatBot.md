### **HR Chatbot**
The HR Chatbot is an intelligent virtual assistant built using Power Virtual Agents, integrated into Power Apps, Power Automate and Dataverse. 
1. Ask questions about leave policies.
2. Check their leave balance.
3. Submit leave requests conversationally.
4. Trigger Power Automate cloud flow to interact with Dataverse.
5. Store and retrieve data from Dataverse.
   
This chatbot makes leave management easier, faster, and self-service driven.

* * * * *

#### **Components Involved:**
1. **Power Virtual Agents** 
2. **Power Automate:(Cloud flows)** 
3. **Dataverse**
4. **Power Apps**  
5. **Power Pages** 
6. **Azure App Service:** 

* * * * *

```
                           		[ Power Apps ]
                                               |
              ------------------------------------------------------------------
               |                                      			|
	[ User Search ]                         		[ User Action ]
               |                                      			|
    [ Power Virtual Agent ]          		              [ Power Virtual Agent ]
               |                                      			|
       [ Semantic Search ]         			[ Power Automate (User Inputs - Cloud Flow) ]
               |                                      			|
     [ Knowledge Base Search ]              			  [ Dataverse ]
               |                                      			|
    [ Retrive Relevant Chunks ]                       		[ Email Connector ]
               |                                      			|
    [ Response Generation ]                   		      [ Leave Request Submission ]
               |                                      			
    [ Response Delivery ]                 			
                                     					
					

```


* * * * *

#### **Flow 1: User search leave policy related queries to HRChatbot via Power Apps(Leave Assistant System - Canvas App)**

1.  **Power Apps:** User access **Leave Assistant System - Canvas App**, search some query to understand leave policy. Example - **What are the leave policies?**
2.  **Power Virtual Agent:** Checkes **Starter Prompts** and **Topics**, provide search result based on knowldge is boosted with HRChatbot.
3.  **Power Virtual Agent:** Provides all possible related results and link to the document. 

* * * * *

#### **Flow 2: User raise a leave request using HRChatbot via Power Pages(Leave Assistant System)**

1.   **Power Pages:** User navigates to Leave Policy page, search the query like **Need to apply leave.**
2.   **Power Virtual Agent:** Checkes **Starter Prompts** and **Topics**, triggers Topic flow. Collected all related information to raise the leave request and validates it.
3.   **Power Automate:**
   
	- Reads user input from HRChatbot and store it local variables. 
	- Add an entry in Dataverse Table. 
	- Trigger an email for the leave submission.
	- Send return message to HRChatbot.
5.  **Power Virtual Agent:** Receive the status message from Power Automate flow. 
6.  **Power Pages:** User will get an confirmation message from HRChatbot. 

* * * * *

#### **Flow 3: User raise a leave request using HRChatbot via Power Apps(Leave Assistant System - Canvas)**

1.   **Power Apps:** User navigates to Leave History. 
2.   **Dataverse:** Fetch the leave history and provide the results with basic operations like search, reload and filter. 
3.   **Power Apps:** User navigates to Leave Balance.
4.   **Dataverse:** Fetch the leave balance details.

* * * * *

#### **Demo Links ** 

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













 
