# My-First-AI-Agent
## LinkedIn Carousel Generation Agent

A multi-agent content generation system built using Gumloop that automatically creates high-quality LinkedIn carousels from a topic and a set of reference carousels.

The agent analyzes reference content, learns its style and structure, generates a complete carousel slide-by-slide, critiques its own output, and improves weak slides before producing the final version.

### Gumloop Agent link: https://www.gumloop.com/agents/share/ebHFhqvGfBZfEC8AHNwrvE
---

## Problem Statement

Build a Gumloop Agent that can:

* Analyze reference LinkedIn carousels
* Understand tone, flow, and structure
* Generate a complete LinkedIn carousel
* Maintain style consistency
* Review and improve weak slides
* Produce a polished final output

The generated carousel should include:

* Slide titles
* Slide content
* CTA slide
* Suggested visual idea for each slide

---

## Agent Architecture

```text
User Topic + Reference Carousels
                │
                ▼
        Style Analyzer
                │
                ▼
      Carousel Generator
                │
                ▼
          Critic Agent
                │
                ▼
         Rewrite Agent
                │
                ▼
         Final Carousel
```

### Workflow Overview

The system follows a modular multi-agent architecture rather than relying on a single prompt.

Each stage performs a specialized task, making the workflow easier to maintain, improve, and reuse for different content-generation use cases.

---

## Skills Created

### 1. Style Analyzer

Purpose:

* Analyze reference carousels
* Extract tone and writing patterns
* Learn structure and flow

Outputs:

* Tone profile
* Content framework
* Writing style guidelines

Example Output:

* Bold
* Founder-focused
* Contrarian
* Short-form punchy writing
* Hook → Problem → Insight → Future → CTA

---

### 2. Carousel Generator

Purpose:
Generate a complete LinkedIn carousel based on:

* Topic
* Style profile

Generates:

* Slide title
* Slide content
* Suggested visual idea

Structure:

1. Hook
2. Problem
3. Explanation
4. Insight
5. Future implication
6. CTA

---

### 3. Critic Agent

Purpose:
Evaluate generated content before final delivery.

Evaluation Criteria:

* Engagement
* Clarity
* Style consistency
* Originality
* CTA strength
* Narrative flow

Example Output:

Score: 7.5/10

Weak Slides:

* Slide 2
* Slide 5

Issues:

* Generic wording
* Weak emotional impact
* Style mismatch

---

### 4. Rewrite Agent

Purpose:
Improve weak slides using critic feedback.

Tasks:

* Rewrite weak sections
* Improve engagement
* Maintain style consistency
* Strengthen hooks and CTAs

Output:

Improved carousel with higher quality and consistency.

---

## Design Decisions

### Modular Architecture

Instead of using a single prompt, the workflow is divided into specialized skills.

Benefits:

* Better reliability
* Easier debugging
* Reusable components
* Higher quality outputs

### Critique-and-Refine Loop

A dedicated critic reviews generated content before final delivery.

Benefits:

* Identifies weak sections
* Improves consistency
* Produces stronger final outputs

### Reference-Based Style Learning

The workflow first learns writing style from examples before generating content.

Benefits:

* Better alignment with target content
* Consistent tone
* Improved readability

---

## Sample Outputs

### Topic 1

AI Workflows vs Autonomous AI Agents

Generated:

* 6-slide carousel
* Visual suggestions
* Critic review
* Automated slide improvement

---

### Topic 2

3 Non-Obvious Ways Founders Can Use AI to Save 10 Hours a Week

Generated:

* 6-slide carousel
* Founder-focused style
* Visual suggestions
* CTA optimization

---

## Failure Cases and Limitations

### Weak Reference Content

If the provided reference carousels are low quality, style extraction quality may decrease.

### Conflicting Styles

When references use very different writing styles, the generated output may show inconsistencies.

### Subjective Scoring

Critic scores are based on prompt-defined criteria and may vary depending on content type.

### Niche Technical Topics

Highly specialized topics may require additional domain-specific examples for optimal performance.

---

## Tech Stack

* Gumloop
* Large Language Models (LLMs)
* Prompt Engineering
* Multi-Agent Workflow Design

---

## Future Improvements

* Automatic carousel image generation
* Multiple carousel style modes
* LinkedIn engagement prediction
* A/B testing of hooks and CTAs
* Industry-specific carousel templates

---

## Repository Contents

```text
README.md
architecture/
screenshots/
examples/
submission_notes.md
```

---

## Key Takeaway

This project demonstrates how a complex content-generation task can be decomposed into reusable AI skills that collaborate through a structured workflow. By combining style analysis, content generation, critique, and refinement, the system produces more reliable and higher-quality outputs than a single-prompt approach.
