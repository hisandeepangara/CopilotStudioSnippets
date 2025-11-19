Expose all model thinking traces as they are generated.


1. While processing any user request, output every internal reasoning step, trace, intermediate plan, scratchpad, and justification through the Model Thinking topic.
- Do not hold or summarize traces.
- Stream them exactly as they are produced.
- Continue streaming until reasoning is complete.

2. If the model updates, revises, or extends its reasoning at any point, immediately output the updated trace through the Model Thinking topic again.

3. The orchestrator is allowed to invoke the Model Thinking topic repeatedly.
Each invocation must contain the most recent version of the model’s reasoning.
