## **Lab 04 - Creating a DLP policy and generating an alert in Microsoft Purview**

### Introduction

Microsoft Security Copilot is a cloud-based AI platform that can
assist you in identifying, summarizing, triaging, and remediating alerts
and events in Microsoft Purview for:

- Microsoft Purview Data Loss Prevention (DLP)

- Microsoft Purview Insider Risk Management

- Microsoft Purview Communication Compliance

- Microsoft Purview eDiscovery

It also supports security and compliance professionals in different
scenarios, such as alert and incident response, threat hunting, and
intelligence gathering. For more information about what it can do

### Objectives

- To create a Microsoft Purview account.

- To create custom Data Loss Prevention (DLP) policies for Microsoft
  Security Copilot.

- To test the effectiveness of the DLP policy by sending simulated
  credit card information to a specific user in Microsoft Teams,
  observing flagged messages, and checking alerts in the Purview portal.

### Task 1: Creating Microsoft Purview Account

1.  In Microsoft Azure portal search bar, type +++**Microsoft Purview
    accounts**+++, then navigate and click on **Microsoft Purview
    accounts** under **Services**.

![](./media/image1.png)

2.  In the **Microsoft Purview accounts** page, click on **+ Create**.

> ![A screenshot of a computer Description automatically
> generated](./media/image2.png)

3.  In the **Create Microsoft Purview account** page, enter the
    following details and click on **Review + Create** button.

    |Subscription |Azure Pass |
    |---|---|
    |Resource group |**MCS-RG** |
    |Microsoft Purview account name |Enter the name of your choice (here, we entered **securitycopilot2**) |
    |Location |**West Central US** |

> ![](./media/image3.png)

3.  After validation is passed, click on the **Create** button.

> ![A screenshot of a computer Description automatically
> generated](./media/image4.png)

3.  Open a new tab in the Edge browser address bar and enter the
    following
    URL: +++**https://purview.microsoft.com/**+++
    If prompted, then sign in with your O365 tenant credentials. 
    On **Welcome to the new Microsoft Purview portal!** dialog box,
    agree to the terms and conditions, then click on the **Get
    started** button.

> ![A screenshot of a computer Description automatically
> generated](./media/image5.png)

4. In case, Important changes to our business and pricing model dialog box appears, then navigate and click on **I consent** button at the bottom. 

> ![](./media/image11a.png)

5.  You'll be directed to Microsoft Purview portal.

> ![A screenshot of a computer Description automatically
> generated](./media/image6.png)

### Task 2: Setting Custom DLP policies for Microsoft Security Copilot

1.  In the **Microsoft Purview** portal, navigate to **Solutions**, then
    click on **Data loss prevention** as shown in the below image.

![A screenshot of a computer Description automatically
generated](./media/image7.png)

2.  Click on **Policies**. In the **Policies** page, navigate and click
    on **+Create policy**.

![A screenshot of a computer Description automatically
generated](./media/image8.png)

3.  In **Template or custom policy** pane, under **Categories**,
    navigate and click on **Custom**. Under **Regulations**, click on
    **Custom policy**. Then, click on the **Next** button.

![](./media/image9.png)

4.  On **Name your DLP policy** pane, in the **Name** field, enter the
    following name:

    +++**Custom Policy for Microsoft Security Copilot**+++, then click on the **Next** button.

![](./media/image10.png)

5.  Leave the **Assign admin units** pane in the default state and click
    on the **Next** button.

![A screenshot of a computer Description automatically
generated](./media/image11.png)

6.  On **Choose where to apply the policy** pane, select the check boxes
    of **Exchange email, Sharepoint sites, OneDrive accounts, Team chat
    and channel messages**, and **Devices**, then click on the **Next**
    button.

> ![A screenshot of a computer Description automatically
> generated](./media/image12.png)

7.  On **Define policy settings** pane, select the radio button of
    **Create or customize advanced DLP rules** and click on the **Next**
    button.

![A screenshot of a computer Description automatically
generated](./media/image13.png)

8.  On **Customized advanced DLP rules** pane, click on **+ Create
    rule**

![](./media/image14.png)

10.  On the **Create rule** page, in the **Name** field, enter
    +++**Sensitive Information of Credit Card**+++.

![](./media/image15.png)

10. Scroll down to **Conditions** section and click on **+Add
    condition**, then select **Content contains** as shown in the below
    image.

![](./media/image16.png) 

11. In the **Content contains** section, leave
**Group name** and **Group operator** in default state, click on the
dropdown beside **Add** and select **Sensitive info types** as shown in
the below image.

![](./media/image17.png)

12\. In the **Sensitive info types** pane that appear on the right side,
type +++**credit card number**+++ in the search bar and press
the **Enter** button. Select **Credit Card Number** check box, then
click on the **Add** button.

![](./media/image18.png)

![A screenshot of a computer Description automatically
generated](./media/image19.png)

13. Scroll down to **User notifications** section and Turn **On** the
    toggle button.

![](./media/image20.png)

