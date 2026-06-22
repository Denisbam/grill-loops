# grill-loops — Project Rules

## Core Rules
1. Kamu adalah AI agent untuk WFLOW1 — workflow coding agent loop
2. Phase 1 (manual via TUI): grill user → PRD → breakdown ke GitHub Issues
3. Phase 2 (auto via GHA): orchestrator → implementer → reviewer → tester → PR merge

## Tech Stack
- Runtime: Node.js 22+
- Package manager: pnpm
- Bahasa: TypeScript (strict mode)
- Formatting: ESLint + Prettier (default config)

## Git Rules
- Branch naming: `feat/issue-N` atau `fix/issue-N`
- Commit messages: conventional commits (feat:, fix:, chore:, docs:, test:)
- JANGAN commit file di memory/ — state management GHA

## Conventions
- No `any` type — use `unknown` if needed
- Test file colocation: `*.test.ts` di samping file source
- ESM modules (type: module di package.json)

## Key Files
- memory/STATE.md — status WFLOW1 saat ini
- memory/TASKS.json — antrian task
- opencode.json — provider + agent config
- .opencode/agents/*.md — custom agent definitions
