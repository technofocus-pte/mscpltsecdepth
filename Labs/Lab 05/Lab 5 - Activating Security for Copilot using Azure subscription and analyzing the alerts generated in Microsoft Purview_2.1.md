**Lab 5 - Activating Security for Copilot using Azure subscription and
analyzing the alerts generated in Microsoft Purview**

**Introduction**

Copilot for Security is a generative AI security product that empowers
security and IT professionals respond to cyber threats, process signals,
and assess risk exposure at the speed and scale of AI. In this lab,
you’ll be activating Security for Copilot utilizing Azure subscription
and analyzing the alerts generated in Microsoft Purview.

**Objectives**

- To set up Microsoft Copilot for Security capacity in Azure portal.

- To change the SCU units.

- To analyze the Custom DLP Policy Alert using Microsoft Copilot for
  Security

**Task 1: Setting up Microsoft Copilot for Security capacity in Azure
portal**

1\. In the Microsoft Azure portal search bar, type **Microsoft Copilot
for Security compute capacity** and then click on it.

<img src="./media/image1.png" style="width:6.5in;height:3.73264in" />

2\. In **Microsoft Copilot for Security compute capacity** window, click
on **+ Create.**

<img src="./media/image2.png" style="width:6.5in;height:4.94097in"
alt="A screenshot of a computer Description automatically generated" />

3\. In **Set up your Copilot capacity** page, in the **Resource group**
field, click on the dropdown and select **MCS-RG**. Then, in the
Capacity name field, enter the capacity name (here, we entered
**SCU5801**). In the Prompt evaluation location field, click on the
dropdown and select **United States (US)**.

<img src="./media/image3.png" style="width:6.5in;height:4.49514in"
alt="A screenshot of a computer Description automatically generated" />

4\. In the **Security compute units per hour** field, click on the
dropdown and select 1. Select the checkbox of acknowledgement and click
on **Review + create** button.

<img src="./media/image4.png" style="width:6.5in;height:5.77986in"
alt="A screenshot of a computer Description automatically generated" />

5\. Click on the **Create** button.

<img src="./media/image5.png" style="width:6.5in;height:5.92083in"
alt="A screenshot of a computer Description automatically generated" />

6\. Click on **View resource** button.

<img src="./media/image6.png" style="width:6.5in;height:5.18403in"
alt="A screenshot of a computer Description automatically generated" />

7\. Again, in the Azure portal search bar, type **Microsoft Copilot for
Security compute capacities**, navigate and click on it.

<img src="./media/image7.png" style="width:6.5in;height:4.57361in" />

8\. Click on the security capacity unit that you’ve deployed (here,
**SCU5801**).

<img src="./media/image8.png" style="width:6.5in;height:3.34514in"
alt="A screenshot of a computer Description automatically generated" />

9\. In the **SCU5801** Microsoft Copilot for Security compute capacity
page, navigate and click on **Access control (IAM)**.

<img src="./media/image9.png" style="width:6.5in;height:4.5125in"
alt="A screenshot of a computer Description automatically generated" />

10\. Click on **+Add**. Then, navigate and click on **Add role
assignment**.

<img src="./media/image10.png" style="width:6.5in;height:3.69514in" />

<img src="./media/image11.png" style="width:6.5in;height:3.70625in"
alt="A screenshot of a computer Description automatically generated" />

12\. Click on **Privileged administrator roles** tab, navigate and click
on **Owner** role, then click on the **Next** button as shown in the
below image.

<img src="./media/image12.png" style="width:6.5in;height:5.66597in"
alt="A screenshot of a computer Description automatically generated" />

13\. Click on **+Select members**.

<img src="./media/image13.png" style="width:6.5in;height:5.87222in"
alt="A screenshot of a computer Description automatically generated" />

14\. In the **Select members** pane that appear on the right side,
navigate to **Select** field and enter your O365 tenant ID, then select
it as shown in the below images.

<img src="./media/image14.png" style="width:6.5in;height:4.06597in"
alt="A screenshot of a computer screen Description automatically generated" />

<img src="./media/image15.png" style="width:6.5in;height:4.12361in"
alt="A screenshot of a computer Description automatically generated" />

15\. Click on the **Next** button.

<img src="./media/image16.png" style="width:6.5in;height:5.87639in"
alt="A screenshot of a computer Description automatically generated" />

16\. In the **Conditions** tab, select the **Allow user to assign all
roles (highly privileged)** radio button and then click on the **Next**
button.

<img src="./media/image17.png" style="width:6.5in;height:4.15069in"
alt="A screenshot of a computer screen Description automatically generated" />

17\. Click on **Review + assign** button.

<img src="./media/image18.png" style="width:6.5in;height:5.28125in"
alt="A screenshot of a computer Description automatically generated" />

18\. Click on **Overview**.

<img src="./media/image19.png" style="width:6.5in;height:5.55833in"
alt="A screenshot of a computer Description automatically generated" />

19\. Scroll down and click on **Go to portal and complete setup link**
as shown in the below image.

