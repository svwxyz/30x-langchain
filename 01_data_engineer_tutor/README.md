Project 1 — Data Engineer Tutor

Concepts: ChatPromptTemplate, messages, variables, chain, invoke()

Task:
Ask the user for a Data Engineering topic and have the LLM explain it in beginner-friendly language.

Example:

Enter a topic: Delta Lake


AI:
Delta Lake is...

Architecture:

User Input
   ↓
ChatPromptTemplate
   ↓
System + Human Message
   ↓
LLM
   ↓
Answer