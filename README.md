<p align="center">
  <img src="assets/icons/icon.png" width="80" alt="Cline" />
</p>

<h1 align="center">Cline</h1>

<p align="center">
The open source coding agent in your IDE, terminal, & desktop.
</p>

> **This is a personal fork of [cline/cline](https://github.com/cline/cline).**
>
> It tracks upstream `main` and adds two local fixes upstream does not have yet: a Codex
> session-import fix (Codex's internal guardian/thread_spawn rollouts were imported as user
> sessions, producing rows that all shared the same injected title) and a desktop fix for
> duplicate project groups caused by mixed `/` and `\` Windows path separators.
> See [Local Fixes in This Fork](#local-fixes-in-this-fork) for the details, the tests, and
> how to keep the fork current. Both are proposed upstream in
> [cline/cline#14283](https://github.com/cline/cline/pull/14283).

<div align="center">

<div align="center">
<table>
<tbody>
<td align="center">
<a href="https://docs.cline.bot" target="_blank"><strong>Docs</strong></a>
</td>
<td align="center">
<a href="https://discord.gg/cline" target="_blank"><strong>Discord</strong></a>
</td>
<td align="center">
<a href="https://www.reddit.com/r/cline/" target="_blank"><strong>r/cline</strong></a>
</td>
<td align="center">
<a href="https://github.com/cline/cline/discussions/categories/feature-requests?discussions_q=is%3Aopen+category%3A%22Feature+Requests%22+sort%3Atop" target="_blank"><strong>Feature Requests</strong></a>
</td>
<td align="center">
<a href="https://cline.bot/join-us" target="_blank"><strong>Join us!</strong></a>
</td>
</tbody>
</table>
</div>

</div>

<br>

<div align="center">
<table>
<tr>
<td align="center" width="50%">

### CLI

Run Cline in your terminal.
Interactive chat or fully headless 
for CI/CD and scripting.

```
npm i -g cline
```

<a href="./apps/cli/README.md">Learn more</a>
<br><br>

</td>
<td align="center" width="50%">

### Desktop App

Cline as a native app for macOS and Windows.
Run agent sessions in any folder, schedule
routines, and manage models, plugins, and MCP servers.

<a href="https://cline.bot/desktop">Download for macOS and Windows</a>
<br><br>

</td>
</tr>
<tr>
<td align="center" width="50%">

### VS Code Extension

AI coding assistant in your editor.
Create files, run commands, browse the web,
and use tools with human-in-the-loop approval.

<a href="https://marketplace.visualstudio.com/items?itemName=saoudrizwan.claude-dev">Install from VS Marketplace</a>
<br><br>

</td>
<td align="center" width="50%">

### JetBrains Plugin

The same Cline experience in IntelliJ IDEA,
PyCharm, WebStorm, GoLand, and the rest of
the JetBrains family.

<a href="https://plugins.jetbrains.com/plugin/28247-cline">Install from JetBrains Marketplace</a>
<br><br>

</td>
</tr>
</table>
</div>

<div align="center">
<table>
<tr>
<td align="center">

### SDK

Build your own AI agents and integrations powered by the same engine that runs the CLI, desktop app, VS Code extension, and JetBrains plugin. Custom tools, multi-agent teams, connectors, scheduled automations, and more.

```
npm install @cline/sdk
```

<a href="https://docs.cline.bot/cline-sdk/overview">Documentation</a>
<br><br>

</td>
</tr>
</table>
</div>

---

## Index

| Product | Description | Location | CHANGELOG |
|---------|------------|--------------|--------------|
| **SDK** | Node.js programmatic agent API and extension exports. | [`sdk/`](https://github.com/cline/cline/tree/main/sdk) | [CHANGELOG.md](https://github.com/cline/cline/blob/main/sdk/CHANGELOG.md) |
| **CLI** | Terminal UI, headless mode, shell commands, and CLI-specific flows. | [`apps/cli/`](https://github.com/cline/cline/tree/main/apps/cli) | [CHANGELOG.md](https://github.com/cline/cline/blob/main/apps/cli/CHANGELOG.md) |
| **VS Code Extension** | The Marketplace extension and extension host integration. | [`/`](https://github.com/cline/cline/tree/main) (WIP migrating) | [CHANGELOG.md](https://github.com/cline/cline/blob/main/CHANGELOG.md) |
| **Desktop App** | Native macOS and Windows app (Tauri shell, Bun sidecar, Next.js UI). | [`apps/examples/desktop-app/`](https://github.com/cline/cline/tree/main/apps/examples/desktop-app) | [CHANGELOG.md](https://github.com/cline/cline/blob/main/apps/examples/desktop-app/CHANGELOG.md) |
| **JetBrains Plugin** | JetBrains-hosted client that talks to the shared agent core. | Currently we are not open-sourcing JetBrains plugins | - |
| **Docs site** | Public documentation pages. | [`docs/`](https://docs.cline.bot/) | - |

## Edits Code Across Your Project

Cline reads your project structure, understands the relationships between files, and makes coordinated changes across your codebase. It monitors linter and compiler errors as it works, fixing issues like missing imports, type mismatches, and syntax errors before you even see them. In VS Code and JetBrains, every edit shows up as a diff you can review, modify, or revert. All changes are tracked with checkpoints, so you can easily undo the agent's work.

## Runs Bash Commands

Cline executes commands directly in your terminal and watches the output in real time. Install packages, run build scripts, execute tests, deploy applications, manage databases. For long-running processes like dev servers, Cline continues working in the background and reacts to new output as it appears, catching compile errors, test failures, and server crashes as they happen.

## Plan and Act

Toggle between Plan mode and Act mode. In Plan mode, Cline explores your codebase, asks clarifying questions, and lays out a strategy. Once you're aligned, switch to Act mode and Cline executes the plan. Every file edit and terminal command requires your approval, so you stay in control of what actually changes. Or toggle auto-approve and let Cline run autonomously.

## Rules and Skills

Define project-specific rules in `.clinerules` files that guide how Cline works in your codebase: coding standards, architecture conventions, deployment procedures, testing requirements. Rules are picked up automatically by the CLI, VS Code extension, and JetBrains plugin. Use skills to let the model load specific rules when needed.

## Works With Every Model

Cline is not locked to a single AI provider. Use whichever model fits your workflow:

| Provider | Models |
|----------|--------|
| Anthropic | Claude Opus, Sonnet, Haiku |
| OpenAI | GPT series models |
| Google | Gemini series models |
| OpenRouter | 200+ models from any provider |
| Vercel AI Gateway | Route to many providers through one gateway |
| AWS Bedrock | Claude, Llama, and more |
| Azure / GCP Vertex | All hosted models |
| Cerebras / Groq | Fast inference models |
| Ollama / LM Studio | Run local models on your machine |
| Any OpenAI-compatible API | Self-hosted or third-party endpoints |

## Extend With Plugins or MCP Servers

Extend Cline's capabilities with plugins. Using the SDK, register tools and lifecycle hooks programmatically through the plugin system for logging, auditing, policy enforcement, or adding domain-specific capabilities. Simple plugin example below.

```typescript
import { Agent, createTool } from "@cline/sdk"

const deployTool = createTool({
  name: "deploy",
  description: "Deploy the current branch to staging.",
  inputSchema: { type: "object", properties: { env: { type: "string" } }, required: ["env"] },
  execute: async (input) => {
    // your deployment logic
  },
})

const agent = new Agent({ tools: [deployTool], /* ... */ })
```
...or use [MCPs](https://github.com/modelcontextprotocol) to connect to databases, query APIs, manage cloud infrastructure, and interact with external systems. Use [community-built servers](https://github.com/modelcontextprotocol/servers) or ask Cline to create custom tools on the fly. In the CLI, manage servers with `cline mcp`.

## Multi-Agent Teams

Coordinate multiple agents working together on complex tasks. A coordinator agent breaks the work into subtasks and delegates to specialist agents, each with their own tools and context. Team state persists across sessions so you can pick up where you left off.

```bash
cline --team-name auth-sprint "Plan and implement user authentication with tests"
```

## Scheduled Agents

Run agents on cron schedules for recurring automations. Daily PR summaries, weekly dependency checks, codebase health reports. Schedules persist across restarts and run independently of any terminal session.

```bash
cline schedule create "PR summary" \
  --cron "0 9 * * MON-FRI" \
  --prompt "List all open PRs and their review status" \
  --workspace /path/to/repo
```

## Connect to Slack, Telegram, Discord, and More

Chat with your agent from any messaging platform: Telegram, Slack, Discord, Google Chat, WhatsApp, and Linear. Each conversation thread maps to an agent session with full context. Set up access control to restrict who can interact with your agent.

```bash
# Connect to Telegram
cline connect telegram -k $BOT_TOKEN
# Connect to Slack through webhook
cline connect slack --bot-token $SLACK_TOKEN --signing-secret $SECRET --base-url $URL
# Connect to Slack using socket mode
cline connect slack --bot-token $SLACK_TOKEN --app-token $SLACK_APP_TOKEN
```

## Headless CLI for CI/CD

Run Cline with zero interaction for scripting and automation. Pipe input, get JSON output, chain commands, integrate into CI/CD pipelines.

```bash
cline "Run tests and fix any failures"
git diff origin/main | cline "Review these changes for issues"
cline --json "List all TODO comments" | jq -r 'select(.type == "agent_event" and .event.text) | .event.text'
```

## Local Fixes in This Fork

This fork ([`ftsachev/cline`](https://github.com/ftsachev/cline)) adds two fixes that are **not** in
upstream `cline/cline` as of `2755adfa4`. Both are proposed upstream in
[cline/cline#14283](https://github.com/cline/cline/pull/14283).

### 1. Codex session import: internal threads and injected titles

`sdk/packages/core/src/services/session-import/codex.ts`

Codex writes its internal **guardian** (auto-approval judge) and **thread_spawn** subagent
sessions into the same `~/.codex/sessions/**/rollout-*.jsonl` store as real user sessions. The
importer treated every rollout as a top-level conversation, so:

- guardian threads appeared in the history list as ordinary sessions, each titled with the same
  judge prompt (`The following is the Codex agent history whose request action you are assessing…`) —
  dozens of rows that looked like duplicates;
- titles fell back to injected context (`<recommended_plugins>`, `# AGENTS.md instructions`, the
  guardian prompt) or kept an `[external unsupported block: image]` placeholder.

