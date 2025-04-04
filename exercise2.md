
---

## 🧪 Distillation Lab: Improve Your Student Model!

The current distillation setup is a solid baseline — but the student model doesn’t seem to improve significantly. That’s **great news** for learning! Now it's your job to **make it better**.

### 🎯 Your Mission

Tinker with the code and try to improve the **student model’s output quality** by the end of training. Below are **suggested areas to explore**. Each suggestion is open-ended — you’ll need to try things out, compare outputs, and decide what works best.

---

## 🔧 Things You Might Improve

### 1. **Training Signal Quality**
- Are the teacher’s logits too similar to the student's?
- Try using a **larger teacher model** (e.g., `flan-t5-base` or `flan-t5-large`) — do better teachers help?

> 💡 Think: What happens when the teacher knows much more than the student?

---

### 2. **More Data**
- You're only training on 20 examples. Try adding more synthetic or real dialogue-summary pairs.

> 💡 Can you generate new examples automatically? Can you create noisy versions of existing ones?

---

### 3. **Prompt Engineering**
- How informative is the `"Task: Summarize this dialogue. Input: ..."` prompt?
- Try changing the prompt format. Even subtle changes might help the teacher (and thus the student) generate better outputs.

> 💡 How does wording affect learning?

---

### 4. **Tokenization**
- The student and teacher use **different tokenizers**. Could that hurt alignment?
- Try using the **same tokenizer** for both.

> 💡 How might mismatched vocabularies affect logits?

---

### 5. **Training Strategy**
- The current loss blends **soft labels** (from the teacher) and **hard labels** (the target summaries). Try:
  - Changing the **alpha** weight.
  - Using **only soft labels** or **only hard labels**.
  - Playing with **temperature**.

> 💡 What does temperature actually *do* to the output distributions?

---

### 6. **Model Usage**
- The training loop **only trains for 2 epochs** — and there’s no validation.
- Try:
  - Training longer.
  - Saving and comparing checkpoints.
  - Adding simple evaluation metrics like BLEU or ROUGE.

> 💡 Is your model just starting to improve when training ends?

---

### 7. **Generation Parameters**
- Try tuning `generate()` params:
  - `num_beams`, `top_p`, `temperature`, etc.
  - Do greedy generations work worse than beam search?

> 💡 How does decoding affect your perception of improvement?

---

### 8. **Distillation Loss Calculation**
- You're currently calculating the **KL divergence** manually.
- Try using a **built-in loss**, like `KLDivergence()` from TensorFlow or experimenting with **mean squared error on logits**.

> 💡 Does your current loss calculation match best practices?

---

## ✅ What to Turn In

- Before vs. After outputs
- A short explanation of:
  - What you tried
  - What worked (or didn’t)
  - What you think is happening

> 🧠 The goal isn't perfection — it's **insight**.

---

