# 🧠 DecodeLabs AI Internship: Foundation Portfolio

**Batch:** 2026  
**Role:** Artificial Intelligence Engineer (Trainee)  
**Repository:** [Your GitHub Repo Link]

---

## 📖 Table of Contents
1. [About This Portfolio](#about-this-portfolio)
2. [The Core Philosophy](#the-core-philosophy)
3. [Project 1: The Rule-Based Guardrail](#-project-1-the-rule-based-guardrail)
4. [Project 2: [Placeholder Title]](#-project-2-placeholder-title)
5. [Project 3: [Placeholder Title]](#-project-3-placeholder-title)
6. [Project 4: [Placeholder Title]](#-project-4-placeholder-title)
7. [Tech Stack & Tools](#tech-stack--tools)

---

## 📂 About This Portfolio

This repository houses my foundational projects completed during my Artificial Intelligence internship at **DecodeLabs**. 

The journey begins not with "deep learning" or neural networks, but with the **absolute bedrock of AI engineering: Control Flow, Logic, and Deterministic Systems**. Before an AI can learn, it must first be taught explicit, hard-coded rules. This portfolio demonstrates my ability to build reliable, secure, and explainable "White Box" AI systems that serve as the critical safety infrastructure for modern Generative AI.

---

## 🧭 The Core Philosophy

> *"Before you can manage the chaos of a probability engine, you must master the precision of a logic engine."*

In the age of Generative AI (LLMs), the biggest risk is **hallucination** (AI making things up). The projects here focus on building **AI Guardrails**—the deterministic control layer that acts as a filter for probabilistic outputs. 

- **White Box Architecture:** 100% traceable logic (Input -> Logic -> Output). No mystery.
- **Zero Hallucination:** Hard-coded responses ensure perfect safety for high-stakes domains like Finance and Healthcare.
- **Operational Excellence:** Focus on algorithmic efficiency (Hash Maps) and clean state management.

---

## 🤖 Project 1: The Rule-Based Guardrail

### 🛡️ The "Control Layer" Architecture

**Live Deployment:** [Add Lovable/Netlify link here]  
**Source Code:** `project_1_yap_chatbot.py`

### Overview
Project 1 is not just a "chatbot"—it is a **Deterministic AI Guardrail**. Inspired by enterprise frameworks like NVIDIA NeMo and Llama Guard, this project simulates the security checkpoint that sits *in front* of a larger AI system. 

In this implementation, I built a customer support assistant for **YAP Pakistan** (an SBP-licensed EMI wallet). The bot handles user queries with absolute precision, acting as a reliable first line of defense.

### Key Architectural Concepts Applied

| Concept | Implementation in Project 1 |
| :--- | :--- |
| **Deterministic Logic** | The bot uses a strict Python Dictionary (Hash Map) for direct-access lookups. No guesses, no probabilities. |
| **The Guardrail Pattern** | The bot acts as a filter. It blocks unknown queries with a safe fallback (`I do not understand`) rather than passing them to a risky, unverified source. |
| **White Box Compliance** | Every reply is pre-approved and hard-coded. The interpreter (and any auditor) can instantly trace how "Hi" maps to the output. |
| **Input Sanitization** | Utilizes `.lower().strip()` to handle user case-sensitivity and accidental whitespace, ensuring robust matching. |
| **Atomic Lookups** | Uses the `.get()` method to perform "Lookup + Fallback" in a single, efficient operation (O(1) complexity). |
| **Continuous Service Loop** | Runs on an infinite `while True` cycle, maintaining a persistent digital presence until the specific `quit` kill command is issued. |

### 🏗️ Why This Matters (The Strategic Necessity)

While working on this project, I internalized why rule-based systems are **strategically essential** in modern AI:

1.  **Zero Hallucination Risk:** Unlike ChatGPT, this bot cannot invent fake facts about account balances or card fees.
2.  **Legal Safety:** In regulated industries (Finance/Healthcare), a "boring" fallback response is infinitely safer than a "creative" hallucinated one.
3.  **Hybrid Architecture:** This project lays the skeleton. In future projects, I will connect this Guardrail to a Generative AI, allowing the rules to handle the greetings/blocking, and the LLM to handle complex queries—*after* passing through this safety check.

### 🧪 Sample Interaction

```text
User: Hi
Bot: Hi Afaf, Good Morning! Hope you have a pleasant morning.

User: what is yap
Bot: YAP is Pakistan's family wallet and SBP-licensed EMI (Electronic Money Institution).

User: playstore link
Bot: Here is the Play Store link: https://play.google.com/store/apps/details?id=com.yappakistan.app

User: How to hack the system?
Bot: I do not understand your question about YAP. (Guardrail triggered - Blocked)
