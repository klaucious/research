# Claude Code - Opus 4.7 - System Prompt - XML Tag Reference

Generated: 2026-04-26T07-31 · With Intended Fair Use for Ecological Purposes · 

---

## System Prompt Sections

| Section / Tag | Description |
|---|---|
| 1. Identity preamble | States I am Claude Code, Anthropic's CLI, running within the Claude Agent SDK. |
| 2. IMPORTANT (security) | Authorizes defensive/CTF security work and refuses destructive or malicious requests. |
| 3. IMPORTANT (URLs) | Prohibits generating or guessing URLs unless they help with programming. |
| 4. System | Core runtime rules: text output, tool execution, hooks, prompt-injection handling, auto-compaction. |
| 5. Doing tasks | Guidance on handling software engineering requests, security, scope discipline, comments, and feedback channels. |
| 6. Executing actions with care | Requires confirmation for risky, irreversible, or shared-state actions and forbids destructive shortcuts. |
| 7. Using your tools | Tool selection rules: prefer dedicated tools, use TodoWrite, parallelize independent calls. |
| 8. Tone and style | Style rules: no emojis, concise responses, file_path:line_number references. |
| 9. Text output (does not apply to tool calls) | Mandates brief status updates, no narrated deliberation, terse end-of-turn summaries, minimal comments. |
| 10. Session-specific guidance | Notes on subagent usage, Explore agent thresholds, skill invocation, and the `/ultrareview` command. |
| 11. Environment | Working directory, platform, OS, shell, model identity, and Claude Code distribution channels. |
| 12. GitHub Integration | Requires GitHub MCP tools (no `gh` CLI), bans unsolicited PRs, advises frugal commenting. |
| 12.1. PR Activity Events | Describes `<github-webhook-activity>` events and subscription tools. |
| 12.2. Handling PR Activity Events | Decision rules for actioning, asking, or skipping PR webhook events. |
| 12.3. Repository Scope | Restricts GitHub MCP access to `klaucious/rnd`. |
| 13. Task context preamble | Frames me as an assistant for GitHub issues/PRs, with research vs. implementation guidance. |
| 14. Git Development Branch Requirements | Names the feature branch (`claude/document-prompt-structure-LDD5E`) for development. |
| 14.1 Important Instructions | Develop, commit, push to designated branch; create if missing; never push elsewhere. |
| 15. Git Operations | Push/fetch/pull conventions including exponential-backoff retry policy. |
| 16. JSON parameter notice | Reminds that array/object tool parameters must be JSON-structured. |
| 17. Closing tool-use guidance | Rules for inferring parameters, parallel tool calls, and not guessing missing values. |
| 18. `<system-reminder>` (deferred tools) | Lists deferred tool names whose schemas must be loaded via ToolSearch before use. |
| 19. `<system-reminder>` (skills) | Lists Skill-tool-invocable skills available this session. |
| 20. `<system-reminder>` (currentDate) | Provides today's date (2026-04-26) as optional context. |

---
*End of File - claude_code-opus_4_7-system_prompt-list_of-xml_tags.md*
