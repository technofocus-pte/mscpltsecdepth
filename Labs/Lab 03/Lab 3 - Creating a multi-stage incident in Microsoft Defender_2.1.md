**Lab 3: Creating a multi-stage incident in Microsoft Defender**

**Introduction**

In this lab, you’ll be creating a multi-stage incident in Microsoft
Defender by executing malicious documents and scripts in testvm1. The
multi-stage incident will be analyzed in the upcoming labs using
Microsoft Copilot for Security.

**Objectives**

- To install Git and download repositories having malware payloads on
  testvm1 in Azure.

- To run malicious documents and scripts.

- To perform a ransomware attack using RanSim.

- To check protection action and recommendations from Windows Security.

## **Task 1: Install git and download the payloads on testvm1**

> 1\. In the Azure portal search bar, type virtual machine, then
> navigate and click on **Virtual machines** under **Services**.

<img src="./media/image1.png" style="width:6.5in;height:3.63194in"
alt="A screenshot of a computer Description automatically generated" />

2\. In the **Virtual machines** page, navigate and click on **testvm1**.
On **testvm1** Virtual machine page, click on the **Start** button.

<img src="./media/image2.png" style="width:6.5in;height:3.23542in" />

<img src="./media/image3.png" style="width:6.5in;height:3.64722in"
alt="A screenshot of a computer Description automatically generated" />

3.  Wait for few minutes for the virtual machine to start, then navigate
    and click on **Connect** on the left side navigation menu, scroll
    down to **Native RDP** tile, and click on the **Download RDP file**.

<img src="./media/image4.png" style="width:6.5in;height:5.16181in"
alt="A screenshot of a computer Description automatically generated" />

4.  On **testvm1.rdp could harm your device. Do you want to keep it
    anyway?** dialog box, click on **Keep** button.

> <img src="./media/image5.png" style="width:6.5in;height:3.44722in"
> alt="A screenshot of a computer Description automatically generated" />

5.  On **testvm1.rdp** file, click on **Open file** link.

> <img src="./media/image6.png" style="width:6.5in;height:2.81042in"
> alt="A screenshot of a computer Description automatically generated" />

6.  On **The publisher of this remote connection can’t be identified. Do
    you want to connect anyway?** dialog box, click on **Connect**
    button.

> <img src="./media/image7.png" style="width:5.62787in;height:2.97652in"
> alt="A screenshot of a computer Description automatically generated" />

7.  On **Enter your credentials** dialog box, enter the password (here,
    **Administrator5801@\***) and click on the **OK** button.

<img src="./media/image8.png" style="width:4.63989in;height:4.01872in"
alt="A screenshot of a computer Description automatically generated" />

8.  On **The identity of the remote computer cannot be verified. Do you
    want to connect anyway?** dialog box, click on **Yes** button.

<img src="./media/image9.png" style="width:3.70189in;height:3.76859in"
alt="A screenshot of a computer error Description automatically generated" />

9.  Open the Edge browser, navigate to the address bar and enter the
    following link: **https://git-scm.com/downloads**

<img src="./media/image10.png" style="width:6.5in;height:3.01736in" />

10. On **git** window, navigate to **Downloads** section and click on
    **Windows** as shown in the below image.

<img src="./media/image11.png" style="width:6.5in;height:3.98889in"
alt="A screenshot of a computer Description automatically generated" />

11. On **Download for Windows** page, navigate to **Standalone
    Installer** and click on **64-bit Git for Windows Setup**.

<img src="./media/image12.png" style="width:6.5in;height:3.55556in"
alt="A screenshot of a computer Description automatically generated" />

12. Click on the **Git.exe** file.

<img src="./media/image13.png" style="width:6.5in;height:2.36736in"
alt="A screenshot of a computer Description automatically generated" />

13. On **Git Setup** - **Information** dialog box, click on the **Next**
    button.

<img src="./media/image14.png" style="width:4.73575in;height:3.67688in"
alt="A screenshot of a computer Description automatically generated" />

14. On **Select Destination Location** dialog box, click on the **Next**
    button.

<img src="./media/image15.png" style="width:4.76076in;height:3.69355in"
alt="A screenshot of a computer Description automatically generated" />

15. On **Select Components** dialog box, click on the **Next** button.

<img src="./media/image16.png"
style="width:4.75242in;height:3.67688in" />

16. On **Select Start Menu Folder** dialog box, click on the **Next**
    button.

<img src="./media/image17.png" style="width:4.73575in;height:3.70189in"
alt="A screenshot of a computer Description automatically generated" />

