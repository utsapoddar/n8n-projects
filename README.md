# n8n Workflows Repository

This repository contains **exported JSON definitions** of workflows created with [n8n](https://n8n.io/), an open-source workflow automation tool. These flows can be imported into your own n8n instance to explore or build upon.

## Contents

| File | Description |
|---|---|
| `discord-ai-agent-workflow.json` | Connects to a Discord server, retrieves messages and events, and processes them through AI-powered nodes using the **Google Gemini Chat Model** and an **AI Agent** with memory and structured output parsing. Requires a Discord Bot API token. |
| `daily-scheduled-workflow.json` | A scheduled variant that runs daily at 20:00, performing similar AI-powered message analysis. Can serve as a starting point for scheduled automation tasks. |

## Using these workflows

1. **Run an n8n instance.** You can self-host or sign up for the cloud version. See the [n8n documentation](https://docs.n8n.io/) for installation instructions.
2. **Import a workflow:**
   - In the n8n editor, click the hamburger menu and choose **Import**.
   - Choose "Import from file" and select one of the JSON files from this repository.
3. **Configure credentials:**
   - The workflows reference a **Discord Bot API** credential. After import, create a new credential with your own bot token and assign it to the node.
   - If you use AI nodes (e.g., Google Gemini), ensure you have configured the appropriate API keys under *Settings > API credentials*.
4. **Activate and test:** Once credentials are configured, click **Execute Workflow** to test it. Adjust channel IDs or other parameters as needed.

## License

This project is licensed under the [MIT License](LICENSE).
