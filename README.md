# 📢 LinkedIn Post Automation Workflow (n8n)

This n8n workflow automates the process of generating and posting professional LinkedIn content using AI.

---

## 💡 What It Does

1. **📝 Collect Input**: A form collects the LinkedIn post title from the user.
2. **🤖 AI Generation**: Gemini 2.0 Flash (Google AI) generates a well-formatted LinkedIn post.
3. **🧹 Cleanup**: A code block parses and cleans the AI output to extract valid JSON.
4. **🔗 Auto-Post**: The final content is posted directly to LinkedIn.

---

## 📂 Files Included

- `Cleaned_LinkedIn_Workflow.json`: The n8n workflow file with all credentials removed.
- `README.md`: This guide to understand and run the workflow.

---

## 🛠 Requirements

To use this workflow, you’ll need:

- n8n (self-hosted or cloud)
- A [LinkedIn App](https://www.linkedin.com/developers/) with OAuth2 set up
- A valid Gemini 2.0 Flash / Google PaLM API key
- Your own form trigger or webhook set up inside n8n

---

## 🔌 Setup Instructions

1. **Import the JSON File**
   - In n8n, click `Import Workflow` and upload `Cleaned_LinkedIn_Workflow.json`.

2. **Add Credentials**
   - Open the `LinkedIn` node → set up your **LinkedIn OAuth2** credentials.
   - Open the `Google Gemini Chat Model` node → add your **Google AI API key**.

3. **Customize Form Trigger**
   - The first node is a form with a single input: **Post Title**.
   - You can add more fields or connect it to a frontend webhook as needed.

4. **Activate the Workflow**
   - Turn the workflow **ON** in n8n.
   - Submit a test form and watch it post to LinkedIn automatically!

---

## 📌 Notes

- The workflow uses markdown (**bold**) and emojis to enhance LinkedIn post readability.
- Content is generated in JSON format like:
  ```json
  {
    "content": "Final post here"
  }
