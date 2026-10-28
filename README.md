<a href="https://github.com/nqedgelab" id="nqlab-top">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="./assets/banner-dark.svg" />
    <source media="(prefers-color-scheme: light)" srcset="./assets/banner-light.svg" />
    <img src="./assets/banner-dark.svg" alt="NQ Lab: Is there an edge? Not proven yet." width="100%" />
  </picture>
</a>

<br>

<div align="center">
  <img src="https://komarev.com/ghpvc/?username=nqedgelab&color=3b82f6&style=flat-square&label=profile+views" alt="profile views" />
  <a href="https://github.com/nqedgelab?tab=followers"><img src="https://img.shields.io/github/followers/nqedgelab?style=flat-square&logo=github&labelColor=1e293b&color=8b5cf6" alt="followers" /></a>
  <a href="https://github.com/nqedgelab?tab=repositories"><img src="https://img.shields.io/github/stars/nqedgelab?style=flat-square&logo=github&labelColor=1e293b&color=14b8a6&label=stars" alt="total stars" /></a>
  <a href="https://github.com/nqedgelab?tab=repositories"><img src="https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fapi.github.com%2Fusers%2Fnqedgelab&query=%24.public_repos&label=repos&style=flat-square&labelColor=1e293b&color=0ea5e9&cacheSeconds=86400" alt="public repos" /></a>
  <a href="https://github.com/nqedgelab/nqedgelab/issues"><img src="https://img.shields.io/github/issues/nqedgelab/nqedgelab?label=open%20questions&style=flat-square&labelColor=1e293b&color=22c55e" alt="open questions" /></a>
  <!-- Enable once nq-research is public:
  <a href="https://github.com/nqedgelab/nq-research/commits"><img src="https://img.shields.io/github/last-commit/nqedgelab/nq-research?label=last%20research%20commit&style=flat-square&labelColor=1e293b&color=6366f1" alt="last research commit" /></a>
  -->
</div>

<br>

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="./assets/section-welcome-dark.svg" />
  <source media="(prefers-color-scheme: light)" srcset="./assets/section-welcome-light.svg" />
  <img src="./assets/section-welcome-dark.svg" alt="Hi, welcome to NQ Lab" width="100%" />
</picture>

This is an open research notebook on Nasdaq-100 E-mini (NQ) futures. The question I'm working on is simple to ask and hard to answer:
<div align="center">
<strong> is there a trading edge here that holds up after costs, on data it wasn't fitted to? </strong>
</div>
I don't have that answer yet, and I'd rather show the work than claim one.


> [!IMPORTANT]
> Everything here is paper traded. Nothing on this profile is financial advice.

<br>

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="./assets/section-process-dark.svg" />
  <source media="(prefers-color-scheme: light)" srcset="./assets/section-process-light.svg" />
  <img src="./assets/section-process-dark.svg" alt="How the research works" width="100%" />
</picture>

Every idea is written down before it's tested, including the result that would prove it wrong. It's then backtested with realistic costs and judged on data held back from the start. Ideas that hold up get paper traded; the rest are published as rejected. Most won't hold up, and that's useful to know.

```mermaid
flowchart LR
    A["Hypothesis"] --> B["Backtest"]
    B --> C{"Holds up?"}
    C -- No --> D["Rejected"]
    C -- Yes --> E["Paper trade"]

    classDef step fill:#1e293b,stroke:#64748b,color:#f1f5f9
    classDef gate fill:#3b82f6,stroke:#1d4ed8,color:#ffffff
    classDef stop fill:#334155,stroke:#64748b,color:#cbd5e1
    class A,B,E step
    class C gate
    class D stop
```

<br>

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="./assets/section-edge-dark.svg" />
  <source media="(prefers-color-scheme: light)" srcset="./assets/section-edge-light.svg" />
  <img src="./assets/section-edge-dark.svg" alt="What counts as an edge" width="100%" />
</picture>

An idea only counts as an edge if its expectancy stays positive after costs, on data it wasn't fitted to. Expectancy is the single number every result here is judged on.

<details>
<summary><b>What is expectancy?</b></summary>
<br>

Expectancy is the average amount you make or lose per trade, over many trades. It's measured in **R**, where 1R is the amount risked on a trade (the distance from entry to stop). Measuring in R makes results comparable no matter the position size.

$$E = p \cdot \bar{W} - (1 - p) \cdot \bar{L}$$

where $p$ is the win rate, $\bar{W}$ the average win and $\bar{L}$ the average loss, both in R.

