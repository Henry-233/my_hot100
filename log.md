---
title: "变更日志"
tags: [log, meta]
---

# 变更日志

## 2026-05-21 — 知识网络骨架初始化

### 目录结构重组
- 删除旧版空目录 `wiki/patterns/`, `wiki/problems/`, `wiki/synthesis/`, `wiki/data-structures/`
- 创建 7 个阶段性子目录 `wiki/patterns/phase1~7-*/`
- 重新创建 `wiki/problems/`, `wiki/synthesis/`, `wiki/data-structures/`

### 新建模式页面（28 个）

**Phase 1 — 数组基础（3 个）**
- `wiki/patterns/phase1-数组/前缀和.md`
- `wiki/patterns/phase1-数组/差分数组.md`
- `wiki/patterns/phase1-数组/二维数组.md`

**Phase 2 — 双指针（4 个）**
- `wiki/patterns/phase2-双指针/数组双指针.md`
- `wiki/patterns/phase2-双指针/滑动窗口.md`
- `wiki/patterns/phase2-双指针/二分搜索.md`
- `wiki/patterns/phase2-双指针/随机算法.md`

**Phase 3 — 基础数据结构（4 个）**
- `wiki/patterns/phase3-基础数据结构/循环数组.md`
- `wiki/patterns/phase3-基础数据结构/栈与队列.md`
- `wiki/patterns/phase3-基础数据结构/哈希.md`
- `wiki/patterns/phase3-基础数据结构/设计类.md`

**Phase 4 — 链表（2 个）**
- `wiki/patterns/phase4-链表/链表双指针.md`
- `wiki/patterns/phase4-链表/递归.md`

**Phase 5 — 二叉树（2 个）**
- `wiki/patterns/phase5-二叉树/递归遍历.md`
- `wiki/patterns/phase5-二叉树/层序遍历.md`

**Phase 6 — 高级数据结构（4 个）**
- `wiki/patterns/phase6-高级数据结构/二叉搜索树.md`
- `wiki/patterns/phase6-高级数据结构/堆.md`
- `wiki/patterns/phase6-高级数据结构/字典树.md`
- `wiki/patterns/phase6-高级数据结构/图.md`

**Phase 7 — 综合算法（9 个）**
- `wiki/patterns/phase7-综合算法/回溯法.md`
- `wiki/patterns/phase7-综合算法/DFS.md`
- `wiki/patterns/phase7-综合算法/BFS.md`
- `wiki/patterns/phase7-综合算法/广度优先搜索.md`
- `wiki/patterns/phase7-综合算法/分治算法.md`
- `wiki/patterns/phase7-综合算法/动态规划.md`
- `wiki/patterns/phase7-综合算法/最短路径.md`
- `wiki/patterns/phase7-综合算法/数学.md`
- `wiki/patterns/phase7-综合算法/贪心算法.md`

### 新建导航 & 综合页面（4 个）
- `wiki/patterns/00-知识网络导航.md` — 主索引 + 依赖图
- `wiki/synthesis/学习路径.md` — 7 阶段推荐学习路径
- `progress.md` — 重写为完整骨架模板
- `index.md` — 更新为新结构导航

### 状态
- 所有页面 `status: not-started`
- 题目页面尚未创建
- 依赖关系已建立

---

## 2026-05-21 — 差分数组 web clip 摄入

### 来源
- `raw/html-lectures/小而美的算法技巧：差分数组.md`（labuladong）

### 更新的页面
- `wiki/patterns/phase1-数组/差分数组.md` — 更新代码模板（Difference 类）、题目列表、易错点

### 新建题目页面（3 个）
- `wiki/problems/370-区间加法.md` — status: todo, 差分数组裸题
- `wiki/problems/1109-航班预订统计.md` — status: todo, 航班编号→索引映射
- `wiki/problems/1094-拼车.md` — status: todo, 上下车区间模型

### 进度更新
- Phase 1 差分数组模式：总计 3 题

---

## 2026-05-21 — 前缀和数组 web clip 摄入

### 来源
- `raw/html-lectures/小而美的算法技巧：前缀和数组.md`（labuladong）

### 更新的页面
- `wiki/patterns/phase1-数组/前缀和.md` — 更新代码模板（NumArray 类封装、二维前缀和 NumMatrix 类）、题目列表、局限性说明

### 新建题目页面（2 个）
- `wiki/problems/303-区域和检索-数组不可变.md` — status: todo, 一维前缀和裸题
- `wiki/problems/304-二维区域和检索-矩阵不可变.md` — status: todo, 二维前缀和 + 容斥原理

### 进度更新
- Phase 1 前缀和模式：总计 2 题
- Phase 1 小计：5 题（前缀和 2 + 差分数组 3）
