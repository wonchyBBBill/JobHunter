# 🚀 JobHunter: Proactive AI-Driven Job Discovery System

JobHunter is a specialized agentic workflow designed to transform the job search from a manual "keyword search" into a strategic, company-first intelligence operation. It is specifically optimized for **New Graduates (e.g., Class of 2026)** and entry-level engineers seeking roles in Applied AI, LLM Engineering, and AI Agents.

## 🎯 The Core Philosophy
Instead of browsing job boards and hoping for a match, JobHunter reverses the process:
1. **Company-First**: Identify every company in target regions (e.g., Shanghai, HK) that has the technical capacity to hire AI engineers.
2. **Portal Mapping**: Locate the direct recruitment gateways for those companies.
3. **Strict Filtering**: Use a "zero-experience" filter to discard over-leveled roles and only capture direct links to "New Grad" or "Entry Level" postings.
4. **Direct-to-Job**: Deliver absolute URLs to specific positions, bypassing general career homepages.

## 🛠️ System Architecture

### 📂 Folder Structure
- `SKILL.md`: The brain of the agent. Contains the operational logic and " personas" for the AI to follow.
- `candidate_profile.json`: The source of truth. Stores skills, target locations, and the critical `total_years_of_experience` filter.
- `candidate_profile_template.json`: The master schema used to initialize new profiles.
- `company_targets.csv`: A database of discovered companies and their official career portals.
- `job_pool.csv`: The final pipeline of qualified, direct-link job opportunities.
- `application_rules.md`: The scoring rubric used to rank a job's fit against the candidate's profile.
- `my-materials/`: Storage for resumes and supporting documents used for profile synchronization.

### ⚙️ The Workflow Pipeline
1. **Profile Sync**: Agent reads the resume $\rightarrow$ Updates `candidate_profile.json` $\rightarrow$ Identifies experience gaps.
2. **Exhaustive Mapping**: Search $\rightarrow$ Identify all companies in target cities $\rightarrow$ Log to `company_targets.csv`.
3. **Deep-Dive Extraction**: Visit portals $\rightarrow$ Scan for "New Grad/Junior" $\rightarrow$ Verify 0-experience eligibility $\rightarrow$ Log direct URLs to `job_pool.csv`.
4. **Review**: The user reviews the `job_pool.csv` and proceeds to apply.

## 🛡️ Constraints
- **No Guessing**: The agent is forbidden from guessing work authorization or salary requirements.
- **No General Links**: Only direct links to specific job postings are permitted in the final pool.
- **Strict Experience Filter**: Roles requiring professional experience beyond the candidate's profile are automatically discarded.

---
*Developed for the 2026 AI Engineering Graduate Hunt.*
