## Lab 2: Connecting Microsoft Sentinel in Microsoft Defender Portal for Threat Hunting, Triage, Investigation, and Response

## Introduction

Microsoft Sentinel's Microsoft Defender XDR incident integration allows
you to stream all Microsoft Defender XDR incidents into Microsoft
Sentinel and keep them synchronized between both portals. Incidents from
Microsoft Defender XDR include all associated alerts, entities, and
relevant information, providing you with enough context to perform
triage and preliminary investigation in Microsoft Sentinel. Once in
Sentinel, incidents will remain bi-directionally synced with Microsoft
Defender XDR, allowing you to take advantage of the benefits of both
portals in your incident investigation using Microsoft Copilot for
Security.

## Objectives

- Creating a workspace and activating Microsoft Sentinel free trial.

- Connecting Microsoft Dender for Endpoint and Microsoft Defender XDR
  data connectors to Sentinel for enhancing security capabilities.

- Connecting Microsoft Sentinel and Microsoft Defender XDR to unify your
  security operation in a single portal.

**Task 1: Creating a workspace and activating Microsoft Sentinel free
trial**

1.  In the Azure portal search box, type **Microsoft Sentinel**, then
    navigate down to **Services** section and click on **Microsoft
    Sentinel** from the list.

> <img src="./media/image1.png" style="width:6.02917in;height:4.1875in"
> alt="A screenshot of a computer Description automatically generated" />

2.  In Microsoft Sentinel page, click on **+Create**.

> <img src="./media/image2.png"
> style="width:6.67477in;height:3.28695in" />

3.  In **Add Microsoft Sentinel to a workspace** page, click on **+**
    **Create a new workspace**.

> <img src="./media/image3.png" style="width:6.26806in;height:4.39931in"
> alt="A screenshot of a computer Description automatically generated" />

4.  In **Create Log Analytics workspace** page, enter the following
    details, then click on **Review and create** button.

| **Subscription** | Select the assigned **Azure Pass – Sponsorship**. |
|----|----|
| **Resource Group** | Select the resource group that you’ve created previously. |
| **Name** | Mylogworkspace+SUFFIX (here, we entered **Mylogworkspace5801**) |
| **Region** | East US |

> <img src="./media/image4.png" style="width:6.5in;height:5.29722in" />

5.  In **Create Log Analytics workspace** page, after Validation passed,
    click on the **Create** button.

<img src="./media/image5.png" style="width:6.5in;height:5.27361in"
alt="A screenshot of a computer Description automatically generated" />

6.  After few minutes, the workspace will be successfully created.

**Note**: In case, you did not see the workspace, then refresh the page.

<img src="./media/image6.png" style="width:6.26806in;height:4.39931in"
alt="A screenshot of a computer Description automatically generated" />

7.  Select the workspace, then click on the **Add** button.

<img src="./media/image7.png" style="width:6.26806in;height:3.87361in"
alt="A screenshot of a computer Description automatically generated" />

8.  On Microsoft Sentinel free trial activated dialog box, click on the
    **OK** button.

<img src="./media/image8.png"
style="width:6.26806in;height:3.70417in" />

<img src="./media/image9.png" style="width:6.00417in;height:3.67917in"
alt="A screenshot of a computer Description automatically generated" />

**Task 2: Connecting Microsoft Dender for Endpoint and Microsoft
Defender XDR data connectors to Sentinel for enhancing security
capabilities**

1.  Scroll down to **Content management** section and click on **Content
    hub**.

<img src="./media/image10.png" style="width:6.5in;height:3.79583in"
alt="A screenshot of a computer Description automatically generated" />

2.  In the **content hub** search bar, type **defender for endpoint**
    and press the enter button.

> <img src="./media/image11.png" style="width:6.26806in;height:3.96389in"
> alt="A screenshot of a computer Description automatically generated" />

3.  Scroll down and select **Microsoft Defender for Endpoint**, then
    select the **Install** button on the right-sided pane.

> <img src="./media/image12.png"
> style="width:6.26806in;height:4.06111in" />

4.  Click on **Manage** button.

> **Note**: In case, you did not see the Manage button, then select
> again **Microsoft Defender for Endpoint** as shown in the below image.
>
> <img src="./media/image13.png" style="width:6.26806in;height:3.92431in"
> alt="A screenshot of a computer Description automatically generated" />

5.  On **Microsoft Defender for Endpoint** page, navigate to **Content
    name** column, check the box beside **Microsoft Defender for
    Endpoint** as shown in the below image. Then, click on **Open
    connector** **page** button.

> <img src="./media/image14.png" style="width:6.26806in;height:3.76319in"
> alt="A screenshot of a computer Description automatically generated" />
>
> <img src="./media/image15.png" style="width:6.26806in;height:3.93125in"
> alt="A screenshot of a computer Description automatically generated" />

6.  Navigate to **Configuration** section and click on **Connect**
    button. You’ll received a notification – **Successfully connected
    Microsoft Defender for Endpoint alerts**.

