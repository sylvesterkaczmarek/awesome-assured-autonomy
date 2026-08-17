# Awesome Assured Autonomy [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

![Awesome Assured Autonomy](assets/social/github-social-card-awesome-assured-autonomy.png)

A curated list of research, tools, benchmarks, standards, and open-source systems for building autonomous systems that can be trusted in the real world.

The focus is assurance for systems that sense, decide, and act with meaningful physical or operational consequences. This includes robotics, autonomous vehicles, aerospace and space systems, learning-enabled control, embodied agents, and agentic software that can invoke consequential tools.

Maintained by [Sylvester Kaczmarek](https://github.com/sylvesterkaczmarek).

> **Curation rule:** inclusion means the resource is useful enough to recommend, not merely related. Prefer primary sources, maintained tools, reproducible work, and resources with clear assurance value.

## Contents

- [Foundations and runtime assurance](#foundations-and-runtime-assurance)
- [Safety filters and safe learning](#safety-filters-and-safe-learning)
- [Formal methods and verification](#formal-methods-and-verification)
- [Runtime monitoring and policy enforcement](#runtime-monitoring-and-policy-enforcement)
- [Assurance cases and evidence](#assurance-cases-and-evidence)
- [Simulation, scenarios, and benchmarks](#simulation-scenarios-and-benchmarks)
- [Robotics and physical autonomy](#robotics-and-physical-autonomy)
- [Aerospace and space autonomy](#aerospace-and-space-autonomy)
- [Standards and assurance guidance](#standards-and-assurance-guidance)
- [Cite this list](#cite-this-list)

## Foundations and runtime assurance

- [The Simplex Architecture for Safe On-Line Control System Upgrades](https://doi.org/10.1109/ACC.1998.703255) - Foundational Simplex architecture paper on safely switching between advanced and trusted control.
- [Neural Simplex Architecture](https://arxiv.org/abs/1908.00528) - Extends Simplex-style runtime assurance to neural controllers, including switching back to advanced control and online retraining.
- [The Black-Box Simplex Architecture for Runtime Assurance of Autonomous CPS](https://arxiv.org/abs/2102.12981) - Runtime assurance without relying on internal information from advanced or baseline controllers.
- [Runtime Safety Assurance for Learning-enabled Control of Autonomous Driving Vehicles](https://arxiv.org/abs/2109.13446) - Simplex-Drive architecture combining a learned controller, a safe baseline controller, and verified switching logic.
- [Synergistic Simplex](https://arxiv.org/abs/2605.08190) - 2026 work on cooperative runtime assurance that allows constrained information flow between learned components and safety monitors while preserving formal safety conditions.
- [Mission-Level Runtime Assurance Framework for Autonomous Driving](https://arxiv.org/abs/2606.06996) - Extends runtime assurance beyond local platform safety to reject high-level commands that make future mission completion infeasible.
- [S3A: Secure System Simplex Architecture for Enhanced Security of Cyber-Physical Systems](https://arxiv.org/abs/1202.5722) - Extends Simplex ideas toward cyber-resilient control and intrusion response.
- [Run Time Assurance for Electric Vertical Takeoff and Landing Aircraft](https://ntrs.nasa.gov/citations/20210026909) - NASA study of RTA for highly automated and autonomous eVTOL functions.
- [A Verification Framework for Runtime Assurance of Autonomous UAS](https://ntrs.nasa.gov/citations/20240010429) - NASA framework for verifying RTA architectures around untrusted components such as AI/ML controllers.
- [Dynamic Assurance of Autonomous Systems Through Ground Control Software](https://ntrs.nasa.gov/citations/20230018233) - NASA work on updating assurance evidence during operations through ground control systems.
- [Considerations in Assuring Safety of Increasingly Autonomous Systems](https://ntrs.nasa.gov/citations/20180006312) - NASA analysis of assurance gaps created by increasingly autonomous aviation systems.
- [A Runtime Assurance Framework for Low-flying Autonomous UAS Medical Operations](https://ntrs.nasa.gov/citations/20250011655) - Runtime assurance for AI/ML perception used in autonomous emergency-response UAS operations.

## Safety filters and safe learning

- [Safe Reinforcement Learning via Shielding](https://arxiv.org/abs/1708.08611) - Synthesizes a reactive shield from temporal-logic specifications to block or correct unsafe actions.
- [End-to-End Safe Reinforcement Learning through Barrier Functions for Safety-Critical Continuous Control Tasks](https://arxiv.org/abs/1903.08792) - Combines model-free RL, control barrier functions, and online dynamics learning.
- [Safe Reinforcement Learning Using Robust Control Barrier Functions](https://arxiv.org/abs/2110.05415) - Uses a differentiable robust-CBF safety layer around learned control.
- [SAC-RCBF](https://github.com/yemam3/SAC-RCBF) - Reference implementation combining Soft Actor-Critic with robust control barrier functions.
- [neural_clbf](https://github.com/MIT-REALM/neural_clbf) - Toolkit for learning robust control Lyapunov-barrier functions with neural networks.
- [BarrierNet](https://github.com/Weixy21/BarrierNet) - Differentiable control-barrier-function layers for safety-constrained robot learning.
- [VSRL Framework](https://github.com/IBM/vsrl-framework) - Framework connecting reinforcement learning with formal verification for verifiably safe policies.
- [Safe Policy Optimization](https://github.com/PKU-Alignment/Safe-Policy-Optimization) - Implementations and benchmarks for constrained and safe reinforcement-learning algorithms.

## Formal methods and verification

- [VerifAI](https://github.com/BerkeleyLearnVerify/VerifAI) - Toolkit for formal design and analysis of AI-enabled systems through specification-guided simulation, falsification, and synthesis.
- [Scenic](https://github.com/BerkeleyLearnVerify/Scenic) - Probabilistic programming language for describing and generating scenarios for cyber-physical systems and autonomous systems.
- [alpha-beta-CROWN](https://github.com/Verified-Intelligence/alpha-beta-CROWN) - GPU-accelerated neural-network verifier with strong performance across VNN-COMP benchmarks.
- [Marabou](https://github.com/NeuralNetworkVerification/Marabou) - Framework for verification and analysis of deep neural networks.
- [NNV](https://github.com/verivital/nnv) - Set-based neural-network verification for deep networks and learning-enabled cyber-physical systems.
- [DNNV](https://github.com/dlshriver/dnnv) - Common framework and property language for deep neural-network verification across multiple back-end verifiers.
- [FRET](https://github.com/NASA-SW-VnV/fret) - NASA framework for eliciting, formalizing, and analyzing requirements for safety-critical and autonomous systems.
- [Verse](https://github.com/AutoVerse-ai/Verse-library) - Modeling, simulation, and verification library for interacting autonomous agents and hybrid systems.
- [Z3](https://github.com/Z3Prover/z3) - Widely used SMT solver for symbolic reasoning and formal verification.
- [cvc5](https://github.com/cvc5/cvc5) - Open-source SMT solver supporting a broad set of logical theories used in verification and synthesis.

## Runtime monitoring and policy enforcement

- [Copilot](https://github.com/Copilot-Language/copilot) - Stream-based runtime-verification framework that generates hard real-time C monitors.
- [Ogma](https://github.com/nasa/ogma) - NASA tooling for integrating runtime monitors into systems including cFS, F Prime, and ROS 2.
- [OpenAI Agents SDK guardrails](https://openai.github.io/openai-agents-python/guardrails) - Runtime input, output, and tool-call validation mechanisms for agentic systems.
- [Cedar](https://github.com/cedar-policy/cedar) - Policy language and authorization engine for explicit allow/deny decisions around consequential actions.
- [Cedar for Agents](https://github.com/cedar-policy/cedar-for-agents) - Agent-oriented authorization tooling, including support for generating Cedar schemas from MCP tool descriptions.
- [Open Policy Agent](https://github.com/open-policy-agent/opa) - General-purpose policy engine for context-aware policy decisions and enforcement.
- [Microsoft Agent Governance Toolkit](https://github.com/microsoft/agent-governance-toolkit) - Runtime governance components and policy-engine interfaces for agent systems.
- [SROS 2](https://github.com/ros2/sros2) - ROS 2 tooling for DDS-Security keys, certificates, encryption, and access-control policies.

## Assurance cases and evidence

- [SACE](https://www.york.ac.uk/assuring-autonomy/guidance/sace/) - University of York methodology for integrating system-level safety assurance into autonomous-system development and constructing structured safety cases for complex environments.
- [AMLAS](https://www.york.ac.uk/assuring-autonomy/guidance/amlas/) - Six-stage methodology for building explicit safety arguments and evidence around machine-learning components used in autonomous systems.
- [Safety Assurance Objectives for Autonomous Systems V4](https://scsc.uk/resources/citation_r1942.html) - Pan-domain guidance from the Safety-Critical Systems Club focused specifically on autonomy and AI/ML assurance objectives.
- [AdvoCATE User Guide](https://ntrs.nasa.gov/citations/20220009664) - NASA guide to an assurance-case toolset connecting hazards, requirements, risk models, structured arguments, and evidence logs.
- [Structured Assurance Case Metamodel 2.3](https://www.omg.org/spec/SACM/About-SACM) - OMG standard for interoperable machine-readable models of claims, argumentation, evidence, and assurance-case artifacts.

## Simulation, scenarios, and benchmarks

- [Safety-Gymnasium](https://github.com/PKU-Alignment/safety-gymnasium) - Standardized environments and APIs for benchmarking safe reinforcement learning.
- [safe-control-gym](https://github.com/learnsyslab/safe-control-gym) - Physics-based benchmark suite for safe learning-based control with explicit safety constraints, disturbances, and implemented safety filters.
- [SafeBench](https://github.com/trust-ai/SafeBench) - Benchmark for evaluating autonomous-driving systems in safety-critical scenarios.
- [CARLA](https://github.com/carla-simulator/carla) - Open-source autonomous-driving simulator for development, training, and validation.
- [CARLA ScenarioRunner](https://github.com/carla-simulator/scenario_runner) - Scenario definition and execution engine for structured autonomous-driving tests.
- [MetaDrive](https://github.com/metadriverse/metadrive) - Lightweight simulator for autonomy research with compositional scenario generation and sensor simulation.
- [MuJoCo](https://github.com/google-deepmind/mujoco) - General-purpose physics engine widely used for robotics and learning-based control research.
- [dm_control](https://github.com/google-deepmind/dm_control) - Google DeepMind environment stack for physics-based control and reinforcement learning on MuJoCo.
- [Isaac Lab](https://github.com/isaac-sim/IsaacLab) - Robot-learning framework built on NVIDIA Isaac Sim for simulation, training, and sim-to-real workflows.

## Robotics and physical autonomy

- [ROS 2](https://github.com/ros2/ros2) - Core open-source robotics middleware ecosystem used across research and deployed autonomous systems.
- [ROS 2 threat model](https://github.com/ros2/design/blob/gh-pages/articles/183_ros2_threat_model.md) - Security threat analysis for robotic systems built on ROS 2.
- [Space Robotics Bench](https://github.com/AndrejOrsula/space_robotics_bench) - Robot-learning benchmark oriented toward planetary and orbital robotics with ROS 2 and Space ROS interoperability.
- [MetaDrive ScenarioNet](https://github.com/metadriverse/scenarionet) - Scenario management and reconstruction for autonomous-driving testing and learning.

## Aerospace and space autonomy

- [Space ROS](https://github.com/space-ros/space-ros) - Space-oriented ROS 2 ecosystem for space robotics and flight-relevant software development.
- [NASA Core Flight System](https://github.com/nasa/cFS) - Reusable flight-software framework maintained by NASA Goddard.
- [F Prime](https://github.com/nasa/fprime) - Flight and embedded software framework originally developed at JPL and deployed on space applications.
- [NASA Operational Simulator for Space Systems](https://github.com/nasa/nos3) - Simulation, integration, test, operations training, and V&V environment for spacecraft software and systems.
- [NASA ISAAC](https://github.com/nasa/isaac) - Integrated System for Autonomous and Adaptive Caretaking for robotic and facility autonomy.
- [NASA Limit Checker](https://github.com/nasa/LC) - cFS application for monitoring telemetry against configured limits and triggering events or actions.
- [NASA Assurance of Autonomy](https://ntrs.nasa.gov/citations/20250002334) - Recent NASA overview of technical challenges and work in autonomy assurance, runtime monitoring, AI assurance, and certification.
- [Research and Development on Complex Autonomous Systems Assurance](https://ntrs.nasa.gov/citations/20250003506) - NASA System-Wide Safety overview of selected design-assurance research for complex autonomous systems.

## Standards and assurance guidance

- [ASTM F3269-21](https://store.astm.org/f3269-21.html) - Active standard practice for safely bounding aircraft-system behavior containing complex functions using runtime assurance.
- [FAA Roadmap for Artificial Intelligence Safety Assurance](https://www.faa.gov/aircraft/air_cert/step/roadmap_for_AI_safety_assurance) - FAA roadmap defining principles and priorities for assuring AI used in aircraft and related inflight systems.
- [EASA Artificial Intelligence Concept Paper Issue 2](https://www.easa.europa.eu/en/document-library/general-publications/easa-artificial-intelligence-concept-paper-issue-2) - EASA guidance for Level 1 and Level 2 machine-learning applications, including learning assurance, explainability, and human-AI teaming.
- [ANSI/UL 4600](https://www.ul.com/services/autonomous-vehicle-safety-training-and-advisory) - Goal-based safety standard for evaluating autonomous products that operate without human supervision.
- [NIST AI Risk Management Framework](https://www.nist.gov/itl/ai-risk-management-framework) - Cross-sector framework for managing risks and trustworthiness across the AI lifecycle.
- [NIST AI Resource Center](https://airc.nist.gov) - NIST resources for operationalizing AI risk management, including testing, evaluation, verification, and validation.
- [RTCA DO-178C](https://www.rtca.org/do-178/) - Core civil-avionics software development assurance guidance.
- [RTCA DO-333](https://my.rtca.org/productdetails?id=a1B36000001IcffEAC) - Formal Methods Supplement to DO-178C and DO-278A.
- [ISO 21448:2022](https://www.iso.org/standard/77490.html) - Safety of the Intended Functionality guidance for road-vehicle functions relying on complex sensing and processing.
- [ISO 26262](https://www.iso.org/standard/68383.html) - Functional-safety standard series for electrical and electronic systems in road vehicles.
- [NASA Software Assurance of Autonomous Systems](https://ntrs.nasa.gov/citations/20205000437) - NASA report examining gaps in traditional software assurance when applied to autonomous systems.
- [NASA Workshop on Assurance for Autonomous Systems for Aviation](https://ntrs.nasa.gov/citations/20170000385) - NASA report capturing assurance challenges, gaps, and research directions for autonomous aviation systems.

## Contributing

Contributions are welcome. Please read [contributing.md](contributing.md) before opening a pull request.

A resource should normally meet at least two of these criteria:

- technically substantive and directly relevant to autonomy assurance;
- primary-source research, official guidance, or maintained open-source software;
- useful for designing, testing, verifying, monitoring, constraining, or certifying autonomous behavior;
- reproducible, documented, or backed by credible evaluation;
- sufficiently mature, influential, or novel to justify recommendation.

Low-signal link dumps, generic AI safety material without an autonomy connection, abandoned projects without historical importance, and promotional submissions are unlikely to be accepted.

## Cite this list

If you use or adapt this curated list, please cite:

> Kaczmarek, S. (2026). *Awesome Assured Autonomy*. GitHub. https://github.com/sylvesterkaczmarek/awesome-assured-autonomy

**BibTeX**

```bibtex
@misc{Kaczmarek_2026_Awesome_Assured_Autonomy,
  author = {Sylvester Kaczmarek},
  title  = {{Awesome Assured Autonomy}},
  year   = {2026},
  url    = {https://github.com/sylvesterkaczmarek/awesome-assured-autonomy}
}
```

CC0-1.0. See [LICENSE](LICENSE).

Curated by **Sylvester Kaczmarek** · [sylvesterkaczmarek.com](https://www.sylvesterkaczmarek.com)