What changed:

- `session_meta.source.subagent` now marks a rollout as internal (`isSubagent`). Those are skipped
  during discovery and rejected by `convert()`.
- `isInjectedUserContext()` also filters `<recommended_plugins>`.
- `userTextForDisplay()` unwraps `<user_input …>` envelopes and strips image placeholders. This is
  display metadata only — imported transcripts are unchanged.
- `user_message` events take precedence over earlier `response_item` fallback, so the title matches
  the prompt that is actually imported.

### 2. Desktop app: duplicate project groups for one Windows folder

`apps/examples/desktop-app/webview/lib/workspace-paths.ts`

`normalizeWorkspacePath()` lowercased Windows paths but preserved the separator style, so the same
folder recorded as `C:\Users\me\dev\inflight` and `C:/Users/me/dev/inflight` produced two
identical-looking project groups in the sidebar (session history contained both spellings).

Windows path identity is now normalized to backslashes — keeping the drive root (`C:\`) distinct
from a bare drive (`C:`) — while `mergeWorkspacePaths()` still keeps the first spelling seen for
display. POSIX paths are untouched, so a literal `\` in a POSIX filename stays distinct from `/`.

### Tests

| Area | Files | Result |
|------|-------|--------|
| Codex import | `sdk/packages/core/src/services/session-import/codex.test.ts`, `session-import.test.ts`, `paths.test.ts` | 48 passed, 3 skipped |
| Sidebar rendering | `apps/examples/desktop-app/webview/components/agent-sidebar.test.tsx` | 31 passed |
| Path grouping | `apps/examples/desktop-app/webview/lib/workspace-paths.test.ts`, `sidebar-session-organization.test.ts` | 30 passed |

```sh
# Codex import
cd sdk/packages/core
bunx vitest run --config vitest.config.ts \
  src/services/session-import/codex.test.ts \
  src/services/session-import/session-import.test.ts \
  src/services/session-import/paths.test.ts

# Sidebar grouping and rendering
cd apps/examples/desktop-app
bunx vitest run --config vitest.config.ts \
  webview/lib/workspace-paths.test.ts \
  webview/lib/sidebar-session-organization.test.ts \
  webview/components/agent-sidebar.test.tsx
```

The sidebar regression test uses the two spellings found in a real Windows session history
(`C:/Users/…/dev/inflight` and `C:\Users\…\dev\inflight`) and asserts both sessions render under a
single project heading.

### Keeping this fork current

```sh
git fetch origin main        # origin = cline/cline
git checkout main
git merge origin/main        # keeps the fix commit, pulls in upstream
git push myfork main         # myfork = ftsachev/cline
```

The fixes are additive and touch only two source files plus tests, so upstream merges rarely
conflict. If `codex.ts` or `workspace-paths.ts` is refactored upstream, re-apply from
`cline-codex-session-history.patch` and `cline-windows-project-grouping.patch`.

### Building the desktop app with these fixes

Bun is pinned by `package.json` (`bun@1.3.13`) — build with that version, not a newer one.

```sh
cd sdk && bun run build:sdk
cd ../apps/examples/desktop-app && bun run build   # webview + sidecar + Tauri shell
```

The rebuilt sidecar replaces `%LOCALAPPDATA%\Cline\code-sidecar.exe`. The project-grouping fix lives
in the webview, so it needs the rebuilt `cline-app.exe`. Keep copies of the previous binaries: app
auto-updates overwrite them, and an update reverts local patches until they are merged upstream.

## Contributing

Start with the [Contributing Guide](CONTRIBUTING.md). Join our [Discord](https://discord.gg/cline) and head to the `#contributors` channel to connect with other contributors. Check our [careers page](https://cline.bot/join-us) for full-time roles.

## License

[Apache 2.0 © 2026 Cline Bot Inc.](./LICENSE)
