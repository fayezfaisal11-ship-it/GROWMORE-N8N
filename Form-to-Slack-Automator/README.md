# ⏱️ Time-Sensitive Form Response Automator (n8n)

## 🚀 Overview

This project is an automated workflow built using n8n that processes incoming form submissions in real time. It evaluates each submission based on a 7-day time threshold and routes the data accordingly, ensuring that recent entries receive immediate attention via Slack notifications.

---

## ⚙️ Workflow Logic

### 🔹 Trigger

* Activates automatically when a new form submission is received.

### 🔹 Condition Check

* Evaluates whether the submission date falls within the last **7 days**.

### 🔹 True Path (Recent Submissions)

* Sends an automated message to a Slack channel.
* Ensures timely visibility and quick response to recent entries.

### 🔹 False Path (Older Submissions)

* Routes data to a placeholder node (`Todo`).
* Can be extended for:

  * Database storage
  * Email archiving
  * Reporting workflows

---

## 🛠️ Tech Stack

* **Automation:** n8n
* **Messaging:** Slack API
* **Logic:** Date-based filtering

---

## 📌 Use Cases

* Lead management systems
* Customer support intake filtering
* Time-sensitive form processing
* Business workflow automation

---

## 📂 Project Structure

```
workflow.json   # Main n8n workflow file
```

---

## ▶️ How to Use

1. Import the `workflow.json` file into your n8n instance
2. Connect your Slack account in the **Send Message** node
3. Map the correct date field from your form submission
4. Customize message content if needed
5. Activate the workflow

---

## ⚠️ Configuration Notes

* Ensure the date field format matches your condition logic
* Slack credentials must be authenticated before activation
* Test the workflow with sample data before going live

---

## 🔄 Current Status

* ⚠️ Slack node requires credential re-authentication
* 🛠️ False path (Todo node) is ready for future enhancements

---

## 🔒 Security Note

Sensitive credentials and personal data have been removed from this workflow before uploading.

---

## 💡 Future Improvements

* Add database integration for storing old submissions
* Implement email notifications for fallback cases
* Add logging and monitoring for workflow tracking
* Enhance filtering logic (e.g., priority-based routing)

---

## 🤝 Contributing

Feel free to fork this repository and improve the workflow. Contributions and suggestions are welcome.

---

## ⭐ Support

If you find this project useful, consider giving it a star!
