HR-ASSIST Agentic AI System
HR-ASSIST is an intelligent agentic AI system designed to streamline and automate routine Human Resources workflows. Acting as a central assistant, it manages tasks such as employee leave requests, meeting scheduling, new employee onboarding, and automated email communication. This example specifically demonstrates the automation of the employee onboarding process, which typically requires manual intervention.

🌟 Key Features
Leave Management: Employees can request leave through the chatbot. HR can review and approve/deny requests, while the system tracks and displays an employee's leave history, including the total number of leaves and specific dates.

Meeting Scheduling: A dedicated function allows users to schedule meetings efficiently.

New Employee Onboarding: The chatbot collects information from new employees, automatically generates their profiles, and stores details in the database, automating a key part of the onboarding process.

Automated Email Communication: HR can provide an email address and a topic, and the agent will automatically draft and send a professional email to the specified recipient.

Ticket/Request Management: Employees or managers can raise a ticket for technical support or to request new hardware like a keyboard or a mouse.

🛠️ Technical Architecture
For the MCP client, we use Claude Desktop, and this codebase represents the MCP server with the necessary tools used by the client.

⚙️ Setup and Configuration
Clone the Repository:

git clone [https://your-repository-url.git](https://your-repository-url.git)
cd atliq-hr-assist

Configure claude_desktop_config.json:
Add the following configuration to your claude_desktop_config.json file.

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

Replace YOUR_EMAIL with your actual email.

Replace YOUR_APP_PASSWORD with your email provider’s app-specific password (e.g., for Gmail).

Create .env File:
Create a new file named .env in the root directory to securely store your email credentials. Use the provided .env.example as a template.

Configure Email Credentials:
Open the .env file and add your email and an app-specific password. If you are using Gmail, you will need to generate a new App Password from your Google Account settings.

# Example .env file content
EMAIL_USER=your_email@example.com
EMAIL_PASS=your_app_password

Install Dependencies:
Make sure you have uv installed. If not, you can install it using pip install uv. Then run the following commands to install the project's dependencies:

uv init
uv add mcp[cli]
# Add any other project-specific dependencies here

🚀 Usage
The system is designed to be interacted with via the Claude Desktop client.

Launch the Agent: Ensure your claude_desktop_config.json is correctly set up, then launch the Claude Desktop application.

Interact with the Agent: Click on the + icon and select the Add from hr-assist option to send a request. You can then use a form or draft a custom prompt for tasks like:

Add New Employee: Fill details in the provided form.

Leave Request: "I would like to request leave for two days, from 2025-10-25 to 2025-10-26."

Check Leave History: "What is the leave history for employee ID employee_id?"

Schedule a Meeting: "Schedule a team meeting for project ABC on Friday at 3:00 PM."

Raise a Ticket: "My mouse is not working; I need a new one." or "I am having a technical issue with my system."

Onboard New Employee: "Onboard a new employee named Jane Doe. Her email is jane.doe@example.com and she starts on 2025-11-01."

Send an Email: "Write and send an email to a.jones@example.com with the subject 'Project Update' and the body 'The project is on track and will be completed by the deadline.'"

🖼️ Illustrative Workflows
You can add your images here to demonstrate the workflows visually.

Add Employee Workflow
Raise Ticket Workflow

**Usage**
- Click on the `+` icon and select the `Add from hr-assist` option, and send the request.
- Fill the details for the new employee:

<img src="resources\image.jpg" alt="Claude desktop prompt with fields" style="width:auto;height:300px;padding-left:30px">

Alternatively, you can draft a custom prompt and let the agent take over.


