# Product Requirements Document (PRD)
## Project: “Determining Which Military Branch of Service to Join — and Why”
### Version: 1.0  
### Owner: David Chang  
### Status: Draft

---

## 1. Project Overview

### Purpose
Create an AI-powered interactive tool that helps users determine which U.S. military branch (Army, Navy, Air Force, Marine Corps, Coast Guard, Space Force) aligns best with their goals, personality, desired career path, and lifestyle preferences. ## Project Overview

Deciding which branch of the U.S. military to join is a complex and highly personal choice. Each branch—Army, Navy, Air Force, Marine Corps, Coast Guard, and Space Force—offers unique missions, cultures, career pathways, expectations, and lifestyle commitments. For prospective service members, especially those without prior military exposure, the differences between branches can be difficult to understand, leading to uncertainty, confusion, or decision fatigue. This project aims to bridge that gap by creating an AI-powered decision support tool that simplifies the process and helps users confidently explore which branch may align most closely with their needs and aspirations.

Many individuals rely on scattered online resources, word-of-mouth stories, or recruiter conversations that may not always provide a fully personalized overview. Traditional guidance materials tend to be either overly high-level or extremely detailed, making it challenging for users to build a clear, practical comparison. This tool centralizes key information and presents it in a structured and accessible format, ensuring that users gain both breadth and depth of understanding. It does so while maintaining neutrality and avoiding recruitment-style framing, focusing instead on informed decision-making.

The system collects user insights through a guided questionnaire covering motivations, preferred career fields, comfort with physical or high-risk environments, desired lifestyle, learning style, and long-term goals. These inputs are processed through a transparent scoring model that maps each response to the intrinsic characteristics and cultural environment of every military branch. Instead of providing a generic or one-size-fits-all answer, the tool uses these weighted factors to create a personalized fit profile for each user, offering a recommendation supported by clear reasoning.

AI is leveraged not to make decisions for users, but to articulate complex comparisons in plain language. The explanation engine transforms scoring outputs into narratives that highlight why certain branches might be a better fit, what each option offers, and what tradeoffs the user should be aware of. This includes day-to-day expectations, operational tempo, travel considerations, training intensity, and career development pathways. The goal is to ensure that users feel fully informed, not directed.

Ethical considerations are central to the system’s design. The tool does not attempt to recruit, predict eligibility, provide medical or legal advice, or make promises about military benefits. Instead, it encourages users to use the output as a conversation starter with official military recruiters, career counselors, mentors, and family members. Transparency about limitations, safety, and neutrality is built into the user experience from the start.

Ultimately, this project seeks to empower individuals with the clarity they need to make a meaningful life decision with confidence. Whether a user is exploring military service for the first time, comparing multiple branches, or seeking guidance on how their personal traits match military environments, this tool provides structured, balanced, and personalized insights. By combining a logical scoring engine with the explanatory power of AI, the project turns a difficult decision into an informed and thoughtful process.

This platform also supports long-term scalability and relevance. As branch missions evolve, careers expand, or cultural characteristics shift, the underlying dataset and logic can be updated to maintain accuracy. In future versions, the system may include advanced comparison tools, recruiter discussion preparation guides, or downloadable reports for schools, counselors, and ROTC programs. This ensures that the tool not only meets user needs today but continues to grow in usefulness over time.


### Problem Statement
Prospective service members often struggle to differentiate between branches and understand how each aligns with their career objectives, values, and long-term aspirations. Existing resources are static, complex, or overly generic.

### Solution
A guided, conversational AI system that:
- Asks structured questions about values, interests, lifestyle preferences, and long-term goals.
- Explains the pros/cons of each branch in simple, personalized language.
- Provides a tailored recommendation with supporting rationale.
- Produces exportable summaries (PDF/Markdown) for decision-making or discussions with recruiters, family, or mentors.

---

## 2. Core Features Implemented

