# Philosophy as Code: Why Before How in AI Agent Governance

**Anonymous / B-LAND Inc.**

support@b-land.co

---

## Abstract

Large language model (LLM) based AI agents are increasingly deployed in production environments. The dominant approaches to governing these agents focus on *how* they operate — through prompt engineering, agent harnesses, retrieval-augmented generation, and skill management systems. However, none of these approaches define *why* an agent should make a particular decision when faced with ambiguity. This paper proposes Philosophy as Code — the practice of defining *why* before *how* by codifying philosophy as a three-layer structure of principles, values, and thinking patterns. We present a concrete implementation architecture consisting of four components (CLAUDE.md, Rules, Skills, and Philosophy Scrum), a recommended directory structure for immediate adoption, and a case study demonstrating qualitative improvement in AI agent consistency, review efficiency, and team autonomy. We argue that harnesses without philosophy are destined for the same fate as methodologies without thought: ritualization.

---

## 1. Introduction

LLM-based AI agents have transitioned from research artifacts to production tools. Software teams now routinely delegate code generation, documentation, and architectural decision-making to AI agents operating within development environments.

As adoption has scaled, so has the sophistication of control mechanisms. Agent harnesses [1] provide structured approaches to orchestrating agent behavior. ReAct [2] and Reflexion [3] establish reasoning and self-correction patterns. DSPy [4] compiles declarative pipelines into optimized prompts. Skill management systems enable modular, reusable agent capabilities.

Yet a structural gap remains. All of these approaches optimize *how* an agent operates. None define *why* it should prefer one decision over another when confronted with ambiguity.

This gap is consequential because ambiguity is not the exception — it is the norm. In any sufficiently complex project, the 101st case will arise: a situation not covered by any existing rule, prompt, or retrieval document. When this occurs, a method-governed agent has two options: halt and request instruction, or proceed on its own interpretation. Neither outcome is acceptable at scale.

Humans have historically navigated this gap through tacit knowledge — unarticulated principles that guided judgment in novel situations. AI agents possess no such faculty. They do not fill gaps between rules. They execute what is specified and disregard what is not.

This paper introduces Philosophy as Code — the practice of making the *why* explicit, codifying it, and placing it ahead of any methodology.

---

## 2. Background

### 2.1 Agent Harnesses

Pan et al. [1] define natural-language agent harnesses as structured architectures for controlling LLM-based agents. Their architecture identifies four key components: agent structure standardization, skill management systems, context optimization, and multi-agent coordination. This work represents the current state of the art in agent governance methodology — yet the question of *why* an agent should prefer one judgment over another remains outside its scope.

### 2.2 Reasoning and Control Patterns

ReAct [2] synergizes reasoning and acting, enabling agents to interleave thought and action. Reflexion [3] introduces verbal reinforcement learning, allowing agents to learn from prior failures. These patterns improve agent performance within defined boundaries but do not address what occurs when the agent encounters a situation beyond those boundaries.

### 2.3 Declarative Pipelines

DSPy [4] and similar systems allow developers to declare desired LLM pipeline behavior and compile it into optimized prompts. This raises the level of abstraction but remains firmly within the domain of *how* — how to structure calls, how to optimize retrieval, how to chain operations.

### 2.4 The Common Gap

All existing approaches share a structural omission: they assume that the correct decision can be derived from the correct method. This assumption fails precisely when it matters most — in novel situations where no method has been defined.

Consider Scrum, a methodology grounded in empiricism, transparency, and adaptation. Organizations routinely adopt Scrum's ceremonies — daily standups, sprint planning, retrospectives — while discarding its underlying philosophy. The standup becomes a status report. The retrospective becomes a complaint session. The methodology degenerates into ritual.

This pattern is not unique to Scrum. It is structural. Any methodology, imported without its underlying philosophy, will ritualize. AI agent governance is no exception.

---

## 3. The Problem

### 3.1 Methods Cannot Handle the Unknown

Define 100 rules, and the 101st unknown case will inevitably arise. The coverage of a rule set is always finite; the space of possible situations is not. No amount of prompt engineering, no volume of retrieval documents, and no depth of skill libraries can close this gap through enumeration alone.

### 3.2 Methodology Without Philosophy Ritualizes

When a team adopts a methodology without understanding *why* it works, the methodology becomes ceremony. Daily standups occur every morning, yet no member can articulate their purpose. Sprint retrospectives proceed on schedule, yet nothing changes as a result. The form persists; the function decays.

