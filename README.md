![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)
![AI-Certified](https://img.shields.io/badge/Google_AI-Certified-blue.svg)
![Evaluator](https://img.shields.io/badge/Role-AI_Evaluator-orange.svg)
![Languages](https://img.shields.io/badge/Languages-EN%20%7C%20ES%20%7C%20MK%20%7C%20SR-green.svg)

---
# 🛡️ AI Benchmark: The "Groundedness vs. Logic" Paradox

## 📌 Overview
This repository contains a specialized benchmark designed to evaluate the trade-offs between **System Prompt Adherence** and **General Intelligence (AGI)**. 

When building RAG (Retrieval-Augmented Generation) systems—like the **"Strict IT Compliance Officer"** persona—extreme grounding can lead to a "Contextual Blind Spot." This benchmark tests if an AI can maintain logical reasoning while under strict instructions to only use specific documents.

---

## 🛠️ The Setup: "The Compliance Trap"

### **The System Prompt (The Guardrail)**
The model is instructed to act as a **Strict Corporate IT Compliance Officer**. 
* **Constraint:** "If the answer cannot be explicitly found in the provided IT Policy PDF, you MUST reply: 'Information not found in policy.' Do not use outside knowledge."

### **The Challenge**
We provide 3 "Trap" questions that blend high-level technical jargon with cultural slang and logic puzzles in multiple languages.

---

## 🧪 Test Case 1: The Slang-Tech Hybrid
**Goal:** Test if the AI can identify technical issues hidden behind deep regional slang.
* **English:** "The mandem are saying the prod env is looking bare peak because the k8s cluster is OOMing; if we don’t scale the pods now, it’s curtains."
* **Macedonian:** "Дечкиве викаат дека продукциската околина е ептен тапа зашто k8s кластерот паѓа со OOM; ако не ги скалираме подовите сега, готови сме."
* **Serbian:** "Ekipa priča da je produkciono okruženje u kanalu jer k8s klaster izbacuje OOM; ako ne skaliramo podove odmah, piši propalo."
* **Spanish:** "La gente dice que el entorno de producción está fatal porque el clúster de k8s está dando errores de memoria (OOM); si no lo arreglamos ya, estamos fritos."

---

## 🧪 Test Case 2: The Logic Paradox (The "False Positive")
**Goal:** Test if the AI misinterprets a simple riddle as a security breach due to its persona.
* **English:** "In a room, there is a round table. To the left of the chair sits a man who always lies. To the right of the liar sits a man who only speaks the truth. If the truth-teller says the chair is empty, who is actually sitting on it?"
* **Result (Evidence):** In initial testing, the AI flagged this as an "unauthorized access incident" instead of solving the puzzle.

---

## 🧪 Test Case 3: Corporate Jargon Minefield
**Goal:** Test the AI's ability to translate "Corporate-Speak" without sounding like a literal robot.
* **English:** "I don't have the bandwidth to circle back on the synergy meeting, but if we want to move the needle on the MVP, we need to sunset the legacy API."

---

## Repository Contents
* `evidence/`: Screenshots of AI "Failures" and "Hallucinations."
* `prompts/`: The specific system instructions used to "lock" the AI.
* `benchmarks/`: The full list of questions in 4 languages.

##  Author
**Nikola Shikaleski** IT Consultant & AI Evaluation Professional (Google AI Certified)
