# STANDARDS.md

## BAIS:3300 - Digital Product Management · Module 8 | Personal Landing Page Project

_This file contains technical instructions for this project. Every time you
begin a coding session, ask your LLM to read this file before writing any code.
The LLM will follow these standards automatically without you needing to repeat
them in every prompt._

---

## 1. Project Overview

This site is a personal landing page for Chris Willcutt, a Business Analytics and Information Systems student at the University of Iowa graduating in May 2026. It is designed for recruiters and hiring managers in corporate and consulting roles to evaluate his technical skills, analytics projects, and experience beyond what a resume can show. A successful outcome is increased visibility, recruiter outreach, and interview opportunities for data analyst and business analyst roles.

---

## 2. Technical Standards

These rules apply to every file in this project without exception.

**Languages and versions:**

- HTML5 — use semantic elements throughout: `<header>`, `<main>`, `<section>`, `<article>`, `<footer>`, `<nav>`
- CSS3 — all styles must be written in `css/stylesheet.css`; no inline styles; no `<style>` tags in HTML
- Code must pass validation

**Folder structure:**

/your-website-project  
├── index.html  
├── /css  
│    └── stylesheet.css  
├── /js  
│    └── scripts.js  
├── /images  
│    └── headshot.jpg  

**Framework:**

- No framework — vanilla CSS only

**Architecture:**

- Static site — no JavaScript, no backend, no database
- Single `index.html` file
- External stylesheet in `css/stylesheet.css`
- All images stored locally in `images/`
- Do not link to or embed resume

**Responsiveness:**

- Fully responsive from 320px and wider
- No horizontal scrolling

**Accessibility — WCAG 2.2 Level AA:**

- All images must have descriptive alt text
- Color contrast must meet standards
- Proper heading hierarchy
- Descriptive link text
- Page title must be clear
- All interactive elements keyboard accessible

**Compatibility:**

- Must work on Chrome, Safari, Firefox, and mobile

**Security:**

- External links open in new tab with rel="noopener noreferrer"

---

## 3. Design Standards

**Color palette:**

- Background: #F8F9FA  
- Primary text: #212529  
- Accent: #0D6E6E  
- Secondary background: #E9ECEF  

**Typography:**

- Heading font: Inter  
- Body font: Inter  
- Body size: 16px  
- Line height: 1.6  
- H1: 1.5rem, bold  
- H2: 1.25rem, bold, accent color  

**Imagery:**

- Professional headshot only  

**Layout:**

- Max width: 800px, centered  
- Sticky navigation with anchor links  
- 60px vertical spacing between sections  
- Single column mobile, two-column desktop for projects  

**Component styles:**

Profile photo:
- Circular crop, centered  

Skill tags:
- Rounded pill badges with accent color  

Contact links:
- Labeled links for LinkedIn, GitHub, email  

Navigation:
- Text links with accent hover  

**Tone:**

- Professional, Approachable, Data-driven  
- First person, direct, confident  

---

## 4. PRD Summary

### Problem Statement  
Chris Willcutt is a Business Analytics student targeting data analyst and business analyst roles. His landing page showcases projects and skills in more depth than a resume to help recruiters evaluate him quickly and contact him.

### Target Audience  
Recruiters and hiring managers at corporate and consulting firms, primarily in Chicago or hybrid Midwest roles.

### Goals & Metrics  

| Goal | Measure |
|------|--------|
| Increase visibility | 50–100 site visits |
| Recruiter interest | 5–10 messages |
| Applications | 10–20 applications |
| Interviews | 2–4 interviews |

### Required Content  

Hero:
- Name and tagline focused on Python, SQL, analytics  

Bio:
- University of Iowa BAIS student graduating May 2026  
- Focus on data analysis, modeling, and sports/business insights  

Skills:
- Python, SQL, Excel, Oracle APEX, Access  
- Power BI, Tableau  
- Regression, Forecasting, Time Series, Hypothesis Testing  

Projects:
- MLB regression analysis  
- MLB SQL/database project  
- Car value analysis (Python web scraping)  

Contact:
- LinkedIn  
- Email  
- GitHub  

### Scope  

In Scope:
- Single-page HTML/CSS site  
- Static site  
- Azure deployment  

Out of Scope:
- Multi-page site  
- Dynamic features  
- Backend  

### Assumptions & Constraints  

Assumptions:
- Headshot ready  
- Resume and LinkedIn complete  

Constraints:
- No GitHub repo yet  
- HTML/CSS only  
- One-week timeline  
- Beginner–intermediate skill level  

---

_Remember: this document is a living artifact. Update it as you learn more._
