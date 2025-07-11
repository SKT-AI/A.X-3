<div align="center">
  <img src="./assets/A.X_logo.png" alt="A.X Logo" width="300"/>
</div>
<br/>
<p align="center">
  <a href="https://huggingface.co/collections/skt/ax-3-686b288b3b05e1234f3f4c73">🤗 Models</a> |
  <a href="https://sktax.chat/chat">💬 Chat</a> |
  <a href="https://github.com/SKT-AI/A.X-3">🖥️ Github</a>
</p>

# A.X 3 Family Highlights

[**🇰🇷 View Korean README**](README.md)

SK Telecom released **A.X 3.1** (pronounced "A dot X"), a large language model (LLM) optimized for Korean-language understanding and enterprise deployment, on July 10, 2025. This **fully sovereign AI model** was developed entirely in-house(from model architecture design and data collection to training) using SKT's private infrastructure. It was trained **from scratch** on **1.65 trillion tokens** multilingual corpus, with Korean as the core language. Focused on high-quality data, A.X 3.1 is the **most training compute-efficient relative to training size** among Korean LLMs.

## What Makes A.X 3.1 Unique?

- **True Korean Sovereign AI**: A.X 3.1 was trained on SKT's TITAN cluster with a 20 trillion token-scale web-based dataset, collected and refined through SKT's internal pipeline.
- **Highly Efficient Multilingual LLM**: A.X 3.1-Light was trained on merely 1.65 trillion tokens, representing the most modest training corpus among open-source Korean LLMs.
- **Superior Korean Proficiency**: Achieved a score of **61.7** on the [KMMLU](https://huggingface.co/datasets/HAERAE-HUB/KMMLU) the leading benchmark for Korean-language evaluation and a Korean-specific adaptation of MMLU, outperforming other Korean-specified models.
- **Deep Language Understanding**: Scored **27.43** on the [KoBALT-700](https://huggingface.co/datasets/snunlp/KoBALT-700), a benchmark for Korean advanced linguistic tasks, outperforming other Korean-specified models.
- **Efficient Token Usage**: A.X 3 model family uses approximately 33% fewer tokens than GPT-4o for the same Korean input, enabling more cost-effective and efficient processing.
- **Deployment Flexibility**: Available in 34B (A.X 3.1) and 7B (A.X 3.1 Light) parameter versions with full on-premise deployment support.
- **Long-Context Handling**: A.X 3.1 supports up to **32,768 tokens**.

## Core Technologies

A.X 3.1 is a **fully original sovereign LLM**, independently developed by SKT—architecture, data, infra, and optimization.

### Model Architecture Specs

| Model         | # Params | # Layers | # KV-Heads | Hidden Dim | FFN Dim |
|:--------------|---------:|---------:|-----------:|-----------:|--------:|
| A.X 3.1 Light | 7B       | 32       | 32         | 4096       | 10880   |
| A.X 3.1       | 34B      | 48       | 8          | 8192       | 21824   |

### Pareto-Optimal Compute Efficiency

A.X 3.1 achieves 5–6× lower compute usage than models of similar performance.

<p align="center">
  <img src="./assets/graph.png" alt="Computational efficiency graph of A.X 3.1 " width="600"/>
</p>

### High-Quality Data Pipeline & Strategic Mixture

- SKT collected 20 trillion web tokens for training.
- All data processed through SKT's internal pipeline with synthetic generation and high-quality filtering.
- Final 1.65T tokens used with a Korean-focused multilingual mix.

### Fully Independent Infrastructure

- No dependency on external cloud services.
- Models are trained on SKT's private high-performance AI clusters.
- Ensures **cost-efficiency**, **security**, and **compute independence**.

## Benchmark Results

A.X 3.1 Light excels in coding and reasoning (e.g., MATH, HumanEval+), and dominates Korean-specific benchmarks (e.g., KMMLU, KoBALT).

<table>
  <thead>
    <tr>
      <th colspan="2">Benchmarks</th>
      <th>A.X 3.1 Light</th>
      <th>Kanana-1.5-8B</th>
      <th>EXAONE-3.5-7.8B</th>
      <th>Qwen2.5-7B</th>
      <th>Qwen3-8B<br/>(w/o reasoning)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td rowspan="4">Knowledge</td>
      <td>KMMLU</td>
      <td>61.70</td>
      <td>48.28</td>
      <td>53.76</td>
      <td>49.56</td>
      <td>63.53</td>
    </tr>
    <tr>
      <td>CLIcK</td>
      <td>71.22</td>
      <td>61.30</td>
      <td>64.11</td>
      <td>58.30</td>
      <td>63.31</td>
    </tr>
    <tr>
      <td>KoBALT</td>
      <td>27.43</td>
      <td>23.14</td>
      <td>21.71</td>
      <td>21.57</td>
      <td>26.57</td>
    </tr>
    <tr>
      <td>MMLU</td>
      <td>66.95</td>
      <td>68.82</td>
      <td>72.20</td>
      <td>75.40</td>
      <td>82.89</td>
    </tr>
    <tr>
      <td rowspan="2">General</td>
      <td>Ko-MT-Bench</td>
      <td>78.56</td>
      <td>76.30</td>
      <td>81.06</td>
      <td>61.31</td>
      <td>64.06</td>
    </tr>
    <tr>
      <td>MT-Bench</td>
      <td>74.38</td>
      <td>77.60</td>
      <td>83.50</td>
      <td>79.37</td>
      <td>65.69</td>
    </tr>
    <tr>
      <td rowspan="2">Instruction Following</td>
      <td>Ko-IFEval</td>
      <td>70.04</td>
      <td>69.96</td>
      <td>65.01</td>
      <td>60.73</td>
      <td>73.39</td>
    </tr>
    <tr>
      <td>IFEval</td>
      <td>79.86</td>
      <td>80.11</td>
      <td>82.61</td>
      <td>76.73</td>
      <td>85.38</td>
    </tr>
    <tr>
      <td rowspan="2">Math</td>
      <td>HRM8K</td>
      <td>41.70</td>
      <td>30.87</td>
      <td>31.88</td>
      <td>35.13</td>
      <td>52.50</td>
    </tr>
    <tr>
      <td>MATH</td>
      <td>70.14</td>
      <td>59.28</td>
      <td>63.20</td>
      <td>65.58</td>
      <td>71.48</td>
    </tr>
    <tr>
      <td rowspan="2">Code</td>
      <td>HumanEval+</td>
      <td>73.78</td>
      <td>76.83</td>
      <td>76.83</td>
      <td>74.39</td>
      <td>77.44</td>
    </tr>
    <tr>
      <td>MBPP+</td>
      <td>61.64</td>
      <td>67.99</td>
      <td>64.29</td>
      <td>68.50</td>
      <td>62.17</td>
    </tr>
  </tbody>
</table>

## Contact

For more information or inquiries, feel free to reach out:

**Email**: [a.x@sk.com](mailto:a.x@sk.com)
