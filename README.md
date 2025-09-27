

# EXP 5: COMPARATIVE ANALYSIS OF DIFFERENT TYPES OF PROMPTING PATTERNS AND EXPLAIN WITH VARIOUS TEST SCENARIOS

## Aim

To test and compare how different prompting patterns influence AI-generated responses when given broad/unstructured versus basic/clear prompts across multiple scenarios. The experiment analyzes response quality, accuracy, and depth.

## Introduction

Prompt engineering has become an essential part of interacting with large language models (LLMs). The way a question (prompt) is structured directly impacts the model’s accuracy, creativity, reasoning, and relevance. Broad or unstructured prompts often give vague answers, while refined and clear prompts tend to generate more focused results.

Different prompting patterns—such as zero-shot, few-shot, chain-of-thought, role-based, and refined structured prompts—are commonly used. Each has advantages and limitations depending on the type of task. This experiment systematically compares different prompting patterns across multiple scenarios.

| **Prompting Pattern**            | **Description**                                           | **Strengths**                        | **Limitations**                   |
| -------------------------------- | --------------------------------------------------------- | ------------------------------------ | --------------------------------- |
| **Zero-Shot Prompting**          | Model is asked without examples.                          | Quick, simple.                       | May lack depth/accuracy.          |
| **Few-Shot Prompting**           | Model given examples before answering.                    | Improves accuracy, provides context. | Needs careful example design.     |
| **Chain-of-Thought (CoT)**       | Asking model to explain reasoning step by step.           | Better logical accuracy.             | Sometimes verbose.                |
| **Role Prompting**               | Assigning a role to the model (e.g., "Act as a teacher"). | More focused tone and style.         | Limited if role not well defined. |
| **Refined/Structured Prompting** | Well-structured, clear, detailed instructions.            | High clarity, accurate responses.    | Requires effort to design.        |

### Methodology

Scenarios Selected:

Mathematical reasoning (e.g., word problems).

Creative writing (story/poem generation).

Factual Q&A (historical/technical facts).

Programming task (debugging/writing code).

Decision-making (pros & cons analysis).

### Test Cases:
### Each scenario is tested using:

Broad/Unstructured prompt

Refined/Structured prompt

Zero-shot, Few-shot, Chain-of-Thought, Role-based

### Evaluation Criteria:

Accuracy (correctness of answer)

Quality (fluency, coherence, creativity)

Depth (detailed explanation, reasoning)

Test Scenarios and Results
### Scenario 1: Mathematical Reasoning
| **Prompt Type**    | **Prompt Example**                                   | **Response Quality**             | **Accuracy** | **Depth** |
| ------------------ | ---------------------------------------------------- | -------------------------------- | ------------ | --------- |
| Broad Prompt       | "Solve 25 × 12"                                      | Direct but sometimes incomplete. | 70%          | Low       |
| Refined Structured | "Multiply 25 by 12 and show step-by-step reasoning." | Detailed calculation             | 100%         | High      |
| Zero-Shot          | Just the problem.                                    | Correct but short.               | 80%          | Medium    |
| Few-Shot           | With 2 solved examples.                              | Correct with explanation.        | 95%          | High      |
| CoT                | "Think step by step…"                                | Always correct, detailed.        | 100%         | Very High |

### Scenario 2: Creative Writing
| **Prompt Type**    | **Prompt Example**                                                               | **Creativity**           | **Quality** | **Depth** |
| ------------------ | -------------------------------------------------------------------------------- | ------------------------ | ----------- | --------- |
| Broad Prompt       | "Write a story."                                                                 | Random, unfocused.       | Medium      | Low       |
| Refined Structured | "Write a 150-word story about a child who finds a hidden map in an old library." | Focused, engaging.       | High        | High      |
| Zero-Shot          | "Tell me a story."                                                               | Average.                 | Medium      | Medium    |
| Few-Shot           | With 2 sample stories.                                                           | Mimics style well.       | High        | Medium    |
| Role Prompting     | "Act as a novelist and write a suspenseful short story."                         | Very creative, thematic. | Very High   | High      |

### Scenario 3: Programming Task
| **Prompt Type**    | **Prompt Example**                                    | **Accuracy**                   | **Clarity** | **Depth** |
| ------------------ | ----------------------------------------------------- | ------------------------------ | ----------- | --------- |
| Broad Prompt       | "Fix this code."                                      | May miss errors.               | Low         | Low       |
| Refined Structured | "Debug this Python code for factorial calculation: …" | Correct, clear fix.            | High        | High      |
| Few-Shot           | Provide 2 debugged codes.                             | Correct, follows style.        | High        | Medium    |
| CoT                | "Explain step by step why this code fails."           | Correct, detailed explanation. | Very High   | High      |
| Role Prompting     | "Act as a Python tutor, explain and fix this code."   | Clear and educational.         | Very High   | Very High |