17. On **Choosing the default editor used by Git** dialog box, click on
    the **Next** button.

<img src="./media/image18.png" style="width:4.71907in;height:3.75191in"
alt="A screenshot of a computer Description automatically generated" />

18. Leave **Adjusting the name of the initial branch in new
    repositories** dialog box in default state and click on the **Next**
    button.

<img src="./media/image19.png" style="width:4.79411in;height:3.66854in"
alt="A screenshot of a computer screen Description automatically generated" />

19. Leave **Adjusting your PATH environment** dialog box in default
    state and click on the **Next** button.

<img src="./media/image20.png" style="width:4.72741in;height:3.70189in"
alt="A screenshot of a computer Description automatically generated" />

20. Leave **Choosing the SSH executable** dialog box in default state
    and click on the **Next** button.

<img src="./media/image21.png" style="width:4.79411in;height:3.76025in"
alt="A screenshot of a computer Description automatically generated" />

21. Leave **Choosing HTTPS transport backend** dialog box in default
    state and click on the **Next** button.

<img src="./media/image22.png" style="width:4.72741in;height:3.73524in"
alt="A screenshot of a computer Description automatically generated" />

22. Leave **Configuring the line ending conversions** dialog box in
    default state and click on the **Next** button.

<img src="./media/image23.png" style="width:4.76076in;height:3.75191in"
alt="A screenshot of a computer Description automatically generated" />

23. Leave **Configuring the terminal emulator to use with Git Bash**
    dialog box in default state and click on the **Next** button.

<img src="./media/image24.png" style="width:4.72741in;height:3.73524in"
alt="A screenshot of a computer Description automatically generated" />

24. Leave **Choose the default behavior of ‘git pull’** dialog box in
    default state and click on the **Next** button.

<img src="./media/image25.png" style="width:4.72741in;height:3.76859in"
alt="A screenshot of a computer Description automatically generated" />

25. Leave **Choose a credential helper** dialog box in default state and
    click on the **Next** button.

<img src="./media/image26.png" style="width:4.7691in;height:3.71856in"
alt="A screenshot of a computer Description automatically generated" />

26. Leave **Configuring extra options** dialog box in default state and
    click on the **Next** button.

<img src="./media/image27.png" style="width:4.72741in;height:3.70189in"
alt="A screenshot of a computer Description automatically generated" />

27. Leave **Configuring experimental options** dialog box in default
    state and click on the **Next** button.

<img src="./media/image28.png" style="width:4.75242in;height:3.7269in"
alt="A screenshot of a computer Description automatically generated" />

28. Wait for few minutes for the installation to complete.

<img src="./media/image29.png" style="width:4.75242in;height:3.74358in"
alt="A screenshot of a computer Description automatically generated" />

29. Select **Launch Git Bash** checkbox and then click on the **Finish**
    button.

<img src="./media/image30.png"
style="width:4.74409in;height:3.74358in" />

## **Task 2: Executing Malicious Documents and Scripts**

1.  In **Git Bash**, execute the following command to download
    **examples** folder containing various malware files and scripts.

**git clone https://github.com/directorcia/examples**

<img src="./media/image31.png" style="width:6.5in;height:1.0625in" />

<img src="./media/image32.png" style="width:6.5in;height:2.68472in"
alt="A computer screen with white text Description automatically generated" />

2.  Navigate to **C:\Users\Admin5802**, then click on **examples**
    folder as shown in the below image.

<img src="./media/image33.png" style="width:6.5in;height:4.56181in"
alt="A screenshot of a computer Description automatically generated" />

3.  You will see various malwares files and script.

<img src="./media/image34.png" style="width:6.5in;height:3.54444in"
alt="A screenshot of a computer Description automatically generated" />

4.  Right click on **RS4_WinATP-Intro-Invoice** and open the file in
    word.

<img src="./media/image35.png" style="width:6.5in;height:4.22708in"
alt="A screenshot of a computer Description automatically generated" />

5.  You will be prompted to enter the password, provide the password as
    +++**WDATP!diy#**+++ and click on the **OK** button.

<img src="./media/image36.png" style="width:6.5in;height:4.01806in"
alt="A screenshot of a computer Description automatically generated" />

6.  The file will open with a **SECURITY WARNING**, click on the
    **Enable content** button as shown in the below image.

<img src="./media/image37.png" style="width:6.5in;height:4.76458in"
alt="A screenshot of a computer Description automatically generated" />

7.  You’ll be prompted about a demo attack, click on the **OK** button.

