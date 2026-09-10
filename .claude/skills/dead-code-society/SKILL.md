---
name: dead-code-society
description: Remove obsolete code, low-value tests and configuration, and unnecessary comments. Use during implementation, refactoring, or code review when cleanup can simplify the result without losing behavior.
---

Always be on the lookout for code or comments to delete or clean up. Especially on tests, if tests aren't actually testing anything or testing parts of deep implementation that shouldn't be tested, or config files where the test is not providing value - delete them. If comments are long and meandering or using complex jargon, clean it up and shorten it, or delete it entirely (ideally the code speaks for itself, see $comment-sicko).
