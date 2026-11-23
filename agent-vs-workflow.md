# Agent vs workflow vs chatbot
**Summary:** A workflow follows a path written in advance by a developer, while an agent decides its own steps. Both are called agentic systems, and simple chatbots without tools are neither.
**Key points:**
- Anthropic groups all variations as agentic systems but separates two kinds: workflows, where LLMs and tools follow predefined code paths, and agents, where the LLM directs its own process and tool use. (Source: source-02)
- Workflows give predictability and consistency for well-defined tasks; agents are better when flexibility and model-driven decisions are needed at scale. (Source: source-02)
- Anthropic advises finding the simplest solution first; agentic systems often trade speed and cost for better results, and one LLM call with retrieval and examples is often enough. (Source: source-02)
- Anthropic lists five workflow patterns: prompt chaining, routing, parallelization, orchestrator-workers and evaluator-optimizer. (Source: source-02)
- The Wikipedia article lists orchestration patterns for combining agents or tools: prompt chaining, routing, parallelization, sequential processing and planner-critic. (Source: source-01)
- IBM says non-agentic chatbots have no tools, memory or reasoning and need constant user input, while agentic chatbots can create subtasks and correct their own plans. (Source: source-03)
- Wikipedia contrasts agentic AI with tool-like AI used for narrow tasks such as answering questions, as in the non-agentic chatbots common in 2023. (Source: source-01)
**Related pages:** [[what-is-an-ai-agent]], [[agent-loop]], [[risks-and-limits]], [[index]]
**Sources:** source-01, source-02, source-03
**Open questions / conflicts:** Terminology differs. Source-01 treats prompt chaining and routing as orchestration patterns for agents, while source-02 calls them workflows and separates them from agents.
