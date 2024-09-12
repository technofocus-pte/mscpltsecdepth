**Lab 3: Creating a multi-stage incident in Microsoft Defender**

**Introduction**

In this lab, you'll be creating a multi-stage incident in Microsoft
Defender by executing malicious documents and scripts in testvm1. The
multi-stage incident will be analyzed in the upcoming labs using
Microsoft Copilot for Security.

**Objectives**

-   To install Git and download repositories having malware payloads on
    testvm1 in Azure.

-   To run malicious documents and scripts.

-   To perform a ransomware attack using RanSim.

-   To check protection action and recommendations from Windows
    Security.

## **Task 1: Install git and download the payloads on testvm1**

> 1\. In the Azure portal search bar, type virtual machine, then
> navigate and click on **Virtual machines** under **Services**.

![A screenshot of a computer Description automatically
generated](./media/image1.png){width="6.5in"
height="3.6319444444444446in"}

2\. In the **Virtual machines** page, navigate and click on **testvm1**.
On **testvm1** Virtual machine page, click on the **Start** button.

![](./media/image2.png){width="6.5in" height="3.2354166666666666in"}

![A screenshot of a computer Description automatically
generated](./media/image3.png){width="6.5in"
height="3.647222222222222in"}

3.  Wait for few minutes for the virtual machine to start, then navigate
    and click on **Connect** on the left side navigation menu, scroll
    down to **Native RDP** tile, and click on the **Download RDP file**.

![A screenshot of a computer Description automatically
generated](./media/image4.png){width="6.5in"
height="5.1618055555555555in"}

4.  On **testvm1.rdp could harm your device. Do you want to keep it
    anyway?** dialog box, click on **Keep** button.

> ![A screenshot of a computer Description automatically
> generated](./media/image5.png){width="6.5in"
> height="3.4472222222222224in"}

5.  On **testvm1.rdp** file, click on **Open file** link.

> ![A screenshot of a computer Description automatically
> generated](./media/image6.png){width="6.5in"
> height="2.810416666666667in"}

6.  On **The publisher of this remote connection can't be identified. Do
    you want to connect anyway?** dialog box, click on **Connect**
    button.

> ![A screenshot of a computer Description automatically
> generated](./media/image7.png){width="5.627870734908137in"
> height="2.9765179352580926in"}

7.  On **Enter your credentials** dialog box, enter the password (here,
    **Administrator5801@\***) and click on the **OK** button.

![A screenshot of a computer Description automatically
generated](./media/image8.png){width="4.639890638670166in"
height="4.018716097987752in"}

8.  On **The identity of the remote computer cannot be verified. Do you
    want to connect anyway?** dialog box, click on **Yes** button.

![A screenshot of a computer error Description automatically
generated](./media/image9.png){width="3.701887576552931in"
height="3.7685892388451445in"}

9.  Open the Edge browser, navigate to the address bar and enter the
    following link: **https://git-scm.com/downloads**

![](./media/image10.png){width="6.5in" height="3.017361111111111in"}

10. On **git** window, navigate to **Downloads** section and click on
    **Windows** as shown in the below image.

![A screenshot of a computer Description automatically
generated](./media/image11.png){width="6.5in"
height="3.988888888888889in"}

11. On **Download for Windows** page, navigate to **Standalone
    Installer** and click on **64-bit Git for Windows Setup**.

![A screenshot of a computer Description automatically
generated](./media/image12.png){width="6.5in"
height="3.5555555555555554in"}

12. Click on the **Git.exe** file.

![A screenshot of a computer Description automatically
generated](./media/image13.png){width="6.5in"
height="2.3673611111111112in"}

13. On **Git Setup** - **Information** dialog box, click on the **Next**
    button.

![A screenshot of a computer Description automatically
generated](./media/image14.png){width="4.735749125109361in"
height="3.676875546806649in"}

14. On **Select Destination Location** dialog box, click on the **Next**
    button.

![A screenshot of a computer Description automatically
generated](./media/image15.png){width="4.760761154855643in"
height="3.6935509623797027in"}

15. On **Select Components** dialog box, click on the **Next** button.

![](./media/image16.png){width="4.752423447069116in"
height="3.676875546806649in"}

16. On **Select Start Menu Folder** dialog box, click on the **Next**
    button.

![A screenshot of a computer Description automatically
generated](./media/image17.png){width="4.735749125109361in"
height="3.701887576552931in"}

17. On **Choosing the default editor used by Git** dialog box, click on
    the **Next** button.

![A screenshot of a computer Description automatically
generated](./media/image18.png){width="4.719073709536308in"
height="3.751913823272091in"}

