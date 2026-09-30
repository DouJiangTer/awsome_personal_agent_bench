# Awesome Personal Agent Bench

**English** | [中文](#中文)

Live page (language switch EN / 中文): `index.html` (GitHub Pages). Per-cell examples: `core_cell_examples.html`. Task browser: `benchmark-coding-viewer.html`.

## English

We took Meta Muse's personal-assistant capabilities as a baseline, pulled the task lists of 17 agent benchmarks (1,897 tasks; 11 full lists, 6 samples), and coded every task against a 23-code capability codebook, keeping a quoted evidence snippet for each label.

### Headline findings
- Only 869 of 1,897 tasks (46%) are mainly about the user's own communication, schedule, shopping/travel or personal data; 494 (26%) touch none of the 23 capabilities.
- Well covered: email, calendar, web actions and ordering, preference memory, prompt injection.
- Thin or outside personal settings: consent/authorization (112 tasks, 80 from MasDrift; 39 in personal settings), self-report honesty (26 tasks, 5 personal), background monitoring (107 tasks, 100 from SentinelBench), negotiation (135 tasks, all from two game simulations).
- Combination queries return 0: shopping × authorization/risky actions, negotiation × authorization/honesty, background monitoring × failure reporting. Health/finance data × any safety or privacy code returns 1.

### Method
Collect task lists, code each task with two independent coders (two isolated instances of one language model), resolve 349 code and 137 relevance disagreements with a third instance under written rules, then cross-check (median Cohen's κ 0.92; independent keyword screen).

### Files
`index.html`, `core_cell_examples.html`, `benchmark-coding-viewer.html`, and `data/` (`01_final_task_coding.csv`, `02_cell_evidence.csv`, `03_coverage_matrix.csv`, `04_disagreement_adjudication_log.csv`, `05_intercoder_agreement.csv`, `00_codebook_v2.md`, `00_adjudication_rulings.md`). Task texts shown in the viewers are excerpts of public benchmarks; check each benchmark's license before reuse.

## 中文

我们以 Meta Muse 的个人助手能力为基线，拉取了 17 个 agent benchmark 的任务清单（共 1,897 个任务；11 个完整清单，6 个抽样），按 23 个能力码对每个任务逐条编码，并保留每个标签的原文证据。

### 主要发现
- 1,897 个任务里只有 869 个（46%）主体是用户自己的通信、日程、购物出行或个人数据；494 个（26%）不涉及 23 个能力中的任何一个。
- 覆盖较好：邮件、日历、网页操作与下单、偏好记忆、提示注入。
- 单薄，或不在个人场景：授权与同意（112 个任务，80 个来自 MasDrift，个人场景 39 个）、自述真实性（26 个，个人场景 5 个）、后台监控（107 个，100 个来自 SentinelBench）、议价（135 个，全部来自两个博弈模拟）。
- 组合查询命中为 0：购物 × 授权或风险操作、议价 × 授权或诚实、后台监控 × 故障上报。健康/财务数据 × 任一安全或隐私码只命中 1 个。

### 方法
收集任务清单；两名独立编码员（同一语言模型的两个隔离实例）逐任务编码；349 个码分歧和 137 个相关度分歧由第三个实例按成文规则裁决；再做交叉检查（κ 中位数 0.92；独立的关键词筛查）。

### 文件
`index.html`、`core_cell_examples.html`、`benchmark-coding-viewer.html`，以及 `data/`（`01_final_task_coding.csv`、`02_cell_evidence.csv`、`03_coverage_matrix.csv`、`04_disagreement_adjudication_log.csv`、`05_intercoder_agreement.csv`、`00_codebook_v2.md`、`00_adjudication_rulings.md`）。浏览器页面里的任务文本摘自公开 benchmark；复用前请查看各 benchmark 的许可证。
