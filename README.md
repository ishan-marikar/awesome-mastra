# Awesome Mastra [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of awesome resources for [Mastra](https://mastra.ai), the TypeScript framework for AI-powered applications and agents.

Mastra gives you agents, workflows, memory, tools, evals, and observability as first-class primitives on a modern TypeScript stack. It runs standalone or inside React, Next.js, Node, and most other JavaScript runtimes.

## Contents

- [Official Resources](#official-resources)
- [Getting Started](#getting-started)
- [Core Concepts](#core-concepts)
- [Templates](#templates)
- [Web Framework Integrations](#web-framework-integrations)
- [Agentic UI](#agentic-ui)
- [Storage and Memory](#storage-and-memory)
- [Vector Stores](#vector-stores)
- [Models and Gateways](#models-and-gateways)
- [Tools and Connections](#tools-and-connections)
- [Channels](#channels)
- [Sandboxes and Browsers](#sandboxes-and-browsers)
- [File Storage](#file-storage)
- [Voice](#voice)
- [Auth](#auth)
- [Observability](#observability)
- [Evals and Testing](#evals-and-testing)
- [Deployment](#deployment)
- [Workshops and Courses](#workshops-and-courses)
- [Coding Agents and Skills](#coding-agents-and-skills)
- [Community Projects](#community-projects)
- [Case Studies](#case-studies)
- [Starters and Boilerplates](#starters-and-boilerplates)
- [Articles and Videos](#articles-and-videos)
- [Comparisons and Research](#comparisons-and-research)
- [Community](#community)

## Official Resources

- [Documentation](https://mastra.ai/docs) - Guides, reference, and integrations.
- [GitHub Repository](https://github.com/mastra-ai/mastra) - Apache 2.0 licensed monorepo for the framework.
- [Blog](https://mastra.ai/blog) - Release notes, engineering deep dives, and tutorials.
- [Changelog](https://mastra.ai/blog/category/changelog) - Weekly summaries of shipped features.
- [Templates Gallery](https://mastra.ai/templates) - Runnable starting points for common agent use cases.
- [Resources](https://mastra.ai/resources) - Workshops, books, and research collected by the team.
- [llms.txt](https://mastra.ai/llms.txt) - Machine-readable index of every documentation page, useful for coding agents.
- [Mastra MCP Docs Server](https://www.npmjs.com/package/@mastra/mcp-docs-server) - Serves Mastra docs to your editor over Model Context Protocol.
- [Announcing Mastra 1.0](https://mastra.ai/blog/announcing-mastra-1) - The 1.0 release and what stabilized in it.

## Getting Started

- [Develop Locally](https://mastra.ai/docs/develop) - Scaffold a project, run the dev server, and iterate in Studio.
- [create-mastra Reference](https://mastra.ai/reference/cli/create-mastra) - Every flag for the project generator.
- [Manual Install](https://mastra.ai/reference/manual-install) - Add Mastra to an existing codebase by hand.
- [Project Structure](https://mastra.ai/reference/project-structure) - Where agents, tools, and workflows are expected to live.
- [Mastra CLI Reference](https://mastra.ai/reference/cli/mastra) - Dev server, build, and deployment commands.
- [Build with AI](https://mastra.ai/reference/build-with-ai) - Wire Mastra docs into Cursor, Windsurf, and other agentic editors.
- [Weather Agent](https://github.com/mastra-ai/weather-agent) - Minimal agent plus workflow, the smallest useful example.
- [Kitchen Sink Example](https://github.com/mastra-ai/kitchen-sink-example) - Every primitive exercised in one project.
- [Mastra Tutorial by Firecrawl](https://www.firecrawl.dev/blog/mastra-tutorial) - Third-party walkthrough of building agents in TypeScript.

## Core Concepts

- [Agent Class](https://mastra.ai/reference/agents/agent) - The central abstraction for model, instructions, tools, and memory.
- [Tools](https://mastra.ai/docs/agents/tools) - Typed functions an agent can call.
- [Structured Output](https://mastra.ai/docs/agents/structured-output) - Constrain model responses to a schema.
- [Guardrails](https://mastra.ai/docs/agents/guardrails) - Block or rewrite unsafe input and output.
- [Processors](https://mastra.ai/docs/agents/processors) - Intercept the agent loop for routing, validation, and drift detection.
- [Code Mode](https://mastra.ai/docs/agents/code-mode) - Let agents write and execute code instead of calling tools one at a time.
- [Workflows](https://mastra.ai/docs/workflows/control-flow) - Graph-based orchestration with branching, loops, and parallelism.
- [Suspend and Resume](https://mastra.ai/docs/workflows/suspend-and-resume) - Pause a run and continue it later with persisted state.
- [Human-in-the-Loop](https://mastra.ai/docs/workflows/human-in-the-loop) - Require approval before a workflow continues.
- [Time Travel](https://mastra.ai/docs/workflows/time-travel) - Replay a workflow from an earlier step.
- [Scheduled Workflows](https://mastra.ai/docs/workflows/scheduled-workflows) - Run workflows on a cron-like schedule.
- [Durable Agents](https://mastra.ai/docs/harness/durable-agents) - Long-running agents that survive restarts.
- [Agent Controller](https://mastra.ai/docs/harness/agent-controller) - Session and event API behind the agent harness.
- [Background Tasks](https://mastra.ai/docs/harness/background-tasks) - Offload work from the conversation loop.
- [Signals](https://mastra.ai/docs/harness/signals) - Wake an agent on external events.
- [Message History](https://mastra.ai/docs/memory/message-history) - Conversation persistence and thread management.
- [Working Memory](https://mastra.ai/docs/memory/working-memory) - A durable profile the agent maintains about the user.
- [Semantic Recall](https://mastra.ai/docs/memory/semantic-recall) - Vector search over past messages.
- [Observational Memory](https://mastra.ai/docs/memory/observational-memory) - Memory the agent forms by watching its own runs.
- [Subagents](https://mastra.ai/docs/subagents) - Delegate scoped work to child agents.
- [Skills](https://mastra.ai/docs/skills) - Packaged instructions and tools an agent can load on demand.
- [Context Engineering Guide](https://mastra.ai/docs/guides/context-engineering) - How to decide what goes into the context window.
- [Agent Lifecycle Guide](https://mastra.ai/docs/guides/agent-lifecycle) - What happens between a request and a response.
- [Streaming Guide](https://mastra.ai/docs/guides/streaming) - Stream tokens, tool calls, and workflow events to a client.

## Templates

Official templates from the Mastra team, each a standalone repository you can clone.

- [Deep Research](https://github.com/mastra-ai/template-deep-research) - Human-in-the-loop research assistant built on workflows.
- [Deep Search](https://github.com/mastra-ai/template-deep-search) - Research agent that evaluates its own work.
- [Agent Harness](https://github.com/mastra-ai/template-agent-harness) - General-purpose agent with workspace, shell tools, memory, and schedules.
- [Agent Builder](https://github.com/mastra-ai/template-agent-builder) - Build Mastra agents from natural language or a visual interface.
- [Coding Agent](https://github.com/mastra-ai/template-coding-agent) - Sandboxed code execution with multi-language file management.
- [Browsing Agent](https://github.com/mastra-ai/template-browsing-agent) - Web automation through Browserbase Stagehand.
- [Browser Agent](https://github.com/mastra-ai/template-browser-agent) - Playwright-driven agent built on the Mastra AgentBrowser package.
- [Text to SQL](https://github.com/mastra-ai/template-text-to-sql) - Natural language queries against a local SQLite database.
- [Chat with PDF](https://github.com/mastra-ai/template-chat-with-pdf) - Index PDFs from URLs, then ask questions and generate quizzes.
- [Flash Cards from PDF](https://github.com/mastra-ai/template-flash-cards-from-pdf) - Turn a PDF into structured study cards.
- [PDF Questions](https://github.com/mastra-ai/template-pdf-questions) - Generate comprehension questions from PDF content.
- [CSV to Questions](https://github.com/mastra-ai/template-csv-to-questions) - Analyze tabular data and produce questions from it.
- [Chat with YouTube](https://github.com/mastra-ai/template-chat-with-youtube) - Summaries and answers with clickable citations.
- [GitHub Review Agent](https://github.com/mastra-ai/template-github-review-agent) - Automated pull request code review.
- [Docs Chatbot](https://github.com/mastra-ai/template-docs-chatbot) - Agent that consumes tools from an MCP server for documentation help.
- [Slack Agent](https://github.com/mastra-ai/template-slack-agent) - Slack bot with streaming responses and thread-scoped memory.
- [Google Sheets](https://github.com/mastra-ai/template-google-sheets) - Read and edit spreadsheets through an agent.
- [Meeting Notes](https://github.com/mastra-ai/template-meeting-notes) - Ingest Zoom recordings and push structured notes to Linear or Notion.
- [Meeting Scheduler](https://github.com/mastra-ai/template-meeting-scheduler) - Turn Gmail threads into Google Calendar events.
- [Company Knowledge](https://github.com/mastra-ai/template-company-knowledge) - Index Linear and Notion into pgvector for semantic recall.
- [Customer Feedback Summarization](https://github.com/mastra-ai/template-customer-feedback-summarization) - Turn raw feedback into actionable summaries.
- [Ad Copy from Content](https://github.com/mastra-ai/template-ad-copy-from-content) - Generate ad copy and promotional images from text or PDFs.
- [Docs Expert](https://github.com/mastra-ai/template-docs-expert) - Research assistant that answers with web-sourced citations.
- [Claw Assistant](https://github.com/mastra-ai/template-claw-assistant) - Autonomous assistant that operates a local workspace.
- [OpenAI OSS](https://github.com/mastra-ai/template-openai-oss) - Running Mastra against a local open-weight model.
- [Software Factory](https://github.com/mastra-ai/softwarefactory-template) - Multi-agent software delivery pipeline.
- [Workflow Builder](https://github.com/mastra-ai/workflow-builder-template) - Compose workflows through a builder interface.

## Web Framework Integrations

- [Next.js](https://mastra.ai/integrations/frameworks/next-js) - App Router and route handler integration.
- [React and Vite](https://mastra.ai/integrations/frameworks/vite-react) - Client-side integration with a Vite dev server.
- [TanStack Start](https://mastra.ai/integrations/frameworks/tanstack-start) - Full-stack React integration.
- [SvelteKit](https://mastra.ai/integrations/frameworks/sveltekit) - Server route integration for Svelte apps.
- [Nuxt](https://mastra.ai/integrations/frameworks/nuxt) - Nitro server integration for Vue apps.
- [Astro](https://mastra.ai/integrations/frameworks/astro) - Server endpoints in Astro projects.
- [Express](https://mastra.ai/integrations/frameworks/express) - Mount Mastra inside an existing Express app.
- [Hono](https://mastra.ai/integrations/frameworks/hono) - Edge-friendly server adapter.
- [NestJS](https://mastra.ai/integrations/frameworks/nestjs) - Module-based integration for NestJS services.
- [Electron](https://mastra.ai/integrations/frameworks/electron) - Run agents inside a desktop app.
- [Server Adapters](https://mastra.ai/docs/server/server-adapters) - Expose agents, workflows, and tools as HTTP endpoints on your existing server.
- [Mastra Client SDK](https://mastra.ai/reference/client-js/mastra-client) - Typed JavaScript client for a running Mastra server.

## Agentic UI

- [AI SDK UI](https://mastra.ai/integrations/agentic-ui/ai-sdk-ui) - Stream Mastra agents into the Vercel AI SDK UI hooks.
- [Assistant UI](https://mastra.ai/integrations/agentic-ui/assistant-ui) - Drop-in chat components wired to Mastra.
- [CopilotKit](https://mastra.ai/integrations/agentic-ui/copilotkit) - In-app copilots backed by Mastra agents.
- [OpenUI](https://mastra.ai/integrations/agentic-ui/openui) - Generative UI rendered from agent output.
- [UI Dojo](https://github.com/mastra-ai/ui-dojo) - Mastra paired with several UI frameworks, side by side.
- [AGUI Dojo](https://github.com/mastra-ai/mastra-agui-dojo) - Reference implementations of the AG-UI protocol with Mastra.
- [agentcn](https://github.com/shadcn-labs/agentcn) - Component registry for agent interfaces, in the shadcn style.
- [Mastra Chat Kit](https://github.com/hamchowderr/mastra-chat-kit) - Chat frontend and agent server for the Mastra agent harness.

## Storage and Memory

- [Storage Overview](https://mastra.ai/docs/storage) - Composite storage and how domains map to backends.
- [PostgreSQL](https://mastra.ai/integrations/databases/postgresql) - Production default for messages, workflows, and traces.
- [Neon](https://mastra.ai/integrations/databases/neon) - Serverless PostgreSQL with database branching.
- [libSQL](https://mastra.ai/integrations/databases/libsql) - Local-first SQLite-compatible store, the default for new projects.
- [Turso](https://www.npmjs.com/package/@mastra/turso) - Hosted libSQL for edge deployments.
- [MongoDB](https://mastra.ai/integrations/databases/mongodb) - Document store adapter.
- [MySQL](https://mastra.ai/integrations/databases/mysql) - Adapter that also covers MariaDB.
- [MSSQL](https://mastra.ai/integrations/databases/mssql) - Microsoft SQL Server adapter.
- [OracleDB](https://mastra.ai/integrations/databases/oracledb) - Oracle Database adapter.
- [Aurora DSQL](https://mastra.ai/integrations/databases/aurora-dsql) - Distributed serverless PostgreSQL on AWS.
- [Google Cloud Spanner](https://mastra.ai/integrations/databases/spanner) - Globally distributed relational store.
- [DynamoDB](https://mastra.ai/integrations/databases/dynamodb) - Key-value adapter for AWS-native stacks.
- [ClickHouse](https://mastra.ai/integrations/databases/clickhouse) - Columnar store, a good fit for observability data.
- [DuckDB](https://mastra.ai/integrations/databases/duckdb) - Embedded analytical store.
- [Redis](https://mastra.ai/integrations/databases/redis) - Cache and stream backend.
- [Valkey](https://mastra.ai/integrations/databases/valkey) - Open-source Redis fork adapter.
- [Upstash](https://mastra.ai/integrations/databases/upstash) - Serverless Redis over HTTP.
- [Cloudflare D1](https://mastra.ai/integrations/databases/cloudflare-d1) - SQLite at the edge for Workers deployments.
- [Cloudflare KV](https://mastra.ai/integrations/databases/cloudflare-kv) - Edge key-value storage.
- [Convex](https://mastra.ai/integrations/databases/convex) - Reactive backend platform adapter.
- [Elasticsearch](https://mastra.ai/integrations/databases/elasticsearch) - Search-backed storage adapter.
- [Multi-User Threads](https://mastra.ai/docs/memory/multi-user-threads) - Scoping memory across users and resources.
- [Memory Processors](https://mastra.ai/docs/memory/memory-processors) - Trim, summarize, or filter recalled context.

## Vector Stores

- [pgvector](https://www.npmjs.com/package/@mastra/vector-pg) - Vector search inside PostgreSQL.
- [libSQL Vector](https://www.npmjs.com/package/@mastra/vector-libsql) - Embedded vector index for local development.
- [Pinecone](https://www.npmjs.com/package/@mastra/vector-pinecone) - Managed vector database.
- [Qdrant](https://www.npmjs.com/package/@mastra/vector-qdrant) - Open-source vector search engine.
- [Chroma](https://www.npmjs.com/package/@mastra/vector-chroma) - Developer-friendly embedding store.
- [Astra DB](https://www.npmjs.com/package/@mastra/vector-astra) - Cassandra-backed vector store.
- [Upstash Vector](https://www.npmjs.com/package/@mastra/vector-upstash) - Serverless vector index.
- [Cloudflare Vectorize](https://www.npmjs.com/package/@mastra/vector-vectorize) - Vector search for Workers.
- [LanceDB](https://mastra.ai/integrations/databases/lancedb) - Embedded columnar vector database.
- [S3 Vectors](https://www.npmjs.com/package/@mastra/s3vectors) - Vector storage backed by Amazon S3.
- [Turbopuffer](https://www.npmjs.com/package/@mastra/turbopuffer) - Object-storage-native vector search.
- [Couchbase](https://www.npmjs.com/package/@mastra/couchbase) - Vector search in Couchbase.
- [OpenSearch](https://www.npmjs.com/package/@mastra/opensearch) - Vector and keyword hybrid search.
- [RAG Package](https://www.npmjs.com/package/@mastra/rag) - Chunking, embedding, and retrieval helpers.
- [FastEmbed](https://www.npmjs.com/package/@mastra/fastembed) - Local embedding model with no API calls.
- [Voyage AI](https://www.npmjs.com/package/@mastra/voyageai) - Hosted embedding provider.
- [Embeddings Reference](https://mastra.ai/models/embeddings) - Supported embedding models and dimensions.

## Models and Gateways

- [Models Overview](https://mastra.ai/models) - Unified routing across 40-plus providers.
- [Environment Variables](https://mastra.ai/models/environment-variables) - Provider keys Mastra reads automatically.
- [MastraModelGateway](https://mastra.ai/reference/core/mastra-model-gateway) - Add a custom gateway or proxy in front of providers.

## Tools and Connections

- [MCP](https://mastra.ai/docs/connections/mcp) - Consume and expose Model Context Protocol servers.
- [A2A](https://mastra.ai/docs/connections/a2a) - Agent-to-agent protocol support.
- [ACP](https://mastra.ai/docs/connections/acp) - Agent Client Protocol support for editor integrations.
- [SDK Agents](https://mastra.ai/docs/connections/sdk-agents) - Bring agents built with other SDKs into Mastra.
- [Firecrawl](https://mastra.ai/integrations/tools/firecrawl) - Crawl and scrape pages into agent context.
- [Tavily](https://mastra.ai/integrations/tools/tavily) - Search API tuned for agents.
- [Perplexity](https://mastra.ai/integrations/tools/perplexity) - Answer-oriented web search.
- [Parallel](https://mastra.ai/integrations/tools/parallel) - High-throughput web research API.
- [Bright Data](https://mastra.ai/integrations/tools/brightdata) - Large-scale web data collection.
- [MCP Agent Proxy](https://github.com/mashh-lab/mcp-agent-proxy) - Expose local and remote agents as MCP tools.
- [Apify MCP Agent](https://github.com/apify/actor-mastra-mcp-agent) - Mastra agent that calls Apify Actors over MCP.

## Channels

- [Channels Overview](https://mastra.ai/docs/channels) - Connect an agent to a messaging surface.
- [Slack](https://mastra.ai/integrations/channels/slack) - Threaded conversations with streaming replies.
- [Discord](https://mastra.ai/integrations/channels/discord) - Bot integration for servers.
- [Telegram](https://mastra.ai/integrations/channels/telegram) - Bot API integration.
- [WhatsApp](https://mastra.ai/integrations/channels/whatsapp) - Business API integration.
- [Microsoft Teams](https://mastra.ai/integrations/channels/teams) - Enterprise chat integration.
- [iMessage](https://mastra.ai/integrations/channels/imessage) - macOS-local messaging channel.
- [GitHub](https://mastra.ai/integrations/channels/github) - React to issues and pull requests.

## Sandboxes and Browsers

- [Sandbox Filesystem](https://mastra.ai/docs/sandbox/filesystem) - Give an agent a scoped working directory.
- [Sandbox Computer](https://mastra.ai/docs/sandbox/computer) - Computer-use control inside a sandbox.
- [Sandbox LSP](https://mastra.ai/docs/sandbox/lsp) - Language server access for coding agents.
- [E2B](https://mastra.ai/integrations/sandboxes/e2b) - Hosted code execution sandboxes.
- [Daytona](https://mastra.ai/integrations/sandboxes/daytona) - Managed development environments.
- [Modal](https://mastra.ai/integrations/sandboxes/modal) - Serverless compute sandboxes.
- [Docker](https://mastra.ai/integrations/sandboxes/docker) - Local container sandboxes.
- [Apple Container](https://mastra.ai/integrations/sandboxes/apple-container) - Native macOS containers.
- [Cloudflare Sandbox](https://mastra.ai/integrations/sandboxes/cloudflare-sandbox) - Sandboxes on the Cloudflare network.
- [Vercel Sandbox](https://mastra.ai/integrations/sandboxes/vercel) - Sandboxed execution on Vercel.
- [Amazon Bedrock AgentCore](https://mastra.ai/integrations/sandboxes/agentcore) - AWS-managed agent runtime.
- [Blaxel](https://mastra.ai/integrations/sandboxes/blaxel) - Agent infrastructure sandboxes.
- [Railway](https://mastra.ai/integrations/sandboxes/railway) - Sandboxes on Railway infrastructure.
- [AgentBrowser](https://mastra.ai/integrations/browsers/agent-browser) - Playwright-based browser built for agents.
- [Stagehand](https://mastra.ai/integrations/browsers/stagehand) - Natural language browser automation from Browserbase.
- [BrowserViewer](https://mastra.ai/integrations/browsers/browser-viewer) - Watch an agent drive a browser in real time.
- [Tupper](https://github.com/lightbearco/tupper) - Open-source local sandboxes for untrusted agent code.

## File Storage

- [AgentFS](https://mastra.ai/integrations/file-storage/agentfs) - Virtual filesystem for agent workspaces.
- [Amazon S3](https://mastra.ai/integrations/file-storage/amazon-s3) - Object storage adapter.
- [Google Cloud Storage](https://mastra.ai/integrations/file-storage/google-cloud-storage) - Object storage on GCP.
- [Azure Blob](https://mastra.ai/integrations/file-storage/azure-blob) - Object storage on Azure.
- [Google Drive](https://mastra.ai/integrations/file-storage/google-drive) - Read and write user documents.
- [Vercel Files](https://mastra.ai/integrations/file-storage/vercel-files) - Blob storage on Vercel.
- [Archil](https://mastra.ai/integrations/file-storage/archil) - Low-latency shared disks for agents.
- [Mesa](https://mastra.ai/integrations/file-storage/mesa) - Managed file storage for agent workloads.

## Voice

- [OpenAI Voice](https://mastra.ai/integrations/voice/openai) - Speech-to-text and text-to-speech, including realtime.
- [ElevenLabs](https://mastra.ai/integrations/voice/elevenlabs) - High-quality synthetic voices.
- [Deepgram](https://mastra.ai/integrations/voice/deepgram) - Low-latency transcription.
- [LiveKit](https://mastra.ai/integrations/voice/livekit) - Realtime audio transport for voice agents.
- [AWS Nova Sonic](https://mastra.ai/integrations/voice/aws-nova-sonic) - Speech-to-speech model on Bedrock.
- [Google Voice](https://mastra.ai/integrations/voice/google) - Google speech services, including Gemini Live.
- [Azure Voice](https://mastra.ai/integrations/voice/azure) - Azure Cognitive Services speech.
- [Gladia](https://mastra.ai/integrations/voice/gladia) - Multilingual transcription API.
- [Inworld](https://mastra.ai/integrations/voice/inworld) - Character-focused voice synthesis.
- [Murf](https://mastra.ai/integrations/voice/murf) - Studio-grade text-to-speech.
- [Sarvam](https://mastra.ai/integrations/voice/sarvam) - Speech models for Indic languages.
- [Speechify](https://mastra.ai/integrations/voice/speechify) - Text-to-speech API.
- [Node Audio](https://github.com/mastra-ai/node-audio) - Cross-platform microphone capture and playback for Node.js.
- [Realtime Voice Agent](https://github.com/mastra-ai/Realtime-Voice-Agent) - End-to-end voice agent example.

## Auth

- [Auth Overview](https://mastra.ai/docs/guides/authentication-identity) - Identity and authorization patterns for agent servers.
- [JSON Web Token](https://mastra.ai/docs/auth/jwt) - Verify JWTs on Mastra routes.
- [Simple Auth](https://mastra.ai/docs/auth/simple-auth) - Shared-secret protection for internal deployments.
- [Composite Auth](https://mastra.ai/docs/auth/composite-auth) - Combine several providers on one server.
- [Fine-Grained Authorization](https://mastra.ai/docs/auth/fga) - Per-resource permission checks.
- [Custom Auth Provider](https://mastra.ai/docs/auth/custom-auth-provider) - Bring your own identity system.
- [Clerk](https://mastra.ai/integrations/auth/clerk) - Hosted user management.
- [Better Auth](https://mastra.ai/integrations/auth/better-auth) - Self-hosted TypeScript auth.
- [Supabase](https://mastra.ai/integrations/auth/supabase) - Auth backed by Supabase.
- [Auth0](https://mastra.ai/integrations/auth/auth0) - Enterprise identity provider.
- [WorkOS](https://mastra.ai/integrations/auth/workos) - SSO and directory sync.
- [Okta](https://mastra.ai/integrations/auth/okta) - Enterprise SSO.
- [Firebase](https://mastra.ai/integrations/auth/firebase) - Identity backed by Google Firebase.
- [Google](https://mastra.ai/integrations/auth/google) - Sign-in with a Google workspace or consumer account.

## Observability

- [Tracing](https://mastra.ai/docs/observability/tracing/overview) - Spans for agent runs, tool calls, and workflow steps.
- [Logging](https://mastra.ai/docs/observability/logging) - Structured logs from the framework and your code.
- [Metrics](https://mastra.ai/docs/observability/metrics/overview) - Token, latency, and cost counters.
- [Feedback](https://mastra.ai/docs/observability/feedback) - Attach human scores to traces.
- [OpenTelemetry](https://mastra.ai/integrations/observability/opentelemetry) - Export to any OTLP-compatible backend.
- [Langfuse](https://mastra.ai/integrations/observability/langfuse) - Open-source LLM observability and prompt management.
- [Braintrust](https://mastra.ai/integrations/observability/braintrust) - Evals and tracing platform.
- [LangSmith](https://mastra.ai/integrations/observability/langsmith) - Tracing and dataset tooling.
- [Arize](https://mastra.ai/integrations/observability/arize) - LLM observability and drift monitoring.
- [Arthur](https://mastra.ai/integrations/observability/arthur) - Model monitoring platform.
- [Confident AI](https://mastra.ai/integrations/observability/confident-ai) - Evaluation-first observability.
- [Laminar](https://mastra.ai/integrations/observability/laminar) - Open-source tracing for agents.
- [Datadog](https://mastra.ai/integrations/observability/datadog) - Traces and metrics in Datadog.
- [Sentry](https://mastra.ai/integrations/observability/sentry) - Error tracking for agent servers.
- [PostHog](https://mastra.ai/integrations/observability/posthog) - Product analytics for AI features.

## Evals and Testing

- [Built-in Scorers](https://mastra.ai/docs/evals/built-in-scorers) - Ready-made scorers for relevance, faithfulness, and more.
- [Custom Scorers](https://mastra.ai/docs/evals/custom-scorers) - Write your own judge or heuristic.
- [Quick Checks](https://mastra.ai/docs/evals/quick-checks) - Fast assertions during development.
- [Gates and Verdicts](https://mastra.ai/docs/evals/gates-and-verdicts) - Turn scores into pass or fail decisions.
- [Multi-turn Evals](https://mastra.ai/docs/evals/multi-turn) - Score whole conversations, not single replies.
- [Evals with Memory](https://mastra.ai/docs/evals/evals-with-memory) - Test recall and working memory behavior.
- [Datasets](https://mastra.ai/docs/evals/datasets) - Manage evaluation data sets.
- [Experiments](https://mastra.ai/docs/evals/experiments) - Compare prompt and model variants.
- [Running in CI](https://mastra.ai/docs/evals/running-in-ci) - Gate pull requests on eval results.
- [Vitest Integration](https://mastra.ai/docs/evals/vitest-integration) - Run scorers from your existing test suite.
- [Build an Eval Loop](https://mastra.ai/docs/guides/build-an-eval-loop) - End-to-end guide to measuring and improving an agent.
- [LongMemEval](https://www.npmjs.com/package/@mastra/longmemeval) - Long-horizon memory benchmark harness.
- [Eval Workshop](https://github.com/mastra-ai/eval-workshop) - Workshop material for scorers and eval design.

## Deployment

- [Mastra Server](https://mastra.ai/docs/deployment/mastra-server) - Run Mastra as a standalone service.
- [Web Framework Deployment](https://mastra.ai/docs/deployment/web-framework) - Ship Mastra inside an existing app.
- [Monorepo Deployment](https://mastra.ai/docs/deployment/monorepo) - Build and deploy from a workspace.
- [Cloud Providers](https://mastra.ai/docs/deployment/cloud-providers) - Overview of supported targets.
- [Workflow Runners](https://mastra.ai/docs/deployment/workflow-runners) - Execute workflows on durable infrastructure.
- [Vercel](https://mastra.ai/integrations/deploy/vercel) - Deploy to Vercel Functions.
- [Cloudflare](https://mastra.ai/integrations/deploy/cloudflare) - Deploy to Workers.
- [Netlify](https://mastra.ai/integrations/deploy/netlify) - Deploy to Netlify Functions.
- [AWS Lambda](https://mastra.ai/integrations/deploy/aws-lambda) - Serverless deployment on AWS.
- [Amazon EC2](https://mastra.ai/integrations/deploy/amazon-ec2) - Long-running deployment on EC2.
- [Amazon Bedrock AgentCore](https://mastra.ai/integrations/deploy/aws-bedrock-agentcore) - Managed agent runtime on AWS.
- [Azure App Services](https://mastra.ai/integrations/deploy/azure-app-services) - Deployment on Azure.
- [Digital Ocean](https://mastra.ai/integrations/deploy/digital-ocean) - App Platform deployment.
- [Render](https://mastra.ai/integrations/deploy/render) - Managed container deployment.
- [Kubernetes](https://mastra.ai/integrations/deploy/kubernetes) - Self-hosted cluster deployment.
- [Kubernetes Helm Chart](https://mastra.ai/integrations/deploy/kubernetes-helm) - Chart-based install.
- [Inngest](https://mastra.ai/integrations/deploy/inngest) - Durable workflow execution.
- [Temporal](https://mastra.ai/integrations/deploy/temporal) - Workflow orchestration on Temporal.
- [Mastra on AWS](https://github.com/jalpp/mastraonaws) - Community guide and code for AWS deployments.

## Workshops and Courses

- [Mastra 101](https://mastra.ai/course) - Official course on building your first agent.
- [Mastra Agent Course Source](https://github.com/mastra-ai/mastra-agent-course) - Project files that accompany the course.
- [Workshops Collection](https://github.com/mastra-ai/workshops) - Every workshop run by the Mastra team.
- [Mastracode Workshop](https://github.com/mastra-ai/workshop-mastracode) - Build your own coding agent.
- [MCP Server Workshop](https://github.com/mastra-ai/mcp-server-workshop) - Author an MCP server with Mastra.
- [MCP Server Best Practices Workshop](https://github.com/mastra-ai/mcp-server-best-practice-workshop) - Design guidance for MCP servers.
- [Workflows Workshop](https://github.com/mastra-ai/workflows-workshop) - Control flow, suspension, and error handling.
- [Observational Memory Workshop](https://github.com/mastra-ai/mastra-observational-memory-workshop) - Hands-on memory session.
- [Processors Workshop](https://github.com/mastra-ai/workshop-processors-beyond-guardrails) - Control the agent loop with processors.
- [LongMemEval Workshop](https://github.com/mastra-ai/workshop-longmemeval) - Memory evaluation examples.
- [Mastra Editor Workshop](https://github.com/mastra-ai/workshop-mastra-editor) - Building with the visual editor.
- [DeDevs Mastra Courses](https://github.com/DeDevsClub/mastra-courses) - Community course materials.
- [Building AI Agents 101](https://github.com/wahyudesu/building-ai-agents-101) - Step-by-step community course.
- [AI Engineer Starter](https://github.com/mastra-ai/aie-feb-25-starter-mastra) - The AI SDK masterclass rebuilt on Mastra.

## Coding Agents and Skills

- [Mastra Skills](https://github.com/mastra-ai/skills) - Official agent skills for coding agents working with Mastra.
- [Mastra Code UI](https://github.com/mastra-ai/mastra-code-ui) - Desktop coding agent built with Mastracode and Electron.
- [createCodingAgent](https://mastra.ai/reference/coding-agent/create-coding-agent) - Build a coding agent from the framework primitives.
- [Mastra System Check](https://github.com/goldk3y/mastra-system-check) - Claude Code skill that runs 66 checks against a Mastra project.
- [Mastra Coding Agent by Evil Martians](https://github.com/evilmartians/mastra-coding-agent) - Coding agent with E2B sandbox execution.
- [Good Issue](https://github.com/mastra-ai/good-issue) - Agent skill for writing reproducible open-source issues.
- [Shmastra](https://github.com/just-ai/shmastra) - Build agents and workflows from inside Mastra Studio.

## Community Projects

- [Patter](https://github.com/PatterAI/Patter) - Open-source voice AI SDK for giving agents a phone number.
- [DataFoundry](https://github.com/datagallery-ai/dataagent) - Open-source AI workbench for governed data analysis.
- [Coworker](https://github.com/Array-Ventures/coworker) - Agent with MCP UI, app builder, A2A, and a skills marketplace.
- [AgentStack](https://github.com/ssdeanx/AgentStack) - Multi-agent framework on Mastra with 50-plus tools and A2A orchestration.
- [Golem](https://github.com/AvivK5498/Golem) - Self-hosted platform where each agent gets its own Telegram bot.
- [Personal Assistant Example](https://github.com/mastra-ai/personal-assistant-example) - Official personal assistant built with Mastra and MCP.
- [NotebookLM Clone](https://github.com/mastra-ai/notebooklm-mastra) - Source-grounded research notebook.
- [Repo Base](https://github.com/mastra-ai/repo-base) - Turn a repository into a queryable knowledge base.
- [Recursearch](https://github.com/jalpp/recursearch) - Agent that searches the web and writes research reports.
- [PerfAgent](https://github.com/PerfLab-io/perfagent) - Performance insights agent built on Chrome DevTools internals.
- [Aime Chat](https://github.com/DarkNoah/aime-chat) - Cross-platform desktop chat app with RAG and MCP tools.
- [Secure RAG Multi-Agent](https://github.com/ssdeanx/secure-rag-multi-agent) - Role-based access control over a RAG pipeline.
- [MAID](https://github.com/musa-labs/maid) - Agent that organizes your files over MCP filesystem.
- [GitHub Agent](https://github.com/dwarvesf/github-agent) - Pull request monitoring and reminders with Discord notifications.
- [ReadMe Maker](https://github.com/Nika-HISK/ReadMe-maker) - Generates repository documentation by reading the code.
- [DevTrace AI](https://github.com/JexanJoel/devtrace-ai) - Persistent debugging memory with hybrid retrieval.
- [Romeo](https://github.com/verona-ai/Romeo) - Open-source customer support agent.
- [SupportMesh](https://github.com/sholajegede/supportmesh) - Multi-tenant support operations platform.
- [Recipe Agent SaaS](https://github.com/wasp-lang/recipe-agent-saas-with-mastra) - Full SaaS app built on Wasp and Mastra.
- [A2A Mastra Demo](https://github.com/tubone24/a2a_mastra) - Multi-agent system over A2A with Amazon Bedrock.
- [AI Storyboard](https://github.com/Sri01729/template-ai-storyboard-consistent-character) - Storyboard generation with consistent characters.
- [Reddit Analysis](https://github.com/zessu/reddit-sub-ai-analysis) - Workflows that fetch and analyze subreddits.
- [Plus One](https://github.com/adamraziv/plus-one) - Self-hosted household finance agent with audited mutations.
- [AI Buddies](https://github.com/mastra-ai/ai-buddies) - Demo project showing off individual Mastra features.
- [Atlas](https://github.com/MingyiSecLab/Atlas) - Desktop agent for authorized security assessment with a sandboxed Kali environment.
- [ExploitHunter](https://github.com/justsml/ExploitHunter.app) - Chat-based assistant for security research and penetration testing practice.
- [Gordon](https://github.com/general-liquidity/gordon) - Agent harness aimed at financial markets.
- [JARVIS AI OS](https://github.com/Vishwajeetsrk/JARVIS-AI-OS) - Agent marketplace, plugin SDK, and desktop shell in one project.
- [BlinkAI](https://github.com/MohitGoyal09/BlinkAI) - Privacy-first desktop assistant with voice input and screen context.
- [AgentForge](https://github.com/Agentic-Engineering-Agency/agentforge) - Self-hosted daemon that serves agents over HTTP, Discord, and Telegram.
- [Aielia](https://github.com/3IVIS/buildaharness) - Chat assistant that runs an eleven-layer harness on every turn.
- [Chekku](https://github.com/deserveto/chekku) - Agent studio with browser automation and OpenAI-compatible model support.
- [agentproto](https://github.com/agentproto/ts) - Runtime that projects tools, skills, and agents into CLI, HTTP, MCP, and Mastra.
- [WhatsApp Agent](https://github.com/haasonsaas/wa-agent-mastra) - Persistent-memory WhatsApp bot with circuit breaker and retry logic.
- [AI Finance Agent](https://github.com/alexarevalo9/ai-finance-agent) - Financial profile analysis and personalized recommendations.
- [Samson AI](https://github.com/zessu/samson-ai) - Fitness coach that sends daily recommendations over email and SMS.
- [Doodle AI](https://github.com/Type-Think-AI/doodle-ai) - Photo-to-doodle studio with twelve pluggable agent skills.
- [Kakunin Samples](https://github.com/kakunin-ai/kakunin-samples) - Runnable examples for agent identity and compliance.

## Case Studies

Production deployments documented by the Mastra team and its users.

- [Showcase](https://mastra.ai/showcase) - Index of every published customer story.
- [Salesforce](https://mastra.ai/customers/salesforce) - Agent harness behind Agentforce for 100,000 developers.
- [Replit](https://mastra.ai/customers/replit) - Building and running thousands of agent sandboxes.
- [MongoDB](https://mastra.ai/customers/mongodb) - Internal platform for CI log analysis and support triage.
- [Sanity](https://mastra.ai/customers/sanity) - Content agent that reads and edits structured CMS data.
- [WorkOS](https://mastra.ai/customers/workos) - Internal agents that enrich go-to-market prospect data.
- [Factorial](https://mastra.ai/customers/factorial) - HR agent spanning 25 products with user-level permissions.
- [Counsel Health](https://mastra.ai/customers/counsel-health) - Patient and physician agents for virtual care.
- [StarSling](https://mastra.ai/customers/starsling) - DevOps agent that autofixes GitHub, Linear, and Sentry alerts.
- [Docker](https://www.docker.com/blog/beyond-the-chatbot-event-driven-agents-in-action/) - Event-driven agents that analyze and respond to pull requests.
- [Elastic](https://www.elastic.co/search-labs/blog/agentic-rag) - Agentic retrieval assistant for search and analytics workflows.

## Starters and Boilerplates

- [Mastra Starter](https://github.com/BunsDev/mastra-starter) - General-purpose starter kit for agents and workflows.
- [Nuxt Starter Kit](https://github.com/Strift/nuxt-mastra-starter-kit) - Nuxt 4 app wired to Mastra.
- [TanStack Start Example](https://github.com/ataschz/tanstack-start-mastra-example) - Travel assistant with agent networks and dynamic tool UI.
- [Next.js Example](https://github.com/foxytanuki/mastra-nextjs-example) - Mastra and Next.js following the official docs.
- [Next.js with Assistant UI](https://github.com/koji/mastra-app-template) - Template pairing Mastra with assistant-ui.
- [Chakra](https://github.com/xmlking/chakra) - TanStack Start monorepo with Drizzle, Better Auth, and i18n.
- [Agentic RAG](https://github.com/laoposkj/mastra-agentic-rag) - Local-first RAG pipeline with libSQL or pgvector.
- [DocBank](https://github.com/KenjiPcx/DocBank) - Full-stack RAG-as-a-service template.
- [Mem0 Backend](https://github.com/yashksaini-coder/mastra-mem0-backend) - Dockerized agent server with tools, memory, and workflows.
- [S3 Vector RAG](https://github.com/tied-inc/mastra-s3-vector-rag) - RAG backed by Amazon S3 Vectors.
- [Vibe Stack](https://github.com/CodeAlive-AI/vibe-stack) - Opinionated default stack for AI-native products.

## Articles and Videos

- [Mastra YouTube Channel](https://www.youtube.com/@mastra-ai) - Official talks, demos, and release walkthroughs.
- [Mastra 101 Course Video](https://www.youtube.com/watch?v=dv_SqIhhCuE) - Full course recording on building and deploying agents.
- [Introducing Mastra 101](https://mastra.ai/blog/mastra-101) - How the MCP-led course works inside your editor.
- [Build Your First Agent in TypeScript](https://mastra.ai/blog/build-your-first-agent-course) - Course announcement and curriculum.
- [Examples Blog Category](https://mastra.ai/blog/category/examples) - Worked examples published by the team.
- [AI Agent Observability](https://mastra.ai/ai-agent-observability) - How tracing and evaluation fit together.
- [AI Agent Framework Overview](https://mastra.ai/ai-agent-framework) - The case for a TypeScript-first agent stack.
- [Multi-Agent Workflows with Couchbase](https://dev.to/couchbase/building-multi-agent-workflows-using-mastra-ai-and-couchbase-198n) - Community walkthrough of a multi-agent build.
- [Top TypeScript AI Agent Frameworks](https://dev.to/ialijr/top-5-typescript-ai-agent-frameworks-you-should-know-in-2026-139c) - Where Mastra sits among its peers.
- [Building Exhibit](https://dev.to/humphery7/building-exhibit-an-ai-powered-portfolio-agent-with-mastra-a2a-and-telex-5d15) - Portfolio agent built with A2A and Telex, written up end to end.
- [Building StudySync AI](https://dev.to/paulscreate/building-studysync-ai-how-i-created-a-conversational-study-partner-with-mastra-and-telex-1m6n) - Conversational study partner, from idea to deployment.

## Comparisons and Research

- [Mastra vs LangChain](https://github.com/sholajegede/mastra-vs-langchain) - The same pipeline built twice, with measurements.
- [AI SDK Comparison](https://github.com/kometolabs/ai-sdk-comparison) - Identical examples across Vercel AI SDK, Mastra, LangChain.js, and Genkit.
- [LLM Agent Research](https://github.com/Lin-Guanguo/llm-agent-research) - Source-level control-flow analysis across eight agent frameworks.
- [Memory and Storage Architecture](https://deepwiki.com/mastra-ai/mastra/7-memory-and-storage-architecture) - Generated deep dive into how memory is layered.

## Community

- [Discord](https://discord.gg/mastra-ai) - Official server for questions, help, and project showcases.
- [Discord Guide](https://mastra.ai/docs/community/discord) - How the server is organized and where to ask what.
- [X](https://x.com/mastra) - Release announcements and demos.
- [Newsletter](https://mastra.ai/newsletter) - Periodic updates, tutorials, and ecosystem news.
- [GitHub Issues](https://github.com/mastra-ai/mastra/issues) - Bug reports and feature requests.
- [Contributing to Mastra](https://github.com/mastra-ai/mastra/blob/main/CONTRIBUTING.md) - How to set up the monorepo and land a change.
- [Triage](https://github.com/mastra-ai/mastra-triage) - How incoming issues get sorted.
- [mastra Topic on GitHub](https://github.com/topics/mastra) - Every public repository tagged with the framework.
- [Product Hunt](https://www.producthunt.com/products/mastra) - Launch thread and community feedback.
- [Y Combinator Profile](https://www.ycombinator.com/companies/mastra) - Company background and hiring.

## Contributing

Contributions are welcome. Read the [contribution guidelines](CONTRIBUTING.md) first.
