**Lab 5 - Activating Security for Copilot using Azure subscription and
analyzing the alerts generated in Microsoft Purview**

**Introduction**

Copilot for Security is a generative AI security product that empowers
security and IT professionals respond to cyber threats, process signals,
and assess risk exposure at the speed and scale of AI. In this lab,
you'll be activating Security for Copilot utilizing Azure subscription
and analyzing the alerts generated in Microsoft Purview.

**Objectives**

-   To set up Microsoft Copilot for Security capacity in Azure portal.

-   To change the SCU units.

-   To analyze the Custom DLP Policy Alert using Microsoft Copilot for
    Security

**Task 1: Setting up Microsoft Copilot for Security capacity in Azure
portal**

1\. In the Microsoft Azure portal search bar, type **Microsoft Copilot
for Security compute capacity** and then click on it.

![](./media/image1.png){width="6.5in" height="3.732638888888889in"}

2\. In **Microsoft Copilot for Security compute capacity** window, click
on **+ Create.**

![A screenshot of a computer Description automatically
generated](./media/image2.png){width="6.5in"
height="4.940972222222222in"}

3\. In **Set up your Copilot capacity** page, in the **Resource group**
field, click on the dropdown and select **MCS-RG**. Then, in the
Capacity name field, enter the capacity name (here, we entered
**SCU5801**). In the Prompt evaluation location field, click on the
dropdown and select **United States (US)**.

![A screenshot of a computer Description automatically
generated](./media/image3.png){width="6.5in"
height="4.495138888888889in"}

4\. In the **Security compute units per hour** field, click on the
dropdown and select 1. Select the checkbox of acknowledgement and click
on **Review + create** button.

![A screenshot of a computer Description automatically
generated](./media/image4.png){width="6.5in"
height="5.779861111111111in"}

5\. Click on the **Create** button.

![A screenshot of a computer Description automatically
generated](./media/image5.png){width="6.5in"
height="5.920833333333333in"}

6\. Click on **View resource** button.

![A screenshot of a computer Description automatically
generated](./media/image6.png){width="6.5in"
height="5.184027777777778in"}

7\. Again, in the Azure portal search bar, type **Microsoft Copilot for
Security compute capacities**, navigate and click on it.

![](./media/image7.png){width="6.5in" height="4.573611111111111in"}

8\. Click on the security capacity unit that you've deployed (here,
**SCU5801**).

![A screenshot of a computer Description automatically
generated](./media/image8.png){width="6.5in"
height="3.345138888888889in"}

9\. In the **SCU5801** Microsoft Copilot for Security compute capacity
page, navigate and click on **Access control (IAM)**.

![A screenshot of a computer Description automatically
generated](./media/image9.png){width="6.5in" height="4.5125in"}

10\. Click on **+Add**. Then, navigate and click on **Add role
assignment**.

![](./media/image10.png){width="6.5in" height="3.6951388888888888in"}

![A screenshot of a computer Description automatically
generated](./media/image11.png){width="6.5in" height="3.70625in"}

12\. Click on **Privileged administrator roles** tab, navigate and click
on **Owner** role, then click on the **Next** button as shown in the
below image.

![A screenshot of a computer Description automatically
generated](./media/image12.png){width="6.5in"
height="5.665972222222222in"}

13\. Click on **+Select members**.

![A screenshot of a computer Description automatically
generated](./media/image13.png){width="6.5in"
height="5.872222222222222in"}

14\. In the **Select members** pane that appear on the right side,
navigate to **Select** field and enter your O365 tenant ID, then select
it as shown in the below images.

![A screenshot of a computer screen Description automatically
generated](./media/image14.png){width="6.5in"
height="4.065972222222222in"}

![A screenshot of a computer Description automatically
generated](./media/image15.png){width="6.5in"
height="4.123611111111111in"}

15\. Click on the **Next** button.

![A screenshot of a computer Description automatically
generated](./media/image16.png){width="6.5in"
height="5.876388888888889in"}

16\. In the **Conditions** tab, select the **Allow user to assign all
roles (highly privileged)** radio button and then click on the **Next**
button.

![A screenshot of a computer screen Description automatically
generated](./media/image17.png){width="6.5in"
height="4.1506944444444445in"}

17\. Click on **Review + assign** button.

![A screenshot of a computer Description automatically
generated](./media/image18.png){width="6.5in" height="5.28125in"}

18\. Click on **Overview**.

![A screenshot of a computer Description automatically
generated](./media/image19.png){width="6.5in"
height="5.558333333333334in"}

19\. Scroll down and click on **Go to portal and complete setup link**
as shown in the below image.

![A screenshot of a computer Description automatically
generated](./media/image20.png){width="6.5in"
height="3.797222222222222in"}

20\. You'll be directed **to Microsoft Copilot for Security** page. If
you see a dialog box -- **Are you familiar with cookies?**, then click
on the **Accept** button.

