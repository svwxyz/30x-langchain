🚀 Project 5 — AI Data Engineering Query Router
Goal

Build an AI application that receives a user's question and routes it to the appropriate expert chain.

The user enters:

Enter your question:
What is repartition in PySpark?

Your application determines the category:

Python
SQL
PySpark
General Data Engineering

Then sends the question to the appropriate chain.


Your task

Use:

ChatOpenAI
ChatPromptTemplate
RunnableBranch
invoke()
Python if/logic where necessary
Important

For your first version, don't try to make the LLM automatically classify the question.

Instead, ask the user:

Enter category (sql/pyspark/python):

Then use RunnableBranch to route the question.

Example:

Question: What is a JOIN?
Category: sql

→ SQL chain

Question: What is repartition?
Category: pyspark

→ PySpark chain

Expected result
Enter category: pyspark
Enter question: What is repartition?


--- PySpark Expert ---


Repartition is used to...
Challenge

Create 3 chains:

chain_sql
chain_pyspark
chain_python

Then route them using RunnableBranch.

Don't use RunnableParallel or Pydantic yet.