### Scenario 4: Summarization Task

Objective: Compare how different prompts affect summarization quality.

| **Prompt Type**    | **Prompt Example**                                                                               | **Conciseness**                   | **Accuracy** | **Depth** |
| ------------------ | ------------------------------------------------------------------------------------------------ | --------------------------------- | ------------ | --------- |
| Broad Prompt       | "Summarize this text."                                                                           | Too short or incomplete.          | Medium       | Low       |
| Refined Structured | "Summarize the following article in 5 bullet points, highlighting key arguments and conclusion." | Focused and precise.              | High         | High      |
| Zero-Shot          | "Summarize this news article."                                                                   | Good but generic.                 | Medium       | Medium    |
| Few-Shot           | With 2 summary examples.                                                                         | Matches expected style.           | High         | High      |
| Role Prompting     | "Act as a journalist and provide a concise summary of this article for a newspaper column."      | Very natural and reader-friendly. | High         | Very High |

### Scenario 5: Translation Task

Objective: Test prompt impact on accuracy and fluency in translations
| **Prompt Type**    | **Prompt Example**                                                        | **Fluency**                 | **Accuracy** | **Context Handling** |
| ------------------ | ------------------------------------------------------------------------- | --------------------------- | ------------ | -------------------- |
| Broad Prompt       | "Translate into French."                                                  | Literal but awkward.        | Medium       | Low                  |
| Refined Structured | "Translate this English paragraph into French while keeping tone formal." | Smooth, accurate.           | High         | High                 |
| Zero-Shot          | "Translate this."                                                         | Works well for simple text. | Medium       | Medium               |
| Few-Shot           | Provide 2 translations first.                                             | Consistent and accurate.    | High         | High                 |
| Role Prompting     | "Act as a professional translator and provide a natural French version."  | Very fluent and natural.    | Very High    | High                 |

### Scenario 6: Ethical/Opinion-based Question

Objective: Evaluate depth and balance in sensitive discussions.
| **Prompt Type**    | **Prompt Example**                                                                                | **Neutrality**           | **Depth** | **Clarity** |
| ------------------ | ------------------------------------------------------------------------------------------------- | ------------------------ | --------- | ----------- |
| Broad Prompt       | "Is AI good or bad?"                                                                              | Very shallow.            | Low       | Low         |
| Refined Structured | "List 3 positive and 3 negative impacts of AI on employment, then provide a balanced conclusion." | Balanced, insightful.    | High      | High        |
| Zero-Shot          | "Tell me about AI."                                                                               | Generic overview.        | Medium    | Low         |
| Few-Shot           | With sample pros & cons answers.                                                                  | Follows style, balanced. | High      | High        |
| Role Prompting     | "Act as a technology policy analyst and discuss AI’s ethical implications."                       | Deep, analytical.        | Very High | Very High   |

### Scenario 7: Data Analysis (Table Interpretation)

Objective: Compare how prompts handle structured data (like tables)
| **Prompt Type**    | **Prompt Example**                                                                     | **Accuracy**                | **Interpretation Quality** | **Depth** |
| ------------------ | -------------------------------------------------------------------------------------- | --------------------------- | -------------------------- | --------- |
| Broad Prompt       | "Explain this table."                                                                  | Very vague.                 | Low                        | Low       |
| Refined Structured | "From this dataset, find the highest sales year and explain the trend in 3 sentences." | Precise and clear.          | High                       | High      |
| Zero-Shot          | "Analyze sales."                                                                       | General remarks.            | Medium                     | Medium    |
| Few-Shot           | With 2 example analyses.                                                               | Very structured.            | High                       | High      |
| CoT                | "Think step by step to analyze the sales trend across 5 years."                        | Detailed, logical analysis. | Very High                  | Very High |

### Visual Explanation

You can add charts/graphs like:

Bar Chart – Comparing accuracy across prompt types.

Radar Chart – Quality vs. Depth vs. Accuracy per prompt style.

Flow Diagram – Process of broad → refined prompting.

<img width="1080" height="612" alt="image" src="https://github.com/user-attachments/assets/22a8f3d2-d92d-4f1f-8b31-04e3217bdf8f" />

	  
### Analysis & Discussion

Broad prompts produce vague or shallow responses.

Refined prompts consistently improve accuracy and depth.

Chain-of-thought is the most reliable for reasoning-heavy tasks.

Few-shot works best when examples are available.

Role prompting enhances style, tone, and creativity.

## RESULT

This experiment shows that the structure and clarity of a prompt significantly affect the output quality of LLMs. For factual and reasoning tasks, Chain-of-Thought and Refined Prompting yield the best results. For creative writing and explanatory tasks, Role and Few-Shot prompting are highly effective.
