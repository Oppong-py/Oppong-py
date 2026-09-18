<h1 align="center">Kwabena Oppong Adutwum</h1>

<p align="center">
  First-year Computer Science at <b>KNUST</b>, Kumasi &nbsp;·&nbsp; robotics → applied machine learning<br>
  <b>Open to machine learning internships from summer 2027</b><br>
  <sub>National Robotics Champion 2025 &nbsp;·&nbsp; Regional Cybersecurity Champion 2024</sub>
</p>

<p align="center">
  <a href="https://oppong-py.github.io"><img src="https://img.shields.io/badge/Portfolio-935D0D?style=for-the-badge&logo=githubpages&logoColor=white" alt="Portfolio"></a>
  <a href="https://linkedin.com/in/kwabena-oppong-adutwum"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
  <a href="https://leetcode.com/u/Oppong-py"><img src="https://img.shields.io/badge/LeetCode-FFA116?style=for-the-badge&logo=leetcode&logoColor=black" alt="LeetCode"></a>
  <a href="mailto:oppongkwabena1777dev@gmail.com"><img src="https://img.shields.io/badge/Email-0D6273?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"></a>
</p>

---

### I found the leak in our own evaluation, and it cost us 0.047

Four days on a satellite-imagery problem in September: guess when a building was put up from 40 years of Landsat readings, train on Madrid, make it work in Amsterdam. Our Madrid score came back at **0.6128** macro-F1 and the folds barely disagreed — a standard deviation of 0.0040. That steadiness is what bothered me.

A Landsat pixel is 30 metres across and a building is bigger than that, so splitting the data randomly was putting one half of a roof in training and the other half in the test set. **82.4%** of held-out pixels sat within one pixel of something the model had already seen. Splitting by geography with a five-pixel buffer took that to **0.0%**, and the honest Madrid score to **0.5656** — every number anyone quoted that week, ours included, was about **0.047 too high**.

The second finding is the one worth the picture:

<p align="center">
  <img src="https://raw.githubusercontent.com/Oppong-py/gds-hackathon-2026-building-age/main/results/cv-inversion.png" alt="Slope chart: four feature sets rank one way on Madrid and in exactly the reverse order on Amsterdam" width="760">
</p>

<p align="center"><sub>Four feature sets, ranked on the city we trained on and the city we were graded on. The order reverses exactly.<br>Choosing the way every course teaches — best cross-validation score wins — picks the wrong one.</sub></p>

We didn't place. Adapting to Amsterdam with 25 labelled examples per class scored **0.6220 ± 0.0105**, against 0.5487 for the obvious approach of keeping the source model's trees. Afterwards I found our method comparison had run on a different feature set than the model we shipped, so those numbers don't reproduce — that's written into the repository under a heading saying so.

**[The code →](https://github.com/Oppong-py/gds-hackathon-2026-building-age)** &nbsp;·&nbsp; **[How it went wrong →](https://oppong-py.github.io/blog-the-scoring-was-lying.html)** &nbsp;·&nbsp; **[What transfer learning cost →](https://oppong-py.github.io/blog-transfer-learning-cost.html)**

---

### Now

- **Andrew Ng's ML Specialization** — Course 1, with [the notes published weekly](https://github.com/Oppong-py/ml-specialization-coursera) rather than kept private, so the repo shows exactly how far along it is
- **Logistic regression from scratch** in NumPy, no scikit-learn, to understand what the library has been doing for me
- **Arethos** — an offline-first mental wellness app for KNUST students, built with two others. Private while we finish it; [the engineering write-up is public](https://oppong-py.github.io/blog-arethos-rn.html)

### Written

| | |
|---|---|
| [**The scoring was lying to us**](https://oppong-py.github.io/blog-the-scoring-was-lying.html) | Finding a leak in our own evaluation, and what the honest score cost |
| [**What transfer learning actually costs**](https://oppong-py.github.io/blog-transfer-learning-cost.html) | Three assumptions about moving a model between cities, each measured, each wrong |
| [**From PID control to reinforcement learning**](https://oppong-py.github.io/blog-pid-to-rl.html) | Tuning three numbers on a robot is the same shape of problem as tuning a learning rate |
| [**Three bugs that taught me more than any tutorial**](https://oppong-py.github.io/blog-arethos-rn.html) | React Native's zIndex, a stale closure, and nine haptic iterations on Android |

### Toolkit

<p>
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://skillicons.dev/icons?i=py,cpp,sklearn,arduino,git,linux,vscode&theme=dark">
    <img src="https://skillicons.dev/icons?i=py,cpp,sklearn,arduino,git,linux,vscode&theme=light" alt="Python, C++, scikit-learn, Arduino, Git, Linux, VS Code">
  </picture>
</p>

Plus NumPy, pandas, Matplotlib and Jupyter for the data work, and React Native when something needs a screen. The list is short on purpose — these are the ones I have shipped something with.

---

<p align="center"><sub>Kumasi, Ghana · GMT+0 · replies within a day</sub></p>
