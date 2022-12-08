---
lab:
    title: 'Lab1: Exercise 1 - Investigate Your Microsoft 365 Data '
    type: 'Answer Key'
    module: 'Module 14: Discover and Respond'
---

# Module 14 - Lab 1 - Exercise 1 - Investigate Your Microsoft 365 Data


In your role as Holly Dickson, Adatum’s Security Administrator, you have Microsoft 365 deployed in a virtualized lab environment. As you proceed with your Microsoft 365 pilot project, you now want to test how Adatum can investigate its Microsoft 365 data. You have decided to focus on performing a content search for deleted emails, which is a common request at Adatum, and then you want to analyze eDiscovery functionality by creating an eDiscovery case. You will conclude this portion of the pilot project by creating a GDPR data subject request.

### Task 1 – Perform a content search for deleted emails

In this exercise, you will add Joni Sherman and Holly Dickson as members of the eDiscovery Manger role, and then you will log into the Client VM as Joni and perform a content search that looks for emails with the keywords related to social security numbers.

1. You should still be logged into your Client 1 VM (LON-CL1) as the **LON-CL1\Admin** account, and you should be logged into Microsoft 365 as **Holly Dickson**. 
1. Return to the **Microsoft Purview Compliance portal**: `https://compliance.microsoft.com/`.
1. Click **Permissions** > **Roles** under **Microsoft Purview solutions** > **eDiscovery Manager**.
1. In the **eDiscovery Manager** role group window, scroll down to the **eDiscovery Manager** section and select **Edit**.
1. The **Editing Choose eDiscovery Manager** wizard opens. The list should be empty. Select **Choose eDiscovery Manager**.
1. In the **Choose eDiscovery Manager window**, select **(+) Add**.
1. Search for `Joni Sherman` and then `Holly Dickson` and click the checkbox next to each one. Click **Add**.
1. You should see a banner with the message **2 members added**. Select **Done** and then **Save**. Click **Close**.

10. Switch to the Client 2 VM (**LON-CL2**). You should still be logged into **LON-CL2** as the **LON-CL2\Admin** account, and log into Microsoft 365 as **Joni Sherman**. In the **Sign in** window, enter **JoniS@M365xZZZZZZ.onmicrosoft.com** (where ZZZZZZ is your unique tenant ID provided by your lab hosting provider). Select **Next**. In the **Enter password** window, enter Joni's password (hint: it is probably the same as the MOD password assigned by your lab hoster).

11. If you have a tab open in your **Edge** browser for the **Microsoft Purview compliance portal**, then select it now. Otherwise, select a new tab and enter the following URL in the address bar: `https://compliance.microsoft.com`.

12. In the **Microsoft Purview compliance portal**, in the left navigation pane, select **Search**, and then under it select **Content search**.  

    ‎**Note**: If you cannot see **Search** in the navigation pane yet, you need to reload the browser tab with the **Microsoft Purview compliance portal.**

13. On the **Content search** window, in the **Search** tab, select **+ New search** on the top menu. This will initiate the **New search** wizard.

14. On the Name your search page, enter `Content Search Test` into the **Name** field and then select **Next**.

15. On the Locations page, select **All locations** and then select **Next**.

‎**Note**: If **Specific locations** radio button is selected and **All location** option is not found, then enable the **Status** slider manually for all the available locations.

16. On the **Define your search conditions** page, enter `SSN` press enter and type `social` into the **Keywords** box.  Pressing enter between keywords will separate the words as independent terms in the list. Once the two terms are added select **Next**. On the **Review your search and create it** page review all the details and if any changes required click **Edit** and update the necessary changes. Click **Submit** and then click **Done**.

17. Back on the **Searches** tab, the Search query will run. The Status field in the bottom-left corner of the screen will indicate when the query is complete. It may take many minutes for the query to run and the data to be displayed in the right pane. When the content search finishes, you will see all mailbox items that you have created for the sensitive information test of your custom DLP policy.  

