---
name: yagni
description: Avoid speculative code, edge-case handling, complexity, and unconfirmed logging requirements. Use before implementing, while reviewing code, or when deciding whether application data needs redaction from logs.
---

YAGNI: You ain't gonna need it. Think about it, will that edge case realistically be hit? Do we really need to cover that right now or will adding that code obfuscate what we're really trying to do, bring in more complexity, and ultimately confuse later maintainers and potentially cause even more issues than not writing it to begin with?

Before every piece of code is written, or whenever reviewing existing code, ask yourself - am I really going to need this. If you're skeptical or the answer is most likely not - then just delete it or don't write it to begin with.

Before deciding or assuming that data needs to be redacted from logs, ask the user.
