# Product Management Agent

This workspace contains a custom VS Code Copilot agent designed to act as a conversational Product Management coworker. The agent supports discovery, problem definition, product alignment, and outputs artifacts in both Markdown and JSON.

## Files
- `.copilot-instructions.md` — workspace-level Copilot behavior guidance
- `product-management-agent.agent.md` — agent persona, responsibilities, and behavior rules
- `product-management-agent.prompt.md` — prompt definitions, framework guidance, artifact templates, and use instructions
- `sample-conversation.md` — example conversation flow for using the agent

## Agent capabilities
- Ask clarifying questions before recommending direction
- Recommend product frameworks based on discovery stage
- Generate artifacts:
  - Problem statements
  - User stories formatted for coding-agent handoff
  - Opportunity maps
  - Benefit alignment summaries
- Provide artifacts in both Markdown and JSON
- Persist workspace-specific product context across sessions

## How to use
1. Open the workspace in VS Code.
2. Start a Copilot chat and select or invoke the Product Management Agent.
   - If you have a Copilot Chat pane, choose the agent from the agent selector.
   - If prompted, type a direct request such as: `Use the Product Management Agent to help me discover a new feature.`
3. Describe your product problem, customer segment, or discovery need.
4. Ask the agent for a framework recommendation, a problem statement, a user story, or an opportunity map.

## Best practice
- Provide as much context as possible up front: user type, pain points, current workflow, and product goals.
- Let the agent ask follow-up questions before moving to solution ideas.
- Use the JSON artifact outputs for automated handoff to engineering or coding agents.