### 2.1 User Intake Flow
- Personal motivations (service, education, adventure, stability, etc.)
- Career interests (technical, combat, medical, logistics, aviation)
- Risk tolerance & lifestyle preferences
- Physical and academic background
- Long-term/transition goals

### 2.2 Recommendation Engine
- Weighted scoring model based on user inputs.
- Branch profiles with defined attributes:
  - Mission focus  
  - Career availability  
  - Ops tempo & lifestyle  
  - Training intensity  
  - Culture & environment  
  - Deployment patterns  
- Generates:
  - **Primary Recommendation**
  - **Secondary Fit**
  - **Branches Not Recommended** (with why)

### 2.3 AI-Generated Explanation
- Clear, friendly narrative describing:
  - Why a branch fits the user
  - Tradeoffs to consider
  - Realistic day-to-day expectations

### 2.4 Exportable Output
- Markdown and PDF summary
- Recruiter-ready formatted output

### 2.5 Ethical Guardrails
- Neutrality across branches  
- No glorification of violence  
- Transparency on limitations  

---

## 3. AI Specification
## 3. AI Specification (Final)

### What the AI Does
The AI system powers the reasoning and explanation layer of the tool. After the user completes the questionnaire, the system processes inputs such as motivation, career preferences, lifestyle expectations, and risk tolerance. These inputs are passed into a structured scoring engine and then the AI converts those raw scores into a narrative explanation. The AI outputs:
- A primary branch recommendation,
- A secondary “close match,”
- A rationale explaining the match,
- Pros and cons,
- Lifestyle, culture, and training expectations.

### Where the AI Appears in the User Flow
The AI is only used **after** the user completes the questionnaire and the scoring engine has computed a quantitative fit profile. The flow is:
1. User completes intake questionnaire on the front-end.  
2. Scoring engine processes answers → generates branch scores.  
3. AI receives the scored data + JSON profiles → generates a narrative explanation.  
4. AI optionally formats the results into Markdown or exportable text (PDF-ready).

### Model or Tool Used
This system uses **ChatGPT (GPT-5.1)** as the primary large language model.  
The model is accessed via:
- Local prompt templates,
- A structured scoring-to-explanation pipeline.

The system is model-agnostic and can be adapted to:
- OpenAI Assistants API,
- Gemini API,
- Claude API,
- Local inference models (e.g., Llama 3.1)  
…depending on deployment requirements.

### Constraints, Guardrails, and Boundaries
To ensure accuracy, neutrality, and safety:
- The AI **does not provide legal, medical, or eligibility advice**.
- The AI **does not recruit** or persuade the user toward enlistment.
- Clear disclaimers are added indicating the tool is **informational only**.
- Sensitive topics such as benefits, medical conditions, and eligibility criteria are handled with caution and redirected to official sources.
- Rate limiting is implemented on API calls (e.g., 1 request per quiz completion).
- Prompts include filters preventing:
  - Overly promotional military messaging,
  - Stereotyping about branches,
  - Claims about guaranteed career outcomes or benefits.

---




### 3.1 LLM Capabilities Required
- Strong reasoning for multi-factor decision-making  
- Ability to map user traits to structured branch profiles  
- Clear, concise explanations  
- Text generation in Markdown and conversational style  

### 3.2 Model Behaviors
- Never pressure a user to enlist  
- Provide balanced pros/cons  
- Encourage consultation with certified recruiters  
- Avoid offering medical, legal, or eligibility determinations  

### 3.3 Knowledge Inputs
Branch knowledge includes:
- Culture & mission focus  
- Educational pathways  
- Special operations overview  
- Travel & deployment patterns  
- Career diversity  
- Pay & benefits (general, not numeric promises)  

### 3.4 Output Templates
- **Recommendation Summary**
- **Branch Comparison Matrix**
- **Lifestyle & Culture Analysis**
- **Career Match Breakdown**
- **Final Recommendation Wrap-up**

---

## 4. Technical Architecture

