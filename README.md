<a href="https://github.com/nqedgelab" id="nqlab-top">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="./assets/banner-dark.svg" />
    <source media="(prefers-color-scheme: light)" srcset="./assets/banner-light.svg" />
    <img src="./assets/banner-dark.svg" alt="NQ Lab: Is there an edge? Not proven yet." width="100%" />
  </picture>
</a>

<br>

<p align="center">
  <img src="https://komarev.com/ghpvc/?username=nqedgelab&color=0f172a&style=flat-square&label=profile+views" alt="profile views" />
  <a href="https://github.com/nqedgelab?tab=followers"><img src="https://img.shields.io/github/followers/nqedgelab?style=flat-square&logo=github&color=0f172a" alt="followers" /></a>
  <a href="https://github.com/nqedgelab?tab=repositories"><img src="https://img.shields.io/github/stars/nqedgelab?style=flat-square&logo=github&color=0f172a&label=stars" alt="total stars" /></a>
  <a href="https://github.com/nqedgelab?tab=repositories"><img src="https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fapi.github.com%2Fusers%2Fnqedgelab&query=%24.public_repos&label=repos&style=flat-square&color=0f172a&cacheSeconds=86400" alt="public repos" /></a>
  <a href="https://github.com/nqedgelab/nqedgelab/issues"><img src="https://img.shields.io/github/issues/nqedgelab/nqedgelab?label=open%20questions&style=flat-square&color=0f172a" alt="open questions" /></a>
  <!-- Enable once nq-research is public:
  <a href="https://github.com/nqedgelab/nq-research/commits"><img src="https://img.shields.io/github/last-commit/nqedgelab/nq-research?label=last%20research%20commit&style=flat-square&color=f59e0b" alt="last research commit" /></a>
  -->
</p>

## Hi, welcome to NQ Lab 👋

This is an open research notebook on Nasdaq-100 E-mini (NQ) futures. The question I'm working on is simple to ask and hard to answer: is there a trading edge here that holds up after costs, on data it wasn't fitted to?

I don't have that answer yet, and I'd rather show the work than claim one.

> [!IMPORTANT]
> Everything here is paper traded. Nothing on this profile is financial advice.

## How the research works

Every idea goes through the same steps, and every result gets published, including the ones that don't work. Most won't, and that's useful to know.

```mermaid
flowchart LR
    A["Write the hypothesis<br/>and what would disprove it"] --> B["Backtest<br/>with realistic costs"]
    B --> C{"Holds up on<br/>held-back data?"}
    C -- No --> D["Rejected<br/>and published"]
    C -- Yes --> E["Paper trade"]
    E --> F["Compare live<br/>vs backtest"]

    classDef step fill:#1e293b,stroke:#64748b,color:#f1f5f9
    classDef gate fill:#f59e0b,stroke:#b45309,color:#0f172a
    classDef stop fill:#334155,stroke:#64748b,color:#cbd5e1
    class A,B,E,F step
    class C gate
    class D stop
```

## Where things stand

An idea only counts as an edge if its expectancy, the average result per trade measured in units of risk (R), stays positive after costs:

$$E = p \cdot \bar{W} - (1 - p) \cdot \bar{L}$$

where $p$ is the win rate, $\bar{W}$ the average win and $\bar{L}$ the average loss. A high win rate means nothing if the losses are bigger than the wins.

<table>
  <tr>
    <td align="center" width="140"><h2>0</h2>Written</td>
    <td align="center" width="140"><h2>0</h2>Tested</td>
    <td align="center" width="140"><h2>0</h2>Rejected</td>
    <td align="center" width="140"><h2>0</h2>Supported</td>
    <td align="center" width="160"><h2>–</h2>Best expectancy<br><sub>out of sample, after costs</sub></td>
  </tr>
</table>

**Currently testing:** nothing yet. The first hypothesis is being drafted.

## Tools

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

## Say hello

Questions, ideas to test, or reasons you think something won't work are all welcome.

> [!TIP]
> The easiest way to reach me is to [open an issue](https://github.com/nqedgelab/nqedgelab/issues). Critiques of the method are especially welcome.

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://streak-stats.demolab.com/?user=nqedgelab&hide_border=true&background=0F172A&ring=F59E0B&fire=F59E0B&currStreakLabel=F59E0B&sideLabels=F1F5F9&currStreakNum=F1F5F9&sideNums=F1F5F9&dates=94A3B8&stroke=334155" />
    <img src="https://streak-stats.demolab.com/?user=nqedgelab&hide_border=true&background=F8FAFC&ring=D97706&fire=D97706&currStreakLabel=D97706&sideLabels=0F172A&currStreakNum=0F172A&sideNums=0F172A&dates=475569&stroke=CBD5E1" alt="GitHub streak" />
  </picture>
</p>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f172a,100:f59e0b&height=90&section=footer" width="100%" alt="" />
