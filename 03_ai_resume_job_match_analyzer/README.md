Goal: Compare a candidate's resume/skills with a job description and produce a structured match report.

Input
Resume / Skills:
Python, SQL, PySpark, Azure, Databricks, Airflow, Docker

Job Description:
Looking for a Data Engineer with Python, SQL, PySpark,
Databricks, Kafka, AWS and Kubernetes.
Expected output
Match Score: 72/100

Matching Skills:
- Python
- SQL
- PySpark
- Databricks

Missing Skills:
- Kafka
- AWS
- Kubernetes

Strengths:
Strong Data Engineering fundamentals.

Weaknesses:
Limited AWS and Kubernetes experience.

Recommendation:
Good match. Improve AWS and Kubernetes.
Concepts you'll practice
ChatOpenAI
ChatPromptTemplate
from_messages()
Multiple input variables
Chain
invoke()
Pydantic BaseModel
Field
Lists in Pydantic
with_structured_output()
Architecture
Resume ───────────┐
                  ↓
             Prompt
                  ↑
                  │
Job Description ──┘
                  ↓
                 LLM
                  ↓
       Structured Output
                  ↓
              Pydantic
                  ↓
          JobMatch Object
Pydantic target

You should create something like:

JobMatch
├── match_score
├── matching_skills
├── missing_skills
├── strengths
├── weaknesses
└── recommendation

Your challenge: build Project 3 yourself without looking at your Project 2 code too much. This will test whether you really understand multiple prompt variables + Pydantic structured output + chains.