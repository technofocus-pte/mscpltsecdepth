**Lab 6-Copilot for Security – Microsoft Defender embedded copilot to
standalone copilot investigation**

**Introduction**

Copilot for Security is embedded in the Microsoft Defender portal to
enable security teams to efficiently summarize incidents, analyze
scripts and codes, analyze files, summarize device information, use
guided responses to resolve incidents, generate KQL queries, create
incident reports.

- **Investigate and respond to incidents like an expert**: Enable
  security teams to tackle attack investigations in a timely manner with
  ease and precision. Copilot helps teams to understand attacks
  immediately, quickly analyze suspicious files and scripts, and
  promptly assess and apply appropriate mitigation to stop and contain
  attacks.

- **Summarize incidents quickly**: Investigating incidents with multiple
  alerts can be a daunting task. To immediately understand an incident,
  you can tap Copilot to summarize an incident for you. Copilot creates
  an overview of the attack containing essential information for you to
  understand what transpired in the attack, what assets are involved,
  and the timeline of the attack. Copilot automatically creates a
  summary when you navigate to an incident's page.

**Objectives**

**Task 1: Investigate the Incident in Microsoft Defender embedded
copilot**

1.  In the Microsoft Defender portal, navigate and click
    on **Investigation & response**, then select **Incidents & alerts**,
    click on **Incidents**. In the **Incidents** page, navigate and
    click on the **Multi-stage incident involving Execution &
    Persistence on one endpoint**.

<img src="./media/image1.png" style="width:6.26806in;height:3.44028in"
alt="A screenshot of a computer Description automatically generated" />

2.  On the **Multi-stage incident involving Execution & Persistence on
    one endpoint** pane, Copilot for security automatically creates an
    **Incident summary**. Review the incident summary thoroughly.
    <img src="./media/image2.png" style="width:6.26806in;height:3.99028in"
    alt="A screenshot of a computer Description automatically generated" />

<img src="./media/image3.png" style="width:6.26806in;height:3.50278in"
alt="A screenshot of a computer Description automatically generated" />

<img src="./media/image4.png" style="width:6.26806in;height:3.625in"
alt="A screenshot of a computer Description automatically generated" />

### **Task 2: Analyze malicious scripts in embedded and standalone copilot for security**

