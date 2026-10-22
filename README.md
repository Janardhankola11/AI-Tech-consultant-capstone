# AI-Tech-consultant-capstone
Developed an AI Tech Consultant Capstone featuring three integrated systems: a Knowledge Brain for retrieving support information with citations, an Inbox Agent for classifying emails and drafting responses, and a Meeting-to-Scope system for extracting requirements, estimating tasks, and generating proposals with human approval.
1. Download your project

📦 Download AI Tech Consultant Capstone — Complete Project ZIP

The ZIP contains 25 project files, including source code, configuration files, documentation, evaluation test cases, and sample customer emails.

Your assignment requires three connected systems, with Tasks 2 and 3 calling Task 1 through its API.

2. What is included?
Task	Project	Technology	Main functionality
Task 1	Knowledge Brain	Python, FastAPI, SQLite	Crawls a help-center sitemap, stores article content, retrieves relevant information, and returns answers with citations
Task 2	Inbox Agent	TypeScript, Node.js, Express	Classifies customer emails, calls the Knowledge Brain, drafts replies, and records human feedback
Task 3	Meeting to Scope	Python, FastAPI	Extracts requirements from meeting transcripts, checks product feasibility, estimates work, and generates a proposal

These are the three components specified in your assignment.

Documentation included
README.md — installation and running instructions.
DESIGN.md — architecture, design decisions, limitations, and future improvements.
EVALS.md — 20 evaluation scenarios for each task.
AI_LOG.md — templates for recording your AI coding-tool prompts.
DEMO_STEPS.md — a suggested demonstration sequence.
sample_emails.jsonl — 50 sample customer emails.
sample_transcripts.md — sample meeting transcripts for development and testing.

The assignment specifies these documentation files and a demonstration video of no more than 10 minutes.

Important: This is a starter implementation, not a fully validated final submission. In particular, image understanding, production-grade vector search, scheduled daily ingestion, and some production safeguards still need development. Evaluation results are deliberately marked as pending rather than invented.

3. How to load it on your laptop
Step 1 — Extract the ZIP
Download the ZIP file above.
Right-click it.
Select Extract All.
Open the extracted ai_tech_consultant_capstone folder.
Step 2 — Install the required software

You will need:

Python 3.11 or later
Node.js 20 or later
Visual Studio Code or another code editor
An Anthropic API key if you want Claude-powered responses

You can inspect the source code before adding any API key.

Step 3 — Run Task 1

Open a terminal inside the extracted project folder and execute:

cd task1_knowledge_brain
python -m venv .venv

On Windows, activate the environment:

.venv\Scripts\activate

Then run:

pip install -r requirements.txt

Copy .env.example to .env, then start the API:

uvicorn app.main:app --reload --port 8001

Open this address in your browser:

Knowledge Brain API documentation

You can use the documentation page to inspect and test the available API endpoints.

Step 4 — Run Task 2

Open a second terminal in the project folder:

cd task2_inbox_agent
npm install

Copy .env.example to .env, then run:

npm run dev

Task 2 runs on port 8002.

Keep Task 1 running because Task 2 calls its API to retrieve information for customer replies.

Step 5 — Run Task 3

Open a third terminal:

cd task3_meeting_scope
python -m venv .venv

Activate the environment, then install the dependencies:

pip install -r requirements.txt

Copy .env.example to .env and start the service:

uvicorn app.main:app --reload --port 8003

Open:

Meeting to Scope API documentation

Keep all three services running when testing the complete workflow.

4. What you must finish before submission

Your assignment has a four-day time limit and requires you to explain your own code during a live review.

Prioritize these remaining tasks:

Task 1: Improve incremental sitemap processing, handle removed articles reliably, and implement image understanding.
Task 2: Test the 50 sample emails, verify the human-review workflow, and improve the autonomy safety rules.
Task 3: Conduct three actual role-play meetings and record their transcripts. One must be a follow-up that changes the original scope.
Evaluation: Run at least 20 test cases per task and record actual quality, cost, and speed measurements.
Documentation: Replace the example AI prompts and rejected-answer description with your actual coding-tool history.
Demo: Record a video showing all three systems working together, including one failure case.

These requirements are part of the assignment's submission and scoring criteria.

My recommendation

Download and extract the project first. Then start Task 1 before attempting Tasks 2 and 3. It is the foundation for the other two services.

Once you have extracted the ZIP, tell me whether you're using Windows 10 or Windows 11. I can guide you through running the project step by step, including resolving installation errors and testing each API.
