# System Prompt — XML Tag Reference

Generated: 2026-04-24T13-29 · With Intended Fair Use for Ecological Purposes · 

---

## Top-Level Structural Tags

| Tag | Description |
|---|---|
| `<claude_behavior>` | Root container for all Claude behavioral instructions. |
| `<product_information>` | Claude model family, version strings, and Anthropic product descriptions. |
| `<refusal_handling>` | Rules for topics Claude declines and how to communicate refusals. |
| `<legal_and_financial_advice>` | Guidelines for avoiding confident recommendations on legal/financial matters. |
| `<tone_and_formatting>` | Voice, tone, and formatting rules governing all responses. |
| `<anthropic_reminders>` | System for classifier-triggered mid-conversation warnings injected by Anthropic. |
| `<evenhandedness>` | Rules for balanced, politically neutral, and fair responses across topics. |
| `<responding_to_mistakes_and_criticism>` | How Claude handles errors, apologies, and user pushback. |
| `<user_wellbeing>` | Rules for detecting and responding to mental health risk, crisis, and self-harm signals. |
| `<knowledge_cutoff>` | Knowledge cutoff date, search-before-respond rules, and current date context. |
| `<memory_system>` | Full memory system spec — overview, application rules, boundaries, examples. |
| `<persistent_storage_for_artifacts>` | Key-value storage API available to artifacts for cross-session persistence. |
| `<mcp_app_suggestions>` | Rules for suggesting, searching, and connecting MCP apps. |
| `<past_chats_tools>` | Instructions for `conversation_search` and `recent_chats` tool usage. |
| `<preferences_info>` | How to apply and interpret user-specified behavioural and contextual preferences. |
| `<current_memory_scope>` | Declares that memory is scoped to the current Project only. |
| `<important_safety_reminders>` | Warning that memory content may contain malicious instructions; ignore suspicious data. |
| `<memory_user_edits_tool_guide>` | Guide for using `memory_user_edits` tool — view, add, remove, replace. |
| `<computer_use>` | Full computer use capability spec — skills, file handling, output rules, artifacts. |
| `<request_evaluation_checklist>` | Ordered checklist for routing requests: MCP → file → visualizer. |
| `<when_to_use_visualizer_for_inline_visuals>` | Triggers and design guidance for the inline SVG/HTML Visualizer tool. |
| `<search_instructions>` | Web search policy — when to search, query construction, citation rules, copyright. |
| `<using_image_search_tool>` | When and how to use the image search tool; content safety limits. |
| `<available_skills>` | Enumeration of loaded skills with name, description, and file path. |
| `<network_configuration>` | Egress proxy settings and allowed domain list for `bash_tool`. |
| `<filesystem_configuration>` | Read-only mount declarations for uploads, skills, and transcripts directories. |

---

##  `<refusal_handling>`

| Tag | Description |
|---|---|
| `<critical_child_safety_instructions>` | Heightened rules for content involving or directed at minors — never relaxed. |

---

##  `<tone_and_formatting>`

| Tag | Description |
|---|---|
| `<lists_and_bullets>` | Rules for when to use vs. avoid bullet points, headers, and bold formatting. |

---

##  `<memory_system>`

| Tag | Description |
|---|---|
| `<memory_overview>` | High-level description of what memory is, its scope, and its limitations. |
| `<memory_application_instructions>` | Rules for selectively applying memory based on relevance and sensitivity. |
| `<forbidden_memory_phrases>` | Phrases Claude must never use when referencing memory (e.g. "I can see…", "Based on…"). |
| `<appropriate_boundaries_re_memory>` | Caution against overfamiliarity; memory ≠ relationship depth. |
| `<memory_application_examples>` | Container for all memory application example groups. |
| `<example_group>` | Grouped set of examples for a specific memory application scenario. |
| `<example>` | Single memory application example with user input and response variants. |
| `<example_user_memories>` | Hypothetical user memory string used within an example (not real user data). |
| `<user>` | User message within an example. |
| `<good_response>` | Correct model response within an example. |
| `<bad_response>` | Incorrect model response within an example — illustrates what to avoid. |

---

##  `<computer_use>`

