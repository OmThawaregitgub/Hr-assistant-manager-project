
<div align="center">

╔════════════════════════════════════════════════════════════╗  
**🤖 HR-ASSIST Agentic AI System**  
╚════════════════════════════════════════════════════════════╝  

*An intelligent agentic AI system designed to streamline and automate routine **Human Resources** workflows.*  

</div>

---

### 📦 Overview
HR-ASSIST acts as a **central HR assistant**, managing:
```
🟢 Employee leave requests
🟢 Meeting scheduling
🟢 New employee onboarding
🟢 Automated email communication
```
This example highlights **employee onboarding automation**, reducing manual work.

---

### 🌟 Key Features
╔════════════════════════════════╗  
║ **Leave Management**: Request leave, HR approval, and leave history tracking.  
║ **Meeting Scheduling**: Quickly arrange team or project meetings.  
║ **New Employee Onboarding**: Auto-profile creation & database storage.  
║ **Automated Email**: Drafts & sends professional emails instantly.  
║ **Ticket Management**: Raise requests for IT support or hardware.  
╚════════════════════════════════╝  

---

### 🛠️ Technical Architecture
╔════════════════════════════════════════════╗  
║ **MCP Client**  → Claude Desktop           ║  
║ **MCP Server**  → This codebase & tools    ║  
╚════════════════════════════════════════════╝  

---

### ⚙️ Setup & Configuration
```
1️⃣ Clone Repository:
    git clone https://your-repository-url.git
    cd atliq-hr-assist

2️⃣ Configure claude_desktop_config.json:
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

3️⃣ Create .env File:
    EMAIL_USER=your_email@example.com
    EMAIL_PASS=your_app_password

4️⃣ Install Dependencies:
    pip install uv
    uv init
    uv add mcp[cli]
```

---

### 🚀 Usage
╔════════════════════════════════════════════════════════════╗  
║ Launch Claude Desktop → Configure → **Add from hr-assist** ║  
╚════════════════════════════════════════════════════════════╝  

Example Commands:
```
➕ Add New Employee:
    "Onboard a new employee named Jane Doe. Her email is jane.doe@example.com and she starts on 2025-11-01."

➕ Leave Request:
    "I would like to request leave for two days, from 2025-10-25 to 2025-10-26."

➕ Check Leave History:
    "What is the leave history for employee ID employee_id?"

➕ Schedule a Meeting:
    "Schedule a team meeting for project ABC on Friday at 3:00 PM."

➕ Raise a Ticket:
    "My mouse is not working; I need a new one."

➕ Send an Email:
    "Write and send an email to a.jones@example.com with the subject 'Project Update' and the body 'The project is on track and will be completed by the deadline.'"
```

---

### 🖼️ Illustrative Workflows
╔════════════════════════════╗  
║ 📂 Add Employee Workflow   ║  
║ 🔧 Raise Ticket Workflow   ║  
╚════════════════════════════╝  

Add images/screenshots in the `resources` folder to demonstrate workflows visually.

<img src="resources/image.jpg" alt="Claude Desktop Prompt" style="width:auto;height:300px;padding-left:30px">

---

<div align="center">

💡 **Tip:** Use diagrams and visuals to enhance presentation and improve clarity.

</div>
