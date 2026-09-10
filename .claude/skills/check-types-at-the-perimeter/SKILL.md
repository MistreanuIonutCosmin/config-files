---
name: check-types-at-the-perimeter
description: Apply strict runtime type validation at application boundaries while trusting types inside the application. Use when writing or reviewing TypeScript or Python code that handles APIs, external integrations, databases, or client-server validation.
---

Always check types at the perimeter of the application using zod or pydantic (edges being api, external integrations, db), and then trust the typing inside of our application. Do NOT continuously check types. Be wary of code like "isRecord" in typescript or "getattr" in Python, or returning tuples in Python. Those are all anti-patterns. Be more strict on typing when the data comes from external sources, our client should be the most lenient: i.e. if we check user input for a title on the backend in python and don't allow white spaces, then the client doesn't need to again check for whitespaces, we can trust that our server already did that.
