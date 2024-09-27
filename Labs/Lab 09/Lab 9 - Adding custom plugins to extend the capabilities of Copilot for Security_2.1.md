**Lab 9: Adding custom plugins to extend the capabilities of Copilot for
Security**

**Introduction**

Copilot for Security comes with many default plugins and supports
several non-Microsoft plugins. You can also extend Copilot for
Security's capabilities by adding or creating your own plugin. The
Copilot for Security platform enables developers and users to write
plugins that can be invoked to perform specialized tasks.

**Objectives**

- To integrate a custom plugin into Microsoft Copilot for Security
  Standalone and utilize it to query geolocation information for a
  specified IP address.

**Task 1: Integrating a custom plugin and obtaining complete information
of a specific IP address**

1.  In Microsoft Copilot for Security Standalone, navigate and click on
    **Source** icon beside the prompt bar as shown in the below image.

> <img src="./media/image1.png"
> style="width:6.26806in;height:4.18681in" />

2.  Scroll down to Custom section and click on **Add plugin** as shown
    in the below image.

> <img src="./media/image2.png" style="width:6.26806in;height:3.59653in"
> alt="A screenshot of a computer Description automatically generated" />
>
> <img src="./media/image3.png"
> style="width:6.26806in;height:3.92708in" />

3.  In the **Add a plugin** page, navigate and click on **Copilot for
    Security plugin**.

<img src="./media/image4.png" style="width:6.26806in;height:3.97153in"
alt="A screenshot of a computer Description automatically generated" />

4.  Scroll down and click on **Upload file**.

<img src="./media/image5.png" style="width:6.26806in;height:5.07153in"
alt="A screenshot of a plugin Description automatically generated" />

5.  Navigate to **C:\Labfiles** and select **Geo.yaml** file.

<img src="./media/image6.png"
style="width:6.26806in;height:4.50208in" />

6.  Then, click on **Open** button.

<img src="./media/image7.png" style="width:6.26806in;height:4.96458in"
alt="A screenshot of a computer Description automatically generated" />

7.  After **Geo.yaml** file is successfully uploaded, click on the
    **Add** button.

<img src="./media/image8.png" style="width:6.26806in;height:3.99653in"
alt="A screenshot of a plugin Description automatically generated" />

8.  You will see that the customized plugin i.e., **IP Address
    Geolocation** is successfully added to Microsoft Copilot for
    Security Standalone.

<img src="./media/image9.png" style="width:6.26806in;height:3.85in"
alt="A screenshot of a computer Description automatically generated" />

9.  Go back to the prompt bar and enter the following prompt:

+++**Tell me the geolocation of ip 173.252.167.50?**+++

<img src="./media/image10.png" style="width:6.26806in;height:3.84444in"
alt="A screenshot of a computer Description automatically generated" />

10. You will get the complete information about the IP address city,
    region, country, latitudes and longitude coordinates, timezone,
    zipcode, etc.

<img src="./media/image11.png" style="width:6.26806in;height:3.61042in"
alt="A screenshot of a computer Description automatically generated" />

**Summary**

In this lab, you’ve learned how to add custom plugins to Microsoft
Copilot for Security. You’ve uploaded a Geo.yaml file and successfully
integrated the IP Address Geolocation plugin. Then, you’ve used a prompt
for a specific IP address and gained insights into its city, region,
country, coordinates, timezone, and zipcode, thereby enhancing your
proficiency in custom plugin integration and geolocation querying within
the Microsoft Copilot for Security environment.
