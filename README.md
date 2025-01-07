# IT Helpdesk L1 Technical Issue Resolution: Emails Not Sending or Receiving

## Issue Overview
This document provides a step-by-step guide, similar to a video tutorial, on how I resolved the issue of users being unable to send or receive emails in an organization's email system. The issue was affecting multiple users, and the solution addresses common causes for this problem. You can follow along with the video to see the troubleshooting process in action.

## Steps Taken to Resolve the Issue

### Step 1: Verify Network Connectivity
- **Ping google.com:** To ensure the user's device has an active internet connection, I used the `ping google.com` command in the terminal. A successful ping confirms that the device is connected to the internet and can reach external servers.
- **Check for firewall or DNS issues:** If the ping fails, there may be network-related issues such as firewall or DNS misconfigurations. Troubleshoot these problems by checking network settings or contacting the network administrator.

### Step 2: Check "Send and Receive" Settings and "Work Offline" Mode
- **Check Send/Receive settings:** Open the email client (e.g., Outlook) and go to the **Send/Receive** tab. Make sure that the "Send/Receive All Folders" option is enabled. This ensures that the client is attempting to send and receive emails.
- **Disable Work Offline mode:** Ensure the "Work Offline" option is not enabled in the email client. This mode prevents the email client from connecting to the mail server, causing issues with sending and receiving emails. If it is enabled, disable it to restore connectivity.

### Step 3: Repair Outlook via Control Panel
- **Open Control Panel:** Go to the **Control Panel** on the user’s computer.
- **Select Programs and Features:** Click on **Programs** and then **Programs and Features**.
- **Repair Outlook:** Find **Microsoft Office** in the list of installed programs, right-click on it, and select **Change**. Choose the **Repair** option and follow the on-screen instructions to fix any issues with Outlook. This will repair any broken or corrupted files in the Outlook installation, which can resolve issues with email sending or receiving.

### Step 4: Run the `scanpst.exe` Tool
- **Locate the `scanpst.exe` Tool:** The `scanpst.exe` file is the Inbox Repair Tool provided by Microsoft. It is used to repair corrupted Outlook PST (Personal Storage Table) files. You can find it in the following directory on a Windows machine:
  - For Outlook 2016/2019/Office 365: `C:\Program Files (x86)\Microsoft Office\root\OfficeXX`
  - For older versions of Outlook: `C:\Program Files\Microsoft Office\OfficeXX`
- **Run `scanpst.exe`:** Double-click on the `scanpst.exe` file to launch the tool. When prompted, browse to the location of the corrupted PST file (usually found in `C:\Users\[Your Username]\Documents\Outlook Files`), and click **Start** to begin scanning.
- **Repair PST File:** If the scan detects errors, click **Repair** to fix the corrupted PST file. After the process is complete, reopen Outlook and check if the issue is resolved.

### Step 5: Create a New Outlook Profile
- **Open Control Panel:** Navigate to the **Control Panel** on the user's computer.
- **Access Mail Settings:** Click on **Mail (Microsoft Outlook)** to open the mail setup window.
- **Create New Profile:** In the Mail Setup window, click **Show Profiles**, then click **Add** to create a new profile.
- **Configure the New Profile:** Enter a name for the new profile and follow the prompts to set up the email account (e.g., Outlook or Microsoft 365). Ensure that the correct email settings are applied.
- **Set as Default:** Once the new profile is created, set it as the default profile. This can be done by selecting **Always use this profile** and choosing the newly created profile from the dropdown list.
- **Test the New Profile:** Open Outlook with the new profile and check if the email sending/receiving issue is resolved.

### Step 6: Run Outlook in Safe Mode and Disable Add-ins
- **Run Outlook in Safe Mode:** To start Outlook in Safe Mode, press **Ctrl** while launching Outlook or type `outlook.exe /safe` in the Run dialog (Win+R). This disables all add-ins and customizations that might be causing the issue.
- **Disable Add-ins:** If the issue is resolved in Safe Mode, the problem may be due to an add-in. To disable add-ins:
  - Go to the **File** tab and click **Options**.
  - In the **Outlook Options** window, select **Add-ins**.
  - At the bottom of the window, select **Go** next to Manage: COM Add-ins.
  - Uncheck all add-ins and click **OK**.
  - Restart Outlook to see if the issue is resolved. If it is, enable add-ins one at a time to identify the problematic one.

## Conclusion
By following these easy steps, I was able to resolve the issue of emails not sending or receiving for the affected user. Regular monitoring and maintenance of email configurations can help prevent similar issues in the future.

## Tools Used
- **Microsoft Outlook**
- **CMD (Command Prompt)**
- **Inbox Repair Tool (`scanpst.exe`)**
- **Hyper-V for VM Management**
