# LLM evaluation reading list

These are readings that we have found useful, provided here in the style of
an annotated bibliography.

## Foundations

### [29 LLM Evaluation Concepts Every Engineer Needs to Know](https://newsletter.systemdesign.one/p/llm-evals)
*Anshuman Mishra — April 2026*

A vocabulary and framework guide to LLM evaluation concepts for engineers.

**Why we recommend it**

Written for engineers and builders who are familiar with traditional testing
like unit tests; describes basic concepts around LLM evaluations and commonly
used language.

### [Your AI Product Needs Evals](https://hamel.dev/blog/posts/evals/)
*Hamel Husain — March 2024*

An introduction to domain-specific evaluation systems and the role of evals
in improving AI products.

**Why we recommend it**

Written for a technically inclined product leader, this offers a perspective
on how evals can be used to iteratively improve the quality of an LLM-based
product. Has a "DIY" mindset which is a great way to approach evals.

### [A Field Guide to Rapidly Improving AI Products](https://hamel.dev/blog/posts/field-guide/)
*Hamel Husain — March 2025*

Lessons from more than 30 production AI implementations, covering error
analysis, custom data viewers, domain-expert participation, synthetic data,
trust in evals, and experiment-based roadmaps.

**Why we recommend it**

A practical follow-on to "Your AI Product Needs Evals." Especially useful for
teams deciding how to turn evaluation results into an iterative
product-development process.

## Evaluation methods

### [Using LLM-as-a-Judge For Evaluation: A Complete Guide](https://hamel.dev/blog/posts/llm-judge/)
*Hamel Husain — October 2024; updated September 2026*

A step-by-step process for building an LLM judge and validating it against a
domain expert's pass/fail judgments and written critiques. Covers dataset
construction, true-positive and true-negative rates, and error analysis.

**Why we recommend it**

Useful because it treats an LLM judge as something that must itself be
evaluated, rather than as a trustworthy metric out of the box.

## Agents

### [Demystifying Evals For AI Agents](https://www.anthropic.com/engineering/demystifying-evals-for-ai-agents)
*Anthropic — January 2026*

A framework for structuring agent evals, including single-turn, multi-turn,
and conversational evaluations and eval-driven development.

**Why we recommend it**

For evaluating agents, specifically. Technical guide for engineers.

## Evaluation for public-benefit systems

### [How AI Evaluation Works in Practice: Insights from Implementers](https://www.idinsight.org/article/how-ai-evaluation-works-in-practice-insights-from-implementers/)
*Isha Fuletra and Suzin You — February 2026*

Lessons from organizations deploying AI in health, social protection, justice,
and behavior-change programs. Connects model evaluation with product behavior,
user outcomes, organizational constraints, and social impact.

**Why we recommend it**

Particularly relevant to organizations building AI for public benefit. It
shows why evaluation priorities should reflect risk, practical constraints,
and the decisions an organization needs to make next.

### [How We Built an AI Evaluation Framework with Experts in the Loop](https://datacatalog.urban.org/data-at-urban/how-we-built-ai-evaluation-framework-experts-loop)
*Judah Axelrod and Ridhi Purohit, Urban Institute — July 2026*

A case study on evaluating an AI-ready knowledge base for the Upward Mobility
Initiative with domain experts in the loop.

**Why we recommend it**

A useful peer example for research and mission-driven organizations that need
subject-matter experts to define and review grounded, well-sourced answers.

## Research and standards: deep reading

### [Artificial Intelligence Risk Management Framework (AI RMF 1.0), NIST AI 100-1](https://www.nist.gov/itl/ai-risk-management-framework)
*National Institute of Standards and Technology — January 2023*

A framework for managing AI risk through the GOVERN, MAP, MEASURE,
and MANAGE functions.

**Why we recommend it**

Understand how LLM evaluations might fit into a AI governance approach for
an organization. This is a deep dive for those interested in connecting the
context and consequences of an AI system to the rigor and scope of its
evaluations.

### [Who Validates the Validators? Aligning LLM-Assisted Evaluation of LLM Outputs with Human Preferences](https://arxiv.org/abs/2404.12272)
*Shreya Shankar, J. D. Zamfirescu-Pereira, Björn Hartmann, Aditya G.
Parameswaran, and Ian Arawjo — April 2024*

Presents EvalGen, a system for aligning LLM-generated evaluators with human
judgments. Introduces "criteria drift": grading outputs helps people define
their criteria, so evaluation criteria cannot always be specified completely
in advance.

**Why we recommend it**

Provides research support for an iterative, human-in-the-loop approach to
developing evaluation criteria and validating automated evaluators.

### [Grounding and Evaluation for Large Language Models: Practical Challenges and Lessons Learned](https://arxiv.org/abs/2407.12858)
*Krishnaram Kenthapadi, Mehrnoosh Sameki, and Ankur Taly — July 2024*

A survey of grounding, evaluation, and responsible-AI concerns for generative
systems, including hallucinations, prompt injection, harmful content,
robustness, and observability. A
[companion KDD 2024 tutorial](https://sites.google.com/view/llm-evaluation-tutorial)
provides slides and organizes the material around identification, measurement,
mitigation, and operationalization.

**Why we recommend it**

Useful deep reading for distinguishing grounding from factuality and for
understanding evaluation as one part of a broader process for managing system
risks.
