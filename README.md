# AI Agent Learning

### Level 1
#### Choosing the Right Pattern
- Decision Tree: Which Workflow Pattern?
<img width="1938" height="1144" alt="agent-decision-tree" src="https://github.com/user-attachments/assets/335ed117-6876-4b4d-b357-f2fee9defdea" />

-Quick Reference Table
| Pattern | When to Use | Example | Key Feature |
|---------|-------------|---------|-------------|
| **LLM-based (sub_agents)** | Dynamic orchestration needed | Research + Summarize | LLM decides what to call |
| **Sequential** | Order matters, linear pipeline | Outline → Write → Edit | Deterministic order |
| **Parallel** | Independent tasks, speed matters | Multi-topic research | Concurrent execution |
| **Loop** | Iterative improvement needed | Writer + Critic refinement | Repeated cycles |


 documentation for level 1:

- [Agents in ADK](https://google.github.io/adk-docs/agents/)
- [Sequential Agents in ADK](https://google.github.io/adk-docs/agents/workflow-agents/sequential-agents/)
- [Parallel Agents in ADK](https://google.github.io/adk-docs/agents/workflow-agents/parallel-agents/)
- [Loop Agents in ADK](https://google.github.io/adk-docs/agents/workflow-agents/loop-agents/)
- [Custom Agents in ADK](https://google.github.io/adk-docs/agents/custom-agents/)






<hr>
<hr>
<hr>

### Level 2

- Now that you've seen tools in action, let's understand the complete ADK toolkit:
- It's broadly divided into two categories: **Custom tools** and **Built-in tools**



#### **1. Custom Tools**


<img src="https://storage.googleapis.com/github-repo/kaggle-5days-ai/day2/custom-tools.png" width="800" alt="Custom Tools">

**What**: Tools you build yourself for specific needs

**Advantage**: Complete control over functionality — you build exactly what your agent needs

##### **Function Tools** ✅ (You've used these!)
- **What**: Python functions converted to agent tools
- **Examples**: `get_fee_for_payment_method`, `get_exchange_rate`
- **Advantage**: Turn any Python function into an agent tool instantly

##### **Long Running Function Tools**
- **What**: Functions for operations that take significant time
- **Examples**: Human-in-the-loop approvals, file processing
- **Advantage**: Agents can start tasks and continue with other work while waiting

##### **Agent Tools** ✅ (You've used these!)
- **What**: Other agents used as tools
- **Examples**: `AgentTool(agent=calculation_agent)`
- **Advantage**: Build specialist agents and reuse them across different systems

##### **MCP Tools**
- **What**: Tools from Model Context Protocol servers
- **Examples**: Filesystem access, Google Maps, databases
- **Advantage**: Connect to any MCP-compatible service without custom integration

##### **OpenAPI Tools**
- **What**: Tools automatically generated from API specifications
- **Examples**: REST API endpoints become callable tools
- **Advantage**: No manual coding — just provide an API spec and get working tools



#### **2. Built-in Tools**


<img width="2088" height="518" alt="built-in-tools" src="https://github.com/user-attachments/assets/b4cf485f-a088-4a07-bcc5-fb9ac7b0ac2b" />

**What**: Pre-built tools provided by ADK

**Advantage**: No development time — use immediately with zero setup

##### **Gemini Tools** ✅ (You've used these!)
- **What**: Tools that leverage Gemini's capabilities
- **Examples**: `google_search`, `BuiltInCodeExecutor`
- **Advantage**: Reliable, tested tools that work out of the box

##### **Google Cloud Tools** [needs Google Cloud access]
- **What**: Tools for Google Cloud services and enterprise integration
- **Examples**: `BigQueryToolset`, `SpannerToolset`, `APIHubToolset`
- **Advantage**: Enterprise-grade database and API access with built-in security

##### **Third-party Tools**
- **What**: Wrappers for existing tool ecosystems
- **Examples**: Hugging Face, Firecrawl, GitHub Tools
- **Advantage**: Reuse existing tool investments — no need to rebuild what already exists


documentation for level 2:

- [ADK Documentation](https://google.github.io/adk-docs/)
- [ADK Tools Documentation](https://google.github.io/adk-docs/tools/)
- [ADK Custom Tools Guide](https://google.github.io/adk-docs/tools-custom/)
- [ADK Function Tools](https://google.github.io/adk-docs/tools/function-tools/)
- [ADK Plugins Overview](https://google.github.io/adk-docs/plugins/)






















