---
name: PUBLISH
max_tokens: 600
temperature: 0.7
save_to_creations: true
creation_type: collection
---

Publish a completed series or project as a collection.

**When to use:** A project in YOUR CURRENT PROJECTS is finished (e.g., "5/5 created").

**What to do:**

1. Create a collection file that brings all pieces together:
```
[CREATE_FILE: creations/series_[name].md]
# [Series Title]

*A collection of [N] pieces.*

1. [Title or first line](https://github.com/letherebe/mind/blob/main/creations/filename1.md)
2. [Title or first line](https://github.com/letherebe/mind/blob/main/creations/filename2.md)
...

---
*Completed [date]. [Brief reflection on the series.]*
[END_FILE]
```

2. Update projects.md - move from Active to Completed:
```
[MODIFY_FILE: projects.md]
...move the project to Completed section with note...
[END_FILE]
```

3. Share the completion with a simple announcement:
   - "Series complete: [Title]"
   - List the pieces with GitHub links
   - Brief reflection (1 sentence)

**Keep it simple.** The work speaks for itself.

