https://aistudio.google.com/apps/drive/1Lpr_xlBKOvYq98Ujkt8k5IOjZDwaGyAR?showAssistant=true&resourceKey=&showPreview=true
# Determining Which Military Branch of Service to Join — AI Decision Support Tool

This repository contains the full Product Requirements Document (PRD), specifications, and architecture for an AI-powered decision-support tool that helps prospective service members understand which branch of the U.S. military may be the best fit for their goals, personality, lifestyle preferences, and long-term career path.

The tool is designed to be **neutral**, **informational**, and **supportive**, providing personalized insights without replacing official guidance from recruiters or the Department of Defense.

---

## 🚀 Project Purpose

Choosing a branch of military service is complex. Each branch has its own:

- Culture and mission
- Training expectations
- Deployment patterns
- Career pathways
- Lifestyle considerations

This project uses a structured questionnaire combined with an AI-driven scoring engine to generate **personalized recommendations** and **branch explanations** that help users make an informed decision.

---

## 📄 Key Documents

### **Product Requirements Document (PRD)**
Located in `/docs/PRD.md` (or in the root if preferred).  
The PRD covers:

- Project Overview  
- Core Features  
- AI Specification  
- Technical Architecture  
- Prompting Strategy & Iteration Log  
- Content Requirements  
- Next Steps and Development Plan

---

## 🧠 How the AI System Works

1. **User Intake Flow**  
   The system collects motivations, interests, lifestyle preferences, career goals, and risk tolerance.

2. **Branch Scoring Engine**  
   A structured JSON dataset defines each branch by measurable attributes.  
   The intake responses are mapped to weights, generating a **branch-fit score**.

3. **AI Explanation Generator**  
   The LLM converts scores into:
   - A primary branch recommendation  
   - A secondary branch recommendation  
   - A clear narrative explaining *why*  

4. **Export Options**  
   Users can export:
   - Markdown summary  
   - PDF reports  
   - Comparison tables  

---

## 🏗️ Technical Architecture


