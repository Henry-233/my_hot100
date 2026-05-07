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