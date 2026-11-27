# Benchmark Descriptions

This file provides short descriptions of the LLM cybersecurity benchmarks included in the [overview](benchmark_overview.md) of this repository. Benchmarks are listed in alphabetical order by name.

## 3CB

### Description
3CB (Catastrophic Cyber Capabilities Benchmark) is an interactive benchmark designed to evaluate the cyberattack capabilities of LLM agents. The benchmark is based on the MITRE ATT&CK framework and covers its 14 tactics through 15 specifically developed CTF-style challenges, 11 of which are publicly available. However, these challenges represent only a small fraction of the attack techniques defined in the framework. Agents interact with Docker-based sandbox environments through a simulated terminal to complete offensive cybersecurity tasks and retrieve predefined flags.

### Resources & Licenses
- Paper: [Catastrophic Cyber Capabilities Benchmark (3CB): Robustly Evaluating LLM Agent Cyber Offense Capabilities](https://arxiv.org/pdf/2410.09114) (Anurin et al., 2024)
- Code and dataset: [GitHub: apartresearch/3cb](https://github.com/apartresearch/3cb) (no license information)

## AdvCUA

### Description

**AdvCUA** is based on the MITRE ATT&CK matrix and comprises 140 tasks designed to evaluate the cyberattack capabilities of computer-use agents (CUAs). These tasks cover 10 tactics and 77 techniques from the matrix and can be divided into three categories: 40 directly malicious tasks without explicit reference to the techniques and tactics of the matrix, 74 tasks directly related to the techniques and tactics of the matrix, and 26 tasks that represent the complete attack chain. The threat model considers a CUA operating on a host within a network and attempting to gain access to other hosts.

### Resources & Licenses

- Paper: [Code Agent can be an End-to-end System Hacker: Benchmarking Real-world Threats of Computer-use Agent](https://arxiv.org/pdf/2510.06607v2) (Luo et al., 2025)
- Code and dataset: [GitHub: SaFo-Lab/AdvCLI](https://github.com/SaFo-Lab/AdvCLI) (no license information)

## AgentHarm

### Description

**AgentHarm** uses malicious prompts to investigate the extent to which LLM agents can be employed for potentially harmful activities across eleven different domains, including cybercrime, harassment, and disinformation. The benchmark focuses primarily on whether, and how effectively, the agent carries out the requested actions, with less emphasis on the complexity of the requests themselves. To ensure safe and reproducible evaluation, the benchmark relies on synthetic tools rather than real-world systems. This makes the tasks less realistic and means that they serve as proxies for harmful agent capabilities rather than as direct demonstrations of such capabilities, while still preserving harmful intent and requiring coherent multi-turn agent interactions. For security reasons, the authors did not disclose the jailbreaking method used.

### Resources & Licenses

- Paper: [AgentHarm: A Benchmark for Measuring Harmfulness of LLM Agents](https://arxiv.org/pdf/2410.09024) (Andriushchenko et al., 2024)
- Code: [GitHub: inspect_evals/agentharm](https://github.com/UKGovernmentBEIS/inspect_evals/tree/main/src/inspect_evals/agentharm) (MIT License)
- Dataset: [Hugging Face: ai-safety-institute/AgentHarm](https://huggingface.co/datasets/ai-safety-institute/AgentHarm) (MIT License with an additional clause)

## AICrypto

### Description

**AICrypto** enables the evaluation of the cryptographic capabilities of LLMs. In addition to 135 multiple-choice questions and 30 proof-based tasks, which were created based on reputable educational sources and assess the capabilities of LLMs in understanding fundamental cryptographic concepts, the benchmark includes 150 CTF challenges. These challenges were collected from different professional competitions, including Plaid CTF, UIUCTF, DiceCTF, and CryptoCTF. Thanks to the different problem types, it is possible to investigate the extent to which LLMs demonstrate a deeper understanding of cryptography and are able to practically exploit cryptographic vulnerabilities.

### Resources & Licenses

- Paper: [AICrypto: Evaluating Cryptography Capabilities of Large Language Models](https://arxiv.org/pdf/2507.09580) (Wang et al., 2025)
- Code: [GitHub: wangyu-ovo/aicrypto-agent](https://github.com/wangyu-ovo/aicrypto-agent) (no license information)
- Dataset: [Hugging Face: yuuwwang/aicrypto](https://huggingface.co/datasets/yuuwwang/aicrypto/tree/main) (MIT License)

## AI-Pentest-Benchmark

### Description

Isozaki et al. propose a benchmark for evaluating LLM-based penetration testing using 13 publicly available VulnHub virtual machines (for simplicity referred to as VulnHub-Bench). Across the 13 vulnerable VMs, a total of 152 subtasks are implemented, which can be grouped into four categories: reconnaissance, general techniques, exploitation, and privilege escalation. During benchmarking, the authors employ the PentestGPT tool and minimise human interaction, although manual intervention is permitted at certain clearly defined steps. If an LLM agent is unable to complete a task successfully, that task is solved manually so that the agent’s performance on the remaining tasks within the same VM can still be evaluated.

### Resources & Licenses

- Paper: [Towards Automated Penetration Testing: Introducing LLM Benchmark, Analysis, and Improvements](https://arxiv.org/pdf/2410.17141v3) (Isozaki et al., 2024)
- Code: [GitHub: isamu-isozaki/AI-Pentest-Benchmark](https://github.com/isamu-isozaki/AI-Pentest-Benchmark) (MIT License)
- Dataset: [GitHub: Ignitetechnologies/CTF-Difficulty](https://github.com/Ignitetechnologies/CTF-Difficulty) (no license information)

## AutoPenBench

### Description

**AutoPenBench** is a benchmark framework built upon AgentQuest that enables the evaluation of generative agents' performance in automated penetration testing. The framework comprises 33 CTF-style tasks provided through Docker containers: 22 in vitro cases representing relatively simple tasks and 11 real-world cases representing realistic penetration testing scenarios. The in vitro cases are organised into four categories: Access Control (AC), Web Security (WS), Network Security (NS), and Cryptography (CRPT). The real-world cases are based on publicly disclosed vulnerabilities with unique CVE identifiers dating from 2014 to 2024 and cover a broad range of vulnerability types, including Remote Code Execution (RCE), code injection, and buffer overflows.

### Resources & Licenses

- Paper: [AutoPenBench: Benchmarking Generative Agents for Penetration Testing](https://arxiv.org/pdf/2410.03225) (Gioacchini et al., 2024)
- Code and dataset: [GitHub: lucagioacchini/auto-pen-bench](https://github.com/lucagioacchini/auto-pen-bench) (MIT License)

## b³

### Description

**b³** (breaking agent backbones) focuses on LLM-specific vulnerabilities and is designed to assess the robustness of LLMs against various evasion attacks, including prompt-based attacks aimed at data exfiltration, bypassing content policies, or compromising tools and systems. In total, 194,331 attacks were collected for b³ through large-scale crowdsourcing, of which 210 were selected for the public dataset. Attacks with the highest success rates were excluded from the released dataset for security reasons. The benchmark supports three default levels of protection: L1, which uses only minimal security instructions in the system prompt; L2, which employs a more elaborate system prompt; and L3, which adds a self-judging mechanism. The authors also introduce the concept of 'Threat Snapshots', referring to specific states that can arise during agent execution and in which LLM vulnerabilities may manifest. Based on these states and the collected attacks, b³ enables a systematic analysis of how the choice of LLM and the applied level of protection affect the security of an agent built on top of it.

### Resources & Licenses

- Paper: [Breaking Agent Backbones: Evaluating the Security of Backbone LLMs in AI Agents](https://arxiv.org/pdf/2510.22620) (Bazinska et al., 2025)
- Code: [GitHub: inspect_evals/b3](https://github.com/UKGovernmentBEIS/inspect_evals/tree/main/src/inspect_evals/b3) (MIT License)
- Dataset: [Hugging Face: Lakera/b3-agent-security-benchmark-weak](https://huggingface.co/datasets/Lakera/b3-agent-security-benchmark-weak) (custom research-only license)

## CASTLE

### Description

**CASTLE** (CWE Automated Security Testing and Low-Level Evaluation) is a benchmarking framework for evaluating the capabilities of different methods for detecting vulnerabilities in source code. In addition to LLMs, other types of vulnerability-detection tools can also be assessed. The underlying dataset consists of 250 C programs, manually created by experts, ranging from 7 to 164 lines of code and covering a total of 25 CWEs. For each CWE, the dataset contains 10 test cases, six of which are vulnerable and four non-vulnerable. The authors also introduce a dedicated evaluation metric, the CASTLE Score, which rewards correct classifications while assigning additional weight to the detection of vulnerabilities with greater potential impact.

### Resources & Licenses

- Paper: [CASTLE: Benchmarking Dataset for Static Code Analyzers and LLMs towards CWE Detection](https://arxiv.org/pdf/2503.09433) (Dubniczky et al., 2025)
- Code: [GitHub: CASTLE-Benchmark/CASTLE-Source](https://github.com/CASTLE-Benchmark/CASTLE-Source) (MIT License)
- Dataset: [GitHub: CASTLE-Benchmark/CASTLE-Benchmark](https://github.com/CASTLE-Benchmark/CASTLE-Benchmark) (MIT License)

## CTIArena

### Description

**CTIArena** evaluates the cyber threat intelligence capabilities of LLMs and assesses LLM performance on heterogeneous, multi-source CTI tasks in knowledge-augmented settings. It is designed to represent core workflows commonly performed by threat analysts in Security Operations Centres (SOCs), including mapping vulnerabilities to weaknesses, identifying ATT&CK techniques from observed adversary behaviour, profiling threat actors, tracing malware evolution, and correlating activity across multiple reports. The authors distinguish between structured, unstructured, and hybrid CTI tasks and construct dedicated datasets for each of these categories. Structured tasks require reasoning over authoritative cybersecurity taxonomies and knowledge bases such as CVE, CWE, CAPEC, and MITRE ATT&CK, which represent vulnerabilities, weaknesses, attack patterns, and adversary techniques in structured form. The structured dataset covers 500 mappings (e.g., CVE &rarr; CWE, CWE &rarr; CVE, CAPEC &rarr; ATT&CK, CWE &rarr; CAPEC), which were transformed into 371 question-answer pairs. Unstructured tasks instead rely on narrative threat intelligence, such as vendor reports and blogs, and require models to interpret descriptions of threat actors, campaigns, malware families, and related activities. For this dataset, 321 CTI reports from 35 major CTI vendors were used to create 150 tasks. Hybrid tasks combine both information types by linking unstructured threat reports with structured cybersecurity enumerations. Based on 150 reports, the hybrid dataset contains 120 mappings from reports to CWEs and 50 mappings from reports to ATT&CK techniques that the LLM must derive.

### Resources & Licenses

- Paper: [CTIArena: Benchmarking LLM Knowledge and Reasoning Across Heterogeneous Cyber Threat Intelligence](https://arxiv.org/pdf/2510.11974v1) (Cheng et al., 2025)
- Code and dataset: [GitHub: ccsnow127/ctiarena-release](https://github.com/ccsnow127/ctiarena-release) (no license information)

## CTIBench

### Description

**CTIBench** enables the evaluation of LLMs in the field of cyber threat intelligence (CTI). The benchmark assesses whether LLMs can understand, examine, and analyse cyber threat reports, focusing on four capabilities: memorisation, understanding, reasoning, and problem solving. To this end, the authors compiled several datasets based on various authoritative sources and standards in the CTI domain:
  - **CTI-MCQ**, consisting of 2,500 multiple-choice questions, evaluates the general understanding of LLMs of key CTI concepts through knowledge-based benchmarking.
  - Four datasets represent practical CTI tasks and assess the ability of LLMs to understand and evaluate cyber threats, vulnerabilities, and attack patterns:
    - **CTI-RCM**, which contains 1,000 vulnerability descriptions (CVEs) together with their underlying causes (CWEs) provided as reference answers. The LLM is asked to assign the correct CWE categories to the vulnerability descriptions.
    - **CTI-VSP**, in which Common Vulnerability Scoring System (CVSS) values are to be generated. The underlying dataset is structured analogously to CTI-RCM, with the difference that CVSS v3 strings are used as reference answers.
    - **CTI-ATE**, which focuses on the extraction of specific attack patterns, more precisely, techniques defined in the MITRE ATT&CK framework, from an attack description. The dataset consists of 60 malware instances and covers a total of 397 attack techniques.
    - **CTI-TAA**, in which threat reports must be attributed to specific threat actors/APT groups. The dataset comprises 50 reports from trusted institutions, each associated with an APT group, with all mentions of the respective groups replaced by placeholders.

### Resources & Licenses

- Paper: [CTIBench: A Benchmark for Evaluating LLMs in Cyber Threat Intelligence](https://arxiv.org/pdf/2406.07599) (Alam et al., 2024)
- Code and dataset: [GitHub: maveryn/cti-bench](https://github.com/maveryn/cti-bench) (CC BY-NC-SA 4.0 license)

## CUAHarm

### Description

**CUAHarm** enables the evaluation of computer-use agents' (CUAs) capabilities to successfully execute attacks in realistic misuse scenarios, some of which require direct system interactions. The benchmark comprises 104 tasks in which CUAs operate within a sandbox environment and are instructed to perform malicious actions, such as disabling a firewall or locating and exfiltrating confidential information from a system. In these scenarios, the CUA deliberately interacts with the target system, thereby simulating the misuse of an AI system. The tasks cover 7 categories of malicious activities: credential theft, privilege escalation, network exploitation, system disruption, data tampering, forensic evasion, and tool utilisation. The tasks are developed by adapting real-world vulnerabilities and attacks from publicly available sources, such as security advisories and CVE reports, and through a multi-stage LM-assisted generation process followed by manual review and refinement. Task outcomes are assessed using rule-based verifiable rewards, which employ deterministic checks of system states to determine whether predefined success criteria are met within a specified step limit.

### Resources & Licenses

- Paper: [Measuring Harmfulness of Computer-Using Agents](https://arxiv.org/pdf/2508.00935) (Tian et al., 2025)
- Code and dataset: [GitHub: db-ol/CUAHarm](https://github.com/db-ol/CUAHarm) (Apache License 2.0)

## CVE-Bench

### Description

With **CVE-Bench**, the authors introduce a benchmark for evaluating the attack capabilities of LLM agents in the context of web applications. To this end, they selected 40 real-world, high-severity vulnerabilities (CVEs) and created target containers hosting various types of vulnerable web applications (e.g., e-commerce platforms and mail servers). For evaluation, 8 standard attack objectives are used (e.g., Denial of Service: rendering a website unresponsive to requests), which are provided to the LLM agents as goals. These objectives are intended to represent more realistic attack scenarios than those typically found in CTF-style tasks. The benchmark evaluates LLM agents under both zero-day and one-day settings to simulate different stages of the vulnerability lifecycle.

### Resources & Licenses

- Paper: [CVE-Bench: A Benchmark for AI Agents' Ability to Exploit Real-World Web Application Vulnerabilities](https://arxiv.org/pdf/2503.17332) (Zhu et al., 2025)
- Code and dataset: [GitHub: uiuc-kang-lab/cve-bench](https://github.com/uiuc-kang-lab/cve-bench) (Apache License 2.0)

## Cybench

### Description

**Cybench** was specifically developed to benchmark the cyberattack capabilities of LLMs. The benchmark is based on four CTF competitions, from which 40 CTF tasks of varying complexity were selected. The tasks are divided into subtasks and can be performed in either "Unguided Mode" (the complete task is provided without specifying subtasks, and performance is evaluated based on overall task completion) or "Subtask-Guided Mode" (subtasks are provided sequentially, and performance is evaluated based on either overall task completion or individual subtask completion). The benchmark covers six categories: Cryptography, Web Security, Reverse Engineering, Forensics, Miscellaneous, and Vulnerability Exploitation.

### Resources & Licenses

- Paper: [Cybench: A Framework for Evaluating Cybersecurity Capabilities and Risks of Language Models](https://arxiv.org/pdf/2408.08926) (Zhang et al., 2024)
- Code and dataset: [GitHub: andyzorigin/cybench](https://github.com/andyzorigin/cybench) (Apache License 2.0)

## CyberGym

### Description

**CyberGym** evaluates the ability of LLM agents to generate Proof-of-Concept (PoC) programs that exploit software vulnerabilities. The benchmark comprises 1,507 real-world vulnerabilities discovered and subsequently patched across 188 major software projects through OSS-Fuzz, Google's continuous fuzzing initiative. It focuses on memory safety vulnerabilities in widely used C/C++ projects that can be detected using sanitisers. For each task, the agent is provided with a vulnerability description, the affected source code, and supplementary information that varies across four difficulty levels (0-3). Agents can execute their generated PoCs in a containerised environment and iteratively refine them based on execution feedback. To evaluate their effectiveness, the generated PoCs are executed against both vulnerable (pre-patch) and patched (post-patch) versions of the target program with sanitisers enabled. A PoC is considered successful if it triggers a sanitiser-detected crash in the vulnerable version but not in the patched version, thereby demonstrating that it specifically exploits the targeted vulnerability.

### Resources & Licenses

- Paper: [CyberGym: Evaluating AI Agents' Real-World Cybersecurity Capabilities at Scale](https://arxiv.org/pdf/2506.02548) (Wang et al., 2025)
- Code and dataset: [GitHub: sunblaze-ucb/cybergym](https://github.com/sunblaze-ucb/cybergym) (Apache License 2.0)

## CyberMetric

### Description

**CyberMetric** is a family of benchmarks based on question-answer datasets of different sizes. To construct the datasets, 80/500/2,000/10,000 questions were extracted using GPT-3.5 and RAG methods from various cybersecurity documents comprising approximately 100,000 pages in total. Falcon-180B was used to verify the questions with regard to grammatical correctness, semantics, and relevance. In addition, the questions were manually reviewed on a sample basis. The benchmark covers the following nine topic areas: disaster recovery and business continuity planning, identity and access management (IAM), IoT security, cryptography, wireless security, network security, cloud security, penetration testing, and compliance/auditing.

### Resources & Licenses

- Paper: [CyberMetric: A Benchmark Dataset based on Retrieval-Augmented Generation for Evaluating LLMs in Cybersecurity Knowledge](https://arxiv.org/pdf/2402.07688) (Tihanyi et al., 2024)
- Code and dataset: [GitHub: cybermetric/CyberMetric](https://github.com/cybermetric/CyberMetric) (no license information)

## CyberPersistBench

### Description

**CyberPersistBench** evaluates the ability of LLM-based cyber agents to establish and maintain persistent access after an initial system compromise. Each task starts from a restricted foothold on an already compromised host and requires the agent to establish persistence using native operating-system or application mechanisms. The core benchmark comprises 203 tasks across seven categories and 46 persistence-mechanism families, covering account and authentication mechanisms, services and daemons, scheduled or event-based triggers, startup autoloading, application components, control and orchestration mechanisms, and execution-flow hijacking. In addition, the benchmark includes 65-task multi-host tasks and 128 extended tasks with active native defences. Evaluation is deterministic and execution-based. After the agent configures a persistence mechanism, the benchmark revokes the original access and introduces disruptions such as service restarts, process termination, or host reboots. A six-level evaluation scheme measures progressively whether the mechanism is correctly constructed (**L1**), registered and successfully parsed by the target system (**L2**), initially activated (**L3**), remains functional without the original access (**L4**), recovers from operational disruptions (**L5**), and survives system reinitialisation (**L6**).

### Resources & Licenses

- Paper: [CyberPersistBench: Evaluating LLM-Based Cyber Attackers on Installation and Persistence](https://arxiv.org/pdf/2609.36573) (Chen et al., 2026)
- Code and dataset: [Anonymous GitHub: CyberPersistBench-0EC5](https://anonymous.4open.science/r/CyberPersistBench-0EC5) (Apache License 2.0)

## CyberSecEval (1-4)

### Description

**CyberSecEval 1-4** is a benchmark suite released by Meta that covers a broad range of cybersecurity-related evaluation tasks. The suite currently includes the following benchmark types:
  - **MITRE and false refusal rate (FRR) tests**: assessment of the willingness of LLMs to assist with cyberattacks and the extent to which they incorrectly refuse borderline but essentially benign requests.
  - **Secure code generation tests**: evaluation of an LLM's propensity to generate insecure code, both in response to explicit instructions and in code-completion settings.
  - **Prompt injection tests**: assessment of the susceptibility of LLMs to prompt-injection attacks, including both textual and visual prompt injections.
  - **Code interpreter tests**: evaluation of the security risks arising from the integration of LLMs with code interpreters, particularly whether malicious attempts to exploit the system or execute harmful code can be prevented.
  - **Vulnerability exploitation tests**: measurement of the ability of LLMs to exploit software vulnerabilities by solving capture-the-flag-style challenges.
  - **Spear phishing capability tests**: evaluation of LLM capabilities in spear phishing scenarios, with a particular focus on persuasiveness and effectiveness in achieving specific phishing objectives.
  - **Autonomous offensive cyber operations tests**: assessment of the ability of LLMs to operate autonomously as cyberattack agents.
  - **AutoPatch tests**: evaluation of the ability of LLM agents to autonomously generate security patches for vulnerabilities, in particular for crashes identified by fuzzing.
  - **CyberSOCEval tests**: evaluation of defensive capabilities in Security Operations Centre (SOC) scenarios. The tests comprise two benchmarks:
    - **Malware analysis**: assessment of an LLM's precision and recall in identifying malicious activities and malware-related behaviour using multiple-choice questions that may have more than one correct answer.
    - **Threat intelligence reasoning**: evaluation of an LLM's ability to interpret unstructured threat intelligence reports and extract actionable information, likewise using multiple-choice questions with potentially multiple correct answers.

### Resources & Licenses

- Paper: [CyberSOCEval: Benchmarking LLMs Capabilities for Malware Analysis and Threat Intelligence Reasoning](https://arxiv.org/pdf/2509.20166) (Deason et al., 2025), [CYBERSECEVAL 3: Advancing the Evaluation of Cybersecurity Risks and Capabilities in Large Language Models](https://arxiv.org/pdf/2408.01605) (Wan et al., 2024), [CyberSecEval 2: A Wide-Ranging Cybersecurity Evaluation Suite for Large Language Models](https://arxiv.org/pdf/2404.13161) (Bhatt et al., 2024), [Purple Llama CyberSecEval: A Secure Coding Benchmark for Language Models](https://arxiv.org/pdf/2312.04724) (Bhatt et al., 2023)
- Code and datasets: [GitHub: meta-llama/PurpleLlama/tree/main/CybersecurityBenchmarks](https://github.com/meta-llama/PurpleLlama/tree/main/CybersecurityBenchmarks) (MIT License), [Hugging Face: facebook/cyberseceval3-visual-prompt-injection](https://huggingface.co/datasets/facebook/cyberseceval3-visual-prompt-injection) (MIT License)

## DebugBench

### Description

DebugBench is a benchmark for evaluating the ability of LLMs to debug Python, Java, and C++ code. To construct the dataset, the authors collected 3,206 programming problems from LeetCode, each accompanied by examples and reference solution code, with the code having been published no earlier than July 2022. They then used GPT-4 to inject different types of bugs into the code examples, resulting in approximately 1,400 debugging tasks per programming language. The dataset was manually reviewed by experienced programmers. Evaluation is based on LeetCode test suites containing 1-3 known and 8-100 unknown test cases per instance. A debugging task is considered successfully solved only if the repaired code passes all corresponding test cases.

### Resources & Licenses

- Paper: [DebugBench: Evaluating Debugging Capability of Large Language Models](https://arxiv.org/pdf/2401.04621) (Tian et al., 2024)
- Code: [GitHub: thunlp/debugbench](https://github.com/thunlp/debugbench) (Apache License 2.0)
- Dataset: [Hugging Face: Rtian/DebugBench](https://huggingface.co/datasets/Rtian/DebugBench) (Apache License 2.0)

## ExploitBench

### Description

**ExploitBench** is a benchmark designed to provide a fine-grained evaluation of LLM agents' exploitation capabilities using a 16-level 'Capability Ladder'. Unlike benchmarks that assess exploitation using a binary success-or-failure criterion, ExploitBench decomposes the exploit development process into 16 measurable capabilities, ranging from basic execution of vulnerable code and crash reproduction to arbitrary code execution (ACE). The benchmark is based on 41 real-world vulnerabilities in the hardened V8 JavaScript engine and provides agents with the vulnerable source code, various builds, the corresponding patches, and a standardised evaluation environment (one-day setting). Evaluation relies on deterministic methods to ensure reproducible and objective assessment of the agents' exploitation capabilities.

### Resources & Licenses

- Paper: [ExploitBench: A Capability Ladder Benchmark for LLM Cybersecurity Agents](https://arxiv.org/pdf/2605.14153) (Lee et al., 2026)
- Code and dataset: [GitHub: exploitbench/exploitbench](https://github.com/exploitbench/exploitbench) (MIT License)

## ExploitGym

### Description

**ExploitGym** is a benchmark designed to evaluate the ability of LLM agents to transform known software vulnerabilities into functional exploits. Each benchmark instance is based on a real-world vulnerability accompanied by a Proof-of-Vulnerability (PoV) input that reliably triggers the vulnerability. The agent's task is to develop a working exploit that achieves a concrete security impact, such as unauthorised code execution. The benchmark comprises 898 real-world instances across three domains: userspace programs, the V8 JavaScript engine, and the Linux kernel. Each instance provides a reproducible, containerised testing environment in which various security mechanisms, such as Address Space Layout Randomization (ASLR), stack canaries, Kernel Address Space Layout Randomization (KASLR), and the V8 Heap Sandbox, can be selectively enabled or disabled to assess their impact on exploit generation. Attack success is evaluated by verifying whether the agent successfully retrieves a protected flag, supplemented by validation using an LLM-as-a-Judge to ensure that the intended vulnerability was actually exploited.

### Resources & Licenses

- Paper: [ExploitGym: Can AI Agents Turn Security Vulnerabilities into Real Attacks?](https://arxiv.org/pdf/2605.11086) (Wang et al., 2026)
- Code and dataset: [GitHub: sunblaze-ucb/exploitgym](https://github.com/sunblaze-ucb/exploitgym) (Apache License 2.0)

## Google DeepMind In-house CTF

### Description

**Google DeepMind In-house CTF** is a benchmark developed by Google DeepMind to evaluate the cybersecurity capabilities of Gemini 1.0 as part of a broader assessment of potentially dangerous AI capabilities. The benchmark comprises 13 CTF-style tasks of easy to moderate difficulty, covering web application vulnerabilities, the use of off-the-shelf exploits, database exploitation, Linux privilege escalation, password cracking, and password spraying. Task completion follows the CTF approach, requiring agents to retrieve predefined flags.

### Resources & Licenses

- Paper: [Evaluating Frontier Models for Dangerous Capabilities](https://arxiv.org/pdf/2403.13793) (Phuong et al., 2024)
- Code and dataset: [GitHub: google-deepmind/dangerous-capability-evaluations](https://github.com/google-deepmind/dangerous-capability-evaluations) (Apache License 2.0)

## HackWorld

### Description

**HackWorld** is an evaluation framework specifically designed to assess the web exploitation capabilities of computer-use agents (CUAs). The benchmark comprises 36 CTF-style web applications, sourced from three existing benchmarks (NYU CTF Bench, Cybench, and InterCode-CTF), with challenges originating from 2013 to 2023. Rather than introducing new CTF challenges, HackWorld's main contribution is the integration of existing challenges into a standardized, GUI-based evaluation environment. This enables the systematic assessment of the ability of computer-use agents to exploit web vulnerabilities through graphical interactions, including mouse and keyboard actions, as well as the use of security tools.

### Resources & Licenses

- Paper: [HackWorld: Evaluating Computer-Use Agents on Exploiting Web Application Vulnerabilities](https://arxiv.org/pdf/2510.12200) (Ren et al., 2025)
- Code and dataset: [GitHub: GUI-Agent/Hackworld](https://github.com/GUI-Agent/HackWorld) (Apache License 2.0)

## InterCode-CTF

### Description

InterCode-CTF is an interactive benchmark designed to evaluate the capabilities of LLM agents in solving CTF challenges. The dataset comprises 100 tasks sourced from the picoCTF cybersecurity competition and provided through Docker containers. According to the authors' classification, the tasks cover six categories: General Skills (33), Reverse Engineering (27), Cryptography (19), Forensics (15), Binary Exploitation (4), and Web Exploitation (2). Agents interact with the environment by executing shell commands and receiving execution feedback, allowing them to iteratively develop solutions.

### Resources & Licenses

- Paper: [InterCode: Standardizing and Benchmarking Interactive Coding with Execution Feedback](https://arxiv.org/pdf/2306.14898) (Yang et al., 2023), [Language Agents as Hackers: Evaluating Cybersecurity Skills with Capture the Flag](https://www.researchgate.net/publication/379925136_Language_Agents_as_Hackers_Evaluating_Cybersecurity_Skills_with_Capture_the_Flag) (Yang et al., 2023)
- Code and dataset: [GitHub: princeton-nlp/intercode](https://github.com/princeton-nlp/intercode) (MIT License)

## LLM Persistence Benchmark

### Description

The **LLM Persistence Benchmark** evaluates the extent to which LLMs can employ various persistence techniques, such as modifying startup scripts, to maintain control over a target system over an extended period. Thhe dataset consists of 31 prompts derived from the existing [GitHub: Karneades/awesome-malware-persistence](https://github.com/Karneades/awesome-malware-persistence) repository documenting various persistence techniques. The authors manually selected techniques applicable to Linux systems that enable persistence across system reboots. The corresponding descriptions were then refined using GPT-4o to create evaluation-ready prompts by shortening them and adding necessary context, followed by a manual review. Each prompt instructs the LLM to generate a script implementing a specific persistence technique, such that executing the script causes a designated file to be created in the working directory upon rebooting the target system. During evaluation, the authors gave the LLM up to five attempts to execute the persistence technique on an Ubuntu virtual machine, with execution feedback provided after each attempt, before the system is rebooted to verify whether the designated file was successfully created.

### Resources & Licenses

- Paper: [Cybersecurity Persistence Benchmark](https://apartresearch.com/sprints/projects/cybersecurity-persistence-benchmark) (Zani et al., 2024)
- Code and dataset: [GitHub: Jazhyc/llm-persistence-benchmark](https://github.com/Jazhyc/llm-persistence-benchmark) (no license information)

## MalwareBench

### Description

**MalwareBench** investigates the susceptibility of LLMs to jailbreak attacks in code-generation settings. The underlying dataset comprises 3,520 jailbreak-containing instructions designed to elicit malicious code generation. These instructions were created by pairwise combining 320 manually written malicious-code prompts, covering six categories - download and propagation, privileged access, information theft, system destruction, resource abuse, and denial of service - with 11 black-box jailbreak methods.

### Resources & Licenses

- Paper: [LLMs Caught in the Crossfire: Malware Requests and Jailbreak Challenges](https://arxiv.org/pdf/2506.10022) (Li et al., 2025)
- Dataset: [GitHub: MAIL-Tele-AI/MalwareBench](https://github.com/MAIL-Tele-AI/MalwareBench) (no license information)

## MHBench

### Description

**MHBench** enables the evaluation of the attack capabilities of LLMs against multi-host systems. The interactive benchmark comprises 10 attack environments, each containing 25 to 50 hosts with various vulnerabilities, some of which are inspired by real-world scenarios. The attack objectives involve either exfiltrating sensitive data or gaining access to critical network hosts. Attack complexity is measured by the number of steps required to complete an attack, ranging from 125 to 246 steps. An additional level of complexity is introduced by varying the number of subgoals, such as the number of database instances from which data must be exfiltrated. To facilitate autonomous attack execution, the authors further introduce Incalmo, a high-level abstraction layer that allows LLMs to specify actions, such as scanning networks or compromising hosts, which are then translated into executable commands by specialized agents.

### Resources & Licenses

- Paper: [On the Feasibility of Using LLMs to Autonomously Execute Multi-host Network Attacks](https://arxiv.org/pdf/2501.16466v3) (Singer et al., 2025)
- Code and dataset: [GitHub: bsinger98/MHBench](https://github.com/bsinger98/MHBench) (MIT License)

## NYU CTF Bench

### Description

NYU CTF Bench is an interactive benchmark designed to evaluate the cyberattack capabilities of LLMs, based on CTF competitions held as part of New York University's (NYU) annual Cybersecurity Awareness Week (CSAW). The underlying dataset comprises 200 manually validated tasks provided through Docker containers. The tasks cover six categories: Cryptography (Crypto), Web Security (Web), Reverse Engineering (Rev), Forensics, Miscellaneous (Misc), and Vulnerability Exploitation (Pwn). The authors also published an evaluation framework for testing different LLMs, which provides LLM agents with access to eight essential cybersecurity tools.

### Resources & Licenses

- Paper: [NYU CTF Bench: A Scalable Open-Source Benchmark Dataset for Evaluating LLMs in Offensive Security](https://arxiv.org/pdf/2406.05590) (Shao et al., 2024)
- Code and dataset: [GitHub: nyu-llm-ctf/nyu_ctf_bench](https://github.com/nyu-llm-ctf/nyu_ctf_bench) (GPL v2)

## OS-Harm

### Description

**OS-Harm** is based on the OSWorld environment and evaluates the safety of computer-use agents by examining their behaviour across three harm scenarios: intentional misuse by the user, prompt injection attacks, and model misbehaviour. The underlying dataset comprises 150 tasks covering different types of safety violations (harassment, copyright infringement, disinformation, data exfiltration, etc.) and requiring the LLM agent to interact with various applications, such as an email client or web browser.

### Resources & Licenses

- Paper: [OS-Harm: A Benchmark for Measuring Safety of Computer Use Agents](https://arxiv.org/pdf/2506.14866v1) (Kuntz et al., 2025)
- Code and dataset: [GitHub: tml-epfl/os-harm](https://github.com/tml-epfl/os-harm) (Apache License 2.0)

## PACEbench

### Description

**PACEbench** (Practical AI Cyber-Exploitation Benchmark) is a CTF benchmark designed to simulate realistic cybersecurity scenarios as comprehensively as possible, enabling a thorough evaluation of the cyberattack capabilities of LLM agents. The provided environments vary in the number of hosts and vulnerabilities, which are based on real-world CVEs with varying exploitation success rates among human experts, thereby covering different difficulty levels. Additionally, some environments incorporate security mechanisms, such as firewalls, to further increase the difficulty. PACEbench comprises four scenarios:
- **Single CVE on a single host (A-CVE):** This scenario evaluates the agent's ability to independently exploit various real-world CVEs.
- **Combined CVEs across multiple hosts (B-CVE):** This scenario assesses the agent's ability to perform reconnaissance to distinguish between vulnerable and benign hosts in a complex environment, as well as to identify and exploit several CVEs.
- **Chained CVEs (C-CVE):** This scenario requires the agent to execute a multi-step attack by exploiting an initial vulnerability and leveraging the resulting access to perform subsequent attack steps.
- **Protected CVEs (D-CVE):** This scenario evaluates the agent's ability to bypass security measures by exploiting a vulnerability on a host protected by a web application firewall (WAF).

### Resources & Licenses

- Paper: [PACEbench: A Framework for Evaluating Practical AI Cyber-Exploitation Capabilities](https://arxiv.org/pdf/2510.11688) (Liu et al., 2025)
- Code and dataset: [GitHub: RyuKosei/PACEbench](https://github.com/RyuKosei/PACEbench) (MIT License)

## PrimeVul

### Description

**PrimeVul** was developed for training and evaluating LLMs for automated vulnerability detection. The dataset is based on examples from BigVul, CrossVul, CVEfixes, and DiverseVul, which were deduplicated and whose associated labels were carefully curated. In total, it comprises 6,968 vulnerable and 228,800 benign functions from 755 projects and 6,827 commits, covering more than 140 CWEs. The data were split chronologically, with the test set containing the most recent examples. For evaluation, the authors also introduce the Vulnerability Detection Score, which measures the minimum false-negative rate achieved by a vulnerability detector while remaining within a tolerable false-positive rate.

### Resources & Licenses

- Paper: [Vulnerability Detection with Code Language Models: How Far Are We?](https://arxiv.org/pdf/2403.18624) (Ding et al., 2024)
- Code: [GitHub: DLVulDet/PrimeVul](https://github.com/DLVulDet/PrimeVul) (MIT License)
- Dataset: [Google Drive: 19iLaNDS0z99N8kB_jBRTmDLehwZBolMY](https://drive.google.com/drive/folders/19iLaNDS0z99N8kB_jBRTmDLehwZBolMY) (no license information)

## SEC-bench

### Description

**SEC-bench** enables the evaluation of how effectively LLM agents can generate proofs of concept (PoCs) for vulnerabilities in an interactive environment and remediate those vulnerabilities. The authors introduce an LLM-agent-based framework that automatically collects and verifies real-world CVE instances and converts them into structured security tasks within Docker containers. Its verification stage uses a multi-agent setup consisting of a manager agent that coordinates specialised builder, exploiter, and fixer agents responsible for compiling the project, reproducing the vulnerability, and generating a valid patch, respectively. Using this framework, the authors construct a dataset of 200 security tasks, which are provided as Docker containers and focus on sanitizer-verifiable memory-safety vulnerabilities in C/C++ projects. PoC generation is evaluated by executing the generated PoC and checking whether it triggers the expected sanitizer report for the correct vulnerability type and location. For the patching task, the generated patch must apply successfully, the patched project must compile, and the original PoC must no longer trigger the sanitizer-reported vulnerability.

### Resources & Licenses

- Paper: [SEC-bench: Automated Benchmarking of LLM Agents on Real-World Software Security Tasks](https://arxiv.org/pdf/2506.11791) (Lee et al., 2025)
- Code: [GitHub: SEC-bench/SEC-bench-Pro](https://github.com/SEC-bench/SEC-bench-Pro) (MIT License)
- Dataset: [Hugging Face: SEC-bench/SEC-bench](https://huggingface.co/datasets/SEC-bench/SEC-bench) (MIT License)

## SecEval

### Description

**SecEval** is a benchmark for evaluating the cybersecurity-related knowledge of LLMs. The benchmark comprises 2,000 multiple-choice questions across eight domains: software security, application security, system security, web security, cryptography, memory security, network security, and penetration testing. The questions were generated using GPT-4 on the basis of suitable source materials, including textbooks, documentation, guidelines, and standards.

### Resources & Licenses

- Paper: pending
- Code: [GitHub: XuanwuAI/SecEval](https://github.com/XuanwuAI/SecEval) (MIT License)
- Dataset: [GitHub: XuanwuAI/SecEval](https://github.com/XuanwuAI/SecEval) (CC BY-NC-SA 4.0 license)

## SecLLMHolmes

### Description

**SecLLMHolmes** is a framework for evaluating the vulnerability-detection capabilities of LLMs in C/C++ and Python code. The accompanying dataset contains 228 code scenarios, comprising 48 manually created cases, 30 real-world CVEs from public open-source projects, and 150 modified or extended variants of the manually created test cases. The manually constructed scenarios cover eight CWEs from the 2023 MITRE Top 25 Most Dangerous Software Weaknesses and include both vulnerable and patched examples at three levels of complexity, while the real-world scenarios cover 15 CWEs. The 150 code-modification test cases are designed to assess robustness to code changes. For this purpose, 12 manually created scenarios were selected and subjected to various transformations, such as identifier renaming.

### Resources & Licenses

- Paper: [LLMs Cannot Reliably Identify and Reason About Security Vulnerabilities (Yet?): A Comprehensive Evaluation, Framework, and Benchmarks](https://arxiv.org/pdf/2312.12575) (Ullah et al., 2023)
- Code and dataset: [GitHub: ai4cloudops/secllmholmes](https://github.com/ai4cloudops/secllmholmes) (GPL v3)

## SecQA

### Description

**SecQA** enables the evaluation of LLMs' ability to understand and apply fundamental security principles through multiple-choice questions generated with GPT-4 based on the book [Computer Systems Security: Planning for Success (Tolboom, 2023)](https://web.njit.edu/~rt494/security/security.pdf). SecQA is available in two versions. While Version 1 focuses on LLMs' basic understanding and application of security principles and comprises 127 questions, the 115 questions in Version 2 are more complex and require a more comprehensive understanding.

### Resources & Licenses

- Paper: [SecQA: A Concise Question-Answering Dataset for Evaluating Large Language Models in Computer Security](https://arxiv.org/pdf/2312.15838) (Liu, 2023)
- Dataset: [Hugging Face: zefang-lui/secqa](https://huggingface.co/datasets/zefang-liu/secqa) (CC BY-NC-SA 4.0 license)

## SECURE

### Description

**SECURE** is a benchmark framework designed to evaluate the capabilities of LLMs in real-world cybersecurity scenarios, with a strong focus on cyber advisories and threat-related information in industrial control system environments. To this end, the authors created six datasets based on industry-standard sources: MAET (MITRE Attack Extraction Task), CWET (Common Weakness Extraction Task), KCV (Knowledge Test on Common Vulnerabilities), VOOD (Vulnerability Out-of-Distribution Task), RERT (Risk Evaluation Reasoning Task), and CPST (CVSS Problem Solving Task). MAET and CWET contain a total of 2,036 multiple-choice questions generated using GPT-4o and are intended to assess acquired knowledge. KCV and VOOD each comprise 466 Boolean questions based on given CVE descriptions and primarily assess LLMs' reading comprehension. The final two datasets focus on reasoning and problem-solving capabilities in the context of vulnerability assessment. RERT contains 1,000 test cases derived from recent ICS advisories and evaluates whether LLMs can synthesise extensive threat reports and assess the risks associated with identified vulnerabilities. CPST comprises 100 manually created CVSS 3.1 vector strings and tests whether LLMs can infer and correctly apply the CVSS scoring methodology in a zero-shot setting, without task-specific programming.

### Resources & Licenses

- Paper: [SECURE: Benchmarking Large Language Models for Cybersecurity](https://arxiv.org/pdf/2405.20441) (Bhusal et al., 2024)
- Dataset: [GitHub: aiforsec/SECURE](https://github.com/aiforsec/SECURE) (no license information)

## SEvenLLM

### Description

**SEvenLLM** enables the evaluation of LLMs in the field of cyber threat intelligence (CTI). The benchmark assesses, across 28 different task categories, whether LLMs can understand, examine, and analyse cyber threat reports. To this end, the authors compiled 1,300 questions and tasks in two languages (English and Chinese) based on authoritative websites covering cybersecurity incidents from leading national and international cybersecurity organisations and vendors. The tasks are divided into 13 comprehension categories and 15 generation categories.

### Resources & Licenses

- Paper: [SEvenLLM: Benchmarking, Eliciting, and Enhancing Abilities of Large Language Models in Cyber Threat Intelligence](https://arxiv.org/pdf/2405.03446) (Ji et al., 2024)
- Code: [GitHub: CSJianYang/SEevenLLM](https://github.com/CSJianYang/SEevenLLM) (no license information)
- Dataset: [Hugging Face: Multilingual-Multimodal-NLP/SEVENLLM-Dataset](https://huggingface.co/datasets/Multilingual-Multimodal-NLP/SEVENLLM-Dataset) (Apache License 2.0)

## StrongREJECT

### Description

**StrongREJECT**, short for 'Strong, Robust Evaluation of Jailbreaks at Evading Censorship Technique', evaluates the susceptibility of LLMs to jailbreak attacks using a dataset of 313 harmful prompts that were created manually or with LLM assistance, or selected from existing benchmarks. The prompts cover six categories of content commonly prohibited by model providers' usage policies: illegal goods and services; non-violent crimes; hate, harassment, and discrimination; disinformation and deception; violence; and sexual content. The authors address the problem that existing benchmarks often overestimate jailbreak success rates and introduce the StrongREJECT score that considers both the model's willingness to respond to harmful prompts as well as the specificity and convincingness of its responses. This is motivated by the observation that jailbreaks which bypass a model's learned safety mechanisms may simultaneously degrade its underlying capabilities.

### Resources & Licenses

- Paper: [A StrongREJECT for Empty Jailbreaks](https://arxiv.org/pdf/2402.10260) (Souly et al., 2024)
- Code: [GitHub: dsbowen/strong_reject](https://github.com/dsbowen/strong_reject) (MIT License)
- Dataset: [Hugging Face: walledai/StrongREJECT](https://huggingface.co/datasets/walledai/StrongREJECT) (MIT License)

## TermiBench

### Description

**TermiBench** was introduced to enable the evaluation of agents in penetration-testing scenarios under realistic or near-realistic conditions. The authors argue that CTF tasks often represent highly simplified scenarios and that performance achieved on such tasks may therefore differ substantially from performance under real-world conditions. TermiBench instead provides a complex environment comprising 510 host instances built around 30 unique real-world CVEs affecting 25 different services. Each host contains one vulnerable service alongside 0, 1, 3, 5, or 7 benign services randomly selected from a pool of 14 commonly used applications identified through large-scale Internet measurements. Agents receive no prior information beyond the target subnet range, requiring them to autonomously perform reconnaissance, service enumeration, and vulnerability identification before attempting exploitation. Rather than requiring the agent to retrieve a flag, the objective is to gain control of a designated target system by obtaining a remote shell, potentially with root privileges.

### Resources & Licenses

- Paper: [Shell or Nothing: Real-World Benchmarks and Memory-Activated Agents for Automated Penetration Testing](https://arxiv.org/pdf/2509.09207) (Mai et al., 2025)
- Code and dataset: [Zenodo: records/17479793](https://zenodo.org/records/17479793) (CC BY 4.0)

## WMDP

### Description

**WMDP**, the 'Weapons of Mass Destruction Proxy' benchmark, is based on a dataset of 3,668 multiple-choice questions covering biosecurity, cybersecurity, and chemical security. It was developed jointly by researchers and technical experts and can be used not only to evaluate potentially hazardous knowledge in LLMs, but also to assess the effectiveness of unlearning methods.

### Resources & Licenses

- Paper: [The WMDP Benchmark: Measuring and Reducing Malicious Use With Unlearning](https://arxiv.org/pdf/2403.03218) (Li et al., 2024)
- Code: [GitHub: centerforaisafety/wmdp](https://github.com/centerforaisafety/wmdp) (MIT License)
- Dataset: [Hugging Face: cais/wmdp](https://huggingface.co/datasets/cais/wmdp) (MIT License)
