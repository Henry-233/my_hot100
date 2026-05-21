I added a new web clip to raw/html-lectures/小而美的算法技巧：前缀和数组.md.
Follow the web clip ingest rule in CLAUDE.md to:
1. Identify the target pattern page: wiki/patterns/phase1-数组/前缀和数组.md
2. Extract all structured content and update the pattern page
3. Create stub problem pages for all mentioned problems

   with status: todo and pattern linked to [[patterns/phase1-数组/前缀和数组]]
4. Update progress.md problem count
5. Log in log.md




I added a new web clip to raw/html-lectures/.
Find the most recently added or unprocessed .md file in that directory.

Follow the web clip ingest rule in CLAUDE.md:

1. AUTO-DETECT the target pattern:
   - Read the clip title and content
   - Match to the corresponding phase and pattern page in wiki/patterns/
   - If no matching pattern page exists, create one following Pattern page format

2. EXTRACT and update the target pattern page:
   - 前置知识 → depends_on field and prerequisite section
   - 核心思路 → ## 核心思路
   - Reusable class or template code → ## 代码模板
   - Complexity analysis → ## 复杂度
   - 拓展延伸 → ## 关联进阶 (create section if not exists)
   - Preserve all existing content, only add or update

3. AUTO-DETECT all mentioned LeetCode problems:
   - Scan for any problem numbers (e.g. 第 370 题, LeetCode 1109, 力扣 1094)
   - For each problem found:
     - Check if wiki/problems/题号-题目名.md already exists
     - If not: create stub page with status: todo,
       difficulty inferred from content if possible,
       pattern linked to the detected pattern page
     - If yes: add pattern wikilink if missing

4. UPDATE progress.md:
   - Increment problems count by number of new stub pages created
   - Update pattern row in by-pattern table

5. LOG in log.md:
   - Timestamp
   - Source file processed
   - Pattern page updated
   - Problem stubs created (list)
   - Any warnings (e.g. pattern not found, problem already exists)