**Why win rate alone is misleading.** Two strategies, before costs:

<div align="center">

| | Win rate | Average win | Average loss | Expectancy |
|:---|:---:|:---:|:---:|:---:|
| Strategy A | 40% | 2.0R | 1.0R | 0.4 × 2.0 − 0.6 × 1.0 = **+0.20R** |
| Strategy B | 70% | 0.5R | 1.5R | 0.7 × 0.5 − 0.3 × 1.5 = **−0.10R** |

</div>

Strategy B wins far more often and still loses money. Strategy A loses more often than it wins and still makes 0.2R per trade on average.

**Why "after costs" matters.** Commission and slippage come off every trade. A small positive expectancy can turn negative once they're included, especially with tight stops, where costs are a bigger share of 1R.

**Why sample size matters.** Expectancy from 20 trades is mostly noise. Each hypothesis here sets a minimum number of trades in advance, before any result counts.

</details>

<br>

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="./assets/section-status-dark.svg" />
  <source media="(prefers-color-scheme: light)" srcset="./assets/section-status-light.svg" />
  <img src="./assets/section-status-dark.svg" alt="Where things stand" width="100%" />
</picture>

<div align="center">

<table>
  <tr>
    <td align="center" width="140"><h2>0</h2>Written</td>
    <td align="center" width="140"><h2>0</h2>Tested</td>
    <td align="center" width="140"><h2>0</h2>Rejected</td>
    <td align="center" width="140"><h2>0</h2>Supported</td>
    <td align="center" width="160"><h2>–</h2>Best expectancy<br><sub>out of sample, after costs</sub></td>
  </tr>
</table>

</div>

**Currently testing:** nothing yet. The first hypothesis is being drafted.

<br>

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="./assets/section-tools-dark.svg" />
  <source media="(prefers-color-scheme: light)" srcset="./assets/section-tools-light.svg" />
  <img src="./assets/section-tools-dark.svg" alt="Tools" width="100%" />
</picture>

<div align="center">

<table>
  <tr>
    <td align="center" width="33%"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg" width="40" height="40" alt="" /><br><b>Python</b><br><sub>The language everything is written in</sub></td>
    <td align="center" width="33%"><img src="https://cdn.simpleicons.org/pandas/E70488" width="40" height="40" alt="" /><br><b>pandas</b><br><sub>Loading and slicing price data</sub></td>
    <td align="center" width="33%"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/numpy/numpy-original.svg" width="40" height="40" alt="" /><br><b>NumPy</b><br><sub>Fast maths for backtests and statistics</sub></td>
  </tr>
  <tr>
    <td align="center" width="33%"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/jupyter/jupyter-original.svg" width="40" height="40" alt="" /><br><b>Jupyter</b><br><sub>Notebooks for exploring results</sub></td>
    <td align="center" width="33%"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/git/git-original.svg" width="40" height="40" alt="" /><br><b>Git</b><br><sub>Timestamps every hypothesis before it's tested</sub></td>
    <td align="center" width="33%"><img src="https://cdn.simpleicons.org/claude" width="40" height="40" alt="" /><br><b>Claude</b><br><sub>AI research partner that writes code and challenges conclusions</sub></td>
  </tr>
</table>

</div>

<br>

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="./assets/section-hello-dark.svg" />
  <source media="(prefers-color-scheme: light)" srcset="./assets/section-hello-light.svg" />
  <img src="./assets/section-hello-dark.svg" alt="Say hello" width="100%" />
</picture>

Questions, ideas to test, or reasons you think something won't work are all welcome.

> [!TIP]
> The easiest way to reach me is to [open an issue](https://github.com/nqedgelab/nqedgelab/issues). Critiques of the method are especially welcome.

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://streak-stats.demolab.com/?user=nqedgelab&hide_border=true&background=0F172A&ring=60A5FA&fire=60A5FA&currStreakLabel=60A5FA&sideLabels=F1F5F9&currStreakNum=F1F5F9&sideNums=F1F5F9&dates=94A3B8&stroke=334155" />
    <img src="https://streak-stats.demolab.com/?user=nqedgelab&hide_border=true&background=F8FAFC&ring=2563EB&fire=2563EB&currStreakLabel=2563EB&sideLabels=0F172A&currStreakNum=0F172A&sideNums=0F172A&dates=475569&stroke=CBD5E1" alt="GitHub streak" />
  </picture>
</p>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f172a,100:3b82f6&height=90&section=footer" width="100%" alt="" />
