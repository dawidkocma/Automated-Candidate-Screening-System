# 🎯 NexusPrep AI: Deterministic Talent Intelligence Pipeline

NexusPrep is a high-fidelity automation engine built with **n8n** and **GPT-4o** designed to bridge the gap between technical CVs and specific Job Descriptions. Unlike generic evaluators, NexusPrep acts as a "Skeptical Hiring Manager," providing deterministic scoring, culture-fit inference, and a prioritized improvement roadmap.

---

## 🚀 Key Features

* **Deterministic Evaluation:** Implemented zero-temperature LLM modeling to ensure 100% scoring consistency across multiple sessions.
* **Intelligent Extraction:** Custom binary-to-text pipeline that sanitizes and structures unstructured PDF data for high-accuracy analysis.
* **Company DNA Inference:** Uses sentiment analysis of JDs to identify core company values and predict probable technical interview questions.
* **Bento-Style Dashboard:** A custom-coded, responsive UI built with Tailwind CSS, optimized for rapid data digestion.

---

## 🛠️ The Architecture

The pipeline consists of three distinct phases:



### Phase 1: Ingestion & Sanitization
* **Node:** `Candidate Input Portal` (n8n Form Trigger)
* **Process:** Handles multi-part form data and binary PDF buffers.
* **Transformation:** The `PDF Text Extractor` node converts binary data into clean, searchable strings.

### Phase 2: Cognitive Analysis
* **Engine:** OpenAI GPT-4o-mini
* **Configuration:** `Temperature: 0.0` | `JSON Mode: Enabled`
* **Persona:** A "Skeptical Technical Recruiter" system prompt that prioritizes explicit evidence over inference.

### Phase 3: Dynamic Rendering
* **Output:** `Generate Response Dashboard` (n8n Form Ending)
* **Logic:** JavaScript `.map()` functions dynamically render arrays for skills, values, and tips into a custom HTML/CSS template.

---

## 💻 Technical Stack

* **Orchestration:** n8n
* **AI Model:** OpenAI GPT-4o
* **Frontend:** HTML5, Tailwind CSS, Google Fonts (Inter)
* **Data Format:** Structured JSON

---

## 📋 How to Run

1.  Import the `workflow.json` into your n8n instance.
2.  Add your `OpenAI API Key` to the credentials section.
3.  Activate the workflow and open the "Production URL" of the Form Trigger.
4.  Upload a PDF CV and paste a Job Description.

---

## 🧠 Design Philosophy

As a developer with dyslexia, I engineered the dashboard to prioritize **scannability** and **visual hierarchy**. Using a Bento-grid layout and high-contrast color coding for skills ensures that the most critical information is delivered with zero cognitive friction.

---

## 📄 License
MIT © 2026 Dawid Kocma
