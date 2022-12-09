---
lab:
    title: 'Lab1: Exercise 2 -  MFA Conditional Access (Complete an Azure Multi-Factor Authentication pilot roll out) '
    type: 'Answer Key'
    module: 'Module 3: Identity and Access Management'
---

# Module 3 - Lab 1 - Exercise 2 -  MFA Conditional Access (Complete an Azure Multi-Factor Authentication pilot roll out)


In this exercise you will configure a conditional access policy enabling Azure Multi-Factor Authentication (Azure MFA) when logging in to the Azure portal. The policy is deployed to and tested on a specific group of pilot users. Deployment of Azure MFA using conditional access provides significant flexibility for organizations and administrators compared to the traditional enforced method.

- Enable Azure Multi-Factor Authentication
- Test Azure Multi-Factor Authentication


### Task 1: Enable Azure Multi-Factor Authentication

1.  Return to the the Azure portal that is logged in as your Global Admin Holly Dickson.

1.  On the Hub go to **Azure Active Directory**,

1.  Click **Groups** and click **+ New group**.

1.  Enter the following information then select **Create**:

      * Group type; `Security`
      * Group Name: `MFA Pilot`
      * Group description: `MFA Pilot Group`
      * Membership type: `Assigned`
      * Members: Select `Lynne Robbins`
  
  
      ![Screenshot](../Media/5457b62d-dc78-4043-bd72-3d7901bbcd71.png)
  
2.  Browse to **Azure Active Directory**, click **Security** under **Manage** and then click **Conditional access** under **Protect**.


3.  Select **+ New policy**.


4.  Name your policy `MFA Pilot`
5.  Under **Users or workload identities**, click **0 users or workload identities selected**. Choose **Select Users and groups** radio button and check the box **Users and groups** Select.
    * Select your pilot group `MFA Pilot`
    * Click **Select**

6.  In the **Cloud apps or actions** section, click **No cloud apps, actions, or authentication contexts selected**.
1. In the drop down box under **Select what this policy applies to**, ensure that **Cloud apps** is selected.
1. Under **Include** Click **Select apps**. Under **Select** click the word **None**.
1. In the **Select - Cloud apps** blade that opens to the far right, type `Microsoft Azure Management` in the search box to add the cloud app for the Azure portal. Click **Select**.
1.  Skip the **Conditions** section
1.  In the **Access controls** section under **Grant**, click **0 controls selected** and make sure the **Grant access** radio button is selected.
    * Check the box for **Require multi-factor authentication**
    * Click **Select**

9.  Skip the **Session** section
10. Set the **Enable policy** toggle to **On**
11. Click **Create**

    **Note**: If the policy fails check your work and **Create** again. 

### Task 2: Test Azure Multi-Factor Authentication


To prove that your conditional access policy works, you test logging in to a resource that should not require MFA and then to the Azure portal that requires MFA.


2.  Open a new browser window in InPrivate or incognito mode and browse to **`https://portal.azure.com`**

       * Log in with the Lynne Robbins user (Lynne's password is likely the same as the MOD Administrator password provided by your lab hoster) and note that you should now be required to register for and use Azure Multi-Factor Authentication.
       * Close the browser window.



# End of lab
