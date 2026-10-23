# Hi, I am Harmanpreet Singh Sagar

### Final-year Software Engineering student at McMaster University (Class of 2027)

I build protocols, data pipelines, and the tests that prove they behave, from CubeSat Space Protocol services on satellite hardware to a race replay that reproduces live timing tick for tick. I also like taking things I care about outside of software, mostly sports, and turning them into something tangible. The F1 Battle Detector below is both of those at once.

**Working on right now**

- [**jPipe**](https://www.jpipe.org/) at **McSCert**, an LLM pipeline that pulls safety claims and their quoted evidence out of AI model cards and turns them into justification diagrams
- [**F1 Battle Detector**](https://github.com/harmanpreet-sagar/F1-Battle-Detector-Summarizer), a Formula 1 race replay that ranks on-track battles, in FastAPI and Next.js ([live demo](https://f1-battle-detector-summarizer.vercel.app/))
- Organizing events for **DeltaHacks**, including high school outreach and a resume roast

**Some things I am proud of**

- Cut broken builds reaching the Perforce depot **90%** at Synopsys with a two-tier regression system, then took its pre-commit gate from **40 minutes to 18**
- Traced all **7** failed checks among **187** LLM-extracted quotes in jPipe to **5** model errors and **1** PDF parser reading-order fault counted twice, putting the true hallucination rate at **2.7%**
- Proved the F1 replay matches live polling: **8 laps** of the 2025 Hungarian GP run through a fake OpenF1 server and the replay engine give identical battles at every **1.5-second** tick
- Built the CSP service layer for PRESET: **5 service handlers**, CSP over **2 transports**, carried across **2 board revisions**
- **1st place**, RBC Challenge at DeltaHacks IX
- **3.83/4.0** GPA, Dean's Honour List 3x, **$11K** in scholarships

**Looking for** new grad software roles starting **May 2027**. More on my [**website**](https://harmanpreet-sagar.vercel.app/).

---

## Currently

- **Research Assistant, [jPipe](https://www.jpipe.org/) (Part-time)** | McMaster University, McSCert | Sept. 2026 - Present
- **Events Executive** | DeltaHacks | June 2026 - Present

## Previously

- **Firmware Specialist, PRESET CubeSat** | McMaster Interdisciplinary Satellite Team | Sept. 2023 - Oct. 2026
- **Web Developer** | Develop for Good | May 2026 - Aug. 2026
- **System Architecture and Modelling Engineering Intern** | Synopsys Inc. | May 2024 - Aug. 2025
- **Community and Code Co-Lead** | Google Developer Groups McMaster | Sept. 2023 - Aug. 2025
- **Research Assistant, [Drasil](https://github.com/JacquesCarette/Drasil)** | Department of Computing and Software | May 2023 - Aug. 2023
- **Outreach Coordinator** | Google Developer Student Clubs McMaster | Oct. 2022 - Jul. 2023

---

## What I am building

**[F1 Battle Detector](https://github.com/harmanpreet-sagar/F1-Battle-Detector-Summarizer)** - Formula 1 race replay and battle ranking · [**Live demo**](https://f1-battle-detector-summarizer.vercel.app/)
Replays **6** real 2025 Grands Prix (**167k+** OpenF1 rows) through the same detection pipeline live timing uses, stamping every event at the moment a live poller could first have known it. Battles are scored on gap, closing rate, and pace delta, ranked by the championship points at stake, and only surface once they hold across 3 distinct gap readings. Runs on Vercel serverless functions with no long-running process: the broadcast position is worked out from the wall clock, so each request rebuilds its state in about **30-40 ms** and every viewer sees the same race moment. **322** pytest tests in GitHub Actions, including one that replays every race and fails if a battle ever shows under a safety car.
`Python` `FastAPI` `asyncio` `Pydantic` `Next.js` `TypeScript` `Docker` `Vercel` `GitHub Actions`

**[jPipe](https://www.jpipe.org/) model-card pipeline** - checking LLM-extracted safety claims against their source (research, McSCert)
Built a text normalizer (**7** ordered rules, including NFKC and Markdown stripping) and a **5-tier** quote matcher with a PyMuPDF fallback, so a quote the PDF parser scrambled is no longer counted as an LLM hallucination. Covered by **69** pytest cases, including a regression test on the real GPT-5 system card.
`Python` `PyMuPDF` `pytest` `LLMs`

**[SCEMAS](https://github.com/harmanpreet-sagar/sfwreng-3a04-group6-t01-scemas)** - environmental monitoring and alerting · [**Live demo**](https://sfwreng-3a04-group6-t01-scemas.vercel.app/)
Full-stack IoT platform with MQTT ingestion, configurable alert thresholds, and server-sent-event streaming to a React dashboard. Team lead on a 5-person build, owning Threshold Management, the API Facade, and DevOps: a 3-service Docker Compose stack with a TLS MQTT broker, deployed to Render and Vercel, with a 4-job GitHub Actions pipeline.
`FastAPI` `React` `TypeScript` `PostgreSQL` `Docker` `JWT`

**[RBC-BizConnect](https://devpost.com/software/rbc-bizconnect)** - investor-business matching, **1st place at DeltaHacks IX**
Cut investor-business matching from quadratic to linear time with a single-pass algorithm, on a Firebase-authenticated platform with a SQLite data layer.
`Python` `JavaScript` `SQLite` `Firebase`

**[Maze Runner](https://github.com/harmanpreet-sagar/Maze-Runner)** - pathfinding solver
Parses ASCII maze files and computes valid paths using BFS and right-hand traversal, with 27 JUnit tests and a Maven CLI that benchmarks the two strategies against each other.
`Java` `Maven` `JUnit`

---

## Tools I reach for

**Languages**

![Python](https://img.shields.io/badge/Python-3776AB.svg?style=for-the-badge&logo=Python&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6.svg?style=for-the-badge&logo=TypeScript&logoColor=white)
![C++](https://img.shields.io/badge/C++-%2300599C.svg?style=for-the-badge&logo=c%2B%2B&logoColor=white)
![C](https://img.shields.io/badge/C-A8B9CC.svg?style=for-the-badge&logo=C&logoColor=black)
![Java](https://img.shields.io/badge/Java-%23ED8B00.svg?style=for-the-badge&logo=openjdk&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E.svg?style=for-the-badge&logo=JavaScript&logoColor=black)
![C#](https://img.shields.io/badge/C%23-%23239120.svg?style=for-the-badge&logo=csharp&logoColor=white)
![Haskell](https://img.shields.io/badge/Haskell-5D4F85.svg?style=for-the-badge&logo=Haskell&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-003B57.svg?style=for-the-badge&logo=SQLite&logoColor=white)
![Bash](https://img.shields.io/badge/Bash-%23121011.svg?style=for-the-badge&logo=gnu-bash&logoColor=white)
![LaTeX](https://img.shields.io/badge/LaTeX-008080.svg?style=for-the-badge&logo=LaTeX&logoColor=white)

**Frameworks and Libraries**

![React](https://img.shields.io/badge/React-61DAFB.svg?style=for-the-badge&logo=React&logoColor=black)
![Next.js](https://img.shields.io/badge/Next.js-000000.svg?style=for-the-badge&logo=next.js&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688.svg?style=for-the-badge&logo=FastAPI&logoColor=white)
![Pydantic](https://img.shields.io/badge/Pydantic-E92063.svg?style=for-the-badge&logo=pydantic&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-5FA04E.svg?style=for-the-badge&logo=nodedotjs&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-06B6D4.svg?style=for-the-badge&logo=tailwindcss&logoColor=white)
![FreeRTOS](https://img.shields.io/badge/FreeRTOS-2A6E3F.svg?style=for-the-badge&logo=freertos&logoColor=white)
![Pytest](https://img.shields.io/badge/Pytest-0A9EDC.svg?style=for-the-badge&logo=pytest&logoColor=white)

**Infrastructure and Tools**

![Docker](https://img.shields.io/badge/Docker-2496ED.svg?style=for-the-badge&logo=Docker&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF.svg?style=for-the-badge&logo=githubactions&logoColor=white)
![Jenkins](https://img.shields.io/badge/Jenkins-D24939.svg?style=for-the-badge&logo=Jenkins&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032.svg?style=for-the-badge&logo=Git&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624.svg?style=for-the-badge&logo=Linux&logoColor=black)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1.svg?style=for-the-badge&logo=PostgreSQL&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-3FCF8E.svg?style=for-the-badge&logo=supabase&logoColor=black)
![Vercel](https://img.shields.io/badge/Vercel-000000.svg?style=for-the-badge&logo=Vercel&logoColor=white)
![Render](https://img.shields.io/badge/Render-000000.svg?style=for-the-badge&logo=render&logoColor=white)
![Perforce](https://img.shields.io/badge/Perforce-404040.svg?style=for-the-badge&logo=Perforce&logoColor=white)
![MATLAB](https://img.shields.io/badge/MATLAB-0076A8.svg?style=for-the-badge&logo=mathworks&logoColor=white)
![Arduino](https://img.shields.io/badge/Arduino-00979D.svg?style=for-the-badge&logo=Arduino&logoColor=white)
![Firebase](https://img.shields.io/badge/Firebase-FFCA28.svg?style=for-the-badge&logo=Firebase&logoColor=black)
![Confluence](https://img.shields.io/badge/Confluence-172B4D.svg?style=for-the-badge&logo=Confluence&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626.svg?style=for-the-badge&logo=Jupyter&logoColor=white)
![Google Colab](https://img.shields.io/badge/Google%20Colab-F9AB00.svg?style=for-the-badge&logo=Google-Colab&logoColor=white)
![Webflow](https://img.shields.io/badge/Webflow-146EF5.svg?style=for-the-badge&logo=Webflow&logoColor=white)
![Wix](https://img.shields.io/badge/Wix-0C6EFC.svg?style=for-the-badge&logo=Wix&logoColor=white)
![WordPress](https://img.shields.io/badge/WordPress-21759B.svg?style=for-the-badge&logo=WordPress&logoColor=white)
![Figma](https://img.shields.io/badge/Figma-F24E1E.svg?style=for-the-badge&logo=Figma&logoColor=white)
![Notion](https://img.shields.io/badge/Notion-000000.svg?style=for-the-badge&logo=Notion&logoColor=white)

---

## Stats

![Harman's GitHub stats](https://github-profile-summary-cards.vercel.app/api/cards/stats?username=harmanpreet-sagar&theme=2077)
![Harman's Commit stats](https://github-profile-summary-cards.vercel.app/api/cards/most-commit-language?username=harmanpreet-sagar&theme=2077)
![Harman's Repo stats](https://github-profile-summary-cards.vercel.app/api/cards/repos-per-language?username=harmanpreet-sagar&theme=2077)
