# Day 1 Analysis — Agentic AI Foundations

**Student:** Dineshkumar K
**Program:** B.Tech Artificial Intelligence & Data Science
**Scenario:** Private Course-Fee Information

## 1. Scenario

This project uses a small private dataset containing course codes and their fees:

| Course |     Fee |
| ------ | ------: |
| CS101  | ₹12,000 |
| AI202  | ₹18,000 |
| DS303  | ₹15,000 |

The same course-fee questions are tested using a plain chatbot, a rule-based workflow, and an AI agent.

## 2. Plain Chatbot

The plain chatbot uses only an LLM to generate responses. It does not have access to the private course-fee data or any external tools. Therefore, when asked about the actual fees, it may provide an incorrect answer or state that it does not know the information.

Its main limitation is that it cannot reliably retrieve private data that is not provided in the conversation.

## 3. Rule-Based Workflow

The rule-based workflow does not use an LLM. It uses predefined programming rules to identify course codes, retrieve their fees, and perform supported calculations such as applying a scholarship.

It gives consistent results for questions covered by its rules, but it is less flexible. New question formats or tasks require additional rules to be programmed.

## 4. AI Agent

The AI agent combines an **LLM + Tools + Loop**. It can select tools such as:

* `get_course_fee` — retrieves the fee for a course.
* `calculator` — performs arithmetic calculations.

The agent sends the user's request to the LLM, uses the required tools, observes their results, and continues until it can provide the final answer.

This allows it to handle multi-step questions more flexibly than the fixed workflow.

## 5. Comparison

| Basis               | Plain Chatbot                | Rule-Based Workflow     | AI Agent                   |
| ------------------- | ---------------------------- | ----------------------- | -------------------------- |
| Flexibility         | High for conversation        | Low                     | High                       |
| Decision-making     | LLM response generation      | Predefined conditions   | LLM selects tools/actions  |
| Tool usage          | None                         | Program functions       | Yes                        |
| Private-data access | No                           | Yes                     | Yes, through tools         |
| Multi-step handling | Limited                      | Fixed steps             | Dynamic                    |
| Automation          | Basic responses              | High for defined tasks  | High                       |
| Reliability         | Can hallucinate private data | Consistent within rules | Depends on model and tools |

## 6. Suitability Analysis

For this private course-fee scenario, the **AI agent is suitable when questions require multiple steps or different tools**, while the rule-based workflow is suitable for simple, fixed fee calculations. A plain chatbot is suitable for general conversational questions that do not require private data.

The agent provides flexibility by combining the LLM with tools, while the workflow provides predictable results for predefined cases.

## 7. Conclusion

A **plain chatbot** is appropriate for general conversational responses where private data and complex actions are not required.

A **rule-based workflow** is appropriate when the task has fixed steps, clear conditions, and predictable inputs.

An **AI agent** is appropriate when a task requires an LLM to select tools, use information from those tools, handle multiple steps, and produce a final response.
