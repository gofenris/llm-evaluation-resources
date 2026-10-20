# Tooling for LLM evaluation

This guide describes categories of tools and platforms that can support LLM
evaluation workflows. The appropriate tools depend on the use case, and new
ones emerge frequently.

The listed products and libraries are provided as non-exhaustive examples,
not endorsements or comparisons. For the most part, all examples are those
we have used and explored ourselves.

## Observability tools

LLM observability is the ability to inspect what an application did in
production, extending traditional logging with specific features useful in
LLM systems. These include the capture of traces, inputs/outputs, tool
arguments, and model configurations.

Examples of LLM observability systems and tools:
* Langfuse / Langsmith
* Arize Phoenix (open source)
* OpenLIT / OpenLLMetry
* Helicone

## Evaluation platforms and frameworks

There are tools that provide generalized eval harnesses and commonly useful
eval features almost "out of the box". These are designed to help conduct
experiments, compare models, and compare prompt versions. Some can help implement
offline and online evals.

Examples of LLM eval tools:
* Braintrust
* Promptfoo
* DeepEval
* Inspect AI
* Ragas

## Human review and annotation tools

Human review tools help users and domain experts inspect system inputs,
outputs, and traces; record labels and critiques; and curate eval sets.

General annotation platforms can support this work, but if the _purpose_
is dev / product style evals, a custom data viewer can be the best way to
reduce review friction by presenting the context that matters. (Hamel
Husain's [field
guide](https://hamel.dev/blog/posts/field-guide/#the-most-important-ai-investment-a-simple-data-viewer)
explains why a simple, purpose-built data viewer can be a particularly
valuable investment for these types of evals.)

Examples of human review and annotation tools:
* Argilla
* Label Studio
* Custom data viewers built with Streamlit or Marimo, or purpose-built
  “vibe-coded” applications

## LLM gateways

There are many LLM providers (Anthropic, Bedrock, HuggingFace, ...)
and more than one "standard" for APIs. A gateway provides a single
controlled point. This provides several engineering benefits (a unified
API, model routing for optimizations, and fallbacks) and policy benefits
(rate limits, budget management, and access controls).

Examples of LLM gateways:
* LiteLLM
* OpenRouter
* Cloudflare AI Gateway

From an evals perspective, gateways can simplify the implementation of an eval
harness and reduce common observability challenges. They can enable A/B testing
between models and comparisons of model performance, including cost and
latency.

Remember that gateways channel only LLM calls, but most LLM applications use
multiple components, such as information retrieval and custom systems connected
through agent tools, to complete a task. When evaluating an LLM application, we
care about the system _around_ the model, not just the LLM calls.
