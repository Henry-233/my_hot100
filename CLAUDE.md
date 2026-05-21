# Knowledge Base Schema — LeetCode Hot100

## Domain
LeetCode Hot100 algorithm problems — patterns, data structures,
solution approaches, complexity analysis, code templates.

## Directory conventions
- wiki/problems/   → One page per problem
- wiki/patterns/   → One page per algorithm pattern
- wiki/data-structures/ → One page per data structure
- wiki/synthesis/  → Topic summaries, pattern comparisons

## Problem page format
Each problem page must include:
---
title: "题号. 题目名"
tags: [pattern, difficulty, status]
difficulty: easy | medium | hard
status: todo | attempted | solved | reviewed
date_solved: YYYY-MM-DD
---

## 题目描述
(one-line summary)

## 解题思路
(core idea, not step-by-step)

## 关键代码
```python
# 核心代码片段，不需要完整
```

## 复杂度
- 时间：O(?)
- 空间：O(?)

## 关联
- Pattern: [[patterns/滑动窗口]]
- 相似题: [[problems/3-无重复字符的最长子串]]
- 易错点: (one sentence)

## Pattern page format
Each pattern page must include:
- 适用场景（什么情况下用这个模式）
- 代码模板
- 属于该模式的题目列表（wikilinks）
- 与相似模式的区别

## Progress tracking
Maintain progress.md with:
- Total solved / 100
- Per-difficulty breakdown
- Per-pattern breakdown
- Recently solved (last 5)

## Ingest workflow
When asked to ingest a new problem:
1. Create wiki/problems/题号-题目名.md
2. Update or create relevant pattern page
3. Update progress.md statistics
4. Add wikilinks between problem and pattern
5. Update index.md

## Tags convention
difficulty: easy / medium / hard
pattern: 数组 / 双指针 / 滑动窗口 / 哈希表 / 栈 /
         单调栈 / 二分查找 / 回溯 / 动态规划 / 贪心 /
         BFS / DFS / 图 / 堆 / 前缀和 / 位运算 / 链表 / 树
status: todo / attempted / solved / reviewed



## Web clip ingest rule (labuladong / similar structured clips)
When raw/html-lectures/ or raw/references/ contains a clipped .md file
with front matter (title/source/tags: clippings):

1. Identify target pattern from the title or content
2. Extract in order:
   a. 前置知识 section → update depends_on field
   b. 核心思路解释 → update ## 核心思路
   c. The reusable class/template code → update ## 代码模板
   d. All LeetCode problems mentioned (with numbers) → update ## 题目列表
   e. 拓展延伸 section → update ## 关联进阶 (create if not exists)
3. Update (never recreate) the target wiki/patterns/ page
4. For each problem mentioned, check if wiki/problems/ page exists:
   - If not: create a stub problem page with status: todo
   - If yes: add pattern wikilink if missing
5. Preserve the source URL in pattern page front matter
6. Do NOT copy full problem statements into pattern page,
   only link via [[problems/题号-题目名]]
7. Log processed file in log.md

## Auto git sync rule
After EVERY operation that modifies any file in this vault:
1. Stage all changes: git add .
2. Commit with descriptive message: 
   git commit -m "auto: {{operation_type}} - {{affected_files_summary}}"
3. Push to remote: git push

Operation type examples:
- ingest: when processing a new clip
- update: when updating existing pages  
- create: when creating new pages
- progress: when updating progress.md
- restructure: when reorganizing directories

Example commit messages:
- "auto: ingest - 差分数组 pattern + 3 problem stubs"
- "auto: update - 滑动窗口 pattern page"
- "auto: progress - solved 1-两数之和"

Never skip git sync even if only log.md was changed.
Always run git push after commit, not just git commit.