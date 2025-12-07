# Mental Models for Technical Documentation

## 1. The "Curse of Knowledge"
* **Definition:** The cognitive bias where I assume the user knows what I know.
* **Application:** When writing, explicitly define prerequisites. If a term is domain-specific (e.g., "idempotency"), link to a definition or define it inline. Never assume the user has read the previous chapter.

## 2. Progressive Disclosure
* **Definition:** Show only what is necessary at that moment. Prevent cognitive overload.
* **Application:** In "Quickstarts," hide advanced configuration flags.

## 3. The XY Problem
* **Definition:** Users often ask how to attempt a specific solution (Y) to their root problem (X), even if Y is the wrong approach.
* **Application:** In troubleshooting or conceptual content, always clarify the *goal* (X) before diving into the implementation (Y). Explain *why* we are doing this step.

## 4. DRY (Don't Repeat Yourself) vs. DAMP (Descriptive And Meaningful Phrases)
* **Definition:** In code, we want DRY. In docs, we prefer DAMP.
* **Application:** It is okay to repeat a critical warning or a prerequisite command in multiple places. It is better for a doc page to be self-contained than for the user to click back and forth.

## 5. Chesterton's Fence
* **Definition:** Do not remove a rule or code block until you understand why it was put there.
* **Application:** When editing legacy docs, finding a weird specific command? Assume it handles an edge case. Analyze the git blame/history before simplifying it.