## **Lab 5 - Activating Security for Copilot using Azure subscription and analyzing the alerts generated in Microsoft Purview**

**Introduction**

Security Copilot is a generative AI security product that empowers
security and IT professionals respond to cyber threats, process signals,
and assess risk exposure at the speed and scale of AI. In this lab,
you’ll be activating Security for Copilot utilizing Azure subscription
and analyzing the alerts generated in Microsoft Purview.

**Objectives**

- To set up Microsoft Security Copilot capacity in Azure portal.

- To change the SCU units.

- To analyze the Custom DLP Policy Alert using Microsoft Copilot for
  Security

**Task 1: Setting up Microsoft Security Copilot capacity in Azure portal**

1. In the Microsoft Azure portal search bar, type +++**Microsoft Security Copilot compute capacities**+++ and then click on it.

![](./media/m1.png)

2. In **Microsoft Security Copilot compute capacity** window, click
on **+ Create.**

![A screenshot of a computer Description automatically
generated](./media/image2.png)

3. In **Set up your Copilot capacity** page, in the **Resource group**
field, click on the dropdown and select **MCS-RG**. Then, in the
Capacity name field, enter the capacity name (here, we entered
**SCU5801**). In the Prompt evaluation location field, click on the
dropdown and select **United States (US)**.

![A screenshot of a computer Description automatically
generated](./media/image3.png)

4. In the **Security compute units per hour** field, click on the
dropdown and select 1. Select the checkbox of acknowledgement and click
on **Review + create** button.

![A screenshot of a computer Description automatically
generated](./media/image4.png)

5. Click on the **Create** button.

![A screenshot of a computer Description automat cally
generated](./media/image5.png)

6. Click on **View resource** button.

![A screenshot of a computer Description automatically
generated](./media/image6.png)

7. Again, in the Azure portal search bar, type +++**Microsoft Security Copilot compute capacities**+++, navigate and click on it.

![](./media/m1.png)

8. Click on the security capacity unit that you’ve deployed (here, **SCU5801**).

![A screenshot of a computer Description automatically
generated](./media/image8.png)

9. In the **SCU5801** Microsoft Security Copilot compute capacity
page, navigate and click on **Access control (IAM)**.

![A screenshot of a computer Description automatically
generated](./media/image9.png)

10. Click on **+Add**. Then, navigate and click on **Add role
assignment**.

![](./media/image10.png)

![A screenshot of a computer Description automatically
generated](./media/image11.png)

12. Click on **Privileged administrator roles** tab, navigate and click
on **Owner** role, then click on the **Next** button as shown in the
below image.

![A screenshot of a computer Description automatically
generated](./media/image12.png)

13. Click on **+Select members**.

![A screenshot of a computer Description automatically
generated](./media/image13.png)

14. In the **Select members** pane that appear on the right side,
navigate to **Select** field and enter your O365 tenant ID, then select
it as shown in the below images.

![A screenshot of a computer screen Description automatically
generated](./media/image14.png)

![A screenshot of a computer Description automatically
generated](./media/image15.png)

15. Click on the **Next** button.

![A screenshot of a computer Description automatically
generated](./media/image16.png)

16. In the **Conditions** tab, select the **Allow user to assign all
roles (highly privileged)** radio button and then click on the **Next**
button.

![A screenshot of a computer screen Description automatically
generated](./media/image17.png)

17. Click on **Review + assign** button.

![A screenshot of a computer Description automatically
generated](./media/image18.png)

18. Click on **Overview**.

![A screenshot of a computer Description automatically
generated](./media/image19.png)

19. Scroll down and click on **Go to portal and complete setup link**
as shown in the below image.

![A screenshot of a computer Description automatically
generated](./media/image20.png)

21. Click on **Get started** button.

![A screenshot of a computer Description automatically
generated](./media/c1.png)

![A screenshot of a computer Description automatically
generated](./media/c2.png)

22. In **Select the capacity you’d like to use** page, click on the
dropdown and select the SCU capacity that you’ve created (here, we
selected **SCU5801**), then click on the **Continue** button.

![](./media/c3.png)

23. In **Your Customer Data will be stored in United States** page,
click on the **Continue** button.

![](./media/c4.png)

24. In **Help improve Copilot** page, click on the Continue button.

![A screenshot of a computer Description automatically
generated](./media/c6.png)

25. On **Copilot's access and storage of Microsoft 365 service data** page, click on the **Continue** button.

![A screenshot of a computer Description automatically
generated](./media/ca12.png)

25. On **Logging audit data in Microsoft Purview** page, click on **Continue** button.

![A screenshot of a computer Description automatically
generated](./media/c8.png)

26. On the next page, click on **Continue** button.

![A screenshot of a computer Description automatically
generated](./media/cop1.png)

![A screenshot of a computer Description automatically
generated](./media/cop2.png)

27. In **You’re all set** page, click on the **Finish** button.

![](./media/c10.png)

![](./media/c11.png)

28. Microsoft Security Copilot is successfully activated.

![](./media/c12.png)

**Task 2: Changing SCU units**

While using the prompt in Microsoft Security Copilot, you will
encounter a message stating that your SCU units have been consumed and
you need to increase the SCU units. In this task, you will learn how to
increase the SCU units in Microsoft Security Copilot Standalone.

1.  In Microsoft Security Copilot window, click on the three
    horizontal ellipsis and click on **Owner settings**.

![A screenshot of a computer Description automatically
generated](./media/c13.png)

2.  Navigate to **Security compute units** and click on the **Change**
    button.

![A screenshot of a computer Description automatically
generated](./media/c14.png)

3.  Select **9** Security compute units and click on the **Apply**
    button.

![](./media/image32.png)

4.  On **9 capacity units are now available to use** dialog box, click
    on the **Done** button.
 ![A screenshot of a computer Description automatically
 generated](./media/image33.png)

5. Click on **Microsoft Security Copilot** at the top bar of the window as shown in the below image.

 ![A screenshot of a computer Description automatically
 generated](./media/c15.png)

**Task 3: Analyzing the Custom DLP Policy Alert using Microsoft Security Copilot**

1. In Microsoft Security Copilot Standalone, navigate and click on **Source** icon beside the prompt bar as shown in the below image.

 ![](./media/c16.png)

2.  Click on **Show 9 more**, then navigate to **Microsoft Purview** and
    ensure that the toggle is turned on as shown in the below images.

 ![](./media/c17.png)

 ![](./media/c18.png)

3.  Go back to Microsoft Purview. In the **Data Loss Prevention**
    section, navigate and click on **Alerts**, you’ll see the Alerts
    stating – **DLP policy match for Teams conversation** along with the
    **Severity** and **Status** of the alerts.

 ![](./media/image38.png)

4.  In the **Alert: DLP policy match for Teams conversation** pane, scroll down and click on the **Summarize** button and select **Summarize alert** as shown in the below images.

 ![](./media/tw32.png)

 ![](./media/tw31.png)

5. Carefully review the **Alert summary**.

 ![](./media/tw2.png)

6. Go back to Microsoft Security Copilot Standalone mode and enter the following prompt:

    +++**Show me the most recent DLP alerts**+++

 ![](./media/purview1.png)

7.  The most recent Microsoft Purview DLP alerts will be displayed along with
    **Alert ID** and **Severity**, carefully review them.

![](./media/purview2.png)

![](./media/purview3.png)

**Summary**

In this lab, you’ve configured Microsoft Security Copilot capacity
in Azure portal and learned how to increase the SCU units. Then, you’ve
analyzed the Custom DLP Policy Alert using Microsoft Copilot for
Security.
