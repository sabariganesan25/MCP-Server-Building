<h1 align="center">✨ MCP Weather Server</h1>

<p align="center">
  A lightweight MCP server built with <b>Python</b> and <b>FastMCP</b>, providing<br/>
  weather alerts and forecasts via the National Weather Service API.
</p>

---

## 🛠️ 1. Project Setup

### ✔️ Step 1 — Install `uv`

```powershell
powershell -ExecutionPolicy Bypass -Command "irm https://astral.sh/uv/install.ps1 | iex"
```
✔️ Step 2 — Create and Set Up the Project
```bash
Copy code
uv init weather
cd weather
uv venv
.\.venv\Scripts\Activate.ps1
uv add "mcp[cli]" httpx
```
✔️ Step 3 — Add the MCP Server Code
Create a file named weather.py (or main.py if you prefer) and paste your MCP weather server implementation.

✔️ Step 4 — Run the Server
bash
Copy code
uv run weather.py
If the server stays active without errors, it is running correctly ✅.

💬 2. Configure Claude for Desktop
Open the Claude config file:

text
Copy code
%APPDATA%\Claude\claude_desktop_config.json
Add (or merge) the following configuration:

json
Copy code
{
  "mcpServers": {
    "weather": {
      "command": "uv",
      "args": [
        "--directory",
        "D:/Build-mcp/weather",
        "run",
        "weather.py"
      ]
    }
  }
}
🔁 After saving, restart Claude Desktop so it picks up the new MCP server.

🔍 3. Testing the Server
When everything is wired correctly, Claude should show these tools:

get_alerts

get_forecast

Example Queries
You can ask Claude things like:

What are the active weather alerts in Texas?

Give the forecast for 38.5816, -121.4944

If Claude responds using the tools (you’ll see tool calls in the UI), your MCP server is working as expected 🎉.

📸 4. Screenshots
<img width="1919" height="1016" alt="Screenshot 2025-11-17 134458" src="https://github.com/user-attachments/assets/61628e95-e597-4839-a823-2e3f2a2acb88" />
<img width="1914" height="1012" alt="Screenshot 2025-11-17 134640" src="https://github.com/user-attachments/assets/7f61028c-acbc-4559-9728-745c7d11e1e4" />
<img width="1912" height="1018" alt="Screenshot 2025-11-17 134725" src="https://github.com/user-attachments/assets/c1635fe2-4831-42ef-97ff-b05be97888cf" />






📌 5. Status
✅ MCP Weather Server Created

✅ Connected to Claude Desktop

✅ Tools Tested (get_alerts, get_forecast)

✅ Screenshots Added

📂 Tech Stack
🐍 Python

⚙️ FastMCP / MCP CLI

⛅ National Weather Service API

💻 Claude Desktop (MCP client)
