# Tools and tool calling
**Summary:** Tools let an agent do things beyond writing text, such as searching the web, calling an API or running code. The model asks for a tool, the program runs it, and the result goes back to the model.
**Key points:**
- Tool use, also called function calling, lets the model call functions defined by the developer or the provider; the model decides when to call one based on the request and the tool's description. (Source: source-05)
- For client tools, the model replies that it wants a tool (a tool_use block); the application runs the tool and sends the result back in a tool_result block; the model then uses it to answer. (Source: source-05)
- Server tools, such as web search and web fetch, run on the provider's servers and need no implementation by the developer. (Source: source-05)
- A tool is defined by a name, a description and an input schema. (Source: source-05)
- Models may guess a missing parameter, for example inventing a location when asked for the weather without one. (Source: source-05)
- Tool use adds extra tokens (tool definitions, tool calls and results), which affects cost. (Source: source-05)
- IBM says agents use tool calling to get up-to-date information; tools include external datasets, web searches, APIs and other agents. (Source: source-03)
- Anthropic's basic building block is an LLM augmented with retrieval, tools and memory, and tools need clear, well-documented interfaces. (Source: source-02)
- Anthropic spent more time improving tools than the overall prompt on a coding benchmark; requiring absolute file paths removed a common mistake. (Source: source-02)
- OpenAI's function-calling API (late 2023) and Anthropic's Model Context Protocol (late 2024) helped deployment of LLM agents speed up. (Source: source-01)
- An agent harness is the software layer around an LLM that manages prompts, context, tool use, memory, permissions and results. (Source: source-01)
**Related pages:** [[agent-loop]], [[memory-and-planning]], [[glossary]], [[index]]
**Sources:** source-01, source-02, source-03, source-05
**Open questions / conflicts:** Source-05 is documentation for one provider's API, so the exact message format may differ for other providers.
