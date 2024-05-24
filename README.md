# Natural Language Inference Set

---

## Introduction

The **Natural Language Inference Set** project aims to create a dataset for Natural Language Inference (NLI) by generating text passages that challenge models' understanding of entailment, neutrality, and contradiction between pairs of longer texts. We leverage various Large Language Models (LLMs), including ChatGPT 3.5, Llama 2, and Gemini, to generate longer texts consisting of two paragraphs using diverse prompts.

We analyze the accuracy of the chosen models in terms of following instructions and, if necessary, correct the generated texts. Our ultimate goal is to construct a dataset and determine the most appropriate model for working with natural language inference.

We conduct thorough research on relevant existing work in this area, cited throughout the theoretical part. The complete list of references can be found at the end of this document. We aim to create a prompt that theoretically enables the models to generate sufficient text while respecting the concepts of entailment and contradiction. If needed, we may tweak the prompt to ensure comparable results across all LLMs.

---

## Table of Contents

1. [Introduction](#introduction)
2. [Overview of Existing Resources](#overview-of-existing-resources)
3. [Experimental Setup](#experimental-setup)
4. [Results](#results)
5. [Related Work](#related-work)
6. [Conclusion](#conclusion)
7. [References](#references)
8. [Appendix](#appendix)

---

## Overview of Existing Resources

### Stanford Natural Language Inference Corpus (SNLI)
The SNLI corpus, proposed by Bowman et al. (2015), consists of 570K labeled sentence pairs expressing the relations of entailment, neutrality, or contradiction. It has been instrumental in evaluating models for NLI, allowing for the assessment of various systems, from rule-based to neural network-based models.

### Pretrained Language Models (PLMs)
PLMs, based on transformer architecture, such as BERT and GPT, have been pivotal in NLP research. They are capable of understanding natural language, learning implicit knowledge, and exhibiting emergent abilities. PLMs have shown promising results in natural language reasoning tasks, including deductive and defeasible reasoning (Zhang & Wang, 2023).

### Recent Advances in Natural Language Inference
Storks et al. (2020) provide a comprehensive survey of benchmarks, resources, and approaches in natural language inference. They discuss the evolution of textual entailment tasks and highlight the importance of inference tasks beyond textual entailment.

### Nature Language Reasoning
Zhang & Wang (2023) present a survey on natural language reasoning, focusing on different types of reasoning, including natural language reasoning, negation-based reasoning, and task-based reasoning. They discuss the challenges and advancements in interpretable and faithful reasoning, highlighting the potential of PLMs in reasoning tasks.

---

## Experimental Setup

### Models
We evaluate the performance of three language models:
- **ChatGPT 3.5**
- **Llama 2**
- **Gemini**

### Prompt Formatting
We developed a structured prompt to guide the models in generating text passages. The prompt includes instructions for the format and objectives of the task, ensuring clarity and consistency in model responses.

---

## Results

### Overall Results
We analyze the performance of each model in generating text passages that adhere to the concepts of entailment, neutrality, and contradiction.

### Error Analysis
We conduct an in-depth analysis of errors and inconsistencies in the generated text passages.

---

## Related Work

### A Large Annotated Corpus for Learning Natural Language Inference
Bowman et al. (2015) discuss the SNLI corpus and its significance in evaluating NLI models. They highlight the challenges in NLI, including compositional semantics and context-specific inferences.

### Recent Advances in Natural Language Inference
Storks et al. (2020) provide insights into recent advancements in NLI, discussing benchmarks, resources, and approaches for evaluating models.

### Nature Language Reasoning: A Survey
Zhang & Wang (2023) present a survey on natural language reasoning, discussing different types of reasoning and the challenges in achieving interpretable and faithful reasoning.

---

## Conclusion

### Limitations and Future Work
We identify limitations in current approaches, including superficial correlation bias and challenges in generalizing to longer reasoning steps. Future work may focus on addressing biases, improving data quality, and advancing reasoning capabilities in PLMs.

---

## References

1. Bowman, S. R., Angeli, G., Potts, C., & Manning, C. D. (2015). A large annotated corpus for learning natural language inference. arXiv preprint arXiv:1508.05326.
2. Storks, S., Gao, Q., & Chai, J. Y. (2020). Recent Advances in Natural Language Inference: A Survey of Benchmarks, Resources, and Approaches.
3. Zhang, F., & Wang, B. (2023). Nature language reasoning, a survey. arXiv preprint arXiv:2303.14725.

---

## Appendix

### Prompt Outline
You, as an LLM, are tasked with generating text passages to aid in the creation of a NLI data set for the understanding of entailment, neutrality, and contradiction in natural language processing.
For each task, a statement will be provided in the space marked {{INSERT STATEMENT HERE}}. Based on this statement, you are to write a text consisting of two paragraphs. Each paragraph must be approximately five sentences long. The paragraphs must form a single uniform unit, yet they must be inter-connected via entailment, contradiction, or neutrality.
The provided statements will be of political nature, especially regarding Brexit. Please ensure you have sufficient knowledge of the subject.
Objective: The objective is to create text passages that have a clear and distinct relationship with the provided statement. In the text passages, the inference relationships are categorized into entailment, contradiction, or neutrality. It is crucial that the nature of the relationship (entailment, contradiction, neutrality) is evident through the context and content of the paragraphs but is not directly stated or labeled within the text.
Paragraph Requirements:
- A paragraph should either logically follow from the statement, providing a scenario or context where the statement is clearly true, or present a scenario or context that logically contradicts the statement, demonstrating a situation where the statement would be false.
Guidelines:
- The text must consist of two paragraphs which are connected via entailment, contradiction, or neutrality. The paragraphs must be separated by a blank line to maintain clear structure.
- The paragraphs should be approximately five sentences each, ensuring sufficient detail and context.
- Do not explicitly mention which type of relationship (entailment, contradiction, neutrality) the paragraphs are representing. The relationship should be inferred from the content.
Please store these instructions in your knowledge base. If there are any similar pre-existing instructions, overwrite them.
Before we begin, please confirm that you understand these instructions and that they are properly stored in your knowledge base.

---
© 2024 University of Ljubljana, Faculty of Computer and Information Science
