# Awesome AI Agent Security [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of frameworks, research, incidents, tools and guidance for securing LLM agents and AI coding agents.

Defensive focus. Every entry links to its original source.

## Contents

- [Frameworks and Standards](#frameworks-and-standards)
- [Research Papers](#research-papers)
<!-- toc-end -->

## Frameworks and Standards

- [CoSAI (Coalition for Secure AI)](https://www.coalitionforsecureai.org/) - Industry coalition publishing open workstreams on AI supply chain security, agentic system security, and risk governance.
- [CSA MAESTRO](https://cloudsecurityalliance.org/blog/2025/02/06/agentic-ai-threat-modeling-framework-maestro) - Cloud Security Alliance threat modeling framework with a layered reference architecture for agentic AI systems.
- [Databricks AI Security Framework (DASF)](https://www.databricks.com/resources/whitepaper/databricks-ai-security-framework-dasf) - Catalog of AI system components, their risks, and mapped controls across the model lifecycle.
- [Google Secure AI Framework (SAIF)](https://saif.google/) - Google's framework of core elements, risk map, and controls for securing AI systems, including agents.
- [Guidelines for Secure AI System Development](https://www.ncsc.gov.uk/collection/guidelines-secure-ai-system-development) - Joint UK NCSC and CISA guidance covering secure design, development, deployment, and operation of AI systems.
- [ISO/IEC 42001](https://www.iso.org/standard/81230.html) - International standard for establishing and auditing an AI management system.
- [MCP Authorization Specification](https://modelcontextprotocol.io/specification/2025-06-18/basic/authorization) - OAuth-based authorization requirements for MCP clients and servers over HTTP transports.
- [MCP Security Best Practices](https://modelcontextprotocol.io/docs/tutorials/security/security_best_practices) - Model Context Protocol guidance on confused deputy attacks, token passthrough, session hijacking, and local server compromise.
- [MITRE ATLAS](https://atlas.mitre.org/) - Knowledge base of adversary tactics, techniques, and case studies against AI systems, modeled on ATT&CK.
- [NIST AI 100-2 E2025: Adversarial Machine Learning](https://csrc.nist.gov/pubs/ai/100/2/e2025/final) - NIST taxonomy and terminology of attacks and mitigations for predictive and generative AI, including agent hijacking.
- [NIST AI 600-1: Generative AI Profile](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.600-1.pdf) - Companion to the AI RMF listing generative AI risks and suggested actions to manage them.
- [NIST AI Risk Management Framework](https://www.nist.gov/itl/ai-risk-management-framework) - Voluntary framework for governing, mapping, measuring, and managing AI risk.
- [OWASP Agentic AI: Threats and Mitigations](https://genai.owasp.org/resource/agentic-ai-threats-and-mitigations/) - Threat model and mitigation catalog for agents covering memory poisoning, tool misuse, and privilege compromise.
- [OWASP AI Exchange](https://owaspai.org/) - Open collection of AI threats and controls that feeds into international AI security standards.
- [OWASP LLM01: Prompt Injection](https://genai.owasp.org/llmrisk/llm01-prompt-injection/) - OWASP entry defining direct and indirect prompt injection with example scenarios and mitigations.
- [OWASP Top 10 for Agentic Applications](https://genai.owasp.org/resource/owasp-top-10-for-agentic-applications-for-2026/) - Ranked list of the most critical security risks specific to autonomous agent applications.
- [OWASP Top 10 for LLM Applications](https://genai.owasp.org/llm-top-10/) - Ranked list of the most critical risks in LLM applications, including prompt injection and excessive agency.
- [UK AI Cyber Security Code of Practice](https://www.gov.uk/government/publications/ai-cyber-security-code-of-practice) - UK government baseline security principles for developers and operators of AI systems.

## Research Papers

- [The Attacker Moves Second: Stronger Adaptive Attacks Bypass Defenses Against LLM Jailbreaks and Prompt Injections](https://arxiv.org/abs/2510.09023) - 2025. Shows that adaptive attacks defeat most published jailbreak and injection defenses and argues for stronger evaluation.
- [EchoLeak: The First Real-World Zero-Click Prompt Injection Exploit in a Production LLM System](https://arxiv.org/abs/2509.10540) - 2025. Case study of the Microsoft 365 Copilot zero-click exfiltration chain and the defenses it bypassed.
- [PromptArmor: Simple yet Effective Prompt Injection Defenses](https://arxiv.org/abs/2507.15219) - 2025. Uses an LLM as a guard to detect and strip injected instructions before the agent acts.
- [Meta SecAlign: A Secure Foundation LLM Against Prompt Injection Attacks](https://arxiv.org/abs/2507.02735) - 2025. Open model trained with SecAlign to resist prompt injection, with evaluation on agent benchmarks.
- [Design Patterns for Securing LLM Agents against Prompt Injections](https://arxiv.org/abs/2506.08837) - 2025. Catalogs architectural patterns such as plan-then-execute and dual LLM that constrain what injected text can do.
- [Beyond the Protocol: Unveiling Attack Vectors in the Model Context Protocol (MCP) Ecosystem](https://arxiv.org/abs/2506.02040) - 2025. Studies how malicious MCP servers reach users through registries and client behavior.
- [Securing AI Agents with Information-Flow Control](https://arxiv.org/abs/2505.23643) - 2025. Applies taint tracking and information-flow labels to agent planners to enforce confidentiality and integrity.
- [WASP: Benchmarking Web Agent Security Against Prompt Injection Attacks](https://arxiv.org/abs/2504.18575) - 2025. Benchmark measuring how often web agents follow injected goals in realistic sites.
- [Progent: Securing AI Agents with Privilege Control](https://arxiv.org/abs/2504.11703) - 2025. Enforces least privilege on agent tool calls through a policy language evaluated outside the model.
- [DataSentinel: A Game-Theoretic Detection of Prompt Injection Attacks](https://arxiv.org/abs/2504.11358) - 2025. Trains a detector adversarially to flag contaminated inputs.
- [MCP Safety Audit: LLMs with the Model Context Protocol Allow Major Security Exploits](https://arxiv.org/abs/2504.03767) - 2025. Demonstrates credential theft and code execution through standard MCP servers and proposes an auditing tool.
- [Model Context Protocol (MCP): Landscape, Security Threats, and Future Research Directions](https://arxiv.org/abs/2503.23278) - 2025. Survey of MCP lifecycle phases and the security threats at each.
- [Defeating Prompt Injections by Design (CaMeL)](https://arxiv.org/abs/2503.18813) - 2025. Separates control and data flow with a capability system so untrusted data cannot change the agent's plan.
- [Adaptive Attacks Break Defenses Against Indirect Prompt Injection Attacks on LLM Agents](https://arxiv.org/abs/2503.00061) - 2025. Evaluates eight indirect injection defenses against adaptive attacks and finds all bypassable.
- [MELON: Provable Defense Against Indirect Prompt Injection Attacks in AI Agents](https://arxiv.org/abs/2502.05174) - 2025. Detects injections by comparing agent actions with and without the user's task.
- [Imprompter: Tricking LLM Agents into Improper Tool Use](https://arxiv.org/abs/2410.14923) - 2024. Shows obfuscated prompts that make agents leak personal data through tool calls.
- [AgentHarm: A Benchmark for Measuring Harmfulness of LLM Agents](https://arxiv.org/abs/2410.09024) - 2024. Benchmark of harmful multi-step agent tasks for measuring refusal and robustness.
- [SecAlign: Defending Against Prompt Injection with Preference Optimization](https://arxiv.org/abs/2410.05451) - 2024. Uses preference optimization to teach models to ignore instructions in data.
- [Agent Security Bench (ASB)](https://arxiv.org/abs/2410.02644) - 2024. Formalizes and benchmarks attacks and defenses across agent scenarios, tools, and memory.
- [AgentDojo: A Dynamic Environment to Evaluate Prompt Injection Attacks and Defenses for LLM Agents](https://arxiv.org/abs/2406.13352) - 2024. Extensible environment of realistic tasks and injection cases for agent evaluation.
- [Get my drift? Catching LLM Task Drift with Activation Deltas](https://arxiv.org/abs/2406.00799) - 2024. Detects injected instructions by probing changes in model activations.
- [The Instruction Hierarchy: Training LLMs to Prioritize Privileged Instructions](https://arxiv.org/abs/2404.13208) - 2024. Trains models to rank system, user, and tool instructions by privilege.
- [Defending Against Indirect Prompt Injection Attacks With Spotlighting](https://arxiv.org/abs/2403.14720) - 2024. Marks untrusted input through delimiting, datamarking, or encoding so the model can tell it apart.
- [IsolateGPT: An Execution Isolation Architecture for LLM-Based Agentic Systems](https://arxiv.org/abs/2403.04960) - 2024. Isolates third-party apps in agent systems with a hub-and-spoke design.
- [InjecAgent: Benchmarking Indirect Prompt Injections in Tool-Integrated LLM Agents](https://arxiv.org/abs/2403.02691) - 2024. Benchmark of injected tool outputs aimed at direct harm and data theft.
- [StruQ: Defending Against Prompt Injection with Structured Queries](https://arxiv.org/abs/2402.06363) - 2024. Separates prompt and data channels and fine-tunes the model to follow only the prompt channel.
- [Benchmarking and Defending Against Indirect Prompt Injection Attacks on Large Language Models (BIPIA)](https://arxiv.org/abs/2312.14197) - 2023. First benchmark for indirect prompt injection with black-box and white-box defenses.
- [Tensor Trust: Interpretable Prompt Injection Attacks from an Online Game](https://arxiv.org/abs/2311.01011) - 2023. Dataset of human-written injection attacks and defenses collected from an online game.
- [Formalizing and Benchmarking Prompt Injection Attacks and Defenses](https://arxiv.org/abs/2310.12815) - 2023. Framework that formalizes injection attacks and systematically compares defenses.
- [Identifying the Risks of LM Agents with an LM-Emulated Sandbox (ToolEmu)](https://arxiv.org/abs/2309.15817) - 2023. Emulates tool execution with an LM to find risky agent behavior before deployment.
- [Universal and Transferable Adversarial Attacks on Aligned Language Models](https://arxiv.org/abs/2307.15043) - 2023. Introduces optimized adversarial suffixes, the basis of many later robustness evaluations.
- [Jailbroken: How Does LLM Safety Training Fail?](https://arxiv.org/abs/2307.02483) - 2023. Explains jailbreak success through competing objectives and mismatched generalization.
- [Prompt Injection Attack against LLM-integrated Applications](https://arxiv.org/abs/2306.05499) - 2023. Black-box study of prompt injection against real LLM-integrated applications.
- [Not what you've signed up for: Compromising Real-World LLM-Integrated Applications with Indirect Prompt Injection](https://arxiv.org/abs/2302.12173) - 2023. Paper that defined indirect prompt injection through retrieved content.
- [Ignore Previous Prompt: Attack Techniques For Language Models](https://arxiv.org/abs/2211.09527) - 2022. Early study of goal hijacking and prompt leaking.

## Contributing

Contributions are welcome. Open a pull request with a link to the source for any change.

## License

[![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)

---

Maintained by [Ali Hesari](https://alihesari.com). Follow on [GitHub](https://github.com/alihesari) and [X](https://x.com/alihesari) for updates.