![](./media/image21.png){width="6.5in" height="4.159027777777778in"}

21\. Click on **Get started** button.

![A screenshot of a computer Description automatically
generated](./media/image22.png){width="6.5in"
height="4.190972222222222in"}

![A screenshot of a computer Description automatically
generated](./media/image23.png){width="6.5in"
height="4.059027777777778in"}

22\. In **Select the capacity you'd like to use** page, click on the
dropdown and select the SCU capacity that you've created (here, we
selected **SCU5801**), then click on the **Continue** button.

![](./media/image24.png){width="6.5in" height="4.093055555555556in"}

23\. In **Your Customer Data will be stored in United States** page,
click on the **Continue** button.

![](./media/image25.png){width="6.5in" height="4.176388888888889in"}

24\. In **Help improve Copilot** page, click on the Continue button.

![A screenshot of a computer Description automatically
generated](./media/image26.png){width="6.5in"
height="4.129166666666666in"}

25\. Click on **Continue** button.

![A screenshot of a computer Description automatically
generated](./media/image27.png){width="6.5in"
height="4.092361111111111in"}

26\. In **You're all set** page, click on the **Finish** button.

![](./media/image28.png){width="6.5in" height="4.063888888888889in"}

27\. Microsoft Copilot for Security is successfully activated.

![](./media/image29.png){width="6.5in" height="5.050694444444445in"}

**Task 2: Changing SCU units**

While using the prompt in Microsoft Copilot for Security, you will
encounter a message stating that your SCU units have been consumed and
you need to increase the SCU units. In this task, you will learn how to
increase the SCU units in Microsoft Copilot for Security Standalone.

1.  In Microsoft Copilot for Security window, click on the three
    horizontal ellipsis and click on **Owner settings**.

![A screenshot of a computer Description automatically
generated](./media/image30.png){width="6.5in"
height="4.156944444444444in"}

2.  Navigate to **Security compute units** and click on the **Change**
    button.

![A screenshot of a computer Description automatically
generated](./media/image31.png){width="6.5in"
height="4.156944444444444in"}

3.  Select **9** Security compute units and click on the **Apply**
    button.

![](./media/image32.png){width="6.268055555555556in"
height="3.5743055555555556in"}

4.  On **9 capacity units are now available to use** dialog box, click
    on the **Done** button.

> ![A screenshot of a computer Description automatically
> generated](./media/image33.png){width="6.186488407699038in"
> height="2.192785433070866in"}
>
> 5\. Click on **Microsoft Copilot for Security** at the top bar of the
> window as shown in the below image.
>
> ![A screenshot of a computer Description automatically
> generated](./media/image34.png){width="6.268055555555556in"
> height="4.50625in"}
>
> **Task 3: Analyzing the Custom DLP Policy Alert using Microsoft
> Copilot for Security**

1.  In Microsoft Copilot for Security Standalone, navigate and click on
    **Source** icon beside the prompt bar as shown in the below image.

> ![](./media/image35.png){width="6.268055555555556in"
> height="4.186805555555556in"}

2.  Click on **Show 9 more**, then navigate to **Microsoft Purview** and
    ensure that the toggle is turned on as shown in the below images.

> ![](./media/image36.png){width="6.268055555555556in"
> height="3.767361111111111in"}
>
> ![](./media/image37.png){width="6.268055555555556in"
> height="3.754166666666667in"}

3.  Go back to Microsoft Purview. In the **Data Loss Prevention**
    section, navigate and click on **Alerts**, you'll see the Alerts
    stating -- **DLP policy match for Teams conversation** along with
    the **Severity** and **Status** of the alerts.

> ![](./media/image38.png){width="6.5in" height="4.1625in"}

4.  In the **Alert: DLP policy match for Teams conversation** pane,
    click on **Summarize with Copilot** button as shown in the below
    image.

-   ![A screenshot of a computer Description automatically
    generated](./media/image39.png){width="6.268055555555556in"
    height="3.6847222222222222in"}

5.  Carefully review the **Alert summary**.

> ![](./media/image40.png){width="6.5in" height="3.6479166666666667in"}

6.  Go back to Microsoft Copilot for Security Standalone mode and enter
    the following prompt:

+++**Which Purview Data Loss Prevention alerts should I prioritize
today?**+++

> ![](./media/image41.png){width="6.5in" height="4.156944444444444in"}

7.  The top 10 Microsoft Purview DLP alerts will be displayed along with
    **Alert ID** and **Severity**, carefully review them.

> ![](./media/image42.png){width="6.5in" height="4.156944444444444in"}

**Summary**

In this lab, you've configured Microsoft Copilot for Security capacity
in Azure portal and learned how to increase the SCU units. Then, you've
analyzed the Custom DLP Policy Alert using Microsoft Copilot for
Security.