<img src="./media/image20.png" style="width:6.5in;height:3.79722in"
alt="A screenshot of a computer Description automatically generated" />

20\. You’ll be directed **to Microsoft Copilot for Security** page. If
you see a dialog box – **Are you familiar with cookies?**, then click on
the **Accept** button.

<img src="./media/image21.png" style="width:6.5in;height:4.15903in" />

21\. Click on **Get started** button.

<img src="./media/image22.png" style="width:6.5in;height:4.19097in"
alt="A screenshot of a computer Description automatically generated" />

<img src="./media/image23.png" style="width:6.5in;height:4.05903in"
alt="A screenshot of a computer Description automatically generated" />

22\. In **Select the capacity you’d like to use** page, click on the
dropdown and select the SCU capacity that you’ve created (here, we
selected **SCU5801**), then click on the **Continue** button.

<img src="./media/image24.png" style="width:6.5in;height:4.09306in" />

23\. In **Your Customer Data will be stored in United States** page,
click on the **Continue** button.

<img src="./media/image25.png" style="width:6.5in;height:4.17639in" />

24\. In **Help improve Copilot** page, click on the Continue button.

<img src="./media/image26.png" style="width:6.5in;height:4.12917in"
alt="A screenshot of a computer Description automatically generated" />

25\. Click on **Continue** button.

<img src="./media/image27.png" style="width:6.5in;height:4.09236in"
alt="A screenshot of a computer Description automatically generated" />

26\. In **You’re all set** page, click on the **Finish** button.

<img src="./media/image28.png" style="width:6.5in;height:4.06389in" />

27\. Microsoft Copilot for Security is successfully activated.

<img src="./media/image29.png" style="width:6.5in;height:5.05069in" />

**Task 2: Changing SCU units**

While using the prompt in Microsoft Copilot for Security, you will
encounter a message stating that your SCU units have been consumed and
you need to increase the SCU units. In this task, you will learn how to
increase the SCU units in Microsoft Copilot for Security Standalone.

1.  In Microsoft Copilot for Security window, click on the three
    horizontal ellipsis and click on **Owner settings**.

<img src="./media/image30.png" style="width:6.5in;height:4.15694in"
alt="A screenshot of a computer Description automatically generated" />

2.  Navigate to **Security compute units** and click on the **Change**
    button.

<img src="./media/image31.png" style="width:6.5in;height:4.15694in"
alt="A screenshot of a computer Description automatically generated" />

3.  Select **9** Security compute units and click on the **Apply**
    button.

<img src="./media/image32.png"
style="width:6.26806in;height:3.57431in" />

4.  On **9 capacity units are now available to use** dialog box, click
    on the **Done** button.

> <img src="./media/image33.png" style="width:6.18649in;height:2.19279in"
> alt="A screenshot of a computer Description automatically generated" />
>
> 5\. Click on **Microsoft Copilot for Security** at the top bar of the
> window as shown in the below image.
>
> <img src="./media/image34.png" style="width:6.26806in;height:4.50625in"
> alt="A screenshot of a computer Description automatically generated" />
>
> **Task 3: Analyzing the Custom DLP Policy Alert using Microsoft
> Copilot for Security**

1.  In Microsoft Copilot for Security Standalone, navigate and click on
    **Source** icon beside the prompt bar as shown in the below image.

> <img src="./media/image35.png"
> style="width:6.26806in;height:4.18681in" />

2.  Click on **Show 9 more**, then navigate to **Microsoft Purview** and
    ensure that the toggle is turned on as shown in the below images.

> <img src="./media/image36.png"
> style="width:6.26806in;height:3.76736in" />
>
> <img src="./media/image37.png"
> style="width:6.26806in;height:3.75417in" />

3.  Go back to Microsoft Purview. In the **Data Loss Prevention**
    section, navigate and click on **Alerts**, you’ll see the Alerts
    stating – **DLP policy match for Teams conversation** along with the
    **Severity** and **Status** of the alerts.

> <img src="./media/image38.png" style="width:6.5in;height:4.1625in" />

4.  In the **Alert: DLP policy match for Teams conversation** pane,
    click on **Summarize with Copilot** button as shown in the below
    image.

- <img src="./media/image39.png" style="width:6.26806in;height:3.68472in"
  alt="A screenshot of a computer Description automatically generated" />

5.  Carefully review the **Alert summary**.

> <img src="./media/image40.png" style="width:6.5in;height:3.64792in" />

6.  Go back to Microsoft Copilot for Security Standalone mode and enter
    the following prompt:

+++**Which Purview Data Loss Prevention alerts should I prioritize
today?**+++

> <img src="./media/image41.png" style="width:6.5in;height:4.15694in" />

7.  The top 10 Microsoft Purview DLP alerts will be displayed along with
    **Alert ID** and **Severity**, carefully review them.

> <img src="./media/image42.png" style="width:6.5in;height:4.15694in" />

**Summary**

In this lab, you’ve configured Microsoft Copilot for Security capacity
in Azure portal and learned how to increase the SCU units. Then, you’ve
analyzed the Custom DLP Policy Alert using Microsoft Copilot for
Security.
