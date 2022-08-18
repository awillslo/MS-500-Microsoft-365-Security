---
lab:
    title: 'Lab1: Exercise 1 - Conduct a Spear phishing attack '
    type: 'Answer Key'
    module: 'Module 6: Threat Management'
---

# Module 6 - Lab 1 - Exercise 1 - Conduct a Spear phishing attack


Holly Dickson is concerned that some users in her organization may require education about phishing attacks.  In this lab you will use the Microsoft 365 Attack simulator to determine your users' susceptibility to phishing attacks.

### Task 1: Configure and launch a Spear Phishing attack

1. Go to [Microsoft 365 security center - Attack simulation training](https://security.microsoft.com/attacksimulator) and login as **Holly Dickson**.

2. Click the **Simulations** tab. Select **+ Launch a Simulation**.

3. On the **Select Technique** screen. Ensure that **Credential Harvest** is selected. Click **Next**.

4. Name the simulation `Spear Simulation` and select **Next**.

5. On the **Select Payload** screen, select a desired payload from the list of provided payloads. Click **Next**.

6. In the **Target Users** screen, do the following:
	1. Ensure **Include only specific users and groups** is selected. 
	1. Click **Add Users**. 
	1. On the **Add Users** screen, type  **Patti Fernandez** in the search box and hit Enter. 
	1. Select the user from the search results list. 
	1. Click **Add 1 User** at the bottom. 
	1. Click  **Next**.

7. Leave the default settings on the **Assign training** screen. Click **Next**.

8. On the **Landing page** screen, click **Next**.

9. On the **Select end user notification** screen, select **Microsoft default notification (recommended)**.

10. Select **Delivery Preferences** and select **Deliver during campaign**. Click **Next**.

11. On the **Launch Details** page, ensure that **Launch this simulation as soon as I'm done** is selected. Click **Next**.

12. On the **Review Simulation** screen, click **Submit**. Click **Done**

### Task 3: Confirm target received phishing email attack

1.  Open a new browser window in InPrivate or incognito mode and browse to `https://office.com`.

2.  Log in as the user Patti Fernandez **PattiF@M365xZZZZZZ.onmicrosoft.com** where ZZZZZZ is your specific Office 365 tenant. Patti's password is likely the same as the MOD administrator's password provided by your lab hosting providor.

3.  Click the Outlook icon to open Microsoft Outlook for Patti. You should see a spear phishing email that includes the details you just entered in the previous task.

### Task 4: Review the results

1. In your browser session where you are logged in as Holly Dickson go back to the [Attack simulation training](https://security.microsoft.com/attacksimulator). Click the **Simulations** tab.

2. In the simulation details area, notice the Actual and Predicted compromised rates.

3. Click on the **Spear Phishing** simulation and in the Simulation Impact area, click **View users**.  
    
	**Note**: Since you can run multiple spear phishing simulation campaigns simultaneously you could create different simulations for different users and groups.  These different simulations might have enticements that are more appropriate for different users.
	
4. In the list of users select **Export** to export a list of users who fell victim to the simulated spear-phishing attack.
 

# End of lab.
