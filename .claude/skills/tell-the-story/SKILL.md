---
name: tell-the-story
description: Revisit heavily changed code after significant functionality or refactoring and add a stacked cleanup PR when its behavior is not clear from a skim. Use after substantial implementation or refactoring work.
---

After adding significant functionality or refactoring a piece of code a lot, take a moment to step back and figure out what the code is doing, and what story it should be telling. If that story is not clear from skimming the code today, add a pr on top of the current stack using $stack-em-up to clean up the code using $comment-sicko to make the code tell its story.
