# Installing RADPrint

This guide explains how to install the **RADPrint** APEX plugin into your Oracle APEX application.

---

## Installation

1. **Clone the repository**

`git clone https://github.com/RADAPEX/RADPrint.git`

2. **Locate the SQL file**

Inside the repository, find the plugin installation file (e.g., radprint.sql).

3. **Log in to Oracle APEX**

Open your APEX workspace in your browser.

Navigate to the application where you want to install the plugin.

4. **Install the plugin**

Go to Shared Components → Plugins.

Click Import.

Drag and drop the radprint.sql file (or use the file picker).

Follow the wizard steps and click Install.

5. **Verify installation**

After installation, RADPrint will appear under Shared Components → Plugins.

You can now add it to your application pages.

## Updating RADPrint 

To update to the newest version:

1. Get the latest install file via **git pull**
2. In APEX, go to **Shared components -> Plugins -> RADPrint -> Replace**
3. Upload the new sql file