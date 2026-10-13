# Implementation Checklist

Build the application yourself using `PROJECT_BRIEF.md`.

## Initial setup

- [ ] Read the project specification.
- [ ] Review the architecture and data model.
- [ ] Create a Python virtual environment.
- [ ] Install and pin the required dependencies.
- [ ] Configure credentials through environment variables.
- [ ] Review the data privacy and security requirements.

## Project acceptance criteria

- [ ] User can upload at least three file types via API
- [ ] All chunks are embedded and searchable within 2 seconds per 100 KB
- [ ] Neo4j graph contains nodes for each document and extracted entities
- [ ] Summaries ≤ 150 words per document
- [ ] Summaries contain at least two cross‑document references when overlapping concepts exist
- [ ] Natural‑language query returns answer within 3 seconds
- [ ] Answer includes citations (document IDs) when relevant
- [ ] Initialize FastAPI repo, Docker, CI
- [ ] Configure Postgres+pgvector and Neo4j containers
- [ ] Implement LangChain chunking & OpenAI embedding pipeline
- [ ] Define Ingestor and Summarizer agents in CrewAI
- [ ] Integrate summarization LLM (Claude/Local)
- [ ] Store summaries in Postgres
- [ ] Extract entities via spaCy or LLM extraction
- [ ] Populate Neo4j nodes/relationships
- [ ] Design LangGraph state machine for query handling
- [ ] Write unit & integration tests, CI pipeline
- [ ] Add OpenTelemetry tracing
- [ ] Containerise with Docker Compose, draft deployment guide
- [ ] Unit tests for each FastAPI endpoint (pytest)
- [ ] Integration tests that upload a sample doc, verify embedding storage, and retrieve via query
- [ ] Mock LLM calls to test LangGraph state transitions
- [ ] Load test with locust to confirm ≤ 3 seconds response under 10 concurrent users
- [ ] Docker Compose for local dev (api, postgres, neo4j)
- [ ] GitHub Actions builds multi‑arch Docker image and pushes to Docker Hub
- [ ] Optional Helm chart for Kubernetes on self‑hosted clusters
- [ ] Include .env template with API‑key placeholders for local LLMs

## Before completion

- [ ] Implement the planned MVP features.
- [ ] Add unit and integration tests.
- [ ] Run the test suite.
- [ ] Measure the evaluation metrics in the brief.
- [ ] Record actual results and known limitations.
- [ ] Document setup and deployment.
- [ ] Update the README to reflect the implemented features.
- [ ] Add only verified outcomes to your resume.
