# Milestone 1 — MATH-500 Pilot

> 本目录是国创项目「可验证推理任务中大语言模型后训练的轨迹几何机制与因果验证研究」的
> 里程碑 1。原独立仓库 `reasoning-geometry-pilot` 已合并至本仓库；脚本、数据、prompt
> 现位于仓库根目录的 `scripts/`、`data/`、`prompts/`，复现命令见仓库根 `README.md`。

本里程碑为答辩前 pilot 实验材料，用于验证实验 pipeline 可行性。

## 当前进度

已完成：MATH-500 pilot data preparation。

## 当前产物

- `data/math500_pilot_20.jsonl`
- `data/math500_pilot_20_summary.csv`
- `data/math500_pilot_20_readme.md`
- `data/math500_pilot_20_prompts.jsonl`
- `prompts/math_cot_prompt.txt`

## Pilot 子集分布

Level 分布：

- level 3: 6
- level 4: 8
- level 5: 6

Subject 分布：

- Algebra: 4
- Counting & Probability: 3
- Geometry: 3
- Intermediate Algebra: 3
- Number Theory: 3
- Prealgebra: 2
- Precalculus: 2

该 pilot 子集只用于验证实验 pipeline 可行性，不用于报告最终结论。

## 复现命令

```bash
pip install -r requirements.txt
python3 scripts/inspect_math500.py
python3 scripts/select_math500_pilot.py
python3 scripts/build_math500_prompts.py
python3 scripts/validate_math500_pilot.py
```

## 下一步计划

- generation script
- answer extraction
- behavior summary
- hidden states extraction
- linear probe
- ∆logp analysis
- optional activation patching