If you didn't send emails during the DLP lab earlier in the course then no data will appear in this search.  If this happened, while the search is running, you could switch back to **LON-CL1** and send emails with the keyword terms mentioned in this lab to other users in your tenant.  You may have to run this search again to view data if you do that.

You can let the search run while you proceed with the remainder of this exercise. 

18. Leave the Client 2 VM open as well as all browser tabs and continue with the next task.

You have successfully assigned an eDiscovery role to Joni and performed a content search for a specific keyword across all locations of your tenant.

 

### Task 2 – Create an eDiscovery case

In this task, you will create an eDiscovery case with a configured hold and content search for any violations regarding social security numbers. You will continue using Joni Sherman’s user account. Having been assigned the eDiscovery Managers role in the prior task, Joni has the permissions necessary to create an eDiscovery case.

1. You should still be logged into your Client 2 VM (**LON-CL2**) as the **LON-CL2\Admin** account and signed into Microsoft 365 as Joni Sherman. However, if you have been signed out of Microsoft 365, then on the Microsoft 365 sign-in page, sign into Joni’s **JoniS@M365xZZZZZZ.onmicrosoft.com** account using her password assigned by your lab hoster.

2. The **Microsoft Purview compliance portal** should still be open in a tab in Microsoft Edge. If so, select that tab now. If not, then enter the following URL in the address bar: `https://compliance.microsoft.com`. 

3. In the **Microsoft Purview compliance portal**, in the left navigation pane, select **eDiscovery**, and then under it, select **Standard**.

4. On the **eDiscovery** window, select **(+) Create a case** on the top menu.

5. In the **New case** window, enter `Social Security Violation` into the **Name** field and select **Save**.

6. Back on the **eDiscovery** page, select **Open** that appears to the left of the **Social Security Violation** case.

7. On the **Social Security Violation** window, select the **Hold** tab from the top menu.

8. Select **(+) Create** to create a new hold. This initiates the **Create a new hold** wizard.

9. On the **Name your hold** page, enter `Social Security Violation - Content` into the **Name** field and then select **Next**.

10. On the **Choose locations** page, For the location **Exchange mailboxes**, select **Choose users, groups or teams**.

13. Enter **Holly** into the search field and press **Enter**. 

13. Scroll down on the page, and under **Name**, select **Holly Dickson** from the search results and select **Done**.

15. On the **Choose locations** page, **1** is displayed to the right of **Exchange mailboxes**. Select **Next**.

16. On the **Query conditions** page, enter `SSN` press enter and then type `social` into the **Keywords** box.  This will search for those two terms independently. Then select **Next**.

17. On the **Review your settings** page, review the values and select **Edit** next to any that need to be modified. When you are satisfied with the settings, select **Submit**, then select **Done**.

18. Back on the **eDiscovery Case overview**, on the **eDiscovery (Standard) > Social Security Violation > Hold** page, select the **Searches** tab from the top menu.

19. Select **+ New search**.

20. In the **New search** window,in the **Name and description** page enter `Social Security Violation - Search` into the **Name** field and select **Next**. Under the **Locations** page, select **Locations on hold** and click **Next**.

21.  In the **Define your search conditions** page, enter `SSN` press enter and then type `social` in the **Keywords** field and then click **Next**. 

22. On the **Review your search and create it** page, review the values and select **Edit** next to any that need to be modified. When you are satisfied with the settings, select **Submit**, then select **Done**.

23. This will initiate a search query that looks for the keywords **SSN**. Once the query is finished, wait for the preview results to be displayed. 

‎**Note**: If you scroll to the right corner of the newly created search, the **Status** field will show the status of the search whether started or completed, click **Refresh** to view the current status.

You have now created an eDiscovery case, added an In-Place Hold to preserve mailbox content, and created a search to discover data from the hold.


# Proceed to Lab1 - Exercise 2