18. Leave **Adjusting the name of the initial branch in new
    repositories** dialog box in default state and click on the **Next**
    button.

![A screenshot of a computer screen Description automatically
generated](./media/image19.png){width="4.79411198600175in"
height="3.6685378390201224in"}

19. Leave **Adjusting your PATH environment** dialog box in default
    state and click on the **Next** button.

![A screenshot of a computer Description automatically
generated](./media/image20.png){width="4.727411417322835in"
height="3.701887576552931in"}

20. Leave **Choosing the SSH executable** dialog box in default state
    and click on the **Next** button.

![A screenshot of a computer Description automatically
generated](./media/image21.png){width="4.79411198600175in"
height="3.7602515310586178in"}

21. Leave **Choosing HTTPS transport backend** dialog box in default
    state and click on the **Next** button.

![A screenshot of a computer Description automatically
generated](./media/image22.png){width="4.727411417322835in"
height="3.7352384076990375in"}

22. Leave **Configuring the line ending conversions** dialog box in
    default state and click on the **Next** button.

![A screenshot of a computer Description automatically
generated](./media/image23.png){width="4.760761154855643in"
height="3.751913823272091in"}

23. Leave **Configuring the terminal emulator to use with Git Bash**
    dialog box in default state and click on the **Next** button.

![A screenshot of a computer Description automatically
generated](./media/image24.png){width="4.727411417322835in"
height="3.7352384076990375in"}

24. Leave **Choose the default behavior of 'git pull'** dialog box in
    default state and click on the **Next** button.

![A screenshot of a computer Description automatically
generated](./media/image25.png){width="4.727411417322835in"
height="3.7685892388451445in"}

25. Leave **Choose a credential helper** dialog box in default state and
    click on the **Next** button.

![A screenshot of a computer Description automatically
generated](./media/image26.png){width="4.76909886264217in"
height="3.7185629921259844in"}

26. Leave **Configuring extra options** dialog box in default state and
    click on the **Next** button.

![A screenshot of a computer Description automatically
generated](./media/image27.png){width="4.727411417322835in"
height="3.701887576552931in"}

27. Leave **Configuring experimental options** dialog box in default
    state and click on the **Next** button.

![A screenshot of a computer Description automatically
generated](./media/image28.png){width="4.752423447069116in"
height="3.7269006999125107in"}

28. Wait for few minutes for the installation to complete.

![A screenshot of a computer Description automatically
generated](./media/image29.png){width="4.752423447069116in"
height="3.7435761154855642in"}

29. Select **Launch Git Bash** checkbox and then click on the **Finish**
    button.

![](./media/image30.png){width="4.74408573928259in"
height="3.7435761154855642in"}

## **Task 2: Executing Malicious Documents and Scripts**

1.  In **Git Bash**, execute the following command to download
    **examples** folder containing various malware files and scripts.

**git clone https://github.com/directorcia/examples**

![](./media/image31.png){width="6.5in" height="1.0625in"}

![A computer screen with white text Description automatically
generated](./media/image32.png){width="6.5in"
height="2.6847222222222222in"}

2.  Navigate to **C:\\Users\\Admin5802**, then click on **examples**
    folder as shown in the below image.

![A screenshot of a computer Description automatically
generated](./media/image33.png){width="6.5in"
height="4.561805555555556in"}

3.  You will see various malwares files and script.

![A screenshot of a computer Description automatically
generated](./media/image34.png){width="6.5in"
height="3.5444444444444443in"}

4.  Right click on **RS4_WinATP-Intro-Invoice** and open the file in
    word.

![A screenshot of a computer Description automatically
generated](./media/image35.png){width="6.5in"
height="4.227083333333334in"}

5.  You will be prompted to enter the password, provide the password as
    +++**WDATP!diy#**+++ and click on the **OK** button.

![A screenshot of a computer Description automatically
generated](./media/image36.png){width="6.5in"
height="4.018055555555556in"}

6.  The file will open with a **SECURITY WARNING**, click on the
    **Enable content** button as shown in the below image.

![A screenshot of a computer Description automatically
generated](./media/image37.png){width="6.5in"
height="4.764583333333333in"}

7.  You'll be prompted about a demo attack, click on the **OK** button.

![A screenshot of a computer Description automatically
generated](./media/image38.png){width="6.5in"
height="4.5465277777777775in"}

8.  A new file **WinATP-Intro-Backdoor.exe**, which represents the
    backdoor, is created onto the Desktop by a PowerShell script
    launched from the word document.

9.  The script goes on to create a scheduled task to launch the backdoor
    at a predefined time. This mechanism of indirect process launch is
    sometimes used for stealth, as it is harder to trace back to the
    document.

