---
name: ai-tooling-orchestrator
description: Architect for your AI tools stack (ChatGPT, Claude, Gemini, Perplexity). Use this skill when designing which agent/tool handles what, mapping workflows, and minimizing overlap. Outputs workflow diagrams, task allocation, and prompt templates tailored per platform.
---

# AI Tooling & Stack Orchestrator

## Overview

This skill helps you design an efficient AI tools ecosystem, determining which AI platform handles which tasks, avoiding redundancy, and maximizing each tool's strengths.

**Keywords**: AI tools, ChatGPT, Claude, Gemini, Perplexity, workflow automation, AI orchestration, prompt engineering, tool selection

## When to Use This Skill

- Map tasks to appropriate AI tools
- Design AI-powered workflows
- Eliminate tool overlap/waste
- Create platform-specific prompts
- Optimize AI subscription value
- Build AI agent systems

## AI Tool Comparison Matrix

```
TOOL CAPABILITY MATRIX
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

CAPABILITY          | ChatGPT | Claude | Gemini | Perplexity
--------------------|---------|--------|--------|------------
Long context        |   ⭐⭐   |  ⭐⭐⭐  |  ⭐⭐⭐  |    ⭐⭐
Code generation     |  ⭐⭐⭐   |  ⭐⭐⭐  |   ⭐⭐  |    ⭐
Web search          |   ⭐⭐   |   ⭐⭐  |  ⭐⭐⭐  |   ⭐⭐⭐
Document analysis   |   ⭐⭐   |  ⭐⭐⭐  |  ⭐⭐⭐  |    ⭐⭐
Creative writing    |  ⭐⭐⭐   |  ⭐⭐⭐  |   ⭐⭐  |    ⭐
Real-time info      |   ⭐    |   ⭐   |  ⭐⭐⭐  |   ⭐⭐⭐
Image generation    |  ⭐⭐⭐   |   ❌   |  ⭐⭐⭐  |    ❌
Structured output   |  ⭐⭐⭐   |  ⭐⭐⭐  |   ⭐⭐  |    ⭐
Reasoning           |  ⭐⭐⭐   |  ⭐⭐⭐  |   ⭐⭐  |    ⭐⭐
```

## Task Allocation Framework

```
TASK → RECOMMENDED TOOL

RESEARCH & INFORMATION
Current events/news → Perplexity or Gemini
Academic research → Claude (deep analysis)
Quick facts → Perplexity
Market research → Gemini (web access)

WRITING & CONTENT
Long-form content → Claude (context window)
Creative stories → ChatGPT or Claude
Technical docs → Claude
Email drafts → Any (personal preference)
Social media → ChatGPT (concise)

CODE & TECHNICAL
Debugging → Claude or ChatGPT
New project → Claude (thoughtful architecture)
Quick scripts → ChatGPT
Code review → Claude (detailed analysis)

ANALYSIS & STRATEGY
Financial analysis → Claude (detailed reasoning)
Strategy docs → Claude
Data interpretation → ChatGPT or Claude
Trend analysis → Gemini or Perplexity

CREATIVE & VISUAL
Image generation → ChatGPT (DALL-E) or Gemini
Design concepts → ChatGPT
Brainstorming → Any (all good)
Mockups → ChatGPT

PRODUCTIVITY
Meeting summaries → Claude
Email management → ChatGPT or Claude
Task planning → Claude (structured thinking)
Quick answers → Perplexity
```

## Workflow Orchestration Examples

### Workflow 1: Content Creation Pipeline

```
CONTENT CREATION WORKFLOW
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Step 1: RESEARCH (Perplexity)
- Gather current info on topic
- Find trending angles
- Collect sources

Step 2: OUTLINING (Claude)
- Synthesize research
- Create detailed outline
- Structure arguments

Step 3: DRAFTING (Claude)
- Write long-form content
- Maintain consistency
- Deep analysis

Step 4: EDITING (ChatGPT)
- Punch up language
- Shorten where needed
- Polish tone

Step 5: VISUAL (ChatGPT/DALL-E)
- Generate featured image
- Create social graphics

Step 6: REPURPOSING (ChatGPT)
- Create social snippets
- Generate email version
- Pull out quotes
```

### Workflow 2: Product Development

