### 🤖 HR-ASSIST Agentic AI System

Welcome to **HR-ASSIST**!  
This project is an **intelligent agentic AI system** designed to automate and streamline **Human Resources workflows**.  
It acts as a **central HR assistant**, capable of handling tasks like employee leave requests, meeting scheduling, new employee onboarding, and automated email communication.

This example highlights the **automation of the employee onboarding process**, which normally requires manual intervention.

-----

### Key Features ⚡️

HR-ASSIST can perform the following tasks:

* **📆 Leave Management:** Employees can request leave through the chatbot. HR can review and approve/deny requests, while the system keeps a complete leave history.
* **📅 Meeting Scheduling:** Schedule team or project meetings quickly and efficiently.
* **👥 New Employee Onboarding:** Collects information from new employees, generates their profiles automatically, and stores details in the database.
* **📧 Automated Email Communication:** Provide an email address and a topic, and the system drafts and sends a professional email.
* **🎫 Ticket/Request Management:** Raise support tickets or request hardware (like a keyboard or mouse) with ease.

-----

### Architecture 🏗️

HR-ASSIST is built using:
* **MCP Client:** Claude Desktop
* **MCP Server:** This codebase, which provides the tools for client interaction

This architecture enables seamless communication between the Claude Desktop client and the HR automation server.

-----

### Quick Start 🚀

Getting started is simple. Follow these steps to set up HR-ASSIST:

1. **Clone the Repository:**  
   ```bash
   [git clone https://your-repository-url.git
   cd atliq-hr-assist](https://github.com/OmThawaregitgub/Hr-assistant-manager-project)
   ```

2. **Configure `claude_desktop_config.json`:**  
   Add the following configuration:
   ```json
   {
     "mcpServers": {
       "hr-assist": {
         "command": "C:\\Users\\dhaval\\.local\\bin\\uv",
         "args": [
           "--directory",
           "C::\\code\\atliq-hr-assist",
           "run",
           "server.py"
         ],
         "env": {
           "CB_EMAIL": "YOUR_EMAIL",
           "CB_EMAIL_PWD": "YOUR_APP_PASSWORD"
         }
       }
     }
   }
   ```
   🔑 Replace:
   - `YOUR_EMAIL` → Your actual email
   - `YOUR_APP_PASSWORD` → Your email provider’s app-specific password (e.g., Gmail App Password)

3. **Create a `.env` File:**  
   Create a `.env` file in the root directory and add your email credentials:
   ```text
   EMAIL_USER=your_email@example.com
   EMAIL_PASS=your_app_password
   ```

4. **Install Dependencies:**  
   Make sure `uv` is installed. Then run:
   ```bash
   pip install uv
   uv init
   uv add mcp[cli]
   # Add any additional dependencies if required
   ```

-----

### Usage 💡

Interact with the HR-ASSIST system through **Claude Desktop**:

* Launch Claude Desktop after configuration.
* Click on **➕ Add from hr-assist** to send a request.
* Use prompts such as:
  * "Onboard a new employee named Jane Doe. Her email is jane.doe@example.com and she starts on 2025-11-01."
  * "Schedule a team meeting for project ABC on Friday at 3:00 PM."
  * "I would like to request leave for two days, from 2025-10-25 to 2025-10-26."
  * "Write and send an email to a.jones@example.com with the subject 'Project Update' and the body 'The project is on track and will be completed by the deadline.'"

-----

### Workflows 🖼️

Here’s an example workflow:

**Raise token image:**  
<img width="427" height="371" alt="Image" src="https://github.com/user-attachments/assets/5cca4fd7-e7cb-4135-8f70-76c9e4240f51" />

** Leave managment image **
<img width="458" height="325" alt="Image" src="https://github.com/user-attachments/assets/06ad0a73-c8fd-4ebc-8a00-9e6f8625b1c9" />


You can also add more images/screenshots in the `resources` folder to demonstrate additional workflows.

-----

### Copyright

© 2025 Om Thaware. All rights reserved.
