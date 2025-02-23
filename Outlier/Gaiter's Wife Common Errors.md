# In this course, we will cover the most common tasking errors on this project and how to avoid making them.

  **Table of Contents**

- Common Errors

1. Common Error #1 Bad Prompt
2. Common Error #2 Moving Goal Posts
3. Common Error #3 Previous Response References
## Conclusion
**Reminder:** Whether you are new to this project or have been tasking for a while, please review the material carefully. Even simple mistakes can create bad training data, and contributors that consistently submit low quality tasks may be removed from the project.

---
## -A Bad prompt does **NOT** cause the model to make an error in either **instruction following**, **correctness** or **executability IN THE FIRST TURN**.

## -A Good **MUST** cause the model to make an error in either **instruction following**, **correctness** or **executability IN THE FIRST TURN**.

In the first turn, you must confirm that either that:

1. The model response is not following instructions from the prompt.
2. The model response is not correct.
3. The model response is not executing.

**❌ Bad Task**

The prompt tells the mode to do "X Y & Z"

The model does "X Y & Z"

**✅ Good Task**

The prompt tells the mode to do "X Y & Z"

The model does not do "X Y & Z"

---
**The second prompt (that's correcting the first response)** **should not add new constraints to the task****. This second prompt should only aim to correct what the initial response did not already.**

## **How to avoid this error while tasking**

  

- Do not add any new instructions to the prompt in turn 2
- Steer the model to correct the issues it made in the first response

**❌ Bad Task**

_-The original prompt instructs the model with 3 instructions and the second prompt adds an additional and different 4th instruction_

**✅ Good Task**

_-The original prompt instructs the model with 3 instructions. The model only performs 2 of the 3. The second prompt hints the model to perform the 3rd without adding new constraints._

---

**Your rewritten final response should not contain any references to the previous response. It should be self-contained and look like an original response to the prompt.**

---
![[Pasted image 20241024125701.png]]

---

