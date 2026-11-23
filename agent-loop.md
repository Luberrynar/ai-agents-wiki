# The agent loop
**Summary:** An agent works in a repeating cycle: think or plan, act with a tool, look at the result, and repeat until the goal is reached or a limit stops it.
**Key points:**
- Anthropic says agents are typically LLMs using tools based on feedback from their environment in a loop. (Source: source-02)
- At each step the agent should get real results from the environment, such as tool call output or code execution, to judge its progress. (Source: source-02)
- Agents can pause for human feedback at checkpoints or when blocked, and can have stopping conditions such as a maximum number of iterations. (Source: source-02)
- IBM describes three stages: goal initialization and planning, reasoning with available tools, and learning and reflection. (Source: source-03)
- In the ReAct approach the agent thinks and plans after every action and tool result; these Think-Act-Observe loops solve problems step by step. (Source: source-03)
- In the ReWOO approach the agent plans everything up front, so the user can confirm the plan and fewer tokens are used. (Source: source-03)
- Google lists observing, reasoning, planning, acting, collaborating and self-refining as key agent capabilities. (Source: source-04)
- Agents that cannot plan well or reflect may call the same tools repeatedly and get stuck in an infinite loop. (Source: source-03, source-01)
**Related pages:** [[tools]], [[memory-and-planning]], [[risks-and-limits]], [[index]]
**Sources:** source-01, source-02, source-03, source-04
**Open questions / conflicts:** None found between sources. Names differ (Think-Act-Observe in source-03, observe-reason-plan-act in source-04) but describe a similar cycle.
