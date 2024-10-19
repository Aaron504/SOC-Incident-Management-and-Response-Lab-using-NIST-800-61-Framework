# SOC Incident Management and Response Lab using NIST 800 61 Framework
<p align="center">

![Screenshot 2024-10-19 121305](https://github.com/user-attachments/assets/4b928c23-31ad-4262-8333-dd6a921fd567)

</p>

In this lab, I managed and responded to security incidents within Azure Sentinel following the NIST 800-61 Incident Management Lifecycle. I started by analyzing detected alerts, setting severity levels, assigning owners, and investigating timelines and related events to determine whether incidents were legitimate (True Positive) or false alarms. For valid incidents, I applied containment, eradication, and recovery measures using automated playbooks. Finally, I documented my findings and closed the incidents in Sentinel. This lab demonstrates my ability to effectively manage and respond to security incidents in a structured SOC environment.




<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Microsoft Sentinel
- Log Analytics

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Step 1 - Preparation
- (We initiated this already by ingesting all of the logs into Log Analytics Workspace and Sentinel and configuring alert rules)

- Step 2 - Detection & Analysis
- Step 3 - Containment, Eradication, and Recovery
- Step 4 - Document Findings/Info and Clouse out the Incident in Sentinel


<h2>Deployment and Configuration Steps</h2>

- Step 2: Detection & Analysis (You may have different alerts/incidents)
- Set Severity, Status, Owner
  ![Screenshot 2024-10-19 123706](https://github.com/user-attachments/assets/c075c2d3-1aac-42e0-b8d1-f63967bcd9ce)

- View Full Details (New Experience)
  ![Screenshot 2024-10-19 123853](https://github.com/user-attachments/assets/e503d268-3197-4a53-9a08-9ca2bd6b4581)

- Observe the Activity Log (for history of incident)
  ![Screenshot 2024-10-19 124123](https://github.com/user-attachments/assets/e5e10ac5-eeaa-402a-a344-d7c82a1ac3c8)

- Observe Entities and Incident Timelines (are they doing anything else?)
  ![Screenshot 2024-10-19 124336](https://github.com/user-attachments/assets/88f69901-716c-4f9a-8573-fb1ce5e2b03b)
  ![Screenshot 2024-10-19 124619](https://github.com/user-attachments/assets/0c1e04a6-578e-40b3-b7fa-aecf5af56773)


- “Investigate” the incident and continue trying to determine the scope
  ![Screenshot 2024-10-19 124912](https://github.com/user-attachments/assets/d5d5d1b8-5487-4bd6-bdd2-6f45277b4f71)

- Inspect the entities and see if there are any related events
  ![Screenshot 2024-10-19 125350](https://github.com/user-attachments/assets/cf5ba8fb-1356-4803-bef2-aeda95ff35a2)

- Determine legitimacy of the incident (True Positive, False Positive, etc.)
- If True Positive, continue, if False positive, close it out
  ![Screenshot 2024-10-19 132155](https://github.com/user-attachments/assets/3bd5151f-ac0f-4b09-b817-171e58b019fa)

- Running this query let me know that none of the malicious attacker were able to successfully log in to the system making it a false positive.
  ![Screenshot 2024-10-19 131646](https://github.com/user-attachments/assets/77f321a7-0234-4e5b-bef3-0a0d3a8d478e)

- Step 3: Containment, Eradication, and Recovery
- Use the simple Incident Response PlayBook

![Screenshot 2024-10-19 132625](https://github.com/user-attachments/assets/56bb19f1-c273-4e2e-b349-2b0ee7dd063c)

After, here I did some system hardening by allowing traffic to come in from my IP address only.
![Screenshot 2024-10-19 133001](https://github.com/user-attachments/assets/bc82bd0f-f258-41d6-b053-e9dfaf950761)
![Screenshot 2024-10-19 133323](https://github.com/user-attachments/assets/a88015d9-27e4-4b86-b6ae-30e98ce2c814)

Here I'm doing more system hardening by adding a inbound rule to the network security group.
![Screenshot 2024-10-19 134115](https://github.com/user-attachments/assets/c63411ef-dfb2-43ac-9b2a-4a73714b4e34)