This is not a failure of the methodology itself. It is a failure to import the philosophy that gives the methodology meaning.

### 3.3 AI Does Not Fill Gaps Between Rules

Humans implicitly filled the gaps between rules through tacit knowledge — unspoken principles accumulated through experience. A senior engineer recognizes when a design is fragile. A product manager senses when a feature is over-scoped. These judgments are not arbitrary; they are derived from internalized philosophy.

AI agents possess no such faculty. When the gap between rules is reached, the agent either halts (awaiting instruction) or proceeds on its own interpretation (which may diverge from organizational intent). Neither outcome is acceptable.

### 3.4 The Absence of Philosophy Is a Cost

The cost of operating without philosophy is quantifiable, even when unquantified:

- **Inconsistency**: Multiple team members using AI agents without shared principles produce divergent outputs, each requiring human review.
- **Rework**: Outputs that technically satisfy a prompt but violate unstated organizational values must be redone.
- **Dependency**: Without internalized principles, every edge case requires human intervention, preventing autonomous agent operation.
- **Knowledge loss**: When the individual who "just knows" departs the organization, their tacit knowledge departs with them.

---

## 4. The Three-Layer Philosophy

We propose a three-layer philosophy, implemented as a plaintext file (CLAUDE.md) placed at the root of any project.

### 4.1 Layer 1: Principles

Principles are structural facts about how the world operates. They are independent of organizational preference, industry, or context. They are immutable.

Examples:

- Methods alone cannot handle the unknown.
- Tacit knowledge, unless verbalized, cannot be inherited.
- AI does not fill gaps between rules.

Principles constrain the space of valid decisions. Any decision that contradicts a principle is invalid regardless of context.

### 4.2 Layer 2: Values

Values are chosen priorities. Unlike principles, they are not universal — they represent what a specific organization decides to hold most important. Values are selected by will, not derived from observation.

Examples:

1. Define philosophy before selecting methodology.
2. The goal of every engagement is autonomous operation, not dependency.
3. End the era of "obey without thinking."

Values establish priority when principles alone do not determine a unique course of action.

### 4.3 Layer 3: Thinking Patterns

Thinking patterns constitute the interface between philosophy and action. They convert principles and values into concrete decision procedures.

- **Pattern 1**: Derive methodology from philosophy, never the reverse. Ask "why" before "how."
- **Pattern 2**: Define correctness before implementation (TDD thinking). The test — the definition of what is correct — comes first.
- **Pattern 3**: Extract tacit knowledge through questioning, not advice. The purpose of dialogue is to surface the other party's implicit philosophy.
- **Pattern 4**: When in doubt, return to this file. Do not expand the option set; return to higher principles.

### 4.4 The Water Principle

> "Be water, my friend." — Bruce Lee

Water assumes the shape of any container, yet its nature does not change. Similarly, when the three-layer philosophy is held constant, methodology can adapt freely to any situation. The philosophy is the invariant; the method is the variable.

This represents the structural inverse of current practice, where method is fixed (we use Scrum, we use ReAct, we use this prompt template) and philosophy is absent or implicit.

```
+--------------------------------------------------+
|           Layer 1: Principles                     |
|   (Structural facts — immutable)                  |
|                                                   |
|   "Methods alone cannot handle the unknown"       |
|   "Tacit knowledge must be verbalized"            |
|   "AI does not fill gaps between rules"           |
+-------------------------+------------------------+
                          |
                          | constrains
                          v
+--------------------------------------------------+
|           Layer 2: Values                         |
|   (Chosen priorities — organizational will)       |
|                                                   |
|   1. Define philosophy first                      |
|   2. Goal: autonomous operation                   |
|   3. End "obey without thinking"                  |
+-------------------------+------------------------+
                          |
                          | derives
                          v
+--------------------------------------------------+
|           Layer 3: Thinking Patterns              |
|   (Decision interface — derivation circuits)      |
|                                                   |
|   Pattern 1: Philosophy -> Method (never reverse) |
|   Pattern 2: Define correctness first (TDD)       |
|   Pattern 3: Extract tacit knowledge via dialogue |
|   Pattern 4: Return to this file when in doubt    |
+--------------------------------------------------+

          Fig. 1: Three-Layer Philosophy Structure
```

---

## 5. Implementation

Philosophy as Code is implemented through four components. Their relationship can be understood through a legal system analogy: constitution, statutes, case law, and judicial review.

