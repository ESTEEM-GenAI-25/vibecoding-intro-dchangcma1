# Product Requirements Document (PRD)
## Project: “Determining Which Military Branch of Service to Join — and Why”
### Version: 1.0  
### Owner: David Chang  
### Status: Draft

---

## 1. Project Overview

### Purpose
Create an AI-powered interactive tool that helps users determine which U.S. military branch (Army, Navy, Air Force, Marine Corps, Coast Guard, Space Force) aligns best with their goals, personality, desired career path, and lifestyle preferences.

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
