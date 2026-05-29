# MATH-500 Pilot Subset

这个 20 题子集用于答辩前 pilot：验证 Tülu-3-8B 四阶段模型的行为复现、
hidden states 提取、linear correctness probe 和 ∆logp 分析 pipeline 是否能
端到端跑通。它只用于验证实验流程可行性，不用于报告最终结论。

## Source

- Dataset: HuggingFaceH4/MATH-500
- Split: test
- Source file: `data/math500_full.jsonl`
- Output file: `data/math500_pilot_20.jsonl`
- Summary file: `data/math500_pilot_20_summary.csv`
- Random seed: `20260514`

## Requested Level Quota

- 3: 6
- 4: 8
- 5: 6

## Actual Level Distribution

- 3: 6
- 4: 8
- 5: 6

## Requested Subject Quota

- Algebra: 4
- Intermediate Algebra: 3
- Number Theory: 3
- Geometry: 3
- Counting & Probability: 3
- Precalculus: 2
- Prealgebra: 2

## Actual Subject Distribution

- Algebra: 4
- Intermediate Algebra: 3
- Number Theory: 3
- Geometry: 3
- Counting & Probability: 3
- Precalculus: 2
- Prealgebra: 2

## Fallback Notes

- No fallback was needed.
- Exact level and subject quotas were satisfied.
