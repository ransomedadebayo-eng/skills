---
name: prompt-agent-designer
description: Architect for creating custom AI agents and skills. Use this skill when turning agent ideas into formal instruction sets with system prompts, example workflows, constraints, and test scenarios. The meta-skill that helps you build all other skills.
---

# Prompt & Agent Designer

## Overview

This skill helps you design effective AI agents, custom skills, and system prompts—turning concepts into structured, reusable instruction sets.

**Keywords**: prompt engineering, AI agents, system prompts, custom GPTs, Claude skills, agent design, prompt templates, AI workflow design

## Agent Design Framework

```
AGENT DESIGN: [Agent Name]
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

PURPOSE
What this agent does in one sentence:
[Clear, concise statement]

USER NEED
Who needs this:
[Target user profile]

When they'd use it:
[Specific scenarios and triggers]

Problem it solves:
[Pain point or gap it fills]

CORE CAPABILITIES
1. [Capability 1]
2. [Capability 2]
3. [Capability 3]

OUT OF SCOPE
What this agent does NOT do:
- [Limitation 1]
- [Limitation 2]

SUCCESS CRITERIA
A successful interaction looks like:
[Desired outcome description]
```

## System Prompt Template

```
SYSTEM PROMPT: [Agent Name]
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

# Role
You are a [specific role] who specializes in [domain].

# Capabilities
You help users:
- [Capability 1]
- [Capability 2]
- [Capability 3]

# Approach
When a user engages you:
1. [Step 1 of your process]
2. [Step 2 of your process]
3. [Step 3 of your process]

# Output Format
Always provide:
- [Element 1 - e.g., clear structure]
- [Element 2 - e.g., actionable recommendations]
- [Element 3 - e.g., specific examples]

# Constraints
- Do not: [Forbidden action 1]
- Always: [Required behavior 1]
- Never: [Forbidden action 2]

# Tone
[Professional / Friendly / Teaching / etc.]
[Additional style guidance]

# Examples
[1-2 example interactions showing input → output]
```

## Prompt Design Principles

```
EFFECTIVE PROMPT DESIGN
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

1. CLARITY
✓ Be specific about what you want
✗ Vague: "Help me with marketing"
✓ Clear: "Create a 4-week content calendar for B2B SaaS targeting CTOs"

2. CONTEXT
✓ Provide relevant background
Example: "I'm a new dad working full-time in ops..."

3. STRUCTURE
✓ Use formatting to guide the AI
- Bullets for lists
- Headings for sections
- Examples for clarity

4. CONSTRAINTS
✓ Define boundaries
- Word count limits
- Format requirements
- What NOT to include

5. EXAMPLES
✓ Show, don't just tell
- Provide 1-2 examples of desired output
- Demonstrate the format you want

6. ITERATIVE REFINEMENT
✓ First prompt rarely perfect
- Start broad
- Refine based on output
- Add constraints as needed

7. ROLE ASSIGNMENT
✓ Give the AI a specific persona
"You are a senior product manager..."
"You are a financial analyst specializing in..."
```

## Agent Testing Framework

```
AGENT TEST SCENARIOS: [Agent Name]
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

TEST 1: Core Use Case
Input: [Typical user request]
Expected Output: [What agent should produce]
Pass/Fail: [After testing]

TEST 2: Edge Case
Input: [Unusual or boundary case]
Expected Behavior: [How agent should handle]
Pass/Fail:

TEST 3: Out of Scope
Input: [Request outside agent's purpose]
Expected Behavior: [Should politely decline or redirect]
Pass/Fail:

TEST 4: Minimal Input
Input: [Very brief request]
Expected Behavior: [Should ask clarifying questions]
Pass/Fail:

TEST 5: Complex Request
Input: [Multi-part, nuanced request]
Expected Output: [Structured, comprehensive response]
Pass/Fail:

REFINEMENTS NEEDED:
Based on tests:
□ [Improvement 1]
□ [Improvement 2]
```

## Skill File Template (Claude)

```
SKILL.md FILE STRUCTURE
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

---
name: [skill-name-in-kebab-case]
description: [Clear description of what this skill does and when Claude should use it. Should include key triggers and use cases.]
---

# [Skill Name]

## Overview
[2-3 sentences: What this skill does and who it's for]

**Keywords**: [Comma-separated keywords for discoverability]

## When to Use This Skill
Use this skill when you need to:
- [Use case 1]
- [Use case 2]
- [Use case 3]

## [Core Capability 1]
[Detailed explanation with templates/examples]

## [Core Capability 2]
[Detailed explanation with templates/examples]

## [Core Capability 3]
[Detailed explanation with templates/examples]

## Best Practices
[Guidelines for effective use]

## Example Use Cases
[2-3 concrete examples showing input → output]

## Getting Started
To use this skill effectively:
1. [Step 1]
2. [Step 2]
3. [Step 3]
```

## Prompt Library

```
COMMON PROMPT PATTERNS
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

ANALYSIS PROMPT:
"Analyze [subject] focusing on [aspect]. Consider [factors]. Provide [output format]."

CREATION PROMPT:
"Create a [deliverable] for [audience] that [objective]. Include [elements]. Format: [structure]."

COMPARISON PROMPT:
"Compare [option A] and [option B] across these dimensions: [dimension 1], [dimension 2], [dimension 3]. Recommend [decision]."

PLANNING PROMPT:
"Plan a [project/initiative] to achieve [goal]. Break down into [phases/steps]. For each step, provide [details]. Timeline: [duration]."

TRANSFORMATION PROMPT:
"Transform this [input format] into [output format]. Maintain [what to preserve]. Adapt [what to change]."

TEACHING PROMPT:
"Explain [concept] to someone who [knowledge level]. Use [teaching method]. Include [examples/analogies]."

DECISION PROMPT:
"Help me decide whether to [choice]. Consider [factor 1], [factor 2], [factor 3]. Use [framework] to evaluate. Recommend [action]."
```

## Advanced Techniques

```
ADVANCED PROMPTING
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

CHAIN OF THOUGHT:
"Let's think through this step-by-step:
1. First, [step 1]
2. Then, [step 2]
3. Finally, [step 3]"

FEW-SHOT LEARNING:
"Here are 2 examples:
Example 1: [Input] → [Output]
Example 2: [Input] → [Output]
Now do the same for: [New input]"

ROLE + CONTEXT + TASK:
"You are [role] working in [context]. Your task is to [specific task] while considering [constraints]."

STRUCTURED OUTPUT:
"Provide your response in this exact format:
## Section 1
[Content]

## Section 2
[Content]"

SELF-CRITIQUE:
"After providing your answer, critique it and suggest 2 improvements."

MULTI-PERSPECTIVE:
"Approach this from 3 angles:
1. [Perspective 1]
2. [Perspective 2]
3. [Perspective 3]
Then synthesize."
```

## Getting Started

To design a new agent or skill:
1. Define the core need it addresses
2. Outline capabilities and boundaries
3. Write system prompt
4. Create example interactions
5. Test with various scenarios
6. Refine based on results

This is the meta-skill that helps you build all other skills.