<img src="./media/image38.png" style="width:6.5in;height:4.54653in"
alt="A screenshot of a computer Description automatically generated" />

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

<img src="./media/image39.png" style="width:5.98907in;height:3.2524in"
alt="A screenshot of a computer Description automatically generated" />

10. Open
    **TestFile_Block_Office_applications_from_creating_executable** in
    word as shown in the below image.

<img src="./media/image40.png" style="width:6.5in;height:4.60556in" />

11. Click on **Enable content**, it will execute another ransomware
    attack in **testvm1**.

<img src="./media/image41.png" style="width:6.5in;height:3.51667in" />

In case, **Microsoft Word Security Notice** dialog box appears, click on
the **OK** button.

<img src="./media/image42.png" style="width:6.5in;height:3.35694in"
alt="A screenshot of a computer Description automatically generated" />

12. Now, open **TestFile+OfficeChildProcess** file in word.

<img src="./media/image43.png" style="width:6.5in;height:4.20556in"
alt="A screenshot of a computer Description automatically generated" />

13. Click on **Enable Content**. If you see an error, the action was
    blocked. If you see cmd.exe launch, it was not blocked.

<img src="./media/image44.png" style="width:6.5in;height:4.525in"
alt="A screenshot of a computer Description automatically generated" />

<img src="./media/image45.png" style="width:6.5in;height:3.91111in"
alt="A screenshot of a computer Description automatically generated" />

**Running Malicious Script**

**Note**: There are some malicious script that you need to execute to
get the alerts in Microsoft Defender portal. As these scripts are
malicious, the output of the command will not be the same. Sometimes the
script execute, sometimes it will be blocked and you may encounter an
error.

14. Right click inside the folder, then navigate and click on **Open in
    Terminal**.

> <img src="./media/image46.png" style="width:2.28333in;height:1.66667in"
> alt="Screenshot" />

15. Type [**ls**](urn:gd:lg:a:send-vm-keys) to get the list of the
    scripts in the folder. Then, execute the following script:

> +++[**./SQLDumper.exe**](urn:gd:lg:a:send-vm-keys)+++
>
> <img src="./media/image47.png"
> style="width:6.26806in;height:3.69514in" />

16. Run the following command:

> +++[**.\wdtestfile.exe**](urn:gd:lg:a:send-vm-keys)+++
>
> <img src="./media/image48.png"
> style="width:6.26806in;height:3.78819in" />

17. After the command successfully executed, press the **Enter** button.

> <img src="./media/image49.png" style="width:6.26806in;height:3.92986in"
> alt="A screenshot of a computer Description automatically generated" />

**Note**: Alerts generated will be started within 15-30 minutes in
Microsoft Defender Portal.

## **Task 3: Performing a ransomware attack using RanSim**

RanSim is a ransomware simulation script written in PowerShell. It
recursively encrypts files in the target directory using 256-bit AES
encryption. RanSim has no self-spreading capabilities and will only run
on the system you execute it on.

1.  Download the RanSim folder in testvm1 using the following script:

**git clone https://github.com/lawndoc/RanSim.git**

<img src="./media/image50.png" style="width:6.5in;height:2.42153in" />

2.  In testvm1 search bar, type +++**environment variables**+++, then
    navigate and click on **Edit environment variables for your
    account** as shown in the below image.

<img src="./media/image51.png" style="width:6.5in;height:6.47361in" />

3.  In the **System Properties** dialog box, navigate and click on
    **Environment Variables** button.

<img src="./media/image52.png" style="width:4.55232in;height:4.77744in"
alt="A screenshot of a computer program Description automatically generated" />

4.  In the **Environment Variables** dialog box, click on the **New**
    button.

<img src="./media/image53.png"
style="width:5.88634in;height:6.4783in" />

6.  In the next steps, you will be setting the following Parameters:

    - TargetPath : **C:\RanSim**

    - Extension : **.encrypted**

    - Key : **Q5KyUru6wn82hlY9k8xUjJOPIC9da41jgRkpt21jo2L=**

    - TargetFiles : .pdf .xls\* .ppt\* .doc\* .accd\* .rtf .txt .csv
      .jpg .jpeg .png .gif .avi .midi .mov mp3 .mp4 .mpeg .mpeg2 .mpeg3
      .mpg .ogg

7.  On the **New User Variable** dialog box, in the **Variable
    name** field, enter +++**TargetPath+++**, and in the **Variable
    value** field,
    enter +++**[C:\RanSim](urn:gd:lg:a:send-vm-keys)+++**, then press
    the **OK** button.

