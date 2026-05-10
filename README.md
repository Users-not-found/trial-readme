🚀 TeleSync-Pro GitHub Setup
Project Name: TeleSync-Pro
Description: High-integrity Telegram synchronization engine with a real-time FastAPI dashboard and deep history mapping.

📄 README.md
Markdown
# TeleSync-Pro v11.2

TeleSync-Pro is a high-performance synchronization engine for Telegram, featuring a real-time web dashboard. It is engineered for 100% message integrity, using deep-mapping logic to ensure no data gaps during history backfills.

---

## 📂 1. PROJECT STRUCTURE

```text
TeleSync-Pro/
│
├── main.py                # Core Logic, Sync Engine & Web Dashboard
├── .env                   # Configuration & API Credentials (LOCAL ONLY)
├── requirements.txt       # Project dependencies
├── README.md              # Project documentation
│
└── session_data/          # Persistence Folder (Auto-generated)
    ├── jarvis_user.session # Telegram login session
    ├── web_labels.json     # Custom nicknames
    ├── bot_state.json      # Sync progress tracking
    ├── integrity_map.json  # Data gap coverage map
    ├── paused_groups.json  # State management
    └── forwarding_history.log # Main Activity Log
⚙️ 2. PREREQUISITES
Python 3.10+

Telegram API Credentials (my.telegram.org)

VS Code (Recommended)

🛠️ 3. SETUP & INSTALLATION
Step A: Virtual Environment (VENV)
Create the environment:
python -m venv venv

Activate it:

Windows: .\venv\Scripts\activate

Mac/Linux: source venv/bin/activate

Step B: Dependency Installation
Once (venv) is active, run:
pip install -r requirements.txt

🔑 4. .ENV CUSTOMIZATION
Create a .env file in the root folder:

Code snippet
API_ID=your_api_id
API_HASH=your_api_hash
DEST_CHAT=
SOURCE_CHATS=
API_ID/HASH: Obtain from my.telegram.org.

DEST_CHAT: ID of the destination group (obtainable via the dashboard).

SOURCE_CHATS: Comma-separated list of source IDs (obtainable via the dashboard).

🚀 5. RUNNING THE APP
Start the Bot:
python main.py

Authentication: On the first run, enter your Phone Number and the Code sent to your Telegram app.

Access Dashboard: Once startup is complete, open:
http://127.0.0.1:8000

🖥️ 6. DASHBOARD CONTROLS
Start/Stop Sync: Global engine toggle.

Update Chat List: Rescans Telegram for new groups and names.

Nickname Manager: Set custom labels for Chat IDs.

Load Older: Fetches 100 more entries from the log book.

Clear View: Hides session logs for a cleaner workspace.

Click-to-Copy: Click any Group Name or ID to copy to clipboard instantly.

🆘 7. TROUBLESHOOTING
AuthKeyDuplicatedError: Delete session_data/jarvis_user.session and re-authenticate.

Missing Imports: Ensure VS Code is using the venv interpreter (Ctrl+Shift+P).

UI Lag: For 100k+ logs, use Clear View to maintain responsiveness.

📜 LICENSE
Distributed under the MIT License.


---

### 🛡️ IMPORTANT: .gitignore
To make sure you don't leak your private API keys or your Telegram session to the public on GitHub, you **must** include this file.

Create a file named `.gitignore` and paste this:

```text
# Credentials
.env
*.session
*.session-journal

# Data & Logs
session_data/
forwarding_history.log

# System
venv/
__pycache__/
.vscode/
