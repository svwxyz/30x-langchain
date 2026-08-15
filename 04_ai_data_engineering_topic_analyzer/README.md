Project 5 — AI Data Engineering Topic Analyzer 🚀

This one will practice RunnableParallel with 3 chains.

Goal

User enters one topic:

Enter topic: Kafka

Run 3 chains in parallel:

                    Kafka
                      ↓
             RunnableParallel
          ┌───────────┼───────────┐
          ↓           ↓           ↓
      Explanation   Interview   Use Cases
          ↓           ↓           ↓
        Chain 1     Chain 2     Chain 3
Chain 1 — Explanation

Ask:

Explain {topic} in beginner-friendly language.

Chain 2 — Interview

Ask:

Give one beginner-level interview question about {topic}.

Chain 3 — Real-world use

Ask:

Give two real-world Data Engineering use cases of {topic}.

Expected output
--- Explanation ---
Kafka is a distributed event streaming platform...

--- Interview Question ---
What is a Kafka topic?

--- Real-world Use Cases ---
1. Real-time data pipelines
2. Event-driven architectures
Requirements

Use only:

ChatOpenAI
ChatPromptTemplate
3 chains
RunnableParallel
invoke()

Use:

RunnableParallel(
    explanation=chain_one,
    interview=chain_two,
    use_cases=chain_three
)