<img src="./media/image54.png"
style="width:6.26806in;height:1.56528in" />

8.  **TargetPath** variable is successfully added. Now, click on
    the **New** button as shown in the below image.

<img src="./media/image55.png"
style="width:4.82347in;height:4.56001in" />

8.  On the **New User Variable** dialog box, in the **Variable
    name** field, enter +++**[Extension](urn:gd:lg:a:send-vm-keys)+++**,
    and in the **Variable value** field,
    enter +++**[.encrypted](urn:gd:lg:a:send-vm-keys)+++**. Then, click
    on the **OK** button.

<img src="./media/image56.png"
style="width:6.26806in;height:1.59792in" />

9.  **Extension** variable is successfully added. Now, click on
    the **New** button as shown in the below image.

<img src="./media/image57.png" style="width:4.76631in;height:4.44736in"
alt="A screenshot of a computer Description automatically generated" />

10. On the **New User Variable** dialog box, in the **Variable
    name** field, enter +++**[Key](urn:gd:lg:a:send-vm-keys)+++**, and
    in the **Variable value** field,
    enter +++[**Q5KyUru6wn82hlY9k8xUjJOPIC9da41jgRkpt21jo2L=**](urn:gd:lg:a:send-vm-keys)+++
    Then, click on the **OK** button.

<img src="./media/image58.png"
style="width:6.26806in;height:1.54792in" />

11. **Key** variable is successfully added. Now, click on
    the **New** button as shown in the below image.

<img src="./media/image59.png"
style="width:4.17824in;height:3.98104in" />

12. On the **New User Variable** dialog box, in the **Variable
    name** field, enter +++**TargetFiles**+++, and in the **Variable
    value** field, enter

+++.pdf .xls\* .ppt\* .doc\* .accd\* .rtf .txt .csv .jpg .jpeg .png .gif
.avi .midi .mov mp3 .mp4 .mpeg .mpeg2 .mpeg3 .mpg .ogg+++

Then, click on the **OK** button.

<img src="./media/image60.png" style="width:6.26806in;height:1.6in" />

13. **TargetFiles** variable is successfully added. Close
    the **Environment Variables** dialog box.

<img src="./media/image61.png" style="width:4.01184in;height:3.77716in"
alt="A screenshot of a computer Description automatically generated" />

5.  In **testvm1** virtual machine, navigate to **C:\Users\Admin5802\\**
    and copy the **RanSim** folder, then paste the folder in **C:\\**

6.  Open **RanSim** folder. Click anywhere inside the folder, then right
    click and select **Open in terminal**.

**Note:** Please ensure that your RanSim folder is in C:\\

<img src="./media/image62.png" style="width:6.5in;height:4.47569in"
alt="A screenshot of a computer Description automatically generated" />

7.  In the command prompt, execute the following command to initiate a
    ransomware attack. In case, the attack failed to execute
    successfully and showed an error, then ignore and move on to the
    next step.

**.\RanSim.ps1 -Mode encrypt**

<img src="./media/image63.png" style="width:6.5in;height:3.12708in"
alt="A screenshot of a computer Description automatically generated" />

<img src="./media/image64.png"
style="width:5.5709in;height:3.11318in" />

**Task 4: Checking protection action and recommendations from Windows
Security**

1.  In **testvm1** search bar, type **virus and threat protection**,
    then navigate and click on **Virus & threat protection** under
    **Best match** as shown in the below image.

<img src="./media/image65.png" style="width:6.5in;height:5.49583in" />

2.  In **Virus & threat protection** page, under **Current threats**
    section, navigate and click on **Protection history**.

<img src="./media/image66.png" style="width:6.5in;height:3.66111in"
alt="A screenshot of a computer Description automatically generated" />

3.  You can see the protection action and recommendations from Windows
    Security.

<img src="./media/image67.png" style="width:6.5in;height:4.26319in" />

4.  Click on **Threat quarantined** to view the details.

<img src="./media/image68.png" style="width:6.5in;height:4.37569in" />

5.  Similarly, click on **Threat blocked** to view the details.

<img src="./media/image69.png" style="width:6.5in;height:3.84028in" />

**Summary**

In this lab, you've installed and configured Git on testvm1. You've also
executed malicious documents and scripts. Then, you've simulated a
ransomware attack using RanSim. Then, you've checked the protection
actions and recommendations from Windows Security, examining details of
quarantined and blocked threats. All these activities will create a
multi-stage incident, which will be analyzed in the upcoming labs using
Microsoft Copilot for Security.