> <img src="./media/image16.png" style="width:6.26806in;height:3.73403in"
> alt="A screenshot of a computer Description automatically generated" />
>
> <img src="./media/image17.png" style="width:6.26806in;height:3.89931in"
> alt="A screenshot of a computer Description automatically generated" />
>
> <img src="./media/image18.png" style="width:2.73473in;height:1.09222in"
> alt="A screenshot of a computer error Description automatically generated" />

7.  Click on **Microsoft Sentinel \| Content hub** link below the Azure
    search bar as shown in the below image. In the **Microsoft Sentinel
    \| Content hub** page search bar, type **Microsoft Defender XDR**
    and press the enter button. Scroll down and select **Microsoft
    Defender XDR**.

<img src="./media/image19.png" style="width:6.5in;height:4.12778in" />

8.  In **Microsoft Defender XDR** pane that appears on the right side,
    navigate and click on **Install** button.

<img src="./media/image20.png" style="width:6.5in;height:3.40347in" />

9.  Click on the **Manage** button.

> <img src="./media/image21.png" style="width:6.5in;height:3.49653in"
> alt="A screenshot of a computer Description automatically generated" />

10. In **Microsoft Defender XDR** page, navigate and select the check
    box of **Microsoft Defender XDR**, then click on **Open connector
    page** button.

> <img src="./media/image22.png" style="width:6.5in;height:3.33889in"
> alt="A screenshot of a computer Description automatically generated" />

11. Scroll down to **Configuration** section. Ensure to check the box of
    **Turn off all Microsoft incident creation rules for these
    products**, then click on the **Connect incidents & alerts** button.

> <img src="./media/image23.png" style="width:6.26806in;height:4.21458in"
> alt="A screenshot of a computer Description automatically generated" />
>
> <img src="./media/image24.png" style="width:6.26806in;height:3.63819in"
> alt="A screenshot of a computer Description automatically generated" />

12. Select all the Microsoft Defender XDR products except

- Microsoft Defender for Cloud Apps (0/1 connected)​

- Microsoft Defender for Identity (0/3 connected)​

Click on **Apply** **changes** button.

> <img src="./media/image25.png" style="width:6.26806in;height:3.83819in"
> alt="A screenshot of a computer Description automatically generated" />
>
> <img src="./media/image26.png" style="width:6.26806in;height:3.98958in"
> alt="A screenshot of a computer Description automatically generated" />
>
> <img src="./media/image27.png" style="width:6.26806in;height:3.81944in"
> alt="A screenshot of a computer Description automatically generated" />
>
> <img src="./media/image28.png" style="width:6.26806in;height:3.53264in"
> alt="A screenshot of a computer Description automatically generated" />

13. Scroll up to **Configuration** section, if Microsoft Defender XDR is
    successfully connected, then you’ll see the **Disconnect** button as
    shown in the below image. In case, if you see **Connect Incidents &
    alerts** on the button, then click on it.

> <img src="./media/image29.png"
> style="width:6.26806in;height:4.36458in" />

14. Go back to **Microsoft Defender** portal and **Sign out** from it.

<img src="./media/image30.png" style="width:6.5in;height:3.19306in"
alt="A screenshot of a computer Description automatically generated" />

**Task 3: Connecting Microsoft Sentinel and Microsoft Defender XDR**

1.  Open a new address bar and enter the following link to open the
    Microsoft Defender Portal: **<https://security.microsoft.com>**

2.  Select your O365 tenant ID.

<img src="./media/image31.png" style="width:6.5in;height:4.3375in" />

3.  Enter the password.

<img src="./media/image32.png"
style="width:6.16148in;height:5.0359in" />

4.  In **Stay signed in?** window, click on the **Yes** button.

<img src="./media/image33.png"
style="width:4.6357in;height:4.61068in" />

5.  In **Get your SIEM and XDR in one place** dialog box, click on
    **Connect a workspace** button.

<img src="./media/image34.png" style="width:6.5in;height:3.28611in" />

6.  Select MylogworkspaceXXXX workspace and click on the **Next**
    button.

<img src="./media/image35.png" style="width:6.5in;height:3.42083in" />

7.  In the **Review changes** page, click on the **Connect** button.

<img src="./media/image36.png" style="width:6.5in;height:3.47222in"
alt="A screenshot of a computer Description automatically generated" />

8.  Wait for few minutes for the workspace to be successfully connected
    to Microsoft 365 Defender. After workspace successfully connected,
    click on the **Close** button.

<img src="./media/image37.png" style="width:6.5in;height:4.10069in" />

## Summary 

In this lab, you've gained valuable hands-on experience in setting up
and configuring Microsoft Sentinel, a powerful security information and
event management (SIEM) system. By following the detailed instructions,
you successfully created a workspace and activated the Microsoft
Sentinel free trial, ensuring a solid foundation for security monitoring
and incident response. Additionally, you learned to connect crucial data
connectors, such as Microsoft Defender for Endpoint and Microsoft
Defender XDR, enabling seamless integration of security solutions within
the Sentinel environment. Furthermore, you mastered the process of
connecting Microsoft Sentinel and Microsoft Defender XDR, consolidating
security monitoring efforts and enhancing overall defense strategies.
Your proficiency in these tasks equips you with essential skills for
effectively managing and securing your organization's digital assets.