### 4.1 High-Level Diagram (Text-Based)
## 4. Technical Architecture (Reality Check)

### Architecture Overview
The architecture reflects a lightweight, front-end–focused design that interacts with an AI model only at the final step.

### Front-End Technologies
- **HTML/CSS** for layout and styling  
- **Vanilla JavaScript** for scoring, form logic, and state management  
- **Static JSON file** (`branch_profiles.json`) defining branch characteristics  

### Where the AI Is Called
- A single back-end or serverless endpoint (e.g., Vercel Function, Cloudflare Worker, GitHub Action, or direct API call) sends:
  - User scoring data  
  - Branch attribute data  
  - Prompt template  
  …to ChatGPT.

### External APIs or Services (Optional)
- **OpenAI API** (ChatGPT)  
- **GitHub Pages** for static hosting  
- Optional integrations:
  - PDF generation library (server-side),
  - Logging or analytics tool (e.g., PostHog).

This architecture is intentionally minimal to make the project easy to maintain and deploy.

---

## 5. Prompting & Iteration Summary

### Key Prompts Used
1. **Intake Parsing Prompt**  
   Structured the user’s questionnaire answers into categories before scoring.
2. **Scoring Interpretation Prompt**  
   Took numeric scores and mapped them to narrative reasoning elements.
3. **Recommendation Explanation Prompt**  
   Generated the final branch recommendation and explanation.
4. **Markdown Export Prompt**  
   Turned the AI output into clean, exportable Markdown or PDF-formatted text.

### How Prompts Evolved Over Time
- Early prompts were too open-ended and produced inconsistent outputs; later versions used **strict JSON schema** and **role-based instructions** for stability.
- The explanation prompt originally produced long, recruiter-like text; refinements emphasized neutrality and removed promotional language.
- Scoring-related prompts were updated to require “explain your reasoning only from the dataset, not assumptions,” reducing hallucination.

### What Was Learned About Prompt Design
- The AI performs best when given **structured data + structured instructions**.
- Including examples dramatically improves consistency.
- Guardrails must be explicit (e.g., “Do NOT claim benefits”).
- Breaking the process into **multiple small prompts** works better than one giant prompt.

---

## 6. UX & Limitations

### Intended User Journey
1. User visits the tool and reads a brief introduction.  
2. User completes a structured questionnaire (5–10 items).  
3. The scoring engine generates numeric branch fit scores.  
4. The AI transforms these into a readable explanation.  
5. User receives:
   - Recommended branch,
   - Reasoning,
   - Pros and cons,
   - Lifestyle/culture notes.  
6. User can export the result or use it to guide further conversations.

### Known Limitations
- The scoring engine is a simplified model and cannot capture the full nuance of military decision-making.
- The index.html version is static, so the AI call must be done via a server or API proxy.
- Branch profiles are manually curated and may require periodic updates.
- Some users may misinterpret the output as personalized professional guidance despite disclaimers.

### Ethical or Trust-Related Limitations
Users should **not** rely on this tool when:
- Determining medical, legal, or enlistment eligibility.
- Attempting to understand contract terms or benefits.
- Needing official MOS/AFSC job placement guidance.
- Making decisions without discussing options with recruiters, counselors, or family.

The tool emphasizes that it is **informational, not authoritative**.

---

## 7. Future Roadmap

### If Granted More Time or Resources
- **Dynamic Scoring Engine Upgrade**  
  Add multi-factor weighting, user personality inputs, and goal-based branching logic.
- **Interactive Branch Comparison Dashboard**  
  Visual comparisons of lifestyle, tempo, schooling opportunities, and risk tolerance.
- **Deeper AI Integration**  
  Allow multi-turn conversations and follow-up clarifications rather than one-time scoring.
- **Expanded Data Set**  
  More granular categories: special operations pathways, officer vs. enlisted tracks, reserve components.
- **Safety Enhancements**  
  Stronger disclaimers, model-output verification, and bias auditing for all branch descriptions.


