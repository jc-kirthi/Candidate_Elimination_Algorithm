# 🧠 Candidate Elimination Algorithm (Play Tennis Dataset)

## 📌 Overview
This project implements the **Candidate Elimination Algorithm**, a concept from Machine Learning used to find the most specific and most general hypotheses that are consistent with the training data.

The dataset used is a classic **Play Tennis dataset**, where the model learns conditions under which a game of tennis can be played.

---

## 📂 Dataset

The dataset is manually created using Pandas.

### Features:
- `outlook` – Weather condition (sunny, overcast, rain)  
- `temp` – Temperature (hot, mild, cool)  
- `humidity` – Humidity level (high, normal)  
- `wind` – Wind condition (weak, strong)  

### Target:
- `playtennis`
  - yes  
  - no  

---

## ⚙️ Technologies Used
- Python 🐍  
- Pandas  

---

## 🚀 Algorithm Used

### Candidate Elimination Algorithm
It maintains two boundaries:
- **Specific Hypothesis (S)** → Most specific rule  
- **General Hypothesis (G)** → Most general rule  

---

## 🧩 Steps Performed

1. **Data Creation**
   - Dataset is created using Pandas DataFrame.

2. **Initialization**
   - Specific hypothesis (S) is initialized with the first positive example.
   - General hypothesis (G) is initialized with the most general values (`?`).

3. **Training Process**
   - For each training example:
     - If the example is **positive (yes)**:
       - Generalize S where needed
     - If the example is **negative (no)**:
       - Specialize G where needed

4. **Updating Hypotheses**
   - Specific and General hypotheses are updated step-by-step.

5. **Final Hypothesis**
   - Remove overly general hypotheses from G.

---

## 📊 Output
The program displays:
- Training dataset  
- Initial hypotheses (S and G)  
- Step-by-step updates of S and G  
- Final specific hypothesis  
- Final general hypothesis  

---

## 📈 Example Output
```text
Initial specific hypothesis: ['sunny', 'hot', 'high', 'weak']
Initial general hypothesis: [['?', '?', '?', '?'], ...]

Final specific hypothesis: ['?', 'mild', '?', '?']
Final general hypothesis: [['sunny', '?', '?', '?'], ...]

```

## Notes

- This algorithm works only with categorical data.
- It assumes noise-free data.
- Useful for understanding concept learning but not widely used in real-world ML.

## Learning Outcome

- Understanding of version space
- Difference between specific and general hypotheses
- Concept learning in Machine Learning 
