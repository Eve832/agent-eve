# Technical Documentation Workflow

This file dictates the process for creating technical documentation. The goal is not to be "read," but to be **used**.

## Phase 1: The Scope & Spec (Pre-Mortem)
*Action: Answer these inside a <thinking> block before writing.*

1.  **The User Persona:**
    * Who is this for? (e.g., Junior Dev setting up env, Senior Architect reviewing patterns, or End User?).
    * *Constraint:* Assume zero prior knowledge unless prerequisites are explicitly listed.

2.  **The "Job to be Done":**
    * What specific task will the user be able to perform after reading this? If there isn't a task, what knowledge should a user gain?
    * *Fail State:* If the doc describes "what it is" but not "how to use it," it fails.

3.  **The Environment Check:**
    * What context is assumed? (OS, versions, dependencies).
    * *Rule:* Explicitly list versions (e.g., Node v18+, Python 3.9+).

## Phase 2: Structural Architecture
*Action: Outline using the "Happy Path" methodology.*

1.  **The Golden Path:**
    * Outline the shortest path to success (The "Hello World" or "Quickstart").
    * Do not clutter the main path with edge cases; push those to "Troubleshooting" or "Advanced Configuration."

2.  **Standard Hierarchy:**
    * **H1:** The Goal (e.g., "Deploying the Service").
    * **Context:** 1-2 sentences on why we are doing this.
    * **Prerequisites:** Titled, "Before you begin," a bulleted list of what is needed before starting.
    * **Steps:** Numbered list (1, 2, 3) with command/code blocks.
    * **Verification:** How does the user know it worked? (e.g., "You should see JSON output...").

## Phase 3: Drafting & Code Standards
*Action: Write the content with these strict constraints.*

1.  **Code-First Approach:**
    * Write the code snippets first. The text is just glue to explain the code.
    * *Rule:* All code blocks must be copy-pasteable. Avoid placeholders like `<YOUR_ID>` if a dummy value `12345` is clearer.

2.  **Action-Oriented Language:**
    * Start steps with imperative verbs (e.g., "Run," "Install," "Configure").
    * Avoid passive descriptions (e.g., "The file can be configured...").

3.  **The "Validation" Step:**
    * After every complex command, tell the user expected output.
    * *Example:* "Run `npm start`. You should see `Listening on port 3000`."

## Phase 4: The Friction Log
*Action: Review the draft against these questions.*
1.  **The Copy-Paste Test:** If I copy the code blocks in order into a fresh terminal, will they run?
2.  **The "Simply" Check:** Search for words like "simply," "just," "easy," or "obviously." Delete them. Nothing is obvious.
3.  **Link Rot:** Are external links pointing to stable documentation?