```
CLAUDE.md (Constitution — philosophy definition)
    |
    | constrains
    v
.claude/rules/ (Statutes — operational rules derived from philosophy)
    |-- philosophy-first.md      <-- always injected (every session)
    |-- claude-md-governance.md  <-- injected when editing CLAUDE.md
    |-- code-standards.md        <-- injected when editing code files
    |-- skill-authoring.md       <-- injected when editing Skills
    |
    | references as needed
    v
.claude/skills/ (Case law — domain knowledge modules)
    |-- Each SKILL.md (loaded only when invoked)

                    Fig. 2: Implementation Architecture
```

### 5.1 CLAUDE.md — The Philosophy Definition File (Constitution)

CLAUDE.md is a plaintext file placed at the project root. Every AI agent operating within the project reads this file and treats it as the supreme decision-making reference.

The file structure mirrors the three-layer philosophy:

1. **Principles** — immutable structural facts
2. **Values** — organizational priorities, ordered by importance
3. **Thinking Patterns** — decision derivation procedures
4. **Prohibitions** — actions that, if taken, would violate the philosophy
5. **Operating Rules** — governance of the file itself

CLAUDE.md functions simultaneously as implementation, philosophy, and test. Any output that does not satisfy the philosophy defined in this file is not shipped — just as code that fails its test suite is not shipped.

In legal terms, CLAUDE.md serves as the **constitution**. All subordinate rules must be consistent with it.

### 5.2 Rules — The Harness Control Layer (Statutes)

Rules are operational rule files stored in `.claude/rules/`. They translate CLAUDE.md's philosophy into concrete behavioral guidelines that AI agents follow during task execution. In legal terms, they constitute the **statutes** — derived from the constitution, binding on all agents.

The core mechanism of Rules is **context injection control**. Each rule file specifies a `paths` field in its YAML frontmatter, determining when, under what circumstances, and which rules are injected into the agent's context window. This mechanism implements the "context optimization" component identified by Pan et al. [1], driven by philosophical rather than purely technical considerations.

The following examples illustrate the design:

- **`philosophy-first.md`** (no `paths` field = always injected): Directs the agent to confirm philosophy alignment before initiating any task and to return to CLAUDE.md when facing uncertainty. This rule serves as a structural safeguard against philosophical drift during extended sessions.
- **`claude-md-governance.md`** (`paths: CLAUDE.md`): Activated only when the agent edits CLAUDE.md itself. Defines amendment governance — principles are nearly immutable; values may be modified with justification; thinking patterns welcome additions.
- **`code-standards.md`** (`paths: **/*.html, **/*.js`, etc.): Activated only during code editing. Requires that every code change be traceable to a CLAUDE.md value.
- **`skill-authoring.md`** (`paths: .claude/skills/**/*.md`): Activated only when creating or editing Skills. Enforces philosophy traceability in all knowledge artifacts.

This architecture ensures that the agent **maintains continuous philosophical awareness through always-injected rules while receiving context-appropriate behavioral norms through conditionally-injected rules**. The context window is allocated efficiently — only applicable rules are active at any given moment.

### 5.3 Skills — Domain Knowledge Modules (Case Law)

Skills are modular domain knowledge units stored in `.claude/skills/`, derived from the philosophy. In legal terms, they function as **case law and specialist reference texts** — maintained under the authority of the constitution (CLAUDE.md) and statutes (Rules), consulted when specific domain expertise is required.

The critical distinction between Rules and Skills lies in their loading behavior. Rules are automatically injected based on file operations; Skills are loaded only upon explicit invocation by the user or agent. This design permits the system to maintain extensive domain knowledge without consuming context window resources during unrelated tasks.

Each Skill traces its provenance to a specific principle or value, preserving traceability from philosophy to practice.

### 5.4 Philosophy Scrum — The Verification Cycle

A philosophy that is written but never verified will ritualize — precisely the failure described in Section 3.2. Philosophy Scrum addresses this by adapting Scrum's empiricism to philosophy verification.

**Why Scrum.** Scrum's foundation is empiricism — transparency, inspection, and adaptation. These three pillars map directly to philosophy governance:

- **Transparency**: The philosophy is verbalized and accessible (CLAUDE.md exists and is readable).
- **Inspection**: The philosophy's effectiveness is periodically verified (Review).
- **Adaptation**: The philosophy itself evolves in response to evidence (Retrospective).

