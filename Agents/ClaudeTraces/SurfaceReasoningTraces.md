# Surface Reasoning Traces from Anthropic Models in Copilot Studio

## Anthropic Models in Copilot Studio
Copilot Studio now natively supports Anthropic’s benchmark models — **Claude Sonnet 4.5** and **Claude Opus 4.1**.  
These models are **disabled by default** and must be enabled by an administrator.

You can find the activation steps here:  
https://learn.microsoft.com/en-us/power-platform/admin/allow-llm-generative-responses

---

## Reasoning Traces
All large language models generate a hidden chain of reasoning before producing their final response.  
The depth and detail of this reasoning vary across models.

In Copilot Studio:

- **OpenAI models (e.g., GPT-5)** do *not* expose reasoning traces.  
- **Anthropic Claude models** *do* surface these traces, allowing you to view them directly.

This makes Claude models especially valuable for debugging, transparency, auditing, and educational use cases.

---

## Fastest Way to Try It
To explore this capability immediately:

1. Download the [**unmanaged solution**](https://github.com/hisandeepangara/CopilotStudioSnippets/blob/main/Agents/ClaudeTraces/ClaudeTraces_1_0_0_1.zip) containing the demo agent.  
2. Import it into your environment.  
3. Go to **Solutions → Agents → Stocks Agent**.

Inside the agent, you’ll find all custom topics and instructions showing how reasoning traces are surfaced.

---

## Copy Snippets into Your Own Agents
You can also choose to directly copy the **YAML snippets** ([Model Thinking.yaml](https://github.com/hisandeepangara/CopilotStudioSnippets/blob/main/Agents/ClaudeTraces/Model%20Thinking.yaml) and [AI response generated.yaml](https://github.com/hisandeepangara/CopilotStudioSnippets/blob/main/Agents/ClaudeTraces/AI%20response%20generated.yaml)) and [instructions](https://github.com/hisandeepangara/CopilotStudioSnippets/blob/main/Agents/ClaudeTraces/Instructions.md) into your own agents to replicate the functionality without importing the entire solution.