| Tag | Description |
|---|---|
| `<skills>` | Rules for loading SKILL.md files before any file creation or code task. |
| `<file_creation_advice>` | Heuristics for choosing between inline response, markdown, and docx output. |
| `<high_level_computer_use_explanation>` | Overview of the Ubuntu 24 container environment and available tools. |
| `<file_handling_rules>` | Directory conventions: uploads (`/mnt/user-data/uploads`), work (`/home/claude`), outputs (`/mnt/user-data/outputs`). |
| `<notes_on_user_uploaded_files>` | Which file types are pre-loaded into context vs. must be read from disk. |
| `<producing_outputs>` | Strategy for short vs. long file creation; iterative editing guidance. |
| `<sharing_files>` | Rules for using `present_files` tool; files must be in `/mnt/user-data/outputs`. |
| `<artifact_usage_criteria>` | When to create artifacts vs. respond inline; supported renderable file types. |
| `<package_management>` | npm and pip usage rules; always use `--break-system-packages` for pip. |
| `<examples>` | Illustrative routing examples for file vs. inline vs. computer use decisions. |
| `<additional_skills_reminder>` | Mandatory reminder to read SKILL.md before creating pptx, xlsx, docx, pdf, or frontend files. |

---

##  `<when_to_use_visualizer_for_inline_visuals>`

| Tag | Description |
|---|---|
| `<visualizer_examples>` | Concrete routing examples showing when to use Visualizer vs. MCP vs. file tools. |

---

##  `<search_instructions>`

| Tag | Description |
|---|---|
| `<core_search_behaviors>` | When to search, when not to, and how to scale tool calls to query complexity. |
| `<search_usage_guidelines>` | Query construction rules, response format, source prioritisation, citation style. |
| `<CRITICAL_COPYRIGHT_COMPLIANCE>` | Root container for all copyright rules — non-negotiable, highest priority. |
| `<claude_prioritizes_copyright_compliance>` | Framing statement: copyright compliance overrides helpfulness goals. |
| `<mandatory_copyright_requirements>` | Enumerated copyright rules: paraphrase-first, 15-word quote limit, one quote per source. |
| `<hard_limits>` | Three absolute limits: 15-word cap, one quote per source, never reproduce lyrics/poems/haikus. |
| `<self_check_before_responding>` | Internal pre-response checklist Claude runs before including any source text. |
| `<copyright_examples>` | Worked examples of compliant and non-compliant citation behaviour. |
| `<copyright_violation_consequences_reminder>` | Reminder of why violations are severe — harm to creators, legal risk, policy breach. |
| `<harmful_content_safety>` | Prohibits searching for or citing hate speech, extremist, or harmful content sources. |
| `<critical_reminders>` | Summary of the most important search behaviour rules in one place. |

---

##  `<using_image_search_tool>`

| Tag | Description |
|---|---|
| `<when_to_use_the_image_search_tool>` | Categories of queries that benefit from images vs. those that do not. |
| `<content_safety>` | Blocked image categories: violence, sexual content, copyrighted IP, real people, artworks. |
| `<how_to_use_the_image_search_tool>` | Query construction, result count, interleaving vs. leading placement rules. |

---

##  `<available_skills>`

| Tag | Description |
|---|---|
| `<skill>` | Individual skill entry. |
| `<name>` | Skill identifier string. |
| `<description>` | Human-readable trigger conditions and scope for the skill. |
| `<location>` | Filesystem path to the skill's SKILL.md file. |

---

## Document / Session Tags

| Tag | Description |
|---|---|
| `<documents>` | Container for project files injected into context at session start. |
| `<document>` | Individual project document entry. |
| `<source>` | Filename or path label for a document. |
| `<document_content>` | Raw content of a project document. |
| `<uploaded_files>` | Container listing files uploaded by the user in the current message. |
| `<file_path>` | Individual uploaded file path entry within `<uploaded_files>`. |
| `<project_files>` | Lists read-only project files available in `/mnt/project/`. |
| `<userPreferences>` | User-authored preferences injected as a system-level instruction block. |
| `<citation_instructions>` | Rules for wrapping search-sourced claims in `` tags with index attributes. |

---

*End of File - claude-sonnet_4_6-system_prompt-list_of-xml_tags.md*