**Note**: When the backdoor is launched, it creates an auto-start entry
under the registry Run key, allowing it to stay persistent by starting
automatically with Windows. A Command Prompt window opens, indicating
that the simulated backdoor is running. Close the Command Prompt window
to end the **WinATP-Intro-Backdoor.exe** process. In case, you did not
see the Command Prompt window, then move on to the next step.

![A screenshot of a computer Description automatically
generated](./media/image39.png){width="5.98906605424322in"
height="3.252396106736658in"}

10. Open
    **TestFile_Block_Office_applications_from_creating_executable** in
    word as shown in the below image.

![](./media/image40.png){width="6.5in" height="4.605555555555555in"}

11. Click on **Enable content**, it will execute another ransomware
    attack in **testvm1**.

![](./media/image41.png){width="6.5in" height="3.5166666666666666in"}

In case, **Microsoft Word Security Notice** dialog box appears, click on
the **OK** button.

![A screenshot of a computer Description automatically
generated](./media/image42.png){width="6.5in"
height="3.3569444444444443in"}

12. Now, open **TestFile+OfficeChildProcess** file in word.

![A screenshot of a computer Description automatically
generated](./media/image43.png){width="6.5in"
height="4.205555555555556in"}

13. Click on **Enable Content**. If you see an error, the action was
    blocked. If you see cmd.exe launch, it was not blocked.

![A screenshot of a computer Description automatically
generated](./media/image44.png){width="6.5in" height="4.525in"}

![A screenshot of a computer Description automatically
generated](./media/image45.png){width="6.5in"
height="3.911111111111111in"}

**Running Malicious Script**

**Note**: There are some malicious script that you need to execute to
get the alerts in Microsoft Defender portal. As these scripts are
malicious, the output of the command will not be the same. Sometimes the
script execute, sometimes it will be blocked and you may encounter an
error.

14. Right click inside the folder, then navigate and click on **Open in
    Terminal**.

> ![Screenshot](./media/image46.png){width="2.283333333333333in"
> height="1.6666666666666667in"}

15. Type [**ls**](urn:gd:lg:a:send-vm-keys) to get the list of the
    scripts in the folder. Then, execute the following script:

> +++[**./SQLDumper.exe**](urn:gd:lg:a:send-vm-keys)+++
>
> ![](./media/image47.png){width="6.268055555555556in"
> height="3.6951388888888888in"}

16. Run the following command:

> +++[**.\\wdtestfile.exe**](urn:gd:lg:a:send-vm-keys)+++
>
> ![](./media/image48.png){width="6.268055555555556in"
> height="3.7881944444444446in"}

17. After the command successfully executed, press the **Enter** button.

> ![A screenshot of a computer Description automatically
> generated](./media/image49.png){width="6.268055555555556in"
> height="3.9298611111111112in"}

**Note**: Alerts generated will be started within 15-30 minutes in
Microsoft Defender Portal.

## **Task 3: Performing a ransomware attack using RanSim**

RanSim is a ransomware simulation script written in PowerShell. It
recursively encrypts files in the target directory using 256-bit AES
encryption. RanSim has no self-spreading capabilities and will only run
on the system you execute it on.

1.  Download the RanSim folder in testvm1 using the following script:

**git clone https://github.com/lawndoc/RanSim.git**

![](./media/image50.png){width="6.5in" height="2.421527777777778in"}

2.  In testvm1 search bar, type +++**environment variables**+++, then
    navigate and click on **Edit environment variables for your
    account** as shown in the below image.

![](./media/image51.png){width="6.5in" height="6.473611111111111in"}

3.  In the **System Properties** dialog box, navigate and click on
    **Environment Variables** button.

![A screenshot of a computer program Description automatically
generated](./media/image52.png){width="4.552321741032371in"
height="4.777436570428696in"}

4.  In the **Environment Variables** dialog box, click on the **New**
    button.

![](./media/image53.png){width="5.886335301837271in"
height="6.478303805774278in"}

6.  In the next steps, you will be setting the following Parameters:

    -   TargetPath : **C:\\RanSim**

    -   Extension : **.encrypted**

    -   Key : **Q5KyUru6wn82hlY9k8xUjJOPIC9da41jgRkpt21jo2L=**

    -   TargetFiles : .pdf .xls\* .ppt\* .doc\* .accd\* .rtf .txt .csv
        .jpg .jpeg .png .gif .avi .midi .mov mp3 .mp4 .mpeg .mpeg2
        .mpeg3 .mpg .ogg

7.  On the **New User Variable** dialog box, in the **Variable
    name** field, enter +++**TargetPath+++**, and in the **Variable
    value** field,
    enter +++**[C:\\RanSim](urn:gd:lg:a:send-vm-keys)+++**, then press
    the **OK** button.

