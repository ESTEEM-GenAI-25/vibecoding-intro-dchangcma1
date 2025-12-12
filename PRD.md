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