```
PRODUCT DEVELOPMENT WORKFLOW
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Step 1: MARKET RESEARCH (Perplexity + Gemini)
- Current market trends
- Competitor analysis
- User needs research

Step 2: PRODUCT DEFINITION (Claude)
- PRD creation
- User stories
- Feature prioritization

Step 3: TECHNICAL PLANNING (Claude)
- Architecture design
- Tech stack selection
- Implementation plan

Step 4: CODE GENERATION (ChatGPT + Claude)
- Boilerplate code (ChatGPT)
- Complex logic (Claude)
- Code review (Claude)

Step 5: DOCUMENTATION (Claude)
- API docs
- User guides
- Technical specs
```

### Workflow 3: Financial Analysis

```
FINANCIAL ANALYSIS WORKFLOW
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Step 1: DATA GATHERING (Gemini/Perplexity)
- Recent financial news
- Market data
- Economic indicators

Step 2: DEEP ANALYSIS (Claude)
- Interpret data
- Build scenarios
- Risk assessment

Step 3: VISUALIZATION CONCEPTS (ChatGPT)
- Chart recommendations
- Dashboard layout
- Data storytelling

Step 4: REPORTING (Claude)
- Written analysis
- Recommendations
- Executive summary
```

## Platform-Specific Prompt Templates

### For Claude (Best for: Deep analysis, long context)

```
CLAUDE PROMPT TEMPLATE

Context:
[Provide comprehensive background - Claude handles long context well]

Task:
[Be specific and structured]

Format:
[Request structured output - Claude excels at this]

Examples:
[Provide 1-2 examples for complex tasks]

Constraints:
[Any limitations or requirements]
```

### For ChatGPT (Best for: Quick tasks, images, concise)

```
CHATGPT PROMPT TEMPLATE

You are a [specific role].

Task: [Clear, concise instruction]

Output format: [Specify structure]

[If using DALL-E: Describe image in detail]

Keep response: [Length constraint if needed]
```

### For Perplexity (Best for: Research, current info)

```
PERPLEXITY PROMPT TEMPLATE

Research question: [Specific question]

Focus areas:
- [Aspect 1]
- [Aspect 2]

Time range: [Last week / month / year]

Sources to prioritize: [Academic / News / Industry]

Deliver: [Summary / Detailed analysis / Bullet points]
```

### For Gemini (Best for: Web-connected tasks, multimodal)

```
GEMINI PROMPT TEMPLATE

Search for: [Topic with web context]

Include:
- Latest developments
- Real-time data
- [Specific sources if needed]

Analyze: [What to look for in the data]

Format: [How to present findings]
```

## Subscription Optimization

```
AI TOOL SUBSCRIPTION STRATEGY
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

ESSENTIAL (Keep subscribed)
✓ Claude Pro ($20/mo)
  - Use for: Long documents, code, analysis
  - Usage: Daily

✓ ChatGPT Plus ($20/mo)
  - Use for: Image generation, quick tasks
  - Usage: Daily

SITUATIONAL (Evaluate monthly)
◯ Perplexity Pro ($20/mo)
  - Use for: Research-heavy projects
  - Usage: As needed (can use free tier)

◯ Gemini Advanced ($20/mo)
  - Use for: Google Workspace integration
  - Usage: If heavily using Google tools

STRATEGY
- Core stack: Claude + ChatGPT ($40/mo)
- Add others for specific projects
- Re-evaluate quarterly based on usage
```

## Custom AI Agent Architecture

```
PERSONAL AI AGENT SYSTEM
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

RESEARCH AGENT (Perplexity)
- Gathers latest information
- Monitors industry trends
- Curates daily briefings

STRATEGY AGENT (Claude)
- Analyzes decisions
- Creates long-term plans
- Reviews opportunities

EXECUTION AGENT (ChatGPT)
- Drafts communications
- Generates quick content
- Handles routine tasks

CREATIVE AGENT (ChatGPT + DALL-E)
- Generates visual content
- Brainstorms ideas
- Creates designs

WORKFLOW
Input → Research Agent → Strategy Agent → Execution Agent → Output
                    ↓
               Creative Agent (as needed)
```

## Getting Started

Tell me:
1. Current AI tools you use
2. Common tasks you perform
3. Pain points or overlaps

I'll design an optimized AI workflow system.
