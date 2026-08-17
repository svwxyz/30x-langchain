Project 6 — AI Data Engineering Web Research Agent

This will be your first ReAct/Agent project.

Goal

Build an agent that answers Data Engineering questions using two tools:

DuckDuckGo Search → find current information
Calculator → perform calculations

The agent decides which tool to use.

Example

User:

Enter your question:
What is the latest Apache Spark version and how many GB is 2500 MB?

The agent may do:

                    User
                      ↓
                     Agent
                   /       \
                  ↓         ↓
          DuckDuckGo    Calculator
             Search      2500 MB
                  ↓         ↓
              Result      2.5 GB
                  \         /
                   ↓       ↓
                     Agent
                       ↓
                  Final Answer
Your tools

You already know how to create them:

search = DuckDuckGoSearchRun()


@tool
def calculator(...):
    ...

Give both to the agent.

Requirements

Your project should:

Take a question using input()
Have DuckDuckGo as a search tool
Have a calculator tool
Use a LangChain agent
Let the agent decide which tool to use
Print the final answer
Example questions to test
What is the latest version of Apache Spark?
What is 250 * 1024?
Search for the latest Apache Airflow release.
What is 12.5 * 80?

And try a question requiring both tools:

What is the latest Apache Spark version and calculate
how many MB are in 15 GB?
What you should NOT do

Don't manually do:

response.tool_calls[0]

then:

tool.invoke(...)

for this project.

You've already practiced that.

Now the point of the project is to learn:

LLM
 ↓
Agent
 ↓
decides tool
 ↓
executes tool
 ↓
observes result
 ↓
LLM
 ↓
final answer