**Bidirectional verification.** Philosophy Scrum does not enforce philosophy in a single direction. Philosophy and outputs verify each other:

```
CLAUDE.md ---- Review: Does output -----> Rules / Skills / Output
(Philosophy)   align with philosophy?
              <--- Retro: Is this -------- (Deliverables)
                   philosophy working?
```

Unidirectional top-down enforcement risks philosophical drift from reality without corrective feedback. Unidirectional bottom-up governance risks erosion of long-term principles by short-term results. Bidirectional verification ensures that philosophy remains grounded in reality while resisting short-term pressure.

**Permeation and detection.** Two complementary processes sustain the philosophy:

- **Permeation** embeds philosophy into daily work (Planning, Execution). The always-injected rules described in Section 5.2 are the technical implementation of permeation.
- **Detection** measures whether philosophy is actually functioning (Review, Retrospective).

Permeation without detection becomes faith. Detection without permeation becomes surveillance. Both are necessary.

**Three-layer cycle.** Verification operates at three temporal scales:

- **Per-task**: Each task begins with philosophy alignment (Planning), proceeds under philosophical guidance (Execution), and is verified against philosophy (Review).
- **Weekly**: Task-level results are aggregated. Compliance rates, violation patterns, and emerging gaps are analyzed.
- **Monthly**: Trends are reviewed. Principles remain stable. Values and thinking patterns evolve as warranted by evidence.

### 5.5 Adoption Process

Philosophy as Code is introduced through a four-phase process:

1. **Executive dialogue**: Extract the organization's tacit philosophy through structured 1-on-1 sessions (Thinking Pattern 3).
2. **Team permeation**: Disseminate the extracted philosophy across the team.
3. **Codification**: Implement as the three-layer structure: CLAUDE.md, Rules, and Skills.
4. **Verification**: Initiate Philosophy Scrum cycles.

The objective of every engagement is autonomous operation — the client organization operates Philosophy as Code independently, without ongoing external dependency (Value 2).

### 5.6 Recommended Directory Structure

The following directory structure represents the recommended layout for a project adopting Philosophy as Code. It is designed for immediate deployment.

```
project-root/
|
|-- CLAUDE.md                          # Philosophy definition (Constitution)
|                                      # Three-layer structure: Principles, Values,
|                                      # Thinking Patterns + Prohibitions + Rules
|
|-- .claude/
|   |
|   |-- rules/                         # Harness control layer (Statutes)
|   |   |-- philosophy-first.md        # [always injected] Philosophy-first ops
|   |   |-- claude-md-governance.md    # [CLAUDE.md edit] Amendment governance
|   |   |-- code-standards.md          # [code edit] Coding standards
|   |   |-- skill-authoring.md         # [Skills edit] Skill authoring rules
|   |   |-- security.md               # [all files] Security boundaries (optional)
|   |   +-- <domain-specific>.md       # [target paths] Domain-specific rules
|   |
|   +-- skills/                        # Domain knowledge modules (Case law)
|       |-- <skill-name>/
|       |   |-- SKILL.md               # Entry point (loaded on invoke)
|       |   +-- <supplementary>.md     # Supplementary files (templates, etc.)
|       +-- ...
|
+-- (project files)
```

**Design principles:**

- **CLAUDE.md** resides at the project root. It is the first file every agent reads.
- **Rules** govern injection timing via the `paths` frontmatter field. Always-injected rules (no `paths`) and conditionally-injected rules are employed strategically.
- **Skills** are loaded exclusively on invocation. Expanding the skill library does not consume context window resources.
- Rules should be **narrow in scope and numerous** — one file per concern. Files are split when they grow beyond their original scope.
- CLAUDE.md should remain **under 200 lines**. Concrete operational rules belong in `rules/`; domain knowledge belongs in `skills/`.

### 5.7 End-to-End Flow

Figure 3 illustrates the complete operational flow of Philosophy as Code across a single task cycle, from planning through retrospective verification.

