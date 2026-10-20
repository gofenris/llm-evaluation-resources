# LLM Evaluation Resources for Public-Benefit AI
Some resources related to LLM Evaluations.

## Table of Contents
1. [Statement of Scope](#1-statement-of-scope)
2. [Core Concepts to know](#2-core-concepts-to-know)
3. [Start here](#3-start-here)
4. [Tooling](#4-tooling)

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

LLM evaluation is an emerging domain, and its terminology is not yet used
universally. The definitions below explain how this repository uses several
common terms.

**What are LLM Evaluations?**

LLM evaluations, or “evals”, are structured assessments of AI system behavior
against defined expectations or criteria.

An evaluation can examine a model in isolation, but applications should
generally be evaluated as complete systems. Prompts, retrieved information,
tools, application logic, model responses, and user experience can all affect
the system's behavior. A capable model does not guarantee a capable system.

**Key terms**

* An **eval set** is a curated collection of inputs or scenarios used to assess
  a system. It may also include expected outcomes, labels, criteria, and other
  context needed for evaluation.
* An **LLM model** is the underlying language model. An **LLM system** includes
  one or more models and the surrounding prompts, retrieval, tools, application
  logic, interfaces, and operational controls that shape its behavior. An LLM
  system with multiple interacting components is also known as a **compound AI
  system**.
* A **trace** is a record of a system's execution and a primary source of
  observability into its behavior. Traces help show how a system produced an
  outcome and support diagnosing failures across components. They can include
  inputs, outputs, retrieved context, tool calls and results, model and prompt
  configurations, timing, and other intermediate steps.
* **Offline evals** assess a system before deployment or outside live user
  traffic, often by running a fixed set of cases after a change.
* **Online evals** assess behavior in production, using signals from live
  traffic, monitoring, feedback, or controlled experiments.
* An **evaluation harness** is tooling and code to pass evaluation test
  cases to the system, apply judges and evaluators, compare results, and
  produce reports.
* **Human review** uses people, often users or domain experts, to assess system
  behavior. **Automated evaluation** uses code- or model-based evaluators to
  apply checks at greater scale.

## 3. Start here

These three introductory readings provide complementary starting points:

* [29 LLM Evaluation Concepts Every Engineer Needs to Know](https://newsletter.systemdesign.one/p/llm-evals)
  introduces common evaluation concepts and terminology for engineers.
* [Your AI Product Needs Evals](https://hamel.dev/blog/posts/evals/) explains
  domain-specific evaluation systems and how evals support iterative product
  improvement.
* [How AI Evaluation Works in Practice: Insights from Implementers](https://www.idinsight.org/article/how-ai-evaluation-works-in-practice-insights-from-implementers/)
  connects model evaluation with product behavior, user outcomes, practical
  constraints, and social impact.

See our complete annotated [Evaluations Reading List](docs/reading-list.md)
which covers key concepts in LLM evaluation methods.

## 4. Tooling

Several categories of tools and platforms can support LLM evaluation
workflows. See [Tooling for LLM evaluation](docs/tools.md) for an overview of
observability tools, evaluation platforms and frameworks, and LLM gateways.
