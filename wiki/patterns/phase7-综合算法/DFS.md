---
title: "DFS（深度优先搜索）"
tags: [DFS, 图, 树, phase7]
phase: 7
status: not-started
depends_on: [[递归遍历], [图]]
---

## 适用场景
需要遍历图/树的所有节点；连通分量；路径搜索；回溯的基础。
特征：看到"岛屿数量"、"被围绕的区域"、"所有路径"、
"连通分量"、"图的遍历"、"二叉树遍历（递归版）"。

## 代码模板
```python
# 递归 DFS（图）
def dfs(graph, node, visited):
    visited.add(node)
    for neighbor in graph[node]:
        if neighbor not in visited:
            dfs(graph, neighbor, visited)
```

```python
# 迭代 DFS（显式栈）
def dfs_iterative(graph, start):
    visited = set()
    stack = [start]
    while stack:
        node = stack.pop()
        if node not in visited:
            visited.add(node)
            for neighbor in graph[node]:
                stack.append(neighbor)
    return visited
```

```python
# 二维网格 DFS（岛屿问题）
def dfs_grid(grid, i, j):
    if i < 0 or i >= len(grid) or j < 0 or j >= len(grid[0]):
        return
    if grid[i][j] != '1':
        return
    grid[i][j] = '0'  # 标记已访问
    for di, dj in [(0, 1), (0, -1), (1, 0), (-1, 0)]:
        dfs_grid(grid, i + di, j + dj)
```

## 属于该模式的题目列表
- (待录入)

## 与相似模式的区别
- **BFS/广度优先搜索**：DFS 用栈（走到底），BFS 用队列（逐层扩散）；DFS 适合路径存在性，BFS 适合最短路径（无权图）
- **回溯法**：回溯是 DFS 在决策树上的应用
- **递归遍历**：DFS 在二叉树上的特化
