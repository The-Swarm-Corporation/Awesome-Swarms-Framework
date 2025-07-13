# Awesome Swarms ✨

A curated, comprehensive list of awesome libraries, tools, templates, and resources for the **Swarms** framework by [swarms.ai](https://swarms.ai). Swarms is a powerful, modular, and reliable open-source framework for building, deploying, and scaling autonomous agent swarms for any task.

**Unlock the power of collective AI. Star the main repository to show your support\!**

> 🔗 **Main GitHub Repository:** [**https://github.com/kyegomez/swarms**](https://github.com/kyegomez/swarms)

This list is a community effort. We encourage you to contribute by submitting a pull request\!

-----

## Why Swarms? 🚀

Swarms isn't just another agent framework; it's a production-grade multi-agent infrastructure platform designed for reliability, scalability, and state-of-the-art performance.

  * **🤖 Collective Intelligence:** Move beyond the limitations of single agents. Swarms enable multiple specialized agents to collaborate, reason, and solve complex, multi-faceted problems that are impossible for a single agent to tackle.
  * **🧱 Advanced Modular Structures:** Swarms provides a rich set of pre-built, battle-tested agent formations (Structures) like **Concurrent Swarms**, **Hierarchical Swarms**, **Mixture-of-Agents**, and **Agent Councils**. Build sophisticated workflows with minimal code.
  * **🔬 Research-Backed:** Implementations are directly inspired by and often surpass state-of-the-art academic research. Swarms bridges the gap between theoretical papers and production-ready applications.
  * **🛠️ Rich Tooling & Integrations:** A massive ecosystem of tools, from web Browse and code execution to vector databases and third-party framework integrations (LangChain, AutoGen), is available out of the box.
  * **🌐 Real-World Applications:** From automated financial analysis and medical diagnosis to complex scientific research and secure code generation, Swarms provides templates and examples for a vast array of industries.
  * **✅ Reliability & Scalability:** Built with production in mind, Swarms includes features for error handling, concurrent processing, load balancing, and monitoring to ensure your agent systems are robust and efficient.

-----

## 💡 Core Concepts

To get the most out of Swarms, it's helpful to understand a few key concepts:

  * **Agent:** The fundamental building block. An autonomous entity that can perceive its environment, make decisions, and execute tasks. In Swarms, an `Agent` is typically powered by an LLM and can be equipped with tools.
  * **Swarm:** A collection of agents organized into a specific structure to collaborate on a common goal. The Swarm orchestrates the flow of information and tasks between its constituent agents.
  * **Structure:** The architecture or topology of a Swarm. This defines how agents communicate and collaborate. Examples include `HierarchicalSwarm` (for top-down command), `ConcurrentSwarm` (for parallel processing), and `GroupChat` (for interactive sessions).
  * **Tool:** A function or utility that an agent can use to interact with the outside world, such as searching the web, running code, or accessing a database.
  * **Workflow:** A sequence or graph of tasks executed by one or more agents. Swarms allows you to define simple sequential workflows or complex, dynamic graphs of operations.
  * **Multi-modality:** The ability for agents to process and understand information beyond just text, including images, audio, and video.

-----

## ⚡ Getting Started

Getting started with Swarms is incredibly simple.

**1. Installation**
Install the package using pip:

```bash
pip install swarms
```

**2. Your First "Hello, Swarm\!"**
This simple example demonstrates the basic `Agent` class.

```python
from swarms import Agent, OpenAIChat

# Get your API key from https://openai.com/
api_key = "..."

# Initialize the language model
llm = OpenAIChat(
    openai_api_key=api_key,
    temperature=0.5,
)

# Initialize the agent
agent = Agent(
    llm=llm,

    max_loops=1,
    dashboard=True
)

# Run the agent with a task
out = agent("What is the capital of France? Respond in a single word.")
print(out) # Output: Paris
```

-----

## 🔬 Research Paper Implementations

Swarms is at the forefront of AI research, providing production-grade, open-source implementations of influential multi-agent papers. This democratizes access to cutting-edge techniques and allows developers to build with state-of-the-art models.

| Paper Name | Description | Original Paper | Implementation |
| :--- | :--- | :--- | :--- |
| **MALT (Multi-Agent Learning Task)** | A sophisticated orchestration framework coordinating Creator, Verifier, and Refiner agents to tackle complex tasks through structured conversations, ensuring reliability. | [arXiv:2412.01928](https://arxiv.org/pdf/2412.01928) | [`swarms.structs.malt`](https://www.google.com/search?q=%5Bhttps://docs.swarms.world/en/latest/swarms/structs/malt/%5D\(https://docs.swarms.world/en/latest/swarms/structs/malt/\)) |
| **MAI-DxO (Diagnostic Orchestrator)** | An open-source implementation of Microsoft's "Sequential Diagnosis with Language Models," simulating a virtual panel of physician-agents for iterative medical diagnosis. | [Microsoft Research Paper](https://arxiv.org/abs/2506.22405) | [Open-MAI-Dx-Orchestrator](https://github.com/The-Swarm-Corporation/Open-MAI-Dx-Orchestrator) |
| **AI-CoScientist** | A multi-agent framework for collaborative scientific research that uses a tournament-based system to evolve and peer-review hypotheses. | ["Towards an AI Co-Scientist"](https://storage.googleapis.com/coscientist_paper/ai_coscientist.pdf) | [AI-CoScientist](https://github.com/The-Swarm-Corporation/AI-CoScientist) |
| **Mixture of Agents (MoA)** | An architecture that implements parallel processing with iterative refinement, combining diverse expert agents for comprehensive, state-of-the-art analysis. | [arXiv:2406.04692](https://arxiv.org/abs/2406.04692) | [`swarms.structs.moa`](https://www.google.com/search?q=%5Bhttps://docs.swarms.world/en/latest/swarms/structs/moa/%5D\(https://docs.swarms.world/en/latest/swarms/structs/moa/\)) |
| **Deep Research Swarm** | A production-grade research system that conducts comprehensive analysis across multiple domains using parallel processing and advanced AI agents. | Internal Research | [`swarms.structs.deep_research_swarm`](https://www.google.com/search?q=%5Bhttps://docs.swarms.world/en/latest/swarms/structs/deep_research_swarm/%5D\(https://docs.swarms.world/en/latest/swarms/structs/deep_research_swarm/\)) |
| **Agent-as-a-Judge** | An evaluation framework that uses agents to evaluate the quality and performance of other agents, automating the assessment process. | [arXiv:2410.10934](https://arxiv.org/abs/2410.10934) | [`swarms.agents.agent_judge`](https://www.google.com/search?q=%5Bhttps://docs.swarms.world/en/latest/swarms/agents/agent_judge/%5D\(https://docs.swarms.world/en/latest/swarms/agents/agent_judge/\)) |

*For a comprehensive list of influential multi-agent papers, check out the [awesome-multi-agent-papers](https://github.com/kyegomez/awesome-multi-agent-papers) repository.*

-----

## 🏢 Industry Applications & Templates

Swarms provides a vast collection of production-ready templates and applications tailored for specific industries, enabling developers to rapidly deploy sophisticated solutions for real-world problems. Explore these repositories to see how Swarms can be adapted to your domain.

### 🏥 Healthcare & Medical Applications

| Name | Description | Repository |
| :--- | :--- | :--- |
| **MRI-Swarm** | A multi-agent system designed for the advanced analysis and diagnosis of MRI images, leveraging collective intelligence for higher accuracy. | [MRI-Swarm](https://github.com/The-Swarm-Corporation/MRI-Swarm) |
| **DermaSwarm** | A specialized swarm of dermatology-focused agents for analyzing skin conditions from images and patient data. | [DermaSwarm](https://github.com/The-Swarm-Corporation/DermaSwarm) |
| **Multi-Modal X-Ray Diagnosis** | A powerful swarm that uses multi-modal AI agents to provide comprehensive diagnoses from X-ray images and associated medical reports. | [Multi-Modal-XRAY-Diagnosis](https://github.com/The-Swarm-Corporation/Multi-Modal-XRAY-Diagnosis-Medical-Swarm-Template) |
| **Medical Coder Swarm** | An agent swarm that automates the complex process of medical coding, improving efficiency and reducing errors in billing and documentation. | [MedicalCoderSwarm](https://github.com/The-Swarm-Corporation/MedicalCoderSwarm) |
| **Pharma Swarm** | A swarm dedicated to accelerating pharmaceutical research and development, from drug discovery to clinical trial analysis. | [pharma-swarm](https://github.com/The-Swarm-Corporation/pharma-swarm) |
| **Radiology Swarm** | A multi-agent system specifically designed for radiology workflows, assisting with image interpretation and report generation. | [radiology-swarm](https://github.com/The-Swarm-Corporation/radiology-swarm) |
| **MedInsight-Pro** | An advanced medical analytics platform that provides deep insights from vast datasets, powered by a swarm of analytical agents. | [MedInsight-Pro](https://github.com/The-Swarm-Corporation/MedInsight-Pro) |

### 💰 Financial Services & Trading

| Name | Description | Repository |
| :--- | :--- | :--- |
| **Automated Crypto Fund** | Manages a cryptocurrency trading fund by automating analysis, rebalancing, and execution of trades with a team of financial agents. | [automated-crypto-fund](https://github.com/The-Swarm-Corporation/automated-crypto-fund) |
| **Forex Tree Swarm** | A Forex trading system that uses a decision tree swarm architecture to analyze market data and make informed trading decisions. | [ForexTreeSwarm](https://github.com/The-Swarm-Corporation/ForexTreeSwarm) |
| **Open-Aladdin** | An open-source financial risk management system inspired by BlackRock's Aladdin, using agents to monitor portfolios and assess risk. | [Open-Aladdin](https://github.com/The-Swarm-Corporation/Open-Aladdin) |
| **AutoHedge** | An agent-based system for implementing and automating complex hedging strategies to manage financial risk. | [AutoHedge](https://github.com/The-Swarm-Corporation/AutoHedge) |
| **Insurance Swarm** | A swarm designed to automate insurance processes, including claim processing, fraud detection, and policy underwriting. | [InsuranceSwarm](https://github.com/The-Swarm-Corporation/InsuranceSwarm) |
| **Mortgage Underwriting Swarm** | An automated system that streamlines the mortgage underwriting process by using agents to verify information and assess applicant risk. | [MortgageUnderwritingSwarm](https://github.com/The-Swarm-Corporation/MortgageUnderwritingSwarm) |

### 🔬 Scientific & Academic Research

| Name | Description | Repository |
| :--- | :--- | :--- |
| **Auto AI Research Team** | An automated team of AI research agents that can collaborate to conduct experiments, analyze data, and generate insights. | [auto-ai-research-team](https://github.com/The-Swarm-Corporation/auto-ai-research-team) |
| **Research Paper Writer Swarm** | A system that automates the process of writing academic research papers, from literature review to drafting and formatting. | [Research-Paper-Writer-Swarm](https://github.com/The-Swarm-Corporation/Research-Paper-Writer-Swarm) |
| **Generalist Mathematician Swarm** | A swarm of mathematical agents designed to collaborate on solving complex mathematical problems and proving theorems. | [Generalist-Mathematician-Swarm](https://github.com/The-Swarm-Corporation/Generalist-Mathematician-Swarm) |

### 💼 Business, Marketing, & Legal

| Name | Description | Repository |
| :--- | :--- | :--- |
| **Marketing Swarm Template** | A template for building a marketing campaign automation swarm, including agents for content creation, social media posting, and analytics. | [Marketing-Swarm-Template](https://github.com/The-Swarm-Corporation/Marketing-Swarm-Template) |
| **NewsAgent** | An agent that aggregates, analyzes, and summarizes news from various sources to provide tailored intelligence briefings. | [NewsAgent](https://github.com/The-Swarm-Corporation/NewsAgent) |
| **Legal Swarm Template** | A template for legal applications, enabling agents to process, analyze, and summarize legal documents and perform legal research. | [Legal-Swarm-Template](https://github.com/The-Swarm-Corporation/Legal-Swarm-Template) |

-----

## ⚙️ Swarm Structures & Examples

This index organizes **100+ production-ready examples** from the [Swarms Examples Repository](https://github.com/The-Swarm-Corporation/swarms-examples), showcasing the framework's power and versatility.

### Multi-Agent Systems (Swarms)

These examples demonstrate how to build powerful collaborative systems.

#### Core Architectures

| Example | Description | Repository Link |
| :--- | :--- | :--- |
| **Build a Swarm** | The fundamental example for creating a custom swarm with multiple agents. | [build\_a\_swarm.py](https://github.com/The-Swarm-Corporation/swarms-examples/blob/main/examples/structs/swarms/base_swarm/build_a_swarm.py) |
| **Concurrent Swarm** | Shows how to achieve parallel execution of tasks across multiple agents for high-throughput processing. | [concurrent\_swarm\_example.py](https://github.com/The-Swarm-Corporation/swarms-examples/blob/main/examples/structs/swarms/concurrent_swarm/concurrent_swarm_example.py) |
| **Hierarchical Swarm** | Implements a multi-level agent hierarchy, perfect for tasks requiring top-down management and delegation. | [hierarchical\_swarm\_example.py](https://github.com/kyegomez/swarms/blob/master/examples/multi_agent/hiearchical_swarm/hiearchical_examples/hierarchical_swarm_example.py) |
| **Sequential Workflow** | A linear workflow where agents process tasks in a defined sequence, ideal for multi-step processes. | [sequential\_workflow\_example.py](https://github.com/kyegomez/swarms/blob/master/examples/multi_agent/sequential_workflow/sequential_workflow_example.py) |
| **Auto Swarm** | A self-organizing swarm with automatic task distribution and management, adapting to dynamic workloads. | [auto\_swarm\_example.py](https://github.com/The-Swarm-Corporation/swarms-examples/blob/main/examples/structs/swarms/auto_swarm/auto_swarm_example.py) |
| **Graph Workflow** | A minimal but powerful example of a graph-based workflow with two agents and one task. | [graph\_workflow\_basic.py](https://github.com/kyegomez/swarms/blob/main/examples/structs/graph_workflow_basic.py) |

#### Group Chat & Interactive Systems

| Example | Description | Repository Link |
| :--- | :--- | :--- |
| **Group Chat** | A multi-agent group chat system with turn-based communication for collaborative problem-solving. | [group\_chat\_example.py](https://github.com/kyegomez/swarms/blob/master/examples/multi_agent/groupchat/groupchat_examples/group_chat_example.py) |
| **Interactive Group Chat** | An advanced group chat that allows for real-time user participation and intervention. | [interactive\_groupchat\_example.py](https://github.com/kyegomez/swarms/blob/master/examples/multi_agent/groupchat/interactive_groupchat_example.py) |
| **Medical Panel** | A specialized panel of medical expert agents for healthcare discussions and diagnostic collaboration. | [medical\_panel\_example.py](https://github.com/kyegomez/swarms/blob/master/examples/multi_agent/interactive_groupchat_examples/medical_panel_example.py) |

#### Advanced Collaboration & Experimental Architectures

| Example | Description | Repository Link |
| :--- | :--- | :--- |
| **Majority Voting** | A consensus-based decision-making system where multiple agents vote to reach a conclusion. | [majority\_voting.py](https://github.com/The-Swarm-Corporation/swarms-examples/blob/main/examples/structs/swarms/multi_agent_collaboration/majority_voting.py) |
| **Monte Carlo Swarm** | A swarm that uses Monte Carlo simulation for probabilistic decision-making and exploring complex problem spaces. | [monte\_carlo\_swarm.py](https://github.com/The-Swarm-Corporation/swarms-examples/blob/main/examples/structs/swarms/experimental/monte_carlo_swarm.py) |
| **Ant Colony Swarm** | A bio-inspired optimization system using ant colony algorithms for intelligent agent coordination and pathfinding. | [ant\_swarm.py](https://github.com/The-Swarm-Corporation/swarms-examples/blob/main/examples/structs/swarms/experimental/ant_swarm.py) |
| **Federated Swarm** | A distributed learning system that enables privacy-preserving agent collaboration across different environments. | [federated\_swarm.py](https://github.com/The-Swarm-Corporation/swarms-examples/blob/main/examples/structs/swarms/experimental/federated_swarm.py) |

### Single-Agent Systems

These examples cover the foundational agent, its capabilities, and integrations.

| Category | Example | Description | Repository Link |
| :--- | :--- | :--- | :--- |
| **Core** | **Easy Example** | The simplest agent implementation, demonstrating core functionality. Perfect for beginners. | [easy\_example.py](https://github.com/The-Swarm-Corporation/swarms-examples/blob/main/examples/agents/easy_example.py) |
| **Memory** | **Agent with Long-term Memory** | Shows how to give an agent persistent memory to maintain context across sessions. | [agent\_with\_longterm\_memory.py](https://github.com/The-Swarm-Corporation/swarms-examples/blob/main/examples/agents/memory/agents_and_memory/agent_with_longterm_memory.py) |
| **Tools** | **OpenAI Function Calling** | Demonstrates integration with OpenAI's function calling API for structured outputs and tool use. | [openai\_function\_caller\_example.py](https://github.com/The-Swarm-Corporation/swarms-examples/blob/main/examples/agents/tools/function_calling/openai_function_caller_example.py) |
| **Models** | **Groq Agent** | An example of using a high-performance model from Groq for accelerated inference. | [groq\_agent.py](https://github.com/The-Swarm-Corporation/swarms-examples/blob/main/examples/agents/settings/various_models/groq_agent.py) |
| **Models** | **Claude 4 Example** | Integration with Anthropic's Claude 3 model for advanced reasoning capabilities. | [claude\_4\_example.py](https://github.com/kyegomez/swarms/blob/master/examples/models/claude_4_example.py) |
| **RAG** | **Full Agent RAG Example** | A complete Retrieval-Augmented Generation (RAG) implementation for question-answering over documents. | [full\_agent\_rag\_example.py](https://github.com/kyegomez/swarms/blob/master/examples/single_agent/rag/full_agent_rag_example.py) |
| **Vision** | **Multimodal Example** | A multi-modal agent that can process and understand text, image, and audio inputs. | [multimodal\_example.py](https://github.com/kyegomez/swarms/blob/master/examples/single_agent/vision/multimodal_example.py) |

-----

## 🛠️ Developer Tools & Platforms

The Swarms ecosystem includes core platforms and utilities to accelerate development, deployment, and management of agentic systems.

| Name | Description | Repository |
| :--- | :--- | :--- |
| **AgentOS** | A foundational operating system for AI agents, providing core functionalities for agent lifecycle management. | [AgentOS](https://github.com/The-Swarm-Corporation/AgentOS) |
| **Swarm Ecosystem** | The complete ecosystem for swarm development, bundling core libraries and essential tools. | [swarm-ecosystem](https://github.com/The-Swarm-Corporation/swarm-ecosystem) |
| **DevSwarm** | A swarm of agents specifically designed to assist with software development tasks like code generation, debugging, and testing. | [DevSwarm](https://github.com/The-Swarm-Corporation/DevSwarm) |
| **OmniParse** | A universal document parsing system that can extract structured information from any document format (PDF, DOCX, HTML, etc.). | [OmniParse](https://github.com/The-Swarm-Corporation/OmniParse) |
| **doc-master** | An automated documentation generation and management tool to keep your project's docs up-to-date. | [doc-master](https://github.com/The-Swarm-Corporation/doc-master) |
| **swarms-evals** | A comprehensive evaluation framework for testing and benchmarking the performance of your swarm systems. | [swarms-evals](https://github.com/The-Swarm-Corporation/swarms-evals) |

-----

## 📚 Educational Resources & Courses

Learn how to build and deploy enterprise-grade agent systems with these comprehensive resources.

| Name | Description | Repository |
| :--- | :--- | :--- |
| **The Swarms Cookbook** | The definitive collection of detailed walkthroughs, advanced patterns, and recipes for building with Swarms. | [Cookbook](https://github.com/The-Swarm-Corporation/Cookbook) |
| **Enterprise-Grade Agents Course** | A comprehensive course covering the principles and practices for building robust, scalable, and secure AI agents for enterprise use cases. | [Enterprise-Grade-Agents-Course](https://github.com/The-Swarm-Corporation/Enterprise-Grade-Agents-Course) |
| **Agents Beginner Guide** | A beginner-friendly guide to the fundamental concepts of AI agents and how to get started with the Swarms framework. | [Agents-Beginner-Guide](https://github.com/The-Swarm-Corporation/Agents-Beginner-Guide) |
| **Multi-Agent Marketing Course** | An educational course that teaches you how to build and deploy a multi-agent swarm for automating marketing tasks. | [Multi-Agent-Marketing-Course](https://github.com/The-Swarm-Corporation/Multi-Agent-Marketing-Course) |

-----

## 🤝 Community & Support

Join our vibrant community of agent engineers, researchers, and developers\! Get support, share your projects, and stay up-to-date on the latest in multi-agent AI.

| Platform | Description | Link |
| :--- | :--- | :--- |
| 🏠 **Main Repository** | The core Swarms framework repository on GitHub. Star us\! | [**kyegomez/swarms**](https://github.com/kyegomez/swarms) |
| 🏢 **GitHub Org** | Home to all official Swarms projects and templates. | [The-Swarm-Corporation](https://github.com/The-Swarm-Corporation) |
| 🌐 **Website** | Official project website and hub for all things Swarms. | [**swarms.ai**](https://swarms.ai) |
| 📚 **Documentation** | Official documentation, guides, and API reference. | [docs.swarms.world](https://docs.swarms.world) |
| 💬 **Discord** | The main community hub for live chat, support, and collaboration. | [**Join our Discord**](https://discord.gg/jM3Z6M9uMq) |
| 🐦 **Twitter / X** | Follow the creator for the latest news and announcements. | [@kyegomez](https://twitter.com/kyegomez) |
| 📝 **Blog** | In-depth technical articles and updates on the project. | [Medium](https://medium.com/@kyeg) |
| 📺 **YouTube** | Find video tutorials, demos, and community calls. | [Swarms Channel](https://www.youtube.com/channel/UC9yXyitkbU_WSy7bd_41SqQ) |
| 🚀 **Onboarding** | Book a 1-on-1 session with Kye Gomez, the creator of Swarms. | [Book a Session](https://cal.com/swarms/swarms-onboarding-session) |
| 👥 **LinkedIn** | Follow our professional network for company updates. | [The Swarm Corporation](https://www.linkedin.com/company/the-swarm-corporation) |

-----

## Citation

If you use Swarms in your research or projects, please cite the framework:

```bibtex
@misc{SWARMS_2022,
  author       = {Gomez, Kye and Pliny and More, Harshal and Swarms Community},
  title        = {{Swarms: Production-Grade Multi-Agent Infrastructure Platform}},
  year         = {2022},
  howpublished = {\url{https://github.com/kyegomez/swarms}},
  note         = {Documentation available at \url{https://docs.swarms.world}},
  version      = {latest}
}
```
