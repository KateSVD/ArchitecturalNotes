# ArchitecturalNotes
What questions to investigate while choosing application architecture

Architecture guide in Microsoft documentation https://learn.microsoft.com/en-us/azure/architecture/guide/  is a very good step-by-step guide on designing architecture for your application. 

After you have got a bare minimum of requirements from the customer, you can start diving into some more details (which are still quite high level but answers on questions below will help you to choose a general strategy and architecture).
I made a set of questions that in my opinion are quite helpful in the process of designing applications.
1) Domain
   - What are the main entities and their attributes?
   - What types will the attributes be having? Any unusual (large files, video, audio)? 
   - Evaluate what is the overall complexity of the domain?
   - What is special about the domain?
   - Scale of domain: the number of entities, attributes, how is it going to expand over time?
2) Parts of the system (web app, mobile app, wearable device, IOT device ...)
3) Messaging
   - How often and how much data are running back and forth?
   - What parts of application are participating in messaging?
   - What is async model for data transfering?
4) Computing
   - How complex are calculations, data processing?
   - Define time/cpu/memory consuming operations.
5) Reliability
   - What are requirements to the system reliability?
   - Is it critical to minimize downtime?
   - What are requirements to the data backup/replication?
   - Failures handling (behavior on crash, how critical each of failure type is).
6) Security
   - Authentication requirements.
   - Data protection.   
7) Maintenance and distribution (logs, updates, stats, reports, hosting)

Better option if you will investigate those questions in dynamic: MVP and potential scaling, also take into account what parts of the system and when going to be growing.
