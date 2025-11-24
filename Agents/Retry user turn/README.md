# Copilot Studio: AI Response Retry with Adaptive Card

This feature introduces a **Retry** option for AI responses in Copilot Studio using an **adaptive card** and custom topics. It improves user experience by allowing them to retry a previous request without retyping their prompt.

---

## 📎 Topics Included in This Folder

1. **AI Response Generated** – Triggered before the orchestrator sends a composed message.
   - Displays an **adaptive card** containing a retry button (technically an image).
2. **Retry Event** – Triggered only when the retry button is clicked.
   - Handles the retry logic and passes dynamic instructions to the orchestrator.

Both topic YAML files are included in this folder:
- [`ai-response-generated.yaml`](https://github.com/hisandeepangara/CopilotStudioSnippets/blob/main/Agents/Retry%20user%20turn/ai-response-generated.yaml)
- [`retry-event.yaml`](https://github.com/hisandeepangara/CopilotStudioSnippets/blob/main/Agents/Retry%20user%20turn/retry-event.yaml)

---

## 🔍 How It Works

### 1. Adaptive Card in AI Response Generated Topic
- This topic fires **before** the orchestrator sends the composed message.
- The adaptive card includes a **retry button** (implemented as an image).
- The card is displayed alongside the AI response.

### 2. Retry Button Behavior
- When the user clicks **Retry**, the card’s `Submit` action sends a payload.
- The `data` property carries:
  - **User prompt**
  - **Agent response**
- This invokes the **Retry Event** topic.

### 3. Retry Event Topic
- Triggered only when the retry button is clicked.
- Uses **Recognize Intent** action to pass a dynamic instruction
- This dynamic instruction guides the orchestrator to regenerate the response.
- You can customize this message as needed for better context.

---
