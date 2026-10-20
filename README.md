# llm-evaluation-resources
Some resources related to LLM Evaluations.

## Table of Contents
1. [Statement of Scope](#1-statement-of-scope)
2. [Core Concepts to know](#2-core-concepts-to-know)
3. [Resources](#3-resources)
4. [Useful tools](#4-useful-tools)
5. [Articles](#5-articles)

Published by: fenris (`@gofenris`)

Contributors: `@amanahuja`
(contributors, add your github handle here)

## 1. Statement of Scope

This is a list of
* resources related to LLM Evaluations, as defined below.
* primary audience is individuals that are building tools that utilize LLM technologies.
* the tools we have in mind are digital public goods, built for public benefit.

**Opinionated**.  There is a plethora of information available on this
subject, and we are not trying to catalog all of it. Instead we're calling
out resources that we have found valuable. 

What is not included here (Exclusions)
* resources that are primarily promotions for products or services
* model benchmarks or benchmark results

Disclosure: Fenris provides clients with support in implementing LLM evaluations.

## 2. Core Concepts to know

We will not recap key concepts here, as there are already resources and
articles referenced below that provide introductions to evaluation concepts.

On this page and in the comments we use specialized language and refer to
concepts that we want to call out. This is an emerging domain, and
these ideas and terms are not used universally.

**What are LLM Evaluations?**
```txt
Lorem Ipsum. Lorem Ipsum. Lorem Ipsum.
Lorem Ipsum.
Lorem Ipsum.
```

Key terms
* **offline** vs **online** evals.
* **evalsets**
* **traces**
* **LLM model** vs **LLM system**
* Evaluation *harness* 

## 3. Resources

Hamel Husain's resources and blog
* https://hamel.dev/
* Hamel has a blog, online course, trainings, and videos (explainers and interviews/use cases), all focused on LLM evaluations.

## 4. Useful tools

### Observability Tooling

LLM Observability is the ability to inspect what an application did in
production, extending traditional logging with specific features useful in
LLM systems. These include the capture of traces, inputs/outputs, tool
arguments, and model configurations.

Examples of LLM observability systems and tools:
* Langfuse / Langsmith
* Arize Phoenix (open source)
* OpenLIT / OpenLLMetry
* Helicone

### Evaluation Tools

There are tools that provide generalized eval harnesses and commonly useful
eval features almost "out of the box". These are designed to help conduct
experiments, implement offline evals and online evals

Examples of LLM eval tools.
* Braintrust
* Promptfoo

### LLM Gateways

There are many LLM providers (Anthropic, Bedrock, HuggingFace, ...)
and more than one "standard" for APIs. A gateway provides a single
controlled point.  This provides several engineering benefits (a unified
API, also model routing for optimizations, fallbacks), policy benefits
(rate limits, budget management, access controls). 

From an evals perspetive, there are also benefits to using an LLM Gateway, 
as they can simplify the implementation of an eval harness, and offer
simplifications that reduce common observability challenges. They can 
enable A/B testing between models, and compare model performance (ie.
cost/latency). 

Remember that gateways channel only LLM calls, but most LLM applications
utilize multiple components (like information retrieval and custom
systems that might be connected via agent tools) to complete a task. When we
are concerned with evals we care about the system _around_
the model, and not just the LLM model calls. 

## 5. Articles

These are articles that we have found useful, provided here in the style of
an annotated bibliography.

[29 LLM Evaluation Concepts Every Engineer Needs to Know](https://newsletter.systemdesign.one/p/llm-evals), by Anshuman Mishra (April 2026)
- "From 'it looked fine in testing' to a system you can actually trust — a vocabulary/framework guide for engineers new to LLM evals."

Comment by @amanahuja:
> Written for engineers and builders who are familiar with traditional testing like unit-tests; describes basic concepts around LLM evaluations and commonly used language.

[Demystifying Evals For AI agents](https://www.anthropic.com/engineering/demystifying-evals-for-ai-agents) by Anthropic (January 2026)
- "Anthropic's framework for structuring evals for AI agents — single-turn vs. multi-turn, conversational agent evaluation, and eval-driven development."

Comment by @amanahuja:
> For evaluating agents, specifically. Technical guide for engineers.

[Your AI Product Needs Evals](https://hamel.dev/blog/posts/evals/) by Hamel Husain (March 2024)
- A Field Guide to Rapidly Improving AI Products
- Motivation and basics. 

Comment by @amanahuja:
> Written for a technically inclined product leader, this offers a
> perspective on how evals can be used to iteratively improve the quality
> of an LLM-based product. It's 2 years old, but the core concepts still
> stand. Has a "DIY" mindset which is, IMO, a great way to approach evals. 

[A Field Guide to Rapidly Improving AI Products](https://hamel.dev/blog/posts/field-guide/) by Hamel Husain (March 2025)
- Lessons from more than 30 production AI implementations, covering error analysis, custom data viewers, domain-expert participation, synthetic data, trust in evals, and experiment-based roadmaps.

Comment by @amanahuja:
> A practical follow-on to "Your AI Product Needs Evals." Especially useful for teams deciding how to turn evaluation results into an iterative product-development process.

[Using LLM-as-a-Judge For Evaluation: A Complete Guide](https://hamel.dev/blog/posts/llm-judge/) by Hamel Husain (October 2024; updated September 2026)
- A step-by-step process for building an LLM judge and validating it against a domain expert's pass/fail judgments and written critiques.
- Covers dataset construction, true-positive and true-negative rates, and error analysis.

Comment by @amanahuja:
> Useful because it treats an LLM judge as something that must itself be evaluated, rather than as a trustworthy metric out of the box.

[How AI Evaluation Works in Practice: Insights from Implementers](https://www.idinsight.org/article/how-ai-evaluation-works-in-practice-insights-from-implementers/) by Isha Fuletra and Suzin You (February 2026)
- Lessons from organizations deploying AI in health, social protection, justice, and behavior-change programs.
- Connects model evaluation with product behavior, user outcomes, organizational constraints, and social impact.

Comment by @amanahuja:
> Particularly relevant to organizations building AI for public benefit. It shows why evaluation priorities should reflect risk, practical constraints, and the decisions an organization needs to make next.

[How We Built an AI Evaluation Framework with Experts in the Loop](https://datacatalog.urban.org/data-at-urban/how-we-built-ai-evaluation-framework-experts-loop) by Judah Axelrod and Ridhi Purohit, Urban Institute (July 2026)
- A case study on evaluating an AI-ready knowledge base for the Upward Mobility Initiative with domain experts in the loop.

Comment by @amanahuja:
> A useful peer example for research and mission-driven organizations that need subject-matter experts to define and review grounded, well-sourced answers.

[Who Validates the Validators? Aligning LLM-Assisted Evaluation of LLM Outputs with Human Preferences](https://arxiv.org/abs/2404.12272) by Shreya Shankar, J. D. Zamfirescu-Pereira, Björn Hartmann, Aditya G. Parameswaran, and Ian Arawjo (April 2024)
- Presents EvalGen, a system for aligning LLM-generated evaluators with human judgments.
- Introduces "criteria drift": grading outputs helps people define their criteria, so evaluation criteria cannot always be specified completely in advance.

Comment by @amanahuja:
> Provides research support for an iterative, human-in-the-loop approach to developing evaluation criteria and validating automated evaluators.

[Grounding and Evaluation for Large Language Models: Practical Challenges and Lessons Learned](https://arxiv.org/abs/2407.12858) by Krishnaram Kenthapadi, Mehrnoosh Sameki, and Ankur Taly (July 2024)
- A survey of grounding, evaluation, and responsible-AI concerns for generative systems, including hallucinations, prompt injection, harmful content, robustness, and observability.
- A [companion KDD 2024 tutorial](https://sites.google.com/view/llm-evaluation-tutorial) provides slides and organizes the material around identification, measurement, mitigation, and operationalization.

Comment by @amanahuja:
> Useful deep reading for distinguishing grounding from factuality and for understanding evaluation as one part of a broader process for managing system risks.

[Artificial Intelligence Risk Management Framework (AI RMF 1.0), NIST AI 100-1](https://www.nist.gov/itl/ai-risk-management-framework) by the National Institute of Standards and Technology (January 2023)
- A voluntary framework for managing AI risk through the GOVERN, MAP, MEASURE, and MANAGE functions.

Comment by @amanahuja:
> Broader than LLM evaluation, but useful for connecting the context and consequences of an AI system to the rigor and scope of its evaluations.
