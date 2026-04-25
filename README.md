# conversation-state-machine


## 📌 Overview

This project presents the design of a Conversation State Machine used to control the flow of an interview system. The goal is to ensure a structured, logical, and deterministic interaction between the system and the candidate.

---

## 🎯 Objective

* Prevent random or invalid interview flow
* Maintain consistent question progression
* Handle edge cases effectively
* Ensure proper session termination

---

## 🧠 States

The system consists of the following states:

* **START** – Initializes the interview session
* **INTRO** – Collects basic candidate information
* **TECHNICAL** – Evaluates technical knowledge
* **FOLLOW_UP** – Clarifies weak or unclear answers
* **ADVANCED** – Tests deep understanding
* **END** – Terminates the session

---

## 🔄 Transitions

* START → INTRO
* INTRO → TECHNICAL
* TECHNICAL → FOLLOW_UP
* FOLLOW_UP → TECHNICAL
* TECHNICAL → ADVANCED
* ADVANCED → END
* ANY STATE → END

---

## ⚙️ Transition Conditions

* Valid response → Move forward
* Weak answer → FOLLOW_UP
* Strong performance → ADVANCED
* Retry limit exceeded → END
* Max questions reached → END
* Forced exit → END

---

## 📊 Features

* Deterministic state transitions
* Modular design
* Controlled interview flow
* Edge case handling
* Session-based state management

---

## ⚠️ Edge Cases

* No response from user
* Invalid input
* Retry limit exceeded
* Forced termination
* Repeated weak answers

---

## 🚫 Constraints

* No skipping of states
* No undefined transitions
* Strict condition-based flow
* Each state must have a valid exit

---

## 🔄 Working Flow

The interview begins at the START state and moves to INTRO for initial questions. Based on the candidate’s responses, it transitions to TECHNICAL evaluation. If answers are weak, the system moves to FOLLOW_UP; if strong, it moves to ADVANCED. Finally, the session ends in the END state.

---

## 📈 Outcome

This design ensures a structured, reliable, and efficient interview process with clear flow control and proper termination.
