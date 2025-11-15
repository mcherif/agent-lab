# Email Agent Demo

**What**: Build an end-to-end email-processing agent with the [`smolagents`](https://github.com/huggingface/smolagents) toolkit.

**Context**
- Based on the walkthrough "[AI Agent for Email Automation with smolagents](https://www.llmwatch.com/p/ai-agent-for-email-automation-with)".
- Original reference notebook: [Colab link](https://colab.research.google.com/drive/1SvveVaCZ__dxp9DYKKrDPN3PQYAmcJ78?usp=sharing).
- Enhancement here: added Slack webhook notifications.

**Environment variables to set before running**
- `HUGGINGFACEHUB_API_TOKEN`: Hub token for authentication.
- `SLACK_WEBHOOK_URL` (optional): for Slack notifications.
- Future Gmail integration: configure Google API client secrets/OAuth per your workflow.

**This notebook covers**
- Setup: install dependencies and authenticate to the [Hugging Face Hub](https://huggingface.co/docs/hub).
- Tools: calendar lookup, mock knowledge search, Slack notifications; `web_search` is a static placeholder.
- Agent: remote LLM-backed [`CodeAgent`](https://huggingface.co/docs/huggingface_hub/smolagents/index) with tuned prompt and policy templates.
- Usage: run on sample emails; can be extended to a real Gmail client via Google APIs/OAuth.

**Why smolagents**
- Validated tool schemas, prompt templates, and multi-step control with state.
- Built-in retries/error handling plus swappable remote or local backends.