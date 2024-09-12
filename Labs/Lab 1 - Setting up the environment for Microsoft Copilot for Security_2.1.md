## **Lab 1 - Setting up the environment for Microsoft Copilot for Security**

**Introduction**

The Microsoft Defender portal combines protection, detection,
investigation, and response to threats across your entire organization
and all its components, in a central place. The Defender portal
emphasizes quick access to information, simpler layouts, and bringing
related information together for easier use. It includes:

-   **Microsoft Defender for Office 365** helps organizations secure
    their enterprise with a set of prevention, detection, investigation
    and hunting features to protect email, and Office 365 resources.

-   **Microsoft Defender for Endpoint** delivers preventative
    protection, post-breach detection, automated investigation, and
    response for devices in your organization.

-   **Microsoft Defender for Identity** is a cloud-based security
    solution that uses your on-premises Active Directory signals to
    identify, detect, and investigate advanced threats, compromised
    identities, and malicious insider actions directed at your
    organization.

-   **Microsoft Defender for Cloud Apps** is a comprehensive cross-SaaS
    and PaaS solution bringing deep visibility, strong data controls,
    and enhanced threat protection to your cloud apps.

-   **Microsoft Sentinel** is a cloud-native security information and
    event management (SIEM) solution that provides proactive threat
    detection, investigation, and response.

In this lab, you'll be configuring the environment that includes
creation of Windows server virtual machine and Windows 11 Pro virtual
machines and onboarding them to Microsoft Defender for Endpoints for
security monitoring. In addition, you'll be creating a new user account
with Office 365 license and installing the Microsoft 365 apps Windows 11
Pro virtual machines.

**Objectives**

-   To assign the Owner role to the Azure subscription.

-   To create a Windows Server virtual machine (**testserver1**) and
    onboard it to Microsoft Defender for Endpoints for security
    monitoring.

-   To create a Windows 11 Pro virtual machine (**testVM1**) and onboard
    it to Microsoft Defender for Endpoints for security monitoring.

-   To create another Windows 11 Pro virtual machine (**testVM2**) and
    onboard it to Microsoft Defender for Endpoints for security
    monitoring.

-   To create a new user account (**Robert Frost**) with Microsoft 365
    E5 and Microsoft teams enterprise licenses for testing purposes.

-   To prepare the testvm1 virtual machine for upcoming tasks, including
    installing Microsoft 365 apps.

## **Task 0: Sync Host environment time**

1.  Login to the Lab Virtual Machine using the credentials provided on
    the Home tab of the Lab interface.

2.  In your VM, navigate and click in the **Search bar**, type
    **Settings** and then click on **Settings** under **Best match**.
    ![](./media/image1.png){width="6.17686789151356in"
    height="5.308339895013123in"}

<!-- -->

2.  On Settings window, navigate and click on **Time & language**.

![](./media/image2.png){width="6.5in" height="5.722222222222222in"}

3.  On **Time & language** page, navigate and click on **Date & time**.

![](./media/image3.png){width="6.5in" height="5.276388888888889in"}

4.  Scroll down and navigate to **Additional settings** section, then
    click on **Syn now** button.

![](./media/image4.png){width="6.5in" height="5.048611111111111in"}

5.  Close the **Settings** window.

![](./media/image5.png){width="6.5in" height="5.122222222222222in"}

## **Task 1: Redeem Azure pass**

