## Hi there I'm Pouya 👋

Data Science student at San José State and backend engineering intern at an AI startup. I build AI systems that have to be right, not just plausible, and most of what I'm proudest of started with noticing that a number was wrong.

I'm also Internal VP of the Mozilla Responsible Computing Club at SJSU, where I teach students to use AI tools without letting them make things up.

## 🛠️ Built

- **[rcc-application-tracking](https://github.com/PA1393/rcc-application-tracking)**: the applicant tracking system for my 300-member student club, built solo in Next.js, TypeScript, and PostgreSQL. It replaced spreadsheet rows, color-coded cells, and Gmail follow-ups with applicant cards and one-click emails, cut application review from a week to a day, and enforces our one-role-per-member rule in code. I shipped 18 fixes in its first four weeks of real use, almost all from reviewer reports.
- **[Dashboard-Engagement](https://github.com/rcc-sjsu/Dashboard-Engagement)**: a club analytics dashboard I built with a team. While writing its queries, I noticed the database had 82 members when the club had about 400, because the import had been failing silently for months. I built a Google Apps Script sync into Supabase and brought it to 399.
- **[Digital Twin](https://github.com/PA1393/ai-engineering-sds)**: a deployed AI version of me that answers questions from my own documents. I wrote the chunker myself (500-character chunks that back off to a paragraph, sentence, or word break), stored OpenAI embeddings in ChromaDB, and added a tool-calling loop that can chain actions, plus a rule that it says it doesn't know instead of guessing.
- **[More RAG and agent experiments](https://github.com/PA1393/ai-engineering-sds)**: a RAG chatbot built from scratch over the Netflix culture doc, a two-agent pipeline that researches a topic and turns it into a LinkedIn post, and two models with opposite instructions debating each other.

## 💼 At work

**Phygtl**, backend engineering intern. The repo is private, so here's the short version: 4 pull requests merged to a production Python, FastAPI, and Postgres backend for an AI assistant that helps moms find local events and each other.

- A matching layer that recognizes the same interest phrased two different ways, using embedding search in pgvector plus an LLM check before any two records merge.
- The engine that decides which nearby users to introduce, written as a Postgres function that keeps people who match on only one signal and filters blocked users before scoring.
- Topic-before-distance ranking for event suggestions, including a fix for a step that silently dropped valid results before they were ever scored.

**SettleKit**, software engineering intern. A drafter-plus-judge LLM system for LinkedIn replies: one model writes, a second scores it against a rubric I built from 25 real conversations, and a human reviews every message before it's sent.

## 🚧 Working on

**Retrieval that knows things, not just similar words.** At Phygtl I ran an embedding probe on production-shaped data and found that similarity search misses connections that need real-world knowledge. Someone asking for violin music should find an Italian music night, but those two don't look alike as vectors. I wrote the redesign: a model reads each event once when it's created and writes down what it connects to, so search can make that hop.

**[CasAI](https://github.com/PA1393/CasAI_Provenance-Lab)**: a research simulation platform I'm building with a friend. I built the RAG pipeline in Supabase and pgvector, from ingesting and chunking sources to retrieving the closest chunks and grounding the model's answer in them.

`Python` `TypeScript` `SQL` `PostgreSQL` `pgvector` `FastAPI` `Next.js` `React` `Supabase` `Prisma` `ChromaDB` `OpenAI API` `Anthropic API` `RAG`

📫 [pouya.anvari1393@gmail.com](mailto:pouya.anvari1393@gmail.com) · [LinkedIn](https://www.linkedin.com/in/pouya-anvari/) · open to Summer 2027 SWE and AI engineering internships
