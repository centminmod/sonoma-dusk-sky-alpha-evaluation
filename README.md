Sonoma Dusk Alpha and Sonon Sky Alpha are 2 new stealth LLM models just released with 2 million context window sizes. I wanted to test them for code analysis for my csfa.sh nftables wrapper script and GitHub workflow action test against other LLM models I use. I have paid subscriptions and accounts with:

* OpenAI ChatGPT Plus
* Claude AI Max $100
* Gemini AI Pro
* T3 Chat
* OpenRouter AI
* KiloCode

I tested 13 AI LLM models for code analysis and summaries and then used 6 AI LLM models to rank all 13 AI LLM model responses.

The 6 AI LLM models which did response evaluation rankings are:

* Claude Code Opus 4.1
* ChatGPT GPT-5 Thinking
* Gemini 2.5 Pro Web
* Grok 4 via T3 Chat
* Sonoma Sky Alpha via KiloCode

The 13 AI LLM models evaluated by above 6 models are:

* OpenAI Codex GPT-5 Medium Thinking
* OpenAI ChatGPT GPT-5 Thinking
* Claude Code Opus 4.1
* Claude AI Web Opus 4.1 Thinking
* KiloCode Claude Sonnet 4
* Google Gemini 2.5 Pro Web
* KiloCode Sonoma Dusk Alpha
* KiloCode Sonoma Sky Alpha
* KiloCode MoonshotAI Kimi K2 0905
* KiloCode xAI Grok Code Fast 1
* KiloCode Qwen3 Coder
* OpenRouter Qwen3 Max
* KiloCode Mistral Medium 3.1

## Overall Findings

### Consensus Top Performers

The evaluation reveals a remarkably strong consensus among all 6 evaluating models regarding the top-tier performers:

1. **Claude Code Opus 4.1** - Achieved the highest or near-highest rankings from 3 out of 6 evaluators (98, 97, 98, 97 average), with only ChatGPT GPT-5 Thinking penalizing it for "unverifiable specifics"
2. **OpenRouter Qwen3 Max** - Consistently ranked 2nd or 3rd across all evaluators (96, 93, 98, 97, 93 range), praised for exceptional formatting and comprehensive coverage
3. **KiloCode xAI Grok Code Fast 1** - Strong 3rd place consensus (95, 87, 99, 95, 95 range), particularly lauded by Gemini for its Mermaid diagrams and technical depth

### Clear Performance Tiers

The rankings reveal distinct performance clusters:

**Elite Tier (90-98 average)**
- Claude Code Opus 4.1, OpenRouter Qwen3 Max, KiloCode xAI Grok Code Fast 1
- Characterized by: Professional formatting, comprehensive technical depth, visual aids (diagrams/tables), specific code references

**High Performer Tier (85-94 average)**  
- KiloCode Claude Sonnet 4, Claude AI Web Opus 4.1 Thinking, Google Gemini 2.5 Pro Web
- Characterized by: Good structure and coverage but less technical depth or minor accuracy issues

**Mid-Range Tier (75-89 average)**
- OpenAI ChatGPT GPT-5 Thinking, OpenAI Codex GPT-5 Medium Thinking, KiloCode Sonoma Sky/Dusk Alpha
- Characterized by: Solid basics but lacking implementation details or comprehensive analysis

**Lower Tier (55-78 average)**
- KiloCode Mistral Medium 3.1, KiloCode Qwen3 Coder, KiloCode MoonshotAI Kimi K2 0905
- Characterized by: Brief summaries, surface-level coverage, missing critical technical details

### Key Evaluation Criteria Trends

All evaluators consistently valued:

1. **Technical Accuracy** - Specific line references, correct implementation details, avoiding speculation
2. **Thoroughness** - Coverage of v1.3.1 fixes, CI pipeline details, temporary rule mechanisms
3. **Presentation Quality** - Use of tables, diagrams, structured formatting, clear organization
4. **Practical Value** - Inclusion of examples, limitations, recommendations
5. **Depth vs. Brevity Balance** - Models too brief (Kimi K2, Qwen3 Coder) consistently ranked lower

