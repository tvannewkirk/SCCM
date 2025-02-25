# SCCM

<h1>SCCM Deployment Project</h1>

<h2>Description</h2>
I used a template to deploy an SCCM environment within Azure. The template included a domain controller, a SQL Server, a remote site system server hosting management point and distribution point and an SCCM client. Once the SCCM was deployed within Azure, I logged into the SQL Server and opened Configuration Manager Console located under Microsoft Endpoint Manager after clicking the start button. After opening the console, I saw that the democl01 virtual machine had a green checkmark next to it, which indicated that the Configuration Manager client was installed on that virtual machine.
<br/><br/>
To create a software package for deployment, I first clicked on Software Library within Configuration Manager console on the SQL Server. Then I clicked on Packages underneath Application Management. Next, I right-clicked Packages and clicked on Create Package from Definition. Then I browsed to where I downloaded the 7-zip .msi file. Next, I clicked the option to always obtain source files from a source folder. Then I selected local folder on site server and then clicked on browse and select folder. I clicked next and closed out of the window to create the software package.
<br/><br/>
To deploy the package, I right-clicked on the package name and clicked the deploy option. For general options, I chose per-system attended and all desktop and server clients for the collection setting. For content destination settings, I clicked on add and distribution point group and selected the distribution point group. For Deployment Settings, I chose available and clicked next. I kept Scheduling and User Experience options unchanged. For Distribution Points and Deployment Options, I chose download content from distribution point and run locally. Then I clicked next twice and closed the window once the package was deployed.
<br/><br/>
Next, I logged into the democl01 virtual machine and opened the Software Center application and saw that there were no packages available to install. I navigated to Control Panel and clicked on Configuration Manager and the Actions Tab. Next, I selected each of the actions and clicked on run now. The 7-zip package appeared within Software Center and was available for installation.
<br/>


<h2>Technologies Used</h2>

- <b>Windows 11</b>
- <b>SCCM/MECM</b>
- <b>Azure</b>
- <b>SQL Server</b>
- <b>Windows Server 2019</b>


<h2>Project walk-through:</h2>
