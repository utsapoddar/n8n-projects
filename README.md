# n8n Workflows Repository

This repository contains **exported JSON definitions** of workflows created with [n8n](https://n8n.io/), an open‑source workflow automation tool. These flows are exported via the **“N8N Backup”** feature and can be imported into your own n8n instance to explore or build upon.

## Contents

| File | Description |
|---|---|
| `.json` | A workflow that connects to a Discord server, periodically retrieves messages and events, and pipes them through AI‑powered nodes. It uses the **Google Gemini Chat Model** and an **AI Agent** with a **Simple Memory** and **Structured Output Parser** to analyse incoming messages. Credentials for a **Discord Bot API** are referenced, so you will need to configure your own token when importing. |
| `=undefined.json` | A variant of the above workflow exported from n8n. It contains similar nodes (Discord message retrieval, AI Agent, output parsing) and can serve as a backup or alternative starting point. |

## Using these workflows

1. **Run an n8n instance.** You can self‑host or sign up for the cloud version. See the [n8n documentation](https://docs.n8n.io/) for installation instructions.
2. **Import a workflow:**
   - In the n8n editor, click the *hamburger menu* (☰) and choose **Import**.
   - Choose “Import from file” and select one of the JSON files from this repository.
3. **Configure credentials:**
   - The workflows reference a **Discord Bot API** credential. After import, n8n will highlight missing credentials. Create a new credential with your own bot token and assign it to the node.
   - If you use AI nodes (e.g., Google Gemini), ensure you have configured the appropriate API keys and credentials under *Settings → API credentials*.
4. **Activate and test:** Once credentials are configured, click **Execute Workflow** to test it. You may need to adjust channel IDs or other parameters in the node settings to match your environment.

## Notes

- These workflows demonstrate how to combine messaging platforms with generative‑AI models to automate responses or perform analysis. Use them as a template for your own bots or automation.
- The file names come directly from n8n’s export mechanism. Feel free to rename the JSON files for clarity after importing them.

## License

The workflows are shared under the MIT License. See the [LICENSE](LICENSE) file for details. When using third‑party APIs (Discord, Google Gemini, etc.), ensure you comply with their respective terms of service.