Most attackers rely on sophisticated malware when launching attacks to
avoid detection and analysis. These malwares are usually obfuscated, and
might be in the form of scripts or command lines in PowerShell. Copilot
can quickly [analyze
scripts](https://learn.microsoft.com/en-us/defender-xdr/security-copilot-m365d-script-analysis),
reducing the time for investigation.

1\. In the **Incidents & alerts** page, navigate and click on
**Alerts**. Then, click on **Suspicious PowerShell download or encoded
command execution.**

<img src="./media/image5.png" style="width:6.26806in;height:3.77361in"
alt="A screenshot of a computer Description automatically generated" />

3.  Navigate to **powershell.exe** and click on the dropdown as shown in
    the below image.

<img src="./media/image6.png" style="width:6.26806in;height:3.4625in"
alt="A screenshot of a computer Description automatically generated" />

4.  Click on **Analyze**.

<img src="./media/image7.png" style="width:6.26806in;height:4.15208in"
alt="A screenshot of a computer Description automatically generated" />

5.  In **Copilot** pane, navigate and click on **Show code**, then
    review the code.

<img src="./media/image8.png" style="width:6.26806in;height:3.65486in"
alt="A screenshot of a computer Description automatically generated" />

<img src="./media/image9.png" style="width:6.26806in;height:3.85694in"
alt="A screenshot of a computer Description automatically generated" />

6.  Scroll up and click on the horizontal ellipsis, then navigate and
    click on **Open in Copilot for Security** to open the Standalone
    Copilot for Security.

<img src="./media/image10.png"
style="width:6.26806in;height:3.61528in" />

7.  Then, enter the following prompt - +++**[Provide the key findings of
    script analysis](urn:gd:lg:a:send-vm-keys)+++**

> <img src="./media/image11.png"
> style="width:6.26806in;height:3.86319in" />

8.  Carefully review the key findings of script analysis.

> <img src="./media/image12.png" style="width:6.26806in;height:3.85764in"
> alt="A screenshot of a computer Description automatically generated" />
>
> <img src="./media/image13.png" style="width:6.26806in;height:3.39028in"
> alt="A screenshot of a computer Description automatically generated" />

9.  In Microsoft Copilot for Security Standalone, enter the following
    prompt to obtain the summary of the incident.

+++**Provide me a summary of defender incident 5**+++

**Note**: Number \#5 represent the Incident ID, you may have a different
Incident ID. To know about your Incident ID, navigate to Microsoft
Defender portal, click on Incidents and you will find the Incident ID in
**Multi-stage incident involving Execution & Persistence on one
endpoint** row.

<img src="./media/image14.png" style="width:6.26806in;height:3.43403in"
alt="A screenshot of a computer Description automatically generated" />

<img src="./media/image15.png" style="width:6.26806in;height:4.12639in"
alt="A screenshot of a computer Description automatically generated" />

10. Carefully review the Incident summary.

<img src="./media/image16.png" style="width:6.26806in;height:3.57986in"
alt="A screenshot of a computer Description automatically generated" />

<img src="./media/image17.png" style="width:6.26806in;height:4.13542in"
alt="A screenshot of a computer Description automatically generated" />

<img src="./media/image18.png" style="width:6.26806in;height:3.48958in"
alt="A screenshot of a computer Description automatically generated" />

11. Then, enter the following prompt - +++**Extract the entities from
    script analysis**+++

<img src="./media/image19.png" style="width:6.26806in;height:4.12847in"
alt="A screenshot of a computer Description automatically generated" />

12. Carefully review the extracted entities from script analysis.

<img src="./media/image20.png" style="width:6.26806in;height:4.14236in"
alt="A screenshot of a computer Description automatically generated" />

13. Use the following prompt to generate a report about the incident.

+++**Write a report summarizing the incident**+++

<img src="./media/image21.png"
style="width:6.26806in;height:3.9625in" />

<img src="./media/image22.png" style="width:6.26806in;height:3.88194in"
alt="A screenshot of a computer Description automatically generated" />

<img src="./media/image23.png" style="width:6.26806in;height:3.85556in"
alt="A screenshot of a computer Description automatically generated" />

<img src="./media/image24.png" style="width:6.26806in;height:4.01389in"
alt="A screenshot of a computer Description automatically generated" />

<img src="./media/image25.png" style="width:6.26806in;height:3.95625in"
alt="A screenshot of a computer Description automatically generated" />

### Task 3: Analyze files promptly

Copilot helps security teams quickly assess and understand suspicious
files with file analysis. Copilot provides a file's summary, including
detection information, related file certificates, a list of API calls,
and strings found in the file.

1.  In Microsoft Defender portal, click on the **Incidents**, then click
    on **Multi-stage incident involving Execution & Persistence on one
    endpoint**.

<img src="./media/image26.png"
style="width:6.26806in;height:3.71875in" />

2.  Click on **Attack story** tab, then navigate to the Incident graph
    and select **Files**.

<img src="./media/image27.png" style="width:6.26806in;height:3.74236in"
alt="A screenshot of a computer Description automatically generated" />

3.  Right click on **Files** icon, then navigate and select **File
    details**. In case, you see **View 2 Files**, then select it.

> **Note**: The number of Files may vary.
>
> <img src="./media/image28.png" style="width:6.26806in;height:3.625in"
> alt="A screenshot of a computer Description automatically generated" />

4.  If there are more than one file, then navigate and click
    on **WinATP-Intro-Backdoor.exe**

5.  In the **WinATP-Intro-Backdoor.exe** pane, navigate and click on
    **Open file page**.

<img src="./media/image29.png" style="width:6.26806in;height:3.61667in"
alt="A screenshot of a computer Description automatically generated" />

6.  Review the **File analysis** information provided by Copilot for
    Security.

<img src="./media/image30.png"
style="width:6.26806in;height:3.44236in" />

### **Task 4: Generate device summaries**

Investigating devices involved in incidents can be a tasking job. To
quickly assess a device, Copilot can summarize a device's information,
including the device's security posture, any unusual behaviors, a list
of vulnerable software, and relevant Microsoft Intune information.

1\. Navigate and click on **Assets** and then click on **Devices**.

<img src="./media/image31.png" style="width:6.26806in;height:3.69028in"
alt="A screenshot of a computer Description automatically generated" />

2\. Select **testvm1**.

<img src="./media/image32.png" style="width:6.26806in;height:3.87569in"
alt="A screenshot of a computer Description automatically generated" />

3\. Copilot for security automatically provides **Device summary**.

<img src="./media/image33.png"
style="width:6.26806in;height:3.92569in" />

**Task 5: Microsoft Defender Incident Investigation using Copilot for
Security Promptbook Library**

1.  In Microsoft Copilot for Security Standalone, navigate and click on
    the three horizonal ellipsis, then click on **Promptbook library**.

<img src="./media/image34.png" style="width:6.26806in;height:5.05347in"
alt="A screenshot of a computer Description automatically generated" />

2.  In the Promptbook library page, select **Microsoft 365 Defender
    incident investigation**.

<img src="./media/image35.png" style="width:6.26806in;height:3.55069in"
alt="A screenshot of a computer Description automatically generated" />

3.  Go back to Microsoft Defender portal, click on **Incident &
    alerts**, then click on **Incident**. Note down the Incident ID
    mentioned beside the generated incident. You may have a different
    incident ID.

<img src="./media/image14.png" style="width:6.26806in;height:3.43403in"
alt="A screenshot of a computer Description automatically generated" />

4.  Go back to Microsoft Copilot for Security, click on **Start new
    sesssion** button, in the **Defender Incident ID** field, enter your
    incident ID (here, we entered 5, you may have different Incident ID)
    and click on the **Submit** button.

<img src="./media/image36.png" style="width:6.26806in;height:3.85278in"
alt="A screenshot of a computer Description automatically generated" />

<img src="./media/image37.png"
style="width:6.26806in;height:3.80556in" />

5.  Carefully review the Microsoft 365 Defender incident investigation
    report generated using the prompt library.

<img src="./media/image38.png" style="width:6.26806in;height:4.05in"
alt="A screenshot of a computer Description automatically generated" />

<img src="./media/image39.png" style="width:6.26806in;height:4.08819in"
alt="A screenshot of a computer Description automatically generated" />

<img src="./media/image40.png" style="width:6.26806in;height:3.78958in"
alt="A screenshot of a computer Description automatically generated" />

<img src="./media/image41.png" style="width:6.26806in;height:3.60764in"
alt="A screenshot of a computer Description automatically generated" />

**Summary**

In this lab, you've learned to leverage Microsoft Defender's embedded
and standalone Copilot for Security to investigate and analyze security
incidents. You've navigated to the Defender portal, investigated
multi-stage incidents, and used Copilot to generate incident summaries.
You've developed the skills in analyzing malicious scripts, particularly
obfuscated PowerShell commands, by reviewing key findings and generating
incident summaries. Additionally, you've learned to assess suspicious
files through detailed file analysis and quickly evaluated device
security postures, enhancing the overall incident response and security
investigation capabilities.
