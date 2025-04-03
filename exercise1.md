
# ✅ Follow-up Exercise: Improving Fine-Tuning and Measuring Impact

"""
🚀 Now that you've completed a basic fine-tuning pass, let's expand and evaluate how much the model improves.

### 📚 Instructions:
1. **Expand the dataset** to include more diverse examples (e.g., 8–10 sentences).
2. **Train for 3 epochs** instead of 1 to give the model more time to learn.
3. **Evaluate the model before and after training** using multiple test sentences.
4. **Compare predictions and confidence scores.**

---

### 📝 Example Expanded Dataset:

```python
data = {
    "text": [
        "This product is awful.",
        "I hated this movie. Waste of time.",
        "Terrible customer service experience.",
        "I will never buy this again.",
        "This is a fantastic product!",
        "Absolutely loved the performance.",
        "Great quality and easy to use.",
        "Highly recommended!"
    ],
    "label": [0, 0, 0, 0, 1, 1, 1, 1]
}
```

---

### 🔍 Suggested Test Inputs:
Use these both *before* and *after* fine-tuning:

```python
test_sentences = [
    "This is terrible.",
    "What a wonderful experience!",
    "I would not recommend this.",
    "Best thing I’ve bought this year!"
]
```

---

### 🧠 Your Task:
- Measure the model’s predictions (probabilities and sentiment) for each test sentence
- Present the results in a clear before/after comparison
- Interpret what the model has learned (or hasn’t)

You can even make a chart or table if you're feeling adventurous!

Good luck — and remember: the more data you give your model, the smarter it gets. 😉
"""