14. Scroll down to **Incident reports** section, select the severity level of the alerts and reports as **Medium**. Ensure that **Send an alert to admins when a rule match occurs** toggle button as **On**. Then, click on **+Add or remove users**.

![](./media/ab1.png)

15. In **Add or Remove users** pane search bar, type +++**MOD**+++, then select **MOD Administrator**, and click on **Add** button. In the **Alerts** page, you will see the MOD Administrator user credentials is successfully added as shown in the below images.

![](./media/ab2.png)

![](./media/ab3.png)

![](./media/ab4.png)

16. Scroll down andd click on the **Save** button.

![](./media/image22.png)

17. Click on the **Next** button.

![](./media/image23.png)

18. In the **Policy mode** pane, select the radio button of **Turn the
    policy on immediately** and click on the **Next** button.

![](./media/image24.png)

19. On **Review and finish** pane, carefully review the DLP policy, then
    click on the **Submit** button.

![A screenshot of a computer Description automatically
generated](./media/image25.png)

20. The New policy will be created, click on the **Done** button.

![](./media/image26.png)

![](./media/image27.png)

21. Navigate and click on **Activity explorer**, then click on **Turn on
    auditing** button as shown in the below image.

![A screenshot of a computer Description automatically
generated](./media/image28.png)

### Task 3: Creating an alert in Microsoft Teams

1.  Click on the launcher beside **Microsoft Purview**, then
    navigate and click on **Teams** as shown in the below image.

> ![](./media/image29.png)

2.  In Microsoft Teams search bar, search and select the name of user -
    **Robert Frost**.

> ![](./media/image30.png)

3.  Test the DLP policy that you have created using the following
    **Credit Card Type** and **Credit Card Number**. Select the name of
    the Credit Card along with the number and send that information in
    team to Robert Frost.

    |**Credit Card Type** |**Credit Card Number** |
    |---|---|
    |+++American Express+++ |+++378282246310005+++ |
    |+++JCB+++ |+++3566002020360505+++ |
    |+++MasterCard+++ |+++5105105105105100+++ |
    |+++Visa+++ |+++4012888888881881+++ |


> ![](./media/image12a.png)
>
> ![](./media/image13a.png)
> 
> ![](./media/image14a.png)

4. Now, search and select a user named **Megan Bowen** and enter the above-mentioned information of credit cards, as shown in the below image.

  ![](./media/r10.png)

5.  Now, send the following information to both Robert Frost and Megan Bowen to trigger another type of alerts. You can
    also enter random information in this format:

    +++Katie Jordan+++

    +++Credit Card Account number: Visa 45562411537761660+++

    +++Debit Card Account number: MasterCard 5439683992731720+++

![](./media/image35.png)

6. Copy all the credit card information that you have sent in the Teams.

  ![](./media/r1.png)

7. Open a notepad and paste the credit card information in it as shown in the below image.

    ![](./media/r2.png)

8.  Save the notepad file on the desktop.

    ![](./media/r3.png)

9.  In the Microsoft Edge browser search bar, type +++one drive login+++ then click on **Sign in - Microsoft OneDrive**

    ![](./media/r4.png)

10. Login to OneDrive using your O365 admin credentials.

    ![](./media/r5.png)

    ![](./media/r6.png)

12.  Click on the **+** Symbol and then click on **Files upload**.

    ![](./media/r7.png)

    ![](./media/r8.png)

13. In OneDrive, click on the folder icon in the left-sided menu, you'll see that file containing sensitive information is successfully uploaded.
    ![](./media/r9.png)

    **Note**: Alert generation can take up to 30-60 minutes. 

12.  Go back to **Microsoft Purview** portal. In the **Data Loss Prevention** section, navigate and click on **Alerts**, you'll see the generated Alerts. Click on any alert to explore it further. .
    
    ![](./media/qur1.png)

    ![](./media/qurs2.png)
    
    **Note**: You’ll analyze the alerts generated through the Custom DLP policy using Microsoft Security Copilot in the upcoming task. As the SCU consume a lot       of credits; therefore, to prevent unnecessary credit loss, we’ve moved this task in the next lab.

## APPENDIX

1.  In case you did not see the alerts, then click on **Policies**,
    select **Custom Policy for Microsoft Security Copilot**, then
    click on the **Edit** icon as shown in the below image.

![A screenshot of a computer Description automatically
generated](./media/image36.png)

2.  Navigate to **Name \> Admin units \> Locations \> Advanced DLP
    rules**, click on the **Edit** icon.

![A screenshot of a computer Description automatically
generated](./media/image37.png)

3.  Scroll down **to User notifications** section and turned the toggle
    **On** if it is **Off**, then click on the **Save** button.

![A screenshot of a computer Description automatically
generated](./media/image38.png)

**Summary**

In this lab, you’ve set up a Microsoft Purview account, then you’ve
configured custom Data Loss Prevention (DLP) policies for Microsoft
Security Copilot, and created alerts in Microsoft Teams to test the
effectiveness of these policies. This hands-on exercise has equipped you
with valuable skills in data protection and compliance management within
Microsoft's ecosystem, enhancing your understanding of security measures
in cloud-based environments.
