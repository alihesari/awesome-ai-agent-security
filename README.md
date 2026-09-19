# Awesome AI Agent Security [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of frameworks, research, incidents, tools and guidance for securing LLM agents and AI coding agents.

Defensive focus. Every entry links to its original source.

## Contents

- [Frameworks and Standards](#frameworks-and-standards)
- [Research Papers](#research-papers)
- [Incidents and Writeups](#incidents-and-writeups)
- [Defensive Tools](#defensive-tools)
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

## Incidents and Writeups

- [AgentFlayer: ChatGPT Connectors 0-click attack](https://labs.zenity.io/p/agentflayer-chatgpt-connectors-0click-attack-5b41) - Zenity Labs writeup of a poisoned shared document exfiltrating Google Drive secrets through ChatGPT Connectors.
- [Amazon Q Developer extension code injection (AWS-2025-015)](https://aws.amazon.com/security/security-bulletins/AWS-2025-015/) - AWS bulletin on a malicious prompt merged into the Amazon Q VS Code extension release.
- [Comet browser indirect prompt injection](https://brave.com/blog/comet-prompt-injection/) - Brave's disclosure of webpage content hijacking an agentic browser to reach user accounts.
- [Cursor MCPoison (CVE-2025-54136)](https://research.checkpoint.com/2025/cursor-vulnerability-mcpoison/) - Check Point Research on silently swapping an approved MCP config for a malicious command.
- [CurXecute: RCE in Cursor via MCP auto-start (CVE-2025-54135)](https://www.catonetworks.com/blog/curxecute-rce/) - Aim Labs writeup of prompt injection writing an MCP config that Cursor executed before approval.
- [Disrupting the first reported AI-orchestrated cyber espionage campaign](https://www.anthropic.com/news/disrupting-AI-espionage) - Anthropic threat intelligence report on a state actor using an agentic coding tool to run intrusions.
- [EchoLeak advisory (CVE-2025-32711)](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2025-32711) - Microsoft's advisory for the M365 Copilot information disclosure fixed server-side.
- [EchoLeak: zero-click Microsoft 365 Copilot exfiltration](https://www.catonetworks.com/blog/breaking-down-echoleak/) - Aim Labs breakdown of an email-borne injection that leaked Copilot context through an allowed domain.
- [ForcedLeak in Salesforce Agentforce](https://noma.security/blog/forcedleak-agent-risks-exposed-in-salesforce-agentforce/) - Noma Security on web-to-lead form injection and an expired allowlisted domain used to exfiltrate CRM data.
- [Gemini CLI code execution via deception](https://tracebit.com/blog/code-exec-deception-gemini-ai-cli-hijack) - Tracebit on a README injection plus an allowlist bypass that ran hidden commands in Gemini CLI.
- [GitHub Copilot remote code execution via prompt injection (CVE-2025-53773)](https://embracethered.com/blog/posts/2025/github-copilot-remote-code-execution-via-prompt-injection/) - Injection that flipped Copilot into auto-approve mode by editing workspace settings.
- [GitHub MCP exploited: accessing private repositories](https://invariantlabs.ai/blog/mcp-github-vulnerability) - Invariant Labs on a malicious public issue making an agent leak private repository data through the GitHub MCP server.
- [GitLab Duo remote prompt injection](https://www.legitsecurity.com/blog/remote-prompt-injection-in-gitlab-duo) - Legit Security on hidden comments steering GitLab Duo to leak private source code.
- [Google Bard data exfiltration](https://embracethered.com/blog/posts/2023/google-bard-data-exfiltration/) - Early demonstration of markdown image rendering as an exfiltration channel from a chat assistant.
- [Jumping the line: how MCP servers can attack you before you use them](https://blog.trailofbits.com/2025/04/21/jumping-the-line-how-mcp-servers-can-attack-you-before-you-ever-use-them/) - Trail of Bits on tool descriptions injecting instructions at connect time.
- [M365 Copilot prompt injection and ASCII smuggling](https://embracethered.com/blog/posts/2024/m365-copilot-prompt-injection-tool-invocation-and-data-exfil-using-ascii-smuggling/) - Chain combining automatic tool invocation with invisible Unicode tags to exfiltrate data.
- [MCP Inspector RCE (CVE-2025-49596)](https://www.oligo.security/blog/critical-rce-vulnerability-in-anthropic-mcp-inspector-cve-2025-49596) - Oligo Security on an unauthenticated local proxy reachable from a browser page.
- [mcp-remote OS command injection (CVE-2025-6514)](https://jfrog.com/blog/2025-6514-critical-mcp-remote-rce-vulnerability/) - JFrog on a malicious MCP server triggering command execution on the client through an OAuth URL.
- [Month of AI Bugs](https://embracethered.com/blog/posts/2025/announcement-the-month-of-ai-bugs/) - Series of disclosures across AI coding agents and assistants, one per day for August 2025.
- [Nx s1ngularity postmortem](https://nx.dev/blog/s1ngularity-postmortem) - Postmortem of compromised npm releases that used installed AI CLIs to hunt for secrets.
- [Postmark-mcp analysis](https://snyk.io/blog/malicious-mcp-server-on-npm-postmark-mcp-harvests-emails/) - Snyk analysis of the first documented malicious MCP server on npm.
- [Postmark: malicious postmark-mcp package](https://postmarkapp.com/blog/information-regarding-malicious-postmark-mcp-package) - Vendor notice on an impersonating MCP server that blind-copied all outgoing email.
- [Rules File Backdoor](https://www.pillar.security/blog/new-vulnerability-in-github-copilot-and-cursor-how-hackers-can-weaponize-code-agents) - Pillar Security on hidden Unicode in agent rule files steering Copilot and Cursor output.
- [Slack AI data exfiltration](https://promptarmor.substack.com/p/data-exfiltration-from-slack-ai-via) - PromptArmor on injection in public channels leaking private channel data through Slack AI.
- [Slopsquatting](https://socket.dev/blog/slopsquatting-how-ai-hallucinations-are-fueling-a-new-class-of-supply-chain-attacks) - Socket on attackers registering package names that coding assistants hallucinate.
- [SpAIware: persistent exfiltration via ChatGPT memory](https://embracethered.com/blog/posts/2024/chatgpt-macos-app-persistent-data-exfiltration/) - Injection that planted instructions in long-term memory to exfiltrate future chats.
- [Supabase MCP can leak your entire SQL database](https://www.generalanalysis.com/blog/supabase-mcp-blog) - General Analysis on support ticket text driving a privileged MCP agent to leak tables.
- [The lethal trifecta for AI agents](https://simonwillison.net/2025/Jun/16/the-lethal-trifecta/) - Simon Willison on why private data, untrusted content, and external communication together enable exfiltration.
- [Tool poisoning attacks](https://invariantlabs.ai/blog/mcp-security-notification-tool-poisoning-attacks) - Invariant Labs disclosure of hidden instructions in MCP tool descriptions.
- [Vulnerable MCP Project](https://vulnerablemcp.info/) - Community database of MCP vulnerabilities and security research.
- [WhatsApp MCP exploited](https://invariantlabs.ai/blog/whatsapp-mcp-exploited) - Invariant Labs on a malicious MCP server exfiltrating message history through a trusted WhatsApp server.

## Defensive Tools

- [Agent Scan](https://github.com/snyk/agent-scan) - Scanner for MCP servers, agent configs, and skills that flags tool poisoning and toxic flows (formerly mcp-scan).
- [Agentic Radar](https://github.com/splx-ai/agentic-radar) - Static scanner that maps agent workflows, tools, and MCP servers and reports vulnerabilities.
- [CaMeL reference implementation](https://github.com/google-research/camel-prompt-injection) - Research code for the capability-based CaMeL defense against prompt injection.
- [Claude Code Security Review](https://github.com/anthropics/claude-code-security-review) - GitHub Action that runs a security review of pull request changes.
- [Docker MCP Gateway](https://github.com/docker/mcp-gateway) - Runs MCP servers in isolated containers behind a single gateway with secrets and policy controls.
- [E2B](https://github.com/e2b-dev/E2B) - Open-source cloud sandboxes for running agent-generated code in isolated microVMs.
- [Firecracker](https://github.com/firecracker-microvm/firecracker) - Lightweight microVM monitor used to isolate untrusted workloads such as agent code execution.
- [garak](https://github.com/NVIDIA/garak) - LLM vulnerability scanner that probes for prompt injection, data leakage, and jailbreaks.
- [Guardrails AI](https://github.com/guardrails-ai/guardrails) - Framework of input and output validators for LLM applications.
- [gVisor](https://github.com/google/gvisor) - User-space application kernel that sandboxes containers running untrusted code.
- [Invariant Guardrails](https://github.com/invariantlabs-ai/invariant) - Rule-based guardrail layer that checks agent traces and tool calls against policies.
- [Llama Prompt Guard 2](https://huggingface.co/meta-llama/Llama-Prompt-Guard-2-86M) - Small classifier model for detecting prompt injection and jailbreak inputs.
- [LLM Guard](https://github.com/protectai/llm-guard) - Input and output scanners for injection, secrets, and PII (archived, still usable as reference).
- [MCP Context Protector](https://github.com/trailofbits/mcp-context-protector) - Trail of Bits wrapper that pins MCP server tool descriptions and sanitizes tool output.
- [MCP Scanner](https://github.com/cisco-ai-defense/mcp-scanner) - Cisco scanner that inspects MCP servers and tools for security findings.
- [Model Transparency](https://github.com/sigstore/model-transparency) - Sigstore project for signing and verifying ML models to secure the model supply chain.
- [ModelScan](https://github.com/protectai/modelscan) - Scans serialized model files for unsafe code before loading.
- [NeMo Guardrails](https://github.com/NVIDIA-NeMo/Guardrails) - Toolkit for programmable input, output, and dialog rails around LLM applications.
- [Presidio](https://github.com/data-privacy-stack/presidio) - Detects and redacts PII in text and images before it reaches or leaves a model.
- [promptfoo](https://github.com/promptfoo/promptfoo) - Test and red teaming tool for prompts, agents, and RAG pipelines with CI integration.
- [PurpleLlama](https://github.com/meta-llama/PurpleLlama) - Meta's LLM security tools including LlamaFirewall, Llama Guard, and CyberSecEval.
- [PyRIT](https://github.com/microsoft/PyRIT) - Microsoft's Python Risk Identification Tool for red teaming generative AI systems.
- [Sandbox Runtime](https://github.com/anthropics/sandbox-runtime) - OS-level filesystem and network sandbox for arbitrary processes, used by Claude Code.
- [ToolHive](https://github.com/stacklok/toolhive) - Runs and manages MCP servers in containers with permission profiles and secret handling.
- [Vigil](https://github.com/deadbits/vigil-llm) - Detects prompt injections and risky inputs with vector similarity, YARA, and heuristics (unmaintained since 2024).

## Contributing

Contributions are welcome. Open a pull request with a link to the source for any change.

## License

[![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)

---

Maintained by [Ali Hesari](https://alihesari.com). Follow on [GitHub](https://github.com/alihesari) and [X](https://x.com/alihesari) for updates.
