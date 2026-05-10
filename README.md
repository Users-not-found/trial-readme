# PROJECT NAME: MyLocalBot Sync Engine
### VERSION: 11.2 (Stable)
### DESCRIPTION: A local-first Telegram message synchronization tool with a web dashboard, deep history integrity mapping, and nickname management.

---

### 📂 1. PROJECT STRUCTURE

```
MyLocalBot_Project/
│
├── main.py                		# Core Logic, Sync Engine & Web Dashboard
├── .env                   		# Configuration & API Credentials (HIDDEN FILE)
├── requirements.txt       		# List of Python dependencies
├── README.txt             		# This setup guide
│
└── session_data/          		# Persistence Folder (DO NOT DELETE CONTENT){will be automatically created on first setup}
    ├── jarvis_user.session 		# Telegram login session (Delete if IP changes)
    ├── web_labels.json     		# Custom nicknames/labels
    ├── bot_state.json      		# Last synced message IDs
    ├── integrity_map.json  		# Sync gap tracking data
    ├── paused_groups.json   		# State of paused/resumed groups
    └── forwarding_history.log 		# Full activity log (Main Log Book)

```

### ⚙️ 2. PREREQUISITES

* Python 3.10 or higher installed on your system.
* A Telegram account to generate API credentials.
* VS Code (Recommended) for local development.

---

### 🛠️ 3. SETUP & INSTALLATION

Step A: Virtual Environment (VENV) Setup

Open your terminal (PowerShell or CMD) in the project folder and run:

 1. Create the environment:
    ```python -m venv venv```
    
 3. Activate it:
  * Windows: ```.\venv\Scripts\activate```
  * Mac/Linux: ```source venv/bin/activate```

Step B: Dependency Installation

Once the `(venv)` tag appears in your terminal, run:
  `pip install -r requirements.txt`

---

🔑 4. .ENV CUSTOMIZATION

Create a file named `.env` in the root folder and paste the following:

API_ID=your_api_id_here
API_HASH=your_api_hash_here
DEST_CHAT=
SOURCE_CHATS=

```

API_ID/HASH: Get these from [https://my.telegram.org](https://my.telegram.org) under "API Development Tools".
DEST_CHAT: The ID of the group/channel where messages will be sent.{u can get this from the this app's website itself }
SOURCE_CHATS: Comma-separated list of IDs you want to sync FROM.{u can get this from the this app's website itself }

---

🚀 5. RUNNING THE APP

 1. Start the bot:
  `python main.py`
 2. **First Run Only:** The terminal will ask for your Phone Number and the Code sent to your Telegram app.
 3. Once the terminal says `Application startup complete`, open your browser to:
  `http://127.0.0.1:8000`

---

🖥️ 6. DASHBOARD CONTROLS

* Start/Stop Sync: Global toggle for the background engine.
* Update Chat List: Rescans Telegram to find new groups/names.
* Nickname Manager: Set custom names for IDs. Use "OG Name" to reset.
* Load Older: Fetches 100 more lines from the log book.
* Clear View: Hides current logs from the UI (does NOT delete the log file).
* Click-to-Copy: Click any Group Name or ID to copy it to your clipboard.

---

🆘 7. TROUBLESHOOTING

* AuthKeyDuplicatedError: This happens if your IP changes or the session is used elsewhere. Delete `session_data/jarvis_user.session` and restart to log in fresh.
* Missing Imports: Ensure you have selected the correct Python Interpreter in VS Code (Ctrl+Shift+P -> Select Interpreter -> venv).
* UI Lag: If you have 100k+ logs, click "Clear View" to keep the browser responsive.

---

📜 LICENSE

Distributed under the MIT License. Created for local-first, privacy-focused message archiving.
