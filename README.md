
1) PROJECT TITLE

# Adaptive-cognitive-twin-workforce

===================================================================================================================

2) Problem Statement

Enterprises rely on manual workflows such as refunds, IT access requests, onboarding, etc.
These require human interpretation, multi-step execution, memory, and hand-offs.
Traditional automation (RPA, chatbots) fails due to lack of reasoning, flexibility, memory,
and safe decision-making.

ACTW solves this by using Cognitive Twins to automate workflows end-to-end.
====================================================================================================================

3) Solution Summary

ACTW is an intelligent multi-agent system that:
- Extracts workflow steps from documents
- Retrieves the correct workflow using RAG + FAISS
- Uses LLMs to execute workflows step-by-step
- Uses memory to store past actions
- Routes tasks to other agents using A2A routing
- Enforces safety checks
- Provides observability and logs for every action
=====================================================================================================================

4) Architecture Diagram (Text or Image)
   
[ChatGPT Image Dec 1, 2025, 06_42_34 AM.png
](https://github.com/coder-mq/adaptive-cognitive-twin-workforce/blob/main/ChatGPT%20Image%20Dec%201%2C%202025%2C%2006_42_34%20AM.png)

=====================================================================================================================

5) Features
   
- Workflow ingestion from SOP files
- FAISS + embeddings for workflow matching
- LLM-based action generator
- Multi-step task Executor
- Safety guardrails (no PII, human review rules)
- Short-term and long-term memory
- A2A routing (auto-resolve / escalate)
- Full Observability (logs, metrics, events)
- Gradio UI demo
=====================================================================================================================
6) Tech Stack
  
- Python
- HuggingFace Transformers
- FAISS
- SentenceTransformers
- GPT-based LLMs
- Gradio
======================================================================================================================
7) Project Structure

/README.md
/GCP.ipynb
/refund_process.txt
/it_access_request.txt
/onboarding_sop.txt

=========================================================================================================================
8) How To Run (Setup Instructions)

1. Open GCP.ipynb in Google Colab
2. Install dependencies (already inside notebook)
3. Run all cells top to bottom
4. The FAISS index + Cognitive Twin Engine will load
5. A Gradio UI will launch at the end
6. Type queries like:
   - “Refund for defective item”
   - “User cannot access HR portal”
   - “New employee onboarding”
==========================================================================================================================
9) Example Outputs

1) <img width="335" height="294" alt="image" src="https://github.com/user-attachments/assets/3c4ead26-68b6-4ccf-a423-5cc399be99c7" />
2) <img width="391" height="373" alt="image" src="https://github.com/user-attachments/assets/148f5d24-e3ea-4711-b1b7-7623a4f4e6da" />

===========================================================================================================================

10. Safety Features

- No PII in responses
- Requires human review if confidence < 7
- Stops when intent is unclear
- Logs all low-confidence decisions

===========================================================================================================================

11. Memory System

The system stores task history and long-term memory.
Memory enables improved routing and decision-making over time.

============================================================================================================================

12. A2A Routing

The system decides whether to:
- auto resolve
- escalate to IT agent / HR agent
- request human review

==============================================================================================================================

14. Author

Created by: Anvay Awalgaonkar
Role: AI Engineer / Cognitive Automation

===============================================================================================================================

Final Section — Conclusion

This project demonstrates how Cognitive Twins can autonomously execute
enterprise workflows using reasoning, memory, routing, observability,
and document-based workflow extraction.

===============================================================================================================================








