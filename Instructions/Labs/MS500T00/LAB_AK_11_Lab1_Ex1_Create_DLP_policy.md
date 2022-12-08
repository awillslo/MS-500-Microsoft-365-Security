---
lab:
    title: 'Lab1: Exercise 1 - Manage DLP Policies  '
    type: 'Answer Key'
    module: 'Module 11: Data Loss Prevention'
---

# Module 11 - Lab 1 - Exercise 1 - Manage DLP Policies  


In your role as Holly Dickson, Adatum’s Security Administrator, you have Microsoft 365 deployed in a virtualized lab environment. As you proceed with your Microsoft 365 pilot project, your next steps are to implement Data Loss Prevention (DLP) policies at Adatum. You will begin by creating a custom DLP policy, and then you will test DLP policies related to email message archiving and emails with sensitive data. 

### Task 1 – Create a DLP policy with custom settings

In this exercise you will create a Data Loss Prevention policy in the Security & Compliance Center to protect sensitive data from being shared by users. The DLP Policy that you create will inform your users if they want to share content that contains U.S. Social Security addresses.

1. You should still be logged into your Client 1 VM (**LON-CL1**) as the **LON-CL1\Admin** account, and you should be logged into Microsoft 365 as **Holly Dickson**. 

1. Return to the **Microsoft Purview compliance portal** `https://compliance.microsoft.com/` click **Data loss prevention** > **Policies** > **Create policy**.

1. On the **Start with a template or create a custom policy** page, under **Categories** click **Custom** > **Custom policy** > **Next**.

1. In the **Name your policy** page, type `Social Security DLP Policy` in the **Name** field and `Protect social security numbers from being shared` in the **Description** field. Select **Next**.

1. On the **Choose locations** page, select On for **Exchange email, SharePoint sites, OneDrive accounts, Teams chats and channel messages** and **Off** for **Microsoft Defender for Cloud Apps, On-premises repositories, Power BI** and then select **Next**.

1. On the **Define policy settings** page click **Next**.

1. On the **Customize advanced DLP rules** click **+ Create rule**.

1. On the **Create rule** page, in the **Name** field type `Social Security Number`.

1. Under **Conditions** click **+ Add condition** > **Content Contains**.

1. Leave the value of **Default** for **Group name**, click **Add** > **Sensitive info types**.

1. In the search field type `social` and press enter, and wait until the search results are displayed.

1. In the list of search results, select the **U.S. Social Security Number (SSN)** check box, and then select **Add**.

1. In the U.S. Social Security Number (SSN) row, change the **Instance count** from **1** to **2**.

1. Below the **Content contains** box, click **+ Add Condition** and select **Content is shared from Microsoft 365**.

1. In the field below this, verify that **only with people inside my organization** is displayed.

1. Scroll down to **Actions** section.

1. Click **+ Add an Action** > **Restrict access or encrypt the content in Microsoft 365 locations**.

1. Check the box **Restrict access or encrypt the content in Microsoft 365 locations** and select **Block everyone**.

1. Scroll down to **Incident reports**.

1. Select **Medium** in the field **Use this severity level in admin alerts and reports**.

1. Move the slider bar for **Send and alert to admins when a rule match occurs** to **On**.

1. Select **Save**.

1. Click **Next** > **Next**.

1. On the **Test or turn on policy** page select **Turn it on right away** and select **Next**.

1. Click **Submit** and then select **Done**.

You have now created a DLP policy that scans for US Social Security numbers in emails and documents that are sent or shared in your organization.


# Proceed to Exercise 2 
