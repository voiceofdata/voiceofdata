---
title: Renewals Reporting — SOAR Case Study
permalink: /data/case-studies/renewals-reporting/
---

> **Working title:** From AE-only visibility to team-wide renewal accountability
>
> **Role:** Senior Software Licensing Specialist (later part of Client Operations Specialists)
>
> **Timeline:** Mid-2020 → Early 2021 (active use through 2022)

---

## Situation

At the time, our organization tracked renewals through a central **renewals portal** that was configured around the **Account Executive (AE)** as the owner of record. I was working on the **Software Licensing Specialists (SLS)** team—later evolving into **Client Operations Specialists (COS)**—and had been hired as a **Senior SLS** with ~12 years of licensing experience.

Renewals were business-critical, but **operational staff (Support/COS)** had no consolidated place to view the renewals they were responsible for supporting. Visibility and accountability skewed to AEs, even though Operations did a substantial portion of the work required to land the renewal.

## Obstacle

* **No support team view:** The portal surfaced renewals **by AE only**; Support/COS couldn’t easily see *their* book of upcoming renewals.
* **Fragmented ownership:** Tasks and follow-ups for renewals were spread across email and ad hoc trackers, increasing the chance of misses.
* **Limited reporting:** Leadership lacked a clean roll-up of renewals **by Support/COS owner**, making workload planning and recognition difficult.

## Action

The only tool I had access to at the time was **Excel**, which—after nearly 20 years of experience—was where I was most comfortable. I manually pulled data from the **renewals portal** into an Excel file, since there was no automated export process yet.

Initially, this was a **“just for me” project**, something to make my own workflow more efficient. I imported the raw data and built a **pivot table** organized by **Renewal Date** (columns) and **AE, Customer, and Publisher** (rows). This gave me an at-a-glance view of what was coming up and who was responsible.

During a call with my **Team Lead**, I happened to use the report to quickly find a renewal instead of digging through the portal. She noticed how much faster and clearer it was, and immediately became interested in expanding the idea for the full team.

From there, the report evolved from a simple pivot table into a **full Excel dashboard**. I removed gridlines and tabs to create a clean, app-like layout and used **Shapes** as clickable navigation buttons to move between sections.

The dashboard included:

* A **Team Summary page**, grouped by COS team member and renewal date.
* **Individual pages** for each COS, with subpages for each rep.
* **Navigation buttons** for intuitive movement between sections.

Once it received leadership approval, the dashboard was shared via **OneDrive**, ensuring everyone had access to the same, up-to-date version. The team adopted it quickly, using it regularly—usually monthly—to track renewal progress and spot issues early.

Unfortunately, not long after adoption, the **renewals portion of our job was transitioned to an offshore team**, pausing the dashboard’s further development.

## Result

* **Team Visibility:** For the first time, Support/COS staff had a clear view of their own renewals and workload.
* **Leadership Insight:** The dashboard was showcased in Director meetings, highlighting previously invisible workstreams.
* **Adoption:** Within ~6 weeks, it became part of the team’s monthly workflow.
* **Recognition:** Informal praise from leadership (“There’s nothing in the official company reports that shows this!”).
* **Career Impact:** The project’s success drew management attention and inspired me to begin learning Power BI—starting with a basic COS workload report that later evolved into broader BI initiatives.

## Reflection / Lessons Learned

* Designing **for the real owner of the work** can transform outcomes, even if the system of record is anchored elsewhere.
* Lightweight modeling + the right pivots/filters often beat complex workflows when speed and adoption matter.
* Early **stakeholder demos** (Ops + AE + leadership) align expectations and accelerate adoption.
* Even short-lived projects can have **lasting influence** if they shift thinking about visibility and ownership.

> That project marked the moment I realized data could do more than measure performance—it could illuminate the people and processes that make the work possible.

---

## Tech Summary (for quick scanning)

* **Data:** Renewals portal exports
* **Tools:** Excel
* **Modeling:** Pivot tables, manual data refresh
* **Visuals:** Team dashboard layout, individual & subpages, custom navigation
* **Distribution:** OneDrive shared file

## Artifacts (Optional)

No visuals are included to respect company confidentiality. A generic demo or layout sketch with dummy data may be added later.

## Anonymization Notes

To maintain confidentiality, no original data or screenshots are included. Any future demo versions will use fully synthetic data modeled on public sources.