1.  In your lab VM, open Microsoft Edge and
    enter [**http://www.microsoftazurepass.com**](urn:gd:lg:a:send-vm-keys)

> ![](./media/image6.png){width="6.5in" height="3.8618055555555557in"}

2.  On **Ready to get started?** page, click on the **Start** button.

![Graphical user interface, website Description automatically
generated](./media/image7.jpeg){width="5.3446434820647415in"
height="4.566929133858268in"}

**Note**: Do not use your Company/Work Account to login to redeem the
Azure Pass, another Azure Pass will not be issued.

4.  In the **Sign in** window, enter the **Office 365 Tenant ID** -
    <admin@WWLxxxx.onmicrosoft.com> and click on the **Next** button.

![](./media/image8.png){width="4.106944444444444in"
height="3.2263888888888888in"}

5.  Enter Office **365 Tenant Password** and click on the **Sign in**
    button.

![](./media/image9.png){width="4.020698818897638in"
height="3.834733158355206in"}

6.  On **Stayed signed in?** dialog box, click on **Yes** button.

![A screenshot of a computer Description automatically
generated](./media/image10.png){width="3.9475634295713036in"
height="3.9203849518810148in"}

7.  On **The following Microsoft Account will be used for Azure pass**
    page, click on **Confirm Microsoft Account** button.

> ![](./media/image11.png){width="5.15239501312336in"
> height="3.2841010498687666in"}

8.  Enter the Promocode provided in the lab environment in the **Enter
    Promo code** field, then enter the characters under the **Enter the
    characters you see** field and click on the **Submit** button.

![](./media/image12.png){width="5.034284776902887in"
height="3.4008650481189853in"}

9.  **We are processing your request** page will appear, it may take few
    seconds to process the redemption.

![Screenshot](./media/image13.png){width="5.094488188976378in"
height="1.5150896762904638in"}

10. Enter correct details in **Your Profile** page, tick all the check
    boxes, and then click on **Sign up** button.

> ![A screenshot of a computer Description automatically
> generated](./media/image14.png){width="3.5570647419072614in"
> height="4.09115813648294in"}
>
> ![](./media/image15.png){width="3.494351487314086in"
> height="3.6618886701662294in"}![A screenshot of a computer Description
> automatically
> generated](./media/image16.png){width="3.4659503499562554in"
> height="5.454545056867891in"}

10. On **Protect your account** dialog box, click on the **Next**
    button.

![A screenshot of a computer error Description automatically
generated](./media/image17.png){width="3.7507884951881016in"
height="4.222200349956255in"}

11. Then, on **More information required** dialog box, click on
    the **Next** button.

> ![A screenshot of a computer Description automatically
> generated](./media/image18.png){width="3.4877438757655295in"
> height="3.6430194663167104in"}

12. If prompted, then enter the password and click on the **Sign in**
    button.

![A screen shot of a login page Description automatically
generated](./media/image19.png){width="3.3590726159230098in"
height="3.347782152230971in"}

11. In your mobile, install the **Microsoft Authenticator App**. Then,
    go back to Microsoft Azure port. In the Azure portal, **Microsoft
    Authenticator -** **Start by getting the app** window, navigate and
    click on the **Next** button.

![](./media/image20.png){width="6.5in" height="3.452777777777778in"}

12. In **Microsoft Authenticator --** **Set up your account** window,
    click on the **Next** button.

![A screenshot of a computer Description automatically
generated](./media/image21.png){width="6.5in"
height="3.5597222222222222in"}

13. **Scan the QR code** using the **Authenticator app** installed in
    your mobile phone and click on the **Next** button.

![A screenshot of a computer Description automatically
generated](./media/image22.png){width="6.5in" height="4.29375in"}

14. Enter the number in your mobile authenticator app and select
    **Yes**. In **testvm1**, click on the **Next** button.

![A screenshot of a computer error Description automatically
generated](./media/image23.png){width="6.5in"
height="3.910416666666667in"}

15. Click on the **Next** button.

![A screenshot of a computer Description automatically
generated](./media/image24.png){width="6.5in"
height="3.720833333333333in"}

16. Click on the **Done** button.

![](./media/image25.png){width="6.5in" height="3.115972222222222in"}

17. Enter the number again in your mobile authenticator app and select
    **Yes**..

![](./media/image26.png){width="4.727411417322835in"
height="6.019736439195101in"}

18. In the **Stay signed in?** window, click on the **Yes** button.

![A screenshot of a computer Description automatically
generated](./media/image10.png){width="3.9475634295713036in"
height="3.9203849518810148in"}

## **Task 2: Add Owner role to subscription**

1.  In the Azure portal search box, type **subscription**, navigate and
    click on **Subscriptions** under **Services**.

![A screenshot of a computer Description automatically
generated](./media/image27.png){width="6.762220034995625in"
height="3.7626181102362204in"}

2.  Click on your **Azure Pass -- Sponsorship** subscription name.

![A screenshot of a computer Description automatically
generated](./media/image28.png){width="7.066215004374453in"
height="3.931765091863517in"}

3.  On **Azure Pass -- Sponsorship** page, navigate and click
    on **Access control (IAM)**, click on **+Add** button, navigate and
    click on **Add role assignment** as shown in the below image**.**

> ![A screenshot of a computer Description automatically
> generated](./media/image29.png){width="6.268055555555556in"
> height="4.361111111111111in"}

4.  On **Add role assignment** page, click on **Privileged administrator
    roles** tab, navigate and select **Owner** role, then click on the
    **Next** button**.**

> ![A screenshot of a computer Description automatically
> generated](./media/image30.png){width="6.268055555555556in"
> height="4.361111111111111in"}

5.  Navigate and click on **+Select members** hyperlink. On **Select
    members** pane that appear on the right side, type and select your
    Office 365 tenant ID, then click on the **Select** button as shown
    in the below images.

> ![](./media/image31.png){width="6.5in" height="4.125in"}
>
> ![](./media/image32.png){width="6.5in" height="4.102083333333334in"}

6.  Click on the **Next** button.

> ![A screenshot of a computer Description automatically
> generated](./media/image33.png){width="6.268055555555556in"
> height="4.361111111111111in"}

7.  Click again on **Review + assign** button.

> ![](./media/image34.png){width="6.5in" height="5.295138888888889in"}

8.  In the **Add role assignment** -- **Conditions** tab, navigate to
    **What user can do** row and select the radio button **Allow user to
    assign all roles (highly privileged)**. Then, click on **Review +
    assign** button.

> ![](./media/image35.png){width="6.5in" height="3.986029090113736in"}

9.  Click again on **Review + assign** button.

> ![](./media/image36.png){width="6.5in" height="5.295138888888889in"}

10. You'll receive a notification confirming the Owner role is
    successfully assigned to the subscription.

> ![A white background with black text Description automatically
> generated](./media/image37.png){width="5.336055336832896in"
> height="0.9838353018372703in"}

**Note**: Microsoft 365 E5 license is assigned to your O365 tenant ID,
which included Microsoft Defender for Endpoint feature.

## **Task 3: Onboarding testserver1 in Microsoft Defender for Endpoints**

> 1\. In the Azure portal search bar, type **virtual machine**, then
> navigate and click on **Virtual machines** under **Services**.
>
> ![](./media/image38.png){width="6.5in" height="3.6805555555555554in"}

3.  In the **Virtual machines** page, navigate and click on **Create**,
    then click on **Azure virtual machine**.

> ![A screenshot of a computer Description automatically
> generated](./media/image39.png){width="6.5in"
> height="3.9298611111111112in"}

4.  In the **Create a virtual machine** page, navigate to **Resource
    group** row and click on **Create new**. Enter the name of the
    resource group (here, we entered **MCS-RG** as resource group name),
    then click on the **OK** button.

> ![](./media/image40.png){width="6.5in" height="5.388194444444444in"}

5\. Navigate to **Instance details** section, in the **virtual machine
name** field, enter the name of the virtual machine (here, we
entered [**TESTSERVER1**](urn:gd:lg:a:send-vm-keys)). In
the **Region** field, select **Southeast Asia**. In the **Availability
zone** field, ensure that **Zone 1** is selected. In the **Security
type** field, click on the dropdown and select **Standard**. In
the **Image** field, select **Windows Server 2019 Datacenter -x64
Gen2** from the dropdown.

> ![A screenshot of a computer Description automatically
> generated](./media/image41.png){width="6.268055555555556in"
> height="4.5375in"}
>
> ![](./media/image42.png){width="6.268055555555556in"
> height="4.850694444444445in"}

**Note**: If you encounter the following error - **This size is not
available in zone 1 . Zones '2,3' are supported"**, then scroll up and
uncheck Zone 1, check Zone 2 or 3 box.

5.  Navigate to **Size** field and click on **See all sizes**.
    In **Select a VM size** page, navigate and select **B2ms**, then
    click on the **Select** button.

> ![A screenshot of a computer Description automatically
> generated](./media/image43.png){width="6.268055555555556in"
> height="3.2465277777777777in"}
>
> ![A screenshot of a computer Description automatically
> generated](./media/image44.png){width="6.268055555555556in"
> height="3.7736111111111112in"}
>
> ![A screenshot of a computer Description automatically
> generated](./media/image45.png){width="6.268055555555556in"
> height="4.807638888888889in"}

5.  Scroll down to **Administrator account** section, enter the
    following details:

  -----------------------------------------------------------------------
  Username                          +++**Admin5801**+++
  --------------------------------- -------------------------------------
  Password                          +++**Administrator5801@\***+++

  Confirm password                  +++**Administrator5801@\***+++
  -----------------------------------------------------------------------

> ![A screenshot of a computer Description automatically
> generated](./media/image46.png){width="6.268055555555556in"
> height="4.579166666666667in"}

6.  Scroll down and select the checkbox, then click on **Review +
    create** button as shown in the below image.

![A screenshot of a computer Description automatically
generated](./media/image47.png){width="6.268055555555556in"
height="4.678472222222222in"}

7.  In the **Create a virtual machine** page, navigate and click on the
    **Create** button.

> ![A screenshot of a computer Description automatically
> generated](./media/image48.png){width="6.5in"
> height="5.4215277777777775in"}
>
> ![](./media/image49.png){width="6.5in" height="3.783333333333333in"}

8.  After the TESTSERVER1 virtual machine is successfully created, click
    on the **Go to resource** button.

> ![A screenshot of a computer Description automatically
> generated](./media/image50.png){width="6.5in"
> height="3.8208333333333333in"}

9.  You will be directed to the TESTSERVER1 virtual machine page.

> ![A screenshot of a computer Description automatically
> generated](./media/image51.png){width="6.5in"
> height="3.442361111111111in"}
>
> **Note**: If you see testserver1 virtual machine status is not ready.
> Troubleshoot the issue... then wait for 10-15 minutes and reload the
> page.

10. In **TESTSERVER1** virtual machine page, navigate and click on
    **Connect** on the left side navigation menu, then click on
    **Select** under **Native RDP** section.

![](./media/image52.png){width="6.5in" height="5.247222222222222in"}

11. In the **Native RDP** pane that appears on the right side, after
    fulfilling all the requirements, scroll down and click on **Download
    RDP file** button.

![](./media/image53.png){width="6.5in" height="4.0777777777777775in"}

12. On **TESTSERVER1.rdp could harm your device. Do you want to keep it
    anyway?** dialog box, click on **Keep** button.

> ![A screenshot of a computer Description automatically
> generated](./media/image54.png){width="6.5in"
> height="4.026388888888889in"}

13. On **TESTSERVER1.rdp** file, click on **Open file** link.

> ![](./media/image55.png){width="6.5in" height="3.0819444444444444in"}

14. On **The publisher of this remote connection can't be identified. Do
    you want to connect anyway?** dialog box, click on **Connect**
    button.

> ![A screenshot of a computer Description automatically
> generated](./media/image56.png){width="5.102602799650044in"
> height="2.693040244969379in"}

15. On **Enter your credentials** dialog box, enter the password (here,
    **Administrator5801@\***) and click on the **OK** button.

![](./media/image57.png){width="4.427258311461068in"
height="3.876977252843395in"}

16. On **The identity of the remote computer cannot be verified. Do you
    want to connect anyway?** dialog box, click on **Yes** button.

![](./media/image58.png){width="3.7769258530183727in"
height="3.8603018372703413in"}

17. The TESTSERVER1 VM will be opened. Minimize the Server Manager --
    Dashboard then minimize the virtual machine.

![](./media/image59.png){width="6.5in" height="3.8368055555555554in"}

18. In the Edge browser, open a new address bar and enter the following
    link: **<https://security.microsoft.com>** to open the Microsoft
    Defender Portal

![](./media/image60.png){width="6.5in" height="2.876388888888889in"}

19. Close **Meet your improved security center** dialog box.

![A screenshot of a computer Description automatically
generated](./media/image61.png){width="6.5in"
height="4.180555555555555in"}

19\. In **Microsoft Defender** portal, navigate and click on **System**,
then click on **Settings**. In the Settings page, you'll see **Defender
for** **Endpoints** as shown in the below image.

**Note**:

In case, you did not see **Defender for Endpoint**, ensure that you are
logged into Azure portal, then open a new address bar and enter the
following URL and wait for the configuration to be completed:
<https://security.microsoft.com/securitysettings/endpoints/integration?tid=>

![](./media/image62.png){width="6.5in" height="4.019444444444445in"}

![](./media/image63.png){width="6.5in" height="3.8652777777777776in"}

20\. In the **Endpoints** page, navigate to **Device management**
section and then click on **Onboarding**.

![](./media/image64.png){width="6.5in" height="4.0993055555555555in"}

21. Click on the dropdown under **Select operating system to start
    onboarding process** and select **Windows Server 2019 and 2022**.

![A screenshot of a computer Description automatically
generated](./media/image65.png){width="6.5in"
height="3.2569444444444446in"}

22. Scroll down and click on **Download onboarding package** button.

![A screenshot of a computer Description automatically
generated](./media/image66.png){width="6.5in"
height="3.4479166666666665in"}

23. After onboarding package is successfully downloaded, click on **Open
    file** link.

![A screenshot of a computer Description automatically
generated](./media/image67.png){width="3.801938976377953in"
height="1.0505358705161856in"}

24. Copy the Windows Command script

![](./media/image68.png){width="6.5in" height="4.235416666666667in"}

25. Go back to your server VM and paste the copied Windows Command
    Script on the desktop as shown in the below image.

![](./media/image69.png){width="6.5in" height="4.958333333333333in"}

26. Right click on the script and select **Run as administrator**.

![](./media/image70.png){width="6.5in" height="4.577083333333333in"}

27. Type **Y** and press the **Enter** button to continue the onboarding
    process.

![](./media/image71.png){width="6.5in" height="2.6284722222222223in"}

28. After onboarding the machine successfully on Defender for Endpoint,
    click on any key to continue the onboarding process.

![](./media/image72.png){width="6.5in" height="3.1479166666666667in"}

29. The onboarding of the **testserver1 VM** usually takes **15-30
    minutes**; therefore, continue with the next task.

30. After 15-30 minutes, close the **testserver1 VM**, go back to
    Microsoft Defender portal and refresh the page, navigate and click
    on **Devices**, you\'ll see the **testserver1** was successfully
    onboarded in Microsoft Defender for Endpoint.

![](./media/image73.png){width="6.5in" height="3.098611111111111in"}

## **Task 4: Onboarding testVM1 in Microsoft Defender for Endpoints**

> 1\. In the Azure portal search bar, type virtual machine, then
> navigate and click on **Virtual machines** under **Services**.

![](./media/image74.png){width="6.5in" height="3.6319444444444446in"}

2\. In the Virtual machines page, navigate and click on **Create**, then
click on **Azure virtual machine**.

![](./media/image75.png){width="6.5in" height="3.501388888888889in"}

3.  In **Create a virtual machine**, under the **Resource group** field,
    select **MCS-RG** resource group. Then, navigate to **Instance
    details** section, in the **Virtual machine name** field,
    enter [**testvm1**](urn:gd:lg:a:send-vm-keys). In
    the **Region** field, ensure **Southeast Asia** region is selected.

> ![](./media/image76.png){width="6.268055555555556in"
> height="4.680555555555555in"}

4.  In the **Security type** field, click on the dropdown and
    select **Standard**. In the **Image** field, select **Windows 11
    Pro, version 22H2 -x64 Gen2** from the dropdown.

> ![](./media/image77.png){width="6.268055555555556in"
> height="4.672916666666667in"}

19. Navigate to **Administrator account** section, enter the following
    details and leave all the field in the default state:

  -----------------------------------------------------------------------
  Username                          +++**Admin5802**+++
  --------------------------------- -------------------------------------
  Password                          +++**Administrator5801@\***+++

  Confirm password                  +++**Administrator5801@\***+++
  -----------------------------------------------------------------------

![](./media/image78.png){width="6.5in" height="4.664583333333334in"}

20. Under **Licensing** section, select the checkbox **I confirm I have
    an eligible Windows 10/11 license with multi-tenant hosting
    rights**. Then, click on **Review + create** button.

![](./media/image79.png){width="6.5in" height="5.426388888888889in"}

21. Click on the **Create** button.

![A screenshot of a computer Description automatically
generated](./media/image80.png){width="6.5in"
height="5.185416666666667in"}

![A screenshot of a computer Description automatically
generated](./media/image81.png){width="6.5in"
height="3.047222222222222in"}

22. The virtual machine is successfully created, click on the **Go to
    resource** button.

![](./media/image82.png){width="6.5in" height="3.167361111111111in"}

23. You will be directed to the **vmtest1** virtual machine page.

![A screenshot of a computer Description automatically
generated](./media/image83.png){width="6.5in"
height="3.917361111111111in"}

**Note**: If you see testvm1 virtual machine status is not ready.
Troubleshoot the issue\... then wait for 10-15 minutes and reload the
page.

24. In **testvm1** virtual machine page, navigate and click on
    **Connect** on the left side navigation menu, scroll down to
    **Native RDP** tile, and click on the **Download RDP file**.

![](./media/image84.png){width="6.5in" height="5.1618055555555555in"}

25. On **testvm1.rdp could harm your device. Do you want to keep it
    anyway?** dialog box, click on **Keep** button.

> ![A screenshot of a computer Description automatically
> generated](./media/image85.png){width="6.5in"
> height="3.4472222222222224in"}

26. On **testvm1.rdp** file, click on **Open file** link.

> ![A screenshot of a computer Description automatically
> generated](./media/image86.png){width="6.5in"
> height="2.810416666666667in"}

27. On **The publisher of this remote connection can't be identified. Do
    you want to connect anyway?** dialog box, click on **Connect**
    button.

> ![A screenshot of a computer Description automatically
> generated](./media/image87.png){width="5.627870734908137in"
> height="2.9765179352580926in"}

28. On **Enter your credentials** dialog box, enter the password (here,
    +++**Administrator5801@\***+++) and click on the **OK** button.

![A screenshot of a computer Description automatically
generated](./media/image88.png){width="4.639890638670166in"
height="4.018716097987752in"}

29. On **The identity of the remote computer cannot be verified. Do you
    want to connect anyway?** dialog box, click on **Yes** button.

![A screenshot of a computer error Description automatically
generated](./media/image89.png){width="3.701887576552931in"
height="3.7685892388451445in"}

30. On the **Choose privacy settings for your device** page, click on
    **Next** couple of times and then click on **Accept** button as
    shown in the below images.

![A screenshot of a computer Description automatically
generated](./media/image90.png){width="6.5in"
height="4.5993055555555555in"}

![A screenshot of a computer Description automatically
generated](./media/image91.png){width="6.5in"
height="4.580555555555556in"}

![A screenshot of a computer Description automatically
generated](./media/image92.png){width="6.5in"
height="4.611805555555556in"}

31. Go back to Microsoft Defender portal. In **Microsoft Defender**
    portal, navigate and click on **Settings**. In the **Settings**
    page, click on **Endpoints**.

![A screenshot of a computer Description automatically
generated](./media/image93.png){width="6.5in"
height="4.091666666666667in"}

32. In the **Endpoints** page, navigate to **Device management** section
    and then click on **Onboarding**.

33. Click on the dropdown under **Select operating system to start
    onboarding process** and select **Windows 10 and 11**.

![](./media/image94.png){width="6.5in" height="4.0159722222222225in"}

34. Scroll down and click on the **Download onboarding package** button.

![](./media/image95.png){width="6.5in" height="4.1194444444444445in"}

35. After the onboarding package is successfully downloaded, click on
    **Open file** link.

![A screenshot of a phone Description automatically
generated](./media/image96.png){width="3.7602515310586178in"
height="1.0421981627296588in"}

36. Copy the Windows Command script

![A screenshot of a computer Description automatically
generated](./media/image68.png){width="6.5in"
height="4.235416666666667in"}

37. Go back to **testvm1** and paste the copied Windows Command Script
    on the desktop as shown in the below image.

![](./media/image97.png){width="6.5in" height="4.147222222222222in"}

38. Right click on the script and select **Run as administrator**.

![](./media/image98.png){width="6.5in" height="4.625in"}

39. Type **Y** and press the **Enter** button to continue the onboarding
    process.

![A screenshot of a computer Description automatically
generated](./media/image99.png){width="6.5in"
height="4.279166666666667in"}

40. After onboarding the machine successfully on Defender for Endpoint,
    click on any key to continue the onboarding process.

![](./media/image100.png){width="6.5in" height="3.8569444444444443in"}

41. The onboarding of the **testvm1** usually takes **15-30 minutes**;
    therefore, continue with the next task.

42. After 15-30 minutes, close the **testvm1**, go back to Microsoft
    Defender portal and refresh the page, navigate and click
    on **Devices**, you\'ll see the **testvm1** was successfully
    onboarded in Microsoft Defender for Endpoint.

![](./media/image101.png){width="6.5in" height="4.115972222222222in"}

## **Task 5: Onboarding testVM2 in Microsoft Defender for Endpoints**

> 1\. In the Azure portal search bar, type virtual machine, then
> navigate and click on **Virtual machines** under **Services**.

![](./media/image102.png){width="6.5in" height="4.043055555555555in"}

2\. In the Virtual machines page, navigate and click on **Create**, then
click on **Azure virtual machine**.

![A screenshot of a computer Description automatically
generated](./media/image103.png){width="6.5in"
height="2.7736111111111112in"}

3.  In **Create a virtual machine**, under the **Resource group** field,
    select **MCS-RS** resource group. Then, navigate to **Instance
    details** section, in the **Virtual machine name** field,
    enter [**testvm2**](urn:gd:lg:a:send-vm-keys). In
    the **Region** field, ensure **Southeast Asia** region is selected.

> ![A screenshot of a computer Description automatically
> generated](./media/image104.png){width="5.602148950131234in"
> height="4.1783366141732285in"}

5.  In the **Security type** field, click on the dropdown and select
    **Standard**. In the **Image** field, select **Windows 11 Pro,
    version 22H2 -x64 Gen2** from the dropdown.

![](./media/image105.png){width="6.5in" height="5.009722222222222in"}

6.  Navigate to **Administrator account** section, enter the following
    details and leave all the field in the default state:

  -----------------------------------------------------------------------
  Username                          +++**Admin5803**+++
  --------------------------------- -------------------------------------
  Password                          +++**Administrator5801@\***+++

  Confirm password                  +++**Administrator5801@\***+++
  -----------------------------------------------------------------------

![](./media/image106.png){width="6.5in" height="4.454166666666667in"}

7.  Under **Licensing** section, select the checkbox **I confirm I have
    an eligible Windows 10/11 license with multi-tenant hosting
    rights**. Then, click on **Review + create** button.

![](./media/image79.png){width="6.5in" height="5.426388888888889in"}

8.  Click on the **Create** button.

![A screenshot of a computer Description automatically
generated](./media/image107.png){width="6.5in"
height="4.781944444444444in"}

![A screenshot of a computer Description automatically
generated](./media/image108.png){width="6.5in"
height="3.0083333333333333in"}

9.  The virtual machine is successfully created, click on the **Go to
    resource** button.

![A screenshot of a computer Description automatically
generated](./media/image109.png){width="6.5in"
height="2.970138888888889in"}

**Note**: If you see testvm2 virtual machine status is not ready.
Troubleshoot the issue\... then wait for 10-15 minutes and reload the
page.

10. In **testvm2** virtual machine page, navigate and click on
    **Connect** on the left side navigation menu, scroll down to
    **Native RDP** tile, and click on the **Download RDP file**.

![](./media/image110.png){width="6.5in" height="4.750694444444444in"}

11. In **testvm2.rdp could harm your device. Do you want to keep it
    anyway?** dialog box, click on **Keep** button.

![A screenshot of a computer Description automatically
generated](./media/image111.png){width="6.5in"
height="2.1631944444444446in"}

12. On **testvm2.rdp** file, click on **Open file** link.

> ![A screenshot of a computer Description automatically
> generated](./media/image112.png){width="6.5in"
> height="1.9368055555555554in"}

13. On **The publisher of this remote connection can't be identified. Do
    you want to connect anyway?** dialog box, click on **Connect**
    button.

> ![A screenshot of a computer Description automatically
> generated](./media/image113.png){width="5.7195833333333335in"
> height="2.993193350831146in"}

14. On **Enter your credentials** dialog box, enter the password (here,
    +++**Administrator5801@\***+++) and click on the **OK** button.

![A screenshot of a computer screen Description automatically
generated](./media/image114.png){width="4.7107360017497815in"
height="3.885314960629921in"}

15. On **The identity of the remote computer cannot be verified. Do you
    want to connect anyway?** dialog box, click on **Yes** button.

![A screenshot of a computer error message Description automatically
generated](./media/image115.png){width="4.068742344706911in"
height="4.185468066491689in"}

16. On **Choose privacy settings for your device** page, click on
    **Next** couple of times and then click on **Accept** button as
    shown in the below images.

![A screenshot of a computer Description automatically
generated](./media/image90.png){width="6.5in"
height="4.315972222222222in"}

![A screenshot of a computer Description automatically
generated](./media/image91.png){width="6.5in"
height="4.288888888888889in"}

![A screenshot of a computer Description automatically
generated](./media/image92.png){width="6.5in"
height="4.345138888888889in"}

17. Go back to your VM and open the WindowsDefenderATPOnboardingPackage
    that you have downloaded in **Task 4, Step #22**.

![A screenshot of a phone Description automatically
generated](./media/image96.png){width="3.7602515310586178in"
height="1.0421981627296588in"}

18. Copy the Windows Command script

![A screenshot of a computer Description automatically
generated](./media/image68.png){width="6.5in"
height="4.235416666666667in"}

19. Go back to **testvm2** and paste the copied Windows Command Script
    on the desktop as shown in the below image.

![](./media/image116.png){width="6.5in" height="4.184027777777778in"}

20. Right click on the script and select **Run as administrator**.

![A screenshot of a computer Description automatically
generated](./media/image117.png){width="6.5in"
height="5.2027777777777775in"}

21. Type **Y** and press the **Enter** button to continue the onboarding
    process.

![A screenshot of a computer Description automatically
generated](./media/image118.png){width="6.5in"
height="3.8673611111111112in"}

22. After onboarding the machine successfully on Defender for Endpoint,
    click on any key to continue the onboarding process.

![A screenshot of a computer Description automatically
generated](./media/image119.png){width="6.5in"
height="3.185416666666667in"}

23. **Refresh** Microsoft Defender portal.

![](./media/image120.png){width="6.5in" height="4.215972222222222in"}

43. The onboarding of the **testvm2** usually takes **15-30 minutes**;
    therefore, continue with the next task.

44. After 15-30 minutes, close the **testvm2**, go back to Microsoft
    Defender portal and refresh the page, navigate and click
    on **Devices**, you\'ll see the **testvm2** was successfully
    onboarded in Microsoft Defender for Endpoint.

![A screenshot of a computer Description automatically
generated](./media/image121.png){width="6.5in"
height="3.1347222222222224in"}

45. Close all the VMs.

## Task 6: Create test account using Microsoft Entra ID

1.  Open a new tab and enter the following link:
    **https://admin.microsoft.com/AdminPortal/#/homepage**

![](./media/image122.png){width="6.5in" height="5.702083333333333in"}

2.  Click on the Navigation menu represented by three horizontal bars,
    navigate and click on **Users**, then click on **Active users** as
    shown in the below image.

> ![](./media/image123.png){width="6.5in" height="3.165277777777778in"}

3.  Scroll down and select the user - **Diego Siciliani**, click on the
    vertical ellipsis beside the user name, then navigate and click on
    **Manage product licenses** as shown in the below image.

![A screenshot of a computer Description automatically
generated](./media/image124.png){width="6.5in" height="3.7375in"}

4.  Remove all the licenses assigned to **Diego Siciliani** by
    unchecking thee check boxes and then click on **Save changes**
    button.

![](./media/image125.png){width="6.358418635170604in"
height="4.972075678040245in"}

![](./media/image126.png){width="6.5in" height="4.897916666666666in"}

5.  Go back to **Active users** page. In the **Active users** page,
    click on **Add a user**.

> ![A screenshot of a computer Description automatically
> generated](./media/image127.png){width="6.5in"
> height="2.6041666666666665in"}

6.  Under **Set up the basics** pane, in the **First name** field, enter
    +++**Robert**+++, and in the **Last name** field, enter
    +++**Frost**+++. Navigate to **Username** field, and enter
    +++**bob**+++ as shown in the below image.

7.  Uncheck all the boxes, in the **Password** field, enter the
    following password: +++**Xof37931@**+++

  --------------------------------------------------------------------------------------
  Username                           **[bob@](mailto:bob@WWLx956024.onmicrosoft.com)**
  ---------------------------------- ---------------------------------------------------
  Password                           +++**Xof37931@**+++

  --------------------------------------------------------------------------------------

8.  Click on the **Next** button.

**Note**: You can use the **Username** and **Password** of your choice,
kindly note them on a notepad as these are required in the upcoming
tasks.

> ![A screenshot of a computer Description automatically
> generated](./media/image128.png){width="6.5in" height="4.25in"}
>
> ![](./media/image129.png){width="6.5in" height="4.357638888888889in"}

9.  In the **Product licenses** pane, navigate and select **Microsoft
    365 E5 and Microsoft teams enterprise** license checkboxes, then
    click on the **Next** button.

![](./media/image130.png){width="6.5in" height="3.65in"}

10. In the **Optional settings** pane, enter the following details and
    click on the **Next** button. You can mentioned your address
    details.

  -----------------------------------------------------------------------
  Job title                           +++Financial Analyst+++
  ----------------------------------- -----------------------------------
  Department                          +++Finance+++

  Office                              Alpine

  Mobile phone                        XXX-XXX-XXXX

  Street Address                      Suite 215

  City                                Alpine

  State or province                   Alabama

  Zip or postal code                  35014

  Country or region                   United States
  -----------------------------------------------------------------------

![A screenshot of a computer Description automatically
generated](./media/image131.png){width="6.5in"
height="4.638888888888889in"}

![](./media/image132.png){width="6.5in" height="4.1305555555555555in"}

11. Review the details and click on the **Finish adding** button.

![](./media/image133.png){width="6.5in" height="5.218055555555556in"}

12. On **Robert Frost added to active users** pane, navigate and click
    on the **Close** button.

![A screenshot of a computer Description automatically
generated](./media/image134.png){width="6.5in"
height="4.815277777777778in"}

13. You'll see that Robert Frost is added to the **Active users** page.

![](./media/image135.png){width="6.5in" height="2.845138888888889in"}

## Task 7: Preparing the prerequisite on the testvm1 virtual machine

1\. Go back to Azure portal. In the Azure portal search bar, type
**virtual machines**, then navigate and click on **Virtual machines**
under **Services**.

![](./media/image136.png){width="6.5in" height="4.470833333333333in"}

2\. In the **Virtual machines** page, click on **testvm1**.

![A screenshot of a computer Description automatically
generated](./media/image137.png){width="6.5in" height="3.1875in"}

46. **vmtest1** virtual machine page will be opened.

![A screenshot of a computer Description automatically
generated](./media/image83.png){width="6.5in"
height="3.917361111111111in"}

47. In **testvm1** virtual machine page, navigate and click on
    **Connect** on the left side navigation menu, scroll down to
    **Native RDP** tile, and click on the **Download RDP file**.

![](./media/image84.png){width="6.5in" height="5.1618055555555555in"}

48. On the **testvm1.rdp could harm your device. Do you want to keep it
    anyway?** dialog box, click on **Keep** button.

> ![A screenshot of a computer Description automatically
> generated](./media/image85.png){width="6.5in"
> height="3.4472222222222224in"}

49. On **testvm1.rdp** file, click on **Open file** link.

> ![A screenshot of a computer Description automatically
> generated](./media/image86.png){width="6.5in"
> height="2.810416666666667in"}

50. On **The publisher of this remote connection can't be identified. Do
    you want to connect anyway?** dialog box, click on **Connect**
    button.

> ![A screenshot of a computer Description automatically
> generated](./media/image87.png){width="5.627870734908137in"
> height="2.9765179352580926in"}

51. On **Enter your credentials** dialog box, enter the password (here,
    +++**Administrator5801@\***+++) and click on the **OK** button.

![A screenshot of a computer Description automatically
generated](./media/image88.png){width="4.598217410323709in"
height="4.018716097987752in"}

52. On **The identity of the remote computer cannot be verified. Do you
    want to connect anyway?** dialog box, click on **Yes** button.

![A screenshot of a computer error Description automatically
generated](./media/image89.png){width="3.701887576552931in"
height="3.7685892388451445in"}

53. After logging in to testvm1 virtual machine, open the Edge browser,
    then select **Start without data** button \> **Confirm and
    Continue** button \> **Continue without this data** button \>
    **Confirm and start browsing** button \> **Finish** button) and
    enter the following URL in the address bar:
    [**https://portal.office.com**](https://portal.office.com)

![](./media/image138.png){width="6.5in" height="4.672916666666667in"}

54. Sign in to the Microsoft 365 portal using the following details:

  -----------------------------------------------------------------------
  Username                           **bob@**
  ---------------------------------- ------------------------------------
  Password                           +++**Xof37931@**+++

  -----------------------------------------------------------------------

![](./media/image139.png){width="6.5in" height="5.247916666666667in"}

![](./media/image140.png){width="5.613965441819772in"
height="4.4869739720035in"}

> In the **Stay signed in?** window, click on the **Yes** button.
>
> ![](./media/image141.png){width="4.76909886264217in"
> height="4.669047462817148in"}

55. In **Microsoft 365** page, navigate and click on **Install and
    more** dropdown, then click on **Install Microsoft 365 apps**.

![](./media/image142.png){width="6.5in" height="3.9611111111111112in"}

56. Click on **Install Office**.

![A screenshot of a computer Description automatically
generated](./media/image143.png){width="6.268055555555556in"
height="3.765972222222222in"}

57. **OfficeSetup.exe** file will be downloaded, click on **Open file**
    link.

![A screenshot of a computer Description automatically
generated](./media/image144.png){width="6.5in"
height="3.709722222222222in"}

58. Wait for few minutes while Microsoft 365 and Office downloads.

![A screenshot of a computer Description automatically
generated](./media/image145.png){width="6.5in" height="4.275in"}

![](./media/image146.png){width="6.5in" height="3.6256944444444446in"}

**Note**: The installation will take around 10-20 minutes to complete.

59. On **You're all set!** dialog box, click on the **Close** button.

![](./media/image147.png){width="6.5in" height="3.973611111111111in"}

60. Click on the **Start menu** and then click on **Word** as shown in
    the below image.

![](./media/image148.png){width="6.5in" height="5.5256944444444445in"}

61. Click on **Sign in or create account** button.

![](./media/image149.png){width="6.5in" height="4.159722222222222in"}

62. Login using the following details:

  -----------------------------------------------------------------------
  Username                           **bob@**
  ---------------------------------- ------------------------------------
  Password                           +++**Xof37931@**+++

  -----------------------------------------------------------------------

![A screenshot of a computer Description automatically
generated](./media/image150.png){width="6.5in"
height="4.665277777777778in"}

![](./media/image151.png){width="6.5in" height="4.3625in"}

63. On **Stay signed in to all your apps** dialog box, click on **OK**
    button.

![](./media/image152.png){width="6.5in" height="5.146527777777778in"}

64. On **You're all set** dialog box, click on **Done** button.

![A screenshot of a computer Description automatically
generated](./media/image153.png){width="6.5in"
height="5.501388888888889in"}

65. On the **Accept the license agreement** dialog box, click on
    **Accept** button.

![A screenshot of a computer Description automatically
generated](./media/image154.png){width="6.5in"
height="4.269444444444445in"}

66. On Your privacy matters dialog box, click on the **Close** button.

![](./media/image155.png){width="6.5in" height="4.148611111111111in"}

Task 8: Stop all the Virtual Machines

1\. In the Azure portal search box, type +++virtual machines+++, then
navigate and click on **Virtual machines** under **Services**.

![A screenshot of a computer Description automatically
generated](./media/image156.png){width="6.5in"
height="5.098611111111111in"}

2\. Click on **testvm1** virtual machine.

![A screenshot of a computer Description automatically
generated](./media/image157.png){width="5.292121609798775in"
height="3.3828608923884516in"}

3\. In the **testvm1** virtual machine page, navigate and click on the
**Stop** button.

![A screenshot of a computer Description automatically
generated](./media/image158.png){width="6.5in"
height="3.879861111111111in"}

3.  In **Stop this virtual machine** dialog box, click on the **Yes**
    button.

![A screenshot of a computer Description automatically
generated](./media/image159.png){width="6.5in" height="3.31875in"}

**Summary**

In this lab, you\'ve assigned the Owner role to the Azure subscription,
then you\'ve created and onboarded Windows Server and Windows 11 Pro
virtual machines (testserver1, testVM1, and testVM2) to Microsoft
Defender for Endpoints, bolstering security with real-time monitoring
and threat response capabilities across different VM types. Then,
you\'ve created a test user account (Robert Frost) with Microsoft 365 E5
and Microsoft teams enterprise licenses. Finally, you\'ve installed
Microsoft 365 apps and configured necessary settings, facilitating a
comprehensive testing environment for Azure, Microsoft Defender, and
Microsoft Copilot for Security features.
