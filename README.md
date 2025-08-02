# service-now-urgent-incident-notification-workflow
Workflow created in ServiceNow to send notification to Network Operations group for critical incidents.

System Overview: The workflow triggers when a new inicdent is created and the category is network and the priority is critical. If that critera is met a notification sends to the Network Operations team informing them that a critical incident has been created for them to handle to not miss the SLA. 

Implementation Steps: Updates made to the flow were one on the trigger condition. It was initally set to created only, I set it to cerat or update as an incident could potentially be promoted to a critical and the team would want to be aware. Secondly, I set critera against the trigger to only send if the priority is 1-critical and category is network. Lastly, I created a unique email notification in the notifications model that sends to the Network Operations group and selected that notificaiton to send from the workflow. 

Architecture Diagram: See attached. 

AI Scenario: There are a couple of things that come to mind that an AI agent could use to enhance the incident routing process. One, I'd like to mention that there are innate ServiceNow tools with some of these capabilities like On-call schedule for incidents and major incident management as well as advanced work assignments; yet I think it would be the combination of the AI agent working with some of these capabilities that could really take it to the next level. 

My seggestion would be for an AI agent to review capabilities like the on-call schedule and then be able to look at an engineers previous cases and skills to then determine who to route a case to. It would be able to take into consideration which users are on call on that day in that paritcual time zone, and from those that are on call, based on listed skills and case history, identify which of the on call engieeners should be contacted through a non traditional method (phone call or SMS) to be aware and handle the major incident. 