```
+-------------------------------------------------------------------+
|                        1. PLANNING                                |
|   Task arrives                                                    |
|       |                                                           |
|       v                                                           |
|   Consult CLAUDE.md -- "Which value does this task serve?"        |
|       |                                                           |
|       v                                                           |
|   philosophy-first.md (always injected) enforces the check        |
|       |                                                           |
|       v                                                           |
|   Define correctness before implementation (Pattern 2)            |
+-------------------------------------------------------------------+
       |
       v
+-------------------------------------------------------------------+
|                        2. EXECUTION                               |
|   AI agent executes the task                                      |
|       |                                                           |
|       +-- CLAUDE.md -- supreme decision criteria (always present) |
|       +-- Rules -- context-appropriate norms (paths auto-inject)  |
|       +-- Skills -- domain knowledge (loaded on invoke)           |
|       |                                                           |
|       v                                                           |
|   Deliverable (code / document / design)                          |
+-------------------------------------------------------------------+
       |
       v
+-------------------------------------------------------------------+
|                        3. REVIEW                                  |
|   Verify deliverable against philosophy                           |
|       |                                                           |
|       +-- Does it violate any Principle?                          |
|       +-- Does it respect the Value priority order?               |
|       +-- Was the Thinking Pattern followed in the process?       |
|       +-- Does it touch any Prohibition?                          |
|       |                                                           |
|       v                                                           |
|   Pass -> Ship    Fail -> Revise and return to Execution          |
+-------------------------------------------------------------------+
       |
       v (weekly / monthly)
+-------------------------------------------------------------------+
|                        4. RETROSPECTIVE                           |
|   Verify the philosophy itself                                    |
|       |                                                           |
|       +-- Did this philosophy produce the intended outcomes?      |
|       +-- Were new structural facts discovered?                   |
|       +-- Should new Thinking Patterns be added?                  |
|       |                                                           |
|       v                                                           |
|   Update CLAUDE.md / Rules / Skills (only when warranted)         |
|   Principles are nearly immutable. Values and Patterns may evolve.|
+-------------------------------------------------------------------+

              Fig. 3: End-to-End Operational Flow
```

---

## 6. Case Study

### 6.1 Before: AI Agents Without Philosophy

A software development team adopted LLM-based AI agents for code generation, documentation, and architectural decision-making. Each team member independently configured and prompted their agents. No shared decision-making philosophy existed.

Four problems emerged:

- **Inconsistent judgment**: Identical task types produced divergent outputs depending on which team member's agent executed them. Output direction varied across the team.
- **Uncontrolled scope expansion**: Agents extended implementation beyond the requested scope, advancing the project in unintended directions.
- **Decision paralysis**: Upon encountering unexpected cases, agents either halted entirely or returned clarifying questions, requiring human intervention for every edge case.
- **Knowledge silos**: Prompting techniques and agent configurations remained confined to individual team members' expertise, unreproducible by colleagues.

**Result**: AI adoption, intended to increase efficiency, instead multiplied human workload. Unguided AI outputs proliferated — one per team member — and humans were left to review, reconcile, and quality-control each of them. The agents generated more work than they eliminated.

### 6.2 After: CLAUDE.md Deployment

The same team subsequently deployed CLAUDE.md (the three-layer philosophy). Three changes were observed:

- **Output convergence**: Regardless of which team member invoked an AI agent, identical decision criteria (principles and values) applied. Output direction became consistent across the team.
- **Reduced review burden**: Quality assurance shifted from detailed review of every output to a single verification: "Does this align with the philosophy?" Review cost decreased from O(N), proportional to team size, to O(1), proportional to the philosophy.
- **Agent autonomy**: In novel situations that previously required human intervention, agents derived decisions from thinking patterns. Per-task instruction became unnecessary.

```
WITHOUT Philosophy (Before)          WITH Philosophy (After)
========================          ========================

Member A --> AI --> Output X      Member A --> AI --|
Member B --> AI --> Output Y                       |--> CLAUDE.md --> Consistent
Member C --> AI --> Output Z      Member C --> AI --|    Output

     |                                 |
     v                                 v
+----------------+               +----------------+
| Human reviews  |               | Philosophy     |
| EVERY output   |               | check ONLY     |
| (N x cost)     |               | (1 x cost)     |
+----------------+               +----------------+
     |                                 |
     v                                 v
  Exhaustion                       Autonomy

      Fig. 4: Before and After — With and Without Philosophy
```

**Note on quantitative data.** At the time of writing, formal quantitative measurement has not been conducted. The qualitative improvements described above are clear and consistent across the observation period. A measurement methodology based on Philosophy Scrum metrics (Section 5.4) is planned for subsequent publication.

---

## 7. Discussion

### 7.1 Positioning Against Existing Approaches

