---
lab:
    title: 'Lab1: Exercise 2 - Configure retention tags and policies   '
    type: 'Answer Key'
    module: 'Module 9: Information Protection and Governance'
---

# Module 9 - Lab 1 - Exercise 2 - Configure retention tags and policies  

In this exercise, you will configure retention tags and policies, and you will implement archiving with MRM retention tags. 


### Task 1 – Create an MRM retention tag and policy in the Microsoft Purview compliance portal

As part of your pilot project for Adatum, you will configure MRM retention by creating an MRM retention tag and adding it to a new MRM retention policy. You will also assign several default tags to the policy as well. You will then assign this retention policy to Joni Sherman and Alex Wilber's mailboxes.

1. On LON-CL1 virtual machine. In **Microsoft Edge**, navigate to the [**Microsoft Purview compliance portal**](https://compliance.microsoft.com/).

1. In the in the left navigation pane, select **Data lifecycle management** (you may first need to click **… Show all** if its not available) > **Exchange (legacy)** > **MRM Retention tags** and then select **+ New tag**.

1. In **Name your tag** window, under **Name**, type `3 Years Move – Archive after three years`. Click **Next**.

1. On the **Define how the tag will be applied** window, select the **By users to items and folders** option. Click **Next**.

1. Under **Define retention settings**, select the **When the item reaches the following age (in days)** option, and type `1095` in the retention period field.

1. Select **Submit**.  Select **Done** once successful.

1. On the **MRM Retention policies** tab click **+ New policy**. 

1. In **Configure your policy** window, under **Name**, type `Office Retention Policy`.

1. Click **+ Add tag**.

1. In the **Choose retention tags** window, select the tag that you just created, whose name starts with **3 Years Move...** (the column width will truncate the displayed name).

1. Select **Add** > **Next** > **Submit** > **Done**.

1. Add the following tags to the `Office Retention Policy`:
	- Default 2 year move to archive
	- Deleted Items
	- Junk Email
	- Recoverable Items 14 days move to archive

1. Select the `Office Retention Policy` from the list of policies > **Edit**.
1. Click
1. Search for each of the tags and hold down the **Ctrl** key as you select each tag in the list.
1. Click **Add** > **Next** > **Submit** > **Done**. 

1. On the **new retention policy** window, select **Save**.  Select **OK**.

1. Go to the **Exchange Admin Center** [https://admin.exchange.microsoft.com/]. In the left navigation pane, select **Recipients** > Mailboxes.

1. You are now going to apply this retention policy to the mailboxes for your two test users, Joni and Alex. In the list of recipient mailboxes, select **Joni Sherman** (or search for the name and then click it).

1. In the **Joni Sherman** properties window, select the **Mailbox** tab > **Manage mailbox policies**. From the **Retention policy** dropdown, select the `Office Retention Policy` that you created a while ago > **Save** > close the window by clicking the X in the upper right.
1. Repeat the same steps for **Alex Wilber**.

1. Leave your web browser open and proceed to the next task.

You have now created a new retention policy with several retention tags, including a custom personal retention tag. Then you have assigned the retention tags via a retention policy to Alex and Joni’s mailboxes.

 # End of Lab