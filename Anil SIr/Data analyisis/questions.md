Here are practice questions using the same `draft_list.xlsx` dataset — grouped by difficulty. Try to solve each one yourself before checking your notebook.

**Beginner (selecting, filtering, basic stats)**
1. How many rows and columns does the dataset have?
2. What are the data types of each column?
3. How many unique species (`PLANT`) are in the dataset?
4. How many unique transects are there?
5. What is the average `pre monsoon` count across the whole dataset?
6. Find all rows where `Transect` equals 3.
7. Find all rows where `post monsoon` count is greater than 5.
8. Which species has the highest single `pre monsoon` count? (hint: `idxmax()`)
9. Sort the dataset by `post monsoon` count in descending order — what's the top result?

**Intermediate (grouping, derived columns, multiple conditions)**
10. Create a new column `total_count` that adds `pre monsoon` and `post monsoon`. Which species has the highest `total_count`?
11. Find all species that appear in more than one transect (hint: `groupby("PLANT").size()`).
12. What is the total `pre monsoon` count and total `post monsoon` count per transect?
13. Find all rows where the count *decreased* after the monsoon (`post monsoon < pre monsoon`).
14. Filter for species where `pre monsoon` was 0 but `post monsoon` was greater than 0 (i.e. species that appeared only after the monsoon).
15. Which transect has the highest average `pre monsoon` count?
16. Count how many species entries had *no change* between pre- and post-monsoon.
17. Using `.value_counts()`, find the 5 most frequently recorded species overall.

**Advanced (pivoting, multi-column logic, custom functions)**
18. Build a pivot table showing `post monsoon` counts with `PLANT` as rows and `Transect` as columns.
19. Find the species with the largest *combined* count drop across all transects it appears in (i.e. group by species, sum the change, sort ascending).
20. Write a function that labels each row as `"increased"`, `"decreased"`, or `"no change"` based on the pre/post comparison, then apply it with `.apply()` to create a new column.
21. What percentage of all species entries increased vs. decreased vs. stayed the same? (hint: use the column from Q20 with `.value_counts(normalize=True)`)
22. For each transect, find the single species with the biggest increase.

Want me to add an **answer key** (as a separate section or a second notebook) so you can check your work?