| Approach | Competitive axis | Limitation |
|----------|-----------------|------------|
| Prompt engineering | How (instruction precision) | Fails outside specified context |
| Agent harnesses [1] | How (control structure) | Cannot handle the 101st unknown case |
| RAG / Skill management | What (knowledge volume) | Lacks decision criteria for novel situations |
| **Philosophy as Code** | **Why (philosophy)** | **How is derived from situational context** |

Current approaches compete on How. Philosophy as Code competes on Why. This is not a claim that How is unimportant — harnesses, prompts, and retrieval systems constitute necessary infrastructure. The claim is that How has an inherent ceiling, and that ceiling is reached precisely when the unknown is encountered. Why penetrates that ceiling by providing a derivation mechanism that operates in the absence of specific rules.

### 7.2 The Ritualization Trap

Every methodology is susceptible to ritualization — the process by which form is preserved while function decays. Scrum ritualizes into status meetings. TDD ritualizes into tests written after implementation. Code review ritualizes into perfunctory approval.

Agent harnesses face the same structural risk. A harness that defines control structures without philosophical grounding will, over time, degrade into a set of templates that teams follow without comprehension. The harness will govern the agent's behavior, but no participant will be able to articulate *why* the agent should behave in that manner.

Philosophy as Code is not immune to this risk. This is precisely why Philosophy Scrum exists — bidirectional verification ensures that the philosophy is continuously tested against operational reality and revised when it fails to produce intended outcomes.

### 7.3 Limitations

We acknowledge four principal limitations of this work:

1. **Single-context validation.** Philosophy as Code has been tested within a single organizational context. Cross-organizational validation across different industries, team sizes, and AI maturity levels is required to establish generalizability.
2. **Absence of quantitative measurement.** Formal quantitative metrics have not yet been collected. The measurement methodology defined within Philosophy Scrum (compliance rates, violation patterns, philosophy evolution frequency) will be applied and reported in subsequent work.
3. **Manual verification dependency.** The current implementation relies on plaintext files and human-initiated verification. Automated tooling for continuous philosophy compliance monitoring is under active development.
4. **LLM-specific implementation.** The three-layer philosophy (principles, values, and thinking patterns) is not dependent on any specific LLM. However, the implementation presented in this paper — context injection control via `.claude/rules/` and domain knowledge modularization via `.claude/skills/` — is built on the harness mechanisms of Anthropic's Claude Code. To achieve equivalent philosophy-driven governance with other LLM-based agents, an appropriate control layer must be designed for the target agent's architecture (e.g., rule injection timing control, lazy knowledge loading). The philosophical structure is portable; the harness implementation is redesigned per target platform.

---

## 8. Conclusion

Harnesses are necessary. However, a harness without philosophy will ritualize — just as Scrum without philosophy becomes a collection of meetings, and TDD without philosophy becomes tests written after the code.

Philosophy as Code proposes a structural inversion: define *why* before *how*. Implement philosophy as a three-layer structure of principles, values, and thinking patterns. Codify it as CLAUDE.md. Operationalize it through Rules and Skills. Verify it through Philosophy Scrum. Measure it. Evolve it.

The CLAUDE.md file functions simultaneously as implementation, philosophy, and test. It is the analog of both the Bitcoin whitepaper and the Bitcoin source code — a description of the system that is, itself, the system.

> "Don't think. Obey." — That era is over.
> "Think. And be water."

---

## References

[1] Pan, L., Zou, L., Guo, S., Ni, J., & Zheng, H.-T. (2026). Natural-Language Agent Harnesses. *arXiv preprint arXiv:2603.25723*.

[2] Yao, S., Zhao, J., Yu, D., Du, N., Shafran, I., Narasimhan, K., & Cao, Y. (2023). ReAct: Synergizing Reasoning and Acting in Language Models. In *Proceedings of the International Conference on Learning Representations (ICLR)*.

[3] Shinn, N., Cassano, F., Gopinath, A., Shakkottai, K., Labash, A., & Karpas, E. (2023). Reflexion: Language Agents with Verbal Reinforcement Learning. In *Advances in Neural Information Processing Systems (NeurIPS)*.

[4] Khattab, O., Singhvi, A., Maheshwari, P., Zhang, Z., Santhanam, K., Vardhamanan, S., Haq, S., Sharma, A., Joshi, T. T., Mober, H., et al. (2023). DSPy: Compiling Declarative Language Model Calls into Self-Improving Pipelines. *arXiv preprint arXiv:2310.03714*.