### Notable Divergences

The most significant disagreement occurred with **ChatGPT GPT-5 Thinking's evaluation**, which:
- Ranked itself #1 (94) while others placed it mid-tier (82-92 range)
- Heavily penalized Claude Code Opus 4.1 for "unverifiable specifics" (ranked 12th) while all others ranked it 1st
- Showed potential self-bias by favoring OpenAI models (ranked both OpenAI models in top 3)

### Evaluation Methodology Insights

Different evaluators emphasized different aspects:
- **Gemini 2.5 Pro** valued visual elements heavily (99 score for Grok's Mermaid diagrams)
- **Claude Code Opus 4.1** provided the most granular scoring with detailed strengths/weaknesses
- **Grok 4** balanced accuracy and thoroughness equally in scoring
- **Sonoma Sky Alpha** used a three-factor system (accuracy, thoroughness, overall)

### Critical Success Factors

Analysis reveals the following separated top performers from others:

1. **Structured Documentation** - Winners used executive summaries, clear sections, tables
2. **Visual Communication** - Diagrams and formatted tables significantly boosted scores
3. **Specific Technical Details** - References to exact mechanisms (systemd-run, flock) valued highly
4. **Balanced Coverage** - Both script functionality AND CI testing details needed
5. **Actionable Insights** - Recommendations, limitations, and use cases added value

### Surprising Findings

1. **Self-Evaluation Bias**: Models evaluating themselves showed varying degrees of objectivity, with Claude Code Opus 4.1 showing high self-awareness (ranked itself appropriately) while ChatGPT showed potential positive bias
2. **Brevity Penalty**: All extremely concise responses (under 500 words) were consistently ranked in bottom third, suggesting evaluators prefer comprehensive analysis
3. **Visual Impact**: The inclusion of even one diagram (Mermaid) could boost rankings by 5-10 points
4. **Version-Specific Focus**: Models that explicitly addressed v1.3.1 OUTPUT chain cleanup scored notably higher

### Overall Conclusion

The evaluation consensus strongly indicates that **comprehensive, technically accurate, and well-structured responses with visual aids** are universally valued across different AI evaluators. The top three models (Claude Code Opus 4.1, OpenRouter Qwen3 Max, and KiloCode xAI Grok Code Fast 1) achieved their positions through a combination of depth, accuracy, and presentation quality rather than any single factor. The consistency of these rankings across diverse evaluators suggests these qualities represent objective markers of response quality for technical code analysis tasks.



## The Rankings

---

### Claude Code Opus 4.1 Evaluations

| Rank | Model Name | Score | Accuracy | Thoroughness | Key Strengths | Key Weaknesses |
|------|------------|-------|----------|--------------|---------------|-----------------|
| 1 | Claude Code Opus 4.1 | 98/100 | Excellent | Excellent | Professional report format, executive summary, detailed architecture analysis, comprehensive command tables, specific v1.3.1 fixes, performance characteristics | Could include more code examples |
| 2 | OpenRouter Qwen3 Max | 96/100 | Excellent | Excellent | Exceptional formatting, comprehensive feature tables, includes recommendations and limitations, effective use of visual elements | Slightly verbose in places |
| 3 | KiloCode xAI Grok Code Fast 1 | 95/100 | Excellent | Excellent | Mermaid diagrams, detailed command structure, usage examples, identifies limitations clearly | Could be more concise |
| 4 | KiloCode Claude Sonnet 4 | 94/100 | Excellent | Excellent | Line-by-line references, detailed technical architecture, CI testing innovations section | Less accessible for non-technical readers |
| 5 | Claude AI Web Opus 4.1 Thinking | 88/100 | Very Good | Very Good | Well-structured, clear feature categorization, good v1.3.1 coverage | Less technical depth than top tier |
| 6 | Google Gemini 2.5 Pro Web | 85/100 | Very Good | Very Good | Excellent explanations for broader audience, well-formatted sections | Could include more technical details |
| 7 | OpenAI ChatGPT GPT-5 Thinking | 82/100 | Good | Good | Clear structure and explanations, good coverage | Minor inaccuracies |
| 8 | KiloCode Mistral Medium 3.1 | 78/100 | Good | Good | Good relationship explanation, clear example workflows | Lacks technical depth |
| 9 | OpenAI Codex GPT-5 Medium Thinking | 75/100 | Good | Good | Concise bullet-point format, good coverage | Relatively brief, lacks detailed analysis |
| 10 | KiloCode Sonoma Dusk Alpha | 72/100 | Good | Good | Comprehensive feature list, good CI coverage | Less detailed analysis |
| 11 | KiloCode MoonshotAI Kimi K2 0905 | 68/100 | Good | Moderate | Brief but accurate, covers key points | Lacks depth and examples |
| 12 | KiloCode Qwen3 Coder | 65/100 | Good | Moderate | Concise summary, covers main features | Minimal technical detail |
| 13 | KiloCode Sonoma Sky Alpha | 62/100 | Good | Moderate | Very concise, covers basics | Least comprehensive analysis |

---

### ChatGPT GPT-5 Thinking Evaluations

|  # | Model                                | Accuracy | Thoroughness | Notable strengths                                                                                                                                                            | Notable misses / issues                                                                                                                           | Overall |
| -: | ------------------------------------ | -------: | -----------: | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------- | ------: |
|  1 | **OpenAI ChatGPT GPT-5 Thinking**    |       95 |           92 | Clear mapping of features: `-method`, jq auto/fallback, base chains @ priority 10, temp rules w/ timers, status/check/watch; CI matrix + systemd container captured well.    | Minor omissions (artifact upload detail).                                                                                                         |  **94** |
|  2 | **OpenRouter Qwen3 Max**             |       92 |           94 | Very complete walkthrough of commands, temp directions/ports, handle tracking + timer cleanup; CI steps incl. traffic watch and artifact archiving.                          | A few generalities, but no hard inaccuracies.                                                                                                     |  **93** |
|  3 | **OpenAI Codex GPT-5 Medium**        |       93 |           90 | Concise and correct: dedicated table/priority, ip/port ops, temp TTL with json tracked handles + timers, status/check/test; CI’s OUTPUT-cleanup focus noted.                 | Skipped artifact step specifics.                                                                                                                  |  **92** |
|  4 | **Google Gemini 2.5 Pro Web**        |       90 |           88 | Solid coverage of CLI, temp rules, directions/ports, systemd timers; got CI matrix + AlmaLinux/systemd right.                                                                | Fewer CI details (e.g., artifacts).                                                                                                               |  **89** |
|  5 | **KiloCode xAI Grok Code Fast 1**    |       86 |           88 | Broad, structured rundown (ports/ranges/UDP, directions, timers, CI phases).                                                                                                 | Some speculation/marketing tone; a bit repetitive.                                                                                                |  **87** |
|  6 | **Claude AI Web Opus 4.1 Thinking**  |       88 |           86 | Accurate high-level script + CI overview; calls out timer-based expiry across chains.                                                                                        | Less depth on watch/status/check and artifacts.                                                                                                   |  **87** |
|  7 | **KiloCode Sonoma Dusk Alpha**       |       84 |           85 | Balanced summary of script + CI; touches v1.3.1 OUTPUT cleanup, directions, ports.                                                                                           | Light on specifics (handles, exact flags).                                                                                                        |  **85** |
|  8 | **KiloCode Sonoma Sky Alpha**        |       82 |           84 | Good breadth; includes container + systemd details and CI flow.                                                                                                              | Adds a run-time estimate (speculative).                                                                                                           |  **83** |
|  9 | **KiloCode MoonshotAI Kimi K2 0905** |       85 |           78 | Correct essentials (ports/directions, timers, tracking).                                                                                                                     | Briefer CI coverage; few implementation details.                                                                                                  |  **82** |
| 10 | **KiloCode Qwen3 Coder**             |       84 |           80 | Reliable overview of key capabilities + CI matrix/systemd.                                                                                                                   | Skims advanced diagnostics (watch/status/check).                                                                                                  |  **82** |
| 11 | **KiloCode Mistral Medium 3.1**      |       83 |           76 | Accurate but compact; hits main commands + CI phases.                                                                                                                        | Leaves out OUTPUT-cleanup emphasis + artifacts.                                                                                                   |  **80** |
| 12 | **Claude Code Opus 4.1**             |       78 |           95 | Extremely thorough; dives into design/flows, multi-port sets, directionality, timers.                                                                                        | Several **unverifiable specifics**: exact LOC counts, a “\~2× faster” JSON claim, & named “security fix” not evident in code—so accuracy penalty. |  **84** |
| 13 | **KiloCode Claude Sonnet 4**         |       75 |           90 | Wide coverage with lots of feature bullets (ports/directions, timers, IPv6, checks).                                                                                         | Cites **fake line numbers** and overly precise anchors (e.g., `csfa.sh:1015`) that don’t match the file—accuracy hit.                             |  **82** |

---

### Gemini 2.5 Pro Web Evaluations

| Model                             | Accuracy & Thoroughness Analysis                                                                                                                                                                                                                                                                                                                                                     | Rating (0-100) |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | :------------: |
| **KiloCode xAI Grok Code Fast 1** | **Exceptional.** Provided the deepest technical breakdown, correctly identifying not just the features but the implementation details (e.g., `systemd-run` for timers, `flock` for locking). Its unique inclusion of **Mermaid diagrams** to visualize the script's logic and CI workflow demonstrated a superior level of comprehension.                                          |     **99** |
| **OpenRouter Qwen3 Max** | **Exceptional.** Presented a highly polished, readable, and comprehensive report. It excelled at structuring the information logically with clear headings and summaries. It correctly identified and emphasized the criticality of the v1.3.1 OUTPUT chain cleanup test, and its "Strengths" and "Limitations" sections added significant analytical value.                  |     **98** |
| **Claude Code Opus 4.1** | **Exceptional.** Formatted its output as a professional executive summary and technical report. It was extremely thorough, covering architecture, design patterns, and specific v1.3.1 bug fixes. The formal structure and level of detail were unparalleled, making it feel like a human-written document.                                                                   |     **97** |
| **Google Gemini 2.5 Pro Web** | **Excellent.** Provided a very clear and well-written explanation of *how* the mechanisms work, particularly the "clever" use of `systemd-run` for temporary rules. It correctly highlighted the importance of the systemd-enabled container in the CI for this feature to be testable. The analysis was both deep and easy to understand.                          |     **94** |
| **OpenAI ChatGPT GPT-5** | **Excellent.** A very thorough and accurate analysis. It was one of the few to explicitly mention the `flock` command for preventing race conditions. The "Net effect" summary was a great touch for synthesizing the script's overall purpose. It correctly understood all key mechanisms in both the script and the CI file.                                                   |     **92** |
| **Claude AI Web Opus 4.1** | **Excellent.** A strong, detailed analysis that correctly identified the most critical test in the CI pipeline (v1.3.1 OUTPUT chain cleanup). It clearly explained the core capabilities and how the CI workflow validates them, showing a solid understanding of the project's technical depth.                                                                    |     **90** |
| **KiloCode Claude Sonnet 4** | **Very Good.** A well-structured and detailed analysis that used tables and code blocks effectively. Its unique feature of linking to specific line numbers in the script was a nice touch, although not explicitly requested. It provided a very granular and accurate breakdown of the CI test coverage.                                                                |     **88** |
| **KiloCode Mistral Medium 3.1** | **Good.** A solid, high-level summary that was accurate and well-organized. It correctly identified the relationship between the script and the CI file and mentioned the key technologies (systemd, jq), but lacked the implementation details and depth of the higher-rated models.                                                                                      |     **80** |
| **KiloCode Sonoma Sky Alpha** | **Good.** A competent and accurate summary. It successfully identified the main features and the purpose of the matrix strategy in the CI workflow. However, it remained at a surface level and did not delve into the more complex mechanisms like the systemd timer callbacks or file locking.                                                                   |     **78** |
| **OpenAI Codex GPT-5 Medium** | **Good.** Very concise and to the point. It served as an excellent quick reference, accurately listing the key features. It correctly noted the v1.3.1 focus on OUTPUT chain cleanup but didn't explain the "why" or "how" with the same clarity as top-tier models.                                                                                                    |     **75** |
| **KiloCode Qwen3 Coder** | **Fair.** An accurate but very high-level summary. It correctly listed the main features and CI test areas but was too brief to be considered a thorough analysis. It provided a good "at a glance" overview.                                                                                                                                                                     |     **65** |
| **KiloCode Sonoma Dusk Alpha** | **Fair.** This summary was too brief. While the information was accurate, it lacked sufficient detail to be truly useful. It identified the main components but missed almost all of the nuance regarding the advanced features and the complexity of the CI tests.                                                                                                   |     **60** |
| **KiloCode MoonshotAI Kimi K2 0905** | **Needs Improvement.** Extremely concise to the point of being a TL;DR. It impressively managed to mention the "critical 35-second TTL test," showing some depth, but the overall summary was too sparse. It sacrificed thoroughness for brevity.                                                                                                                 |     **55** |

---

### Grok 4 via T3 Chat Evaluations

| Rank | Model | Accuracy (0-100) | Thoroughness (0-100) | Overall Rating (0-100) | Key Strengths | Key Weaknesses |
|------|-------|------------------|----------------------|------------------------|---------------|----------------|
| 1 | Claude Code Opus 4.1 | 98 | 98 | 98 | Highly detailed with tables, breakdowns, and v1.3.1 specifics; accurate code references and CI coverage. | Slightly verbose in sections. |
| 2 | OpenRouter Qwen3 Max | 97 | 97 | 97 | Comprehensive with overviews, tables, examples, and recommendations; excellent CI breakdown. | Minor repetition in summaries. |
| 3 | KiloCode xAI Grok Code Fast 1 | 95 | 95 | 95 | Accurate with Mermaid diagrams, breakdowns, and examples; strong on CI flow. | Misses some internal helpers (e.g., flock locking). |
| 4 | Claude AI Web Opus 4.1 Thinking | 94 | 93 | 94 | Concise yet thorough; good focus on v1.3.x features and CI innovations. | Less emphasis on code internals like parsing logic. |
| 5 | KiloCode Claude Sonnet 4 | 93 | 92 | 93 | Detailed line references and breakdowns; strong on CI's advanced tests. | Some sections feel list-heavy without synthesis. |
| 6 | Google Gemini 2.5 Pro Web | 92 | 90 | 91 | Clear, structured summary with examples; good balance of features. | Omits CI's matrix and artifact details. |
| 7 | OpenAI Codex GPT-5 Medium Thinking | 90 | 88 | 89 | Solid high-level summary; covers modes and CI phases well. | Lacks depth on v1.3.1 fixes and code helpers. |
| 8 | KiloCode Sonoma Sky Alpha | 88 | 85 | 87 | Accurate summaries with examples; covers both files evenly. | Superficial on CI's temp rule tests; no diagrams. |
| 9 | OpenAI ChatGPT GPT-5 Thinking | 87 | 84 | 86 | Good purpose explanation and net effect; mentions README potential. | High-level; misses specifics like port parsing or CI sleeps. |
| 10 | KiloCode Sonoma Dusk Alpha | 85 | 82 | 84 | Concise feature lists; covers commands well. | Brief; ignores CI's debugging aspects like journalctl. |
| 11 | KiloCode Mistral Medium 3.1 | 80 | 75 | 78 | Basic overview with example; covers relationship. | Very short; inaccurate on some features (e.g., no mention of directions). |
| 12 | KiloCode Qwen3 Coder | 75 | 70 | 73 | Brief bullet points; covers basics. | Inaccurate (e.g., claims IPv6 in CI but misses details); superficial. |
| 13 | KiloCode MoonshotAI Kimi K2 0905 | 70 | 65 | 68 | Ultra-brief; captures essence. | Lacks depth; minor inaccuracies (e.g., oversimplifies temp rules). |

---

### Sonoma Sky Alpha via KiloCode Evaluations

| Rank | Model Name                  | Accuracy Score (0-100) | Thoroughness Score (0-100) | Overall Score (0-100) | Key Strengths | Key Weaknesses |
|------|-----------------------------|-------------------------|-----------------------------|-----------------------|---------------|----------------|
| 1    | Claude Code Opus 4.1       | 98                      | 95                          | 97                    | Detailed architecture, tables/diagrams, v1.3.1 fixes, full CI phases; code snippets. | Slightly verbose; minor repetition in strengths. |
| 2    | KiloCode xAI Grok Code Fast 1 | 97                      | 92                          | 95                    | In-depth internals (handles, timers), Mermaid diagrams, CI flow; accurate command examples. | Less emphasis on limitations; no explicit v1.3.1 bug list. |
| 3    | OpenRouter Qwen3 Max       | 95                      | 90                          | 93                    | Structured sections, examples, CI critical tests; holistic view with recommendations. | Overlooks some CI artifacts details; assumes more than states. |
| 4    | KiloCode Claude Sonnet 4   | 96                      | 88                          | 92                    | Strong CI coverage (timing tests, multi-chain), feature tables; code line refs. | Script section lighter on monitoring commands. |
| 5    | Claude AI Web Opus 4.1 Thinking | 94                      | 85                          | 90                    | Good temp rules depth, CI innovations; clear summary. | Misses port proto parsing details; briefer on IPv6. |
| 6    | Google Gemini 2.5 Pro Web  | 93                      | 82                          | 88                    | Balanced breakdown, temp rules mechanism; CI strategy focus. | Generic on parsing fallback; no visuals or edge cases like UDP. |
| 7    | OpenAI ChatGPT GPT-5 Thinking | 92                      | 80                          | 86                    | Clean feature lists, CI phases; practical examples. | Skips handle management; undercovers v1.3.1 cleanup test. |
| 8    | KiloCode Sonoma Sky Alpha  | 91                      | 78                          | 85                    | Concise summaries, CI timeline; method-specific artifacts. | Brief on internals (e.g., flock); no tables/diagrams. |
| 9    | KiloCode Sonoma Dusk Alpha | 90                      | 75                          | 83                    | Quick overview, test coverage; CI characteristics. | Surface-level; omits direction/port combos in detail. |
| 10   | OpenAI Codex GPT-5 Medium Thinking | 89                      | 72                          | 81                    | Solid basics, v1.3.1 focus; CI functional tests. | Less structured; misses geo-IP fallback logic. |
| 11   | KiloCode Qwen3 Coder       | 88                      | 65                          | 77                    | Core/advanced features split; CI environment. | Too concise; skips monitoring/validation depth. |
| 12   | KiloCode MoonshotAI Kimi K2 0905 | 87                      | 55                          | 71                    | High-level features, CI validation; brief. | Minimal coverage; no specifics on timers or CI steps. |
| 13   | KiloCode Mistral Medium 3.1 | 85                      | 50                          | 68                    | Basic overview, relationship explanation; example. | Shallow; ignores enhanced features like directions. |


