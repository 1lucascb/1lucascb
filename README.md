# Hey, I'm Lucas 👋

I'm a **Back-End Software Engineer** focused on building reliable, scalable systems and understanding the engineering principles behind them.

My primary technologies are **Python, Go, and Java**. I've worked across backend architecture, API development, distributed systems, databases, messaging, cloud infrastructure, and AI-powered applications.

My main interests include **system design, distributed systems, performance engineering, cloud infrastructure, and LLM-based systems**.

I also write about things I learn and build, particularly around AI agents and LLM-powered architectures, on my [personal website](https://ptfl.lcb936.com/).

<!-- CUSTOM_CONTENT_START -->
---
**☕ Daily Engineering Digest - 2026-11-28** · `AI / LLM Research`

### AI / LLM Research Digest

Two papers address critical gaps in LLM evaluation and reasoning robustness.

| Paper | Key Finding |
| :--- | :--- |
| [Attack Policy Selection can Mislead Monitor Evaluators](https://arxiv.org/abs/2611.34934v1) | False negative rates for AI safety monitors vary drastically (0.5%–23.0%) based on how attack policies are generated. |
| [Put the World Back: Timestamps Matter](https://arxiv.org/abs/2611.34848v1) | LLMs often ignore timestamps in time-series reasoning, relying on correlational shortcuts when inputs are pre-aligned. |

**Technical Takeaway:**
When evaluating LLM safety or reasoning capabilities, standard benchmarks may provide false confidence. The monitor evaluation paper demonstrates that proxy-based attack generation can mask vulnerabilities, while the time-series study shows that high accuracy on ordered data does not prove the model is using temporal indices. Engineers should verify that evaluation protocols explicitly test for shortcut reliance and use diverse, non-optimized attack vectors to ensure robustness claims hold in deployment.
<!-- CUSTOM_CONTENT_END -->