![](./media/image54.png){width="6.268055555555556in"
height="1.5652777777777778in"}

8.  **TargetPath** variable is successfully added. Now, click on
    the **New** button as shown in the below image.

![](./media/image55.png){width="4.823467847769029in"
height="4.560009842519685in"}

8.  On the **New User Variable** dialog box, in the **Variable
    name** field, enter +++**[Extension](urn:gd:lg:a:send-vm-keys)+++**,
    and in the **Variable value** field,
    enter +++**[.encrypted](urn:gd:lg:a:send-vm-keys)+++**. Then, click
    on the **OK** button.

![](./media/image56.png){width="6.268055555555556in"
height="1.5979166666666667in"}

9.  **Extension** variable is successfully added. Now, click on
    the **New** button as shown in the below image.

![A screenshot of a computer Description automatically
generated](./media/image57.png){width="4.766311242344707in"
height="4.447360017497813in"}

10. On the **New User Variable** dialog box, in the **Variable
    name** field, enter +++**[Key](urn:gd:lg:a:send-vm-keys)+++**, and
    in the **Variable value** field,
    enter +++[**Q5KyUru6wn82hlY9k8xUjJOPIC9da41jgRkpt21jo2L=**](urn:gd:lg:a:send-vm-keys)+++
    Then, click on the **OK** button.

![](./media/image58.png){width="6.268055555555556in"
height="1.5479166666666666in"}

11. **Key** variable is successfully added. Now, click on
    the **New** button as shown in the below image.

![](./media/image59.png){width="4.17824365704287in"
height="3.981043307086614in"}

12. On the **New User Variable** dialog box, in the **Variable
    name** field, enter +++**TargetFiles**+++, and in the **Variable
    value** field, enter

+++.pdf .xls\* .ppt\* .doc\* .accd\* .rtf .txt .csv .jpg .jpeg .png .gif
.avi .midi .mov mp3 .mp4 .mpeg .mpeg2 .mpeg3 .mpg .ogg+++

Then, click on the **OK** button.

![](./media/image60.png){width="6.268055555555556in" height="1.6in"}

13. **TargetFiles** variable is successfully added. Close
    the **Environment Variables** dialog box.

![A screenshot of a computer Description automatically
generated](./media/image61.png){width="4.011839457567804in"
height="3.777155511811024in"}

5.  In **testvm1** virtual machine, navigate to
    **C:\\Users\\Admin5802\\** and copy the **RanSim** folder, then
    paste the folder in **C:\\**

6.  Open **RanSim** folder. Click anywhere inside the folder, then right
    click and select **Open in terminal**.

**Note:** Please ensure that your RanSim folder is in C:\\

![A screenshot of a computer Description automatically
generated](./media/image62.png){width="6.5in"
height="4.475694444444445in"}

7.  In the command prompt, execute the following command to initiate a
    ransomware attack. In case, the attack failed to execute
    successfully and showed an error, then ignore and move on to the
    next step.

**.\\RanSim.ps1 -Mode encrypt**

![A screenshot of a computer Description automatically
generated](./media/image63.png){width="6.5in"
height="3.127083333333333in"}

![](./media/image64.png){width="5.570897856517935in"
height="3.1131846019247593in"}

**Task 4: Checking protection action and recommendations from Windows
Security**

1.  In **testvm1** search bar, type **virus and threat protection**,
    then navigate and click on **Virus & threat protection** under
    **Best match** as shown in the below image.

![](./media/image65.png){width="6.5in" height="5.495833333333334in"}

2.  In **Virus & threat protection** page, under **Current threats**
    section, navigate and click on **Protection history**.

![A screenshot of a computer Description automatically
generated](./media/image66.png){width="6.5in"
height="3.661111111111111in"}

3.  You can see the protection action and recommendations from Windows
    Security.

![](./media/image67.png){width="6.5in" height="4.263194444444444in"}

4.  Click on **Threat quarantined** to view the details.

![](./media/image68.png){width="6.5in" height="4.375694444444444in"}

5.  Similarly, click on **Threat blocked** to view the details.

![](./media/image69.png){width="6.5in" height="3.8402777777777777in"}

**Summary**

In this lab, you\'ve installed and configured Git on testvm1. You\'ve
also executed malicious documents and scripts. Then, you\'ve simulated a
ransomware attack using RanSim. Then, you\'ve checked the protection
actions and recommendations from Windows Security, examining details of
quarantined and blocked threats. All these activities will create a
multi-stage incident, which will be analyzed in the upcoming labs using
Microsoft Copilot for Security.
