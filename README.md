# DIKWP‑MESH 5.7 NOESIS Ξ

## 外部性保持的人类理解世界生成与超个体提升运行时

**English:** Exteriority‑Preserving Human Understanding World‑Generation and Transindividual Uplift Runtime

**Version:** 1.0.0  
**Evidence grade:** E2 — author-side deterministic reference  
**License:** Apache‑2.0

NOESIS Ξ 不把“理解”定义成记住、复述、答对、接近发送者意图，或得到一个高分。它把理解作为一个持续开放的能力过程：

> 人或群体在目的约束下，从文字、沉默、动作、传感、拒绝与不可访问等异质遭遇中生成并修订局部过程世界；这些世界必须经受预测、干预、反事实、跨表层迁移和延迟复测。局部世界不能拼合时，系统保留阻碍证书；拒绝、不透明和未遭遇外部可以约束行动，但不得被强制内容化。理解只能产生有限、可逆、可复核的行动授权。

## 为什么需要第二次重构

上一代 PARALLAX UPLIFT 已经把理解拆成多维证据，并增加迁移、延迟、校准与原子证据提交。但它仍隐含四个限制：

1. 把个体和文字任务作为默认中心；
2. 容易把语义对齐当成理解的终点；
3. 缺少“局部世界不能拼合”的正式结果；
4. 缺少拒绝、不透明、未遭遇外部和超个体判断的原生对象。

MESH 5.7 允许 NOESIS 把这些限制改造成运行时不变量：载体中立、观察者可选、过程优先、局部拼合、阻碍保留、外部性保护、可逆元语法变异和无单一所有者判断。

## 十二个非总分式能力坐标

| 能力 | 证据问题 |
|---|---|
| purpose_recontracting | 能否发现目的冲突并重新签订目的契约，而非假定唯一目标？ |
| cross_carrier_association | 能否联合文字、沉默、动作、传感、拒绝等异质载体，而不把它们都翻译成文字？ |
| process_world_construction | 能否生成包含参与者、过程、边界、时间和未知项的局部世界？ |
| predictive_intervention | 能否在观察结果前提出可检验预测，并比较干预与不干预？ |
| counterworld_generation | 能否主动生成错误模型、删边世界和替代机制，并保留纠错轨迹？ |
| transfer_invariance | 能否跨表层领域保留深层结构，而非只迁移词汇？ |
| boundary_temporal_awareness | 能否处理多孔、涌现、未决边界及循环、分支、局部时间？ |
| calibration_revision | 信心能否与证据覆盖相称，并在反证后有痕修订？ |
| gluing_obstruction_literacy | 能否区分可拼合局部世界与应当保留的阻碍？ |
| exteriority_integrity | 能否让拒绝、不透明和未遭遇外部产生约束，却不推断其内容？ |
| metagrammar_plasticity | 能否把认知规则本身变成对象，并以可逆方式扩展语法？ |
| transindividual_participation | 能否形成任何单一成员都不能独自拥有的判断，并通过删除测试证明不可约性？ |

每项能力只进入以下状态之一：

`UNOBSERVED → LOCAL-CANDIDATE → INTERVENTION-TESTED → TRANSFER-SUPPORTED → RETENTION-SUPPORTED`

新证据可以把任何既有支持降为 `HELD-CONTRADICTION`。系统没有“总体理解力分数”，也不会宣布理解完成。

## 六阶段证据循环

```text
BASELINE
  → TRAINING / deliberate error
  → TRANSFER / surface shift
  → EXTERIOR / refusal-opacity test
  → COLLECTIVE / deletion and gluing test
  → DELAYED / retention and contradiction reopening
```

每个探针预先声明：目标能力、结构家族、表层家族、预期契约、证伪条件和认知负担。开放回答不能由关键词碰撞直接判定；它必须由结构化直接输入或具名解释复核转换为可审计主张。

## 参考运行结果

确定性合成参考轨迹包含：

- 6 个阶段化理解探针；
- 6 个回答载体；
- 6 个具名解释复核；
- 1 个主动生成错误并纠正的轨迹；
- 6 个误解拓扑；
- 6 个证据对象与 6 个理解前沿快照；
- 1 个 MESH 5.7 原子认知事件包；
- 168 个持久化对象；
- 1 个哈希链事件和 1 个稳定幂等回执。

参考轨迹首先识别出一个“表达流畅、信心很高、但单一目的、强制共识并推断拒绝动机”的伪理解。经过反事实、迁移、外部性和集体删除测试后，11 个能力获得本地延迟支持；目的冲突被保留为 `HELD-CONTRADICTION`，而不是被伪装成已解决。

这只是软件行为证明，不是真实人类提升证据。

## 快速运行

```bash
python -m venv .venv
source .venv/bin/activate

python -m pip install dist/dikwp_mesh57-5.7.0-py3-none-any.whl
python -m pip install dist/dikwp_mesh57_noesis-1.0.0-py3-none-any.whl

noesis57 --version
noesis57 conformance --out outputs/conformance57.json
noesis57 demo --out outputs/reference-local
noesis57 artifacts-validate --root outputs/reference-local
noesis57 pilot-kit --out pilot-local
noesis57 pilot-validate --file pilot-local/session_template57.json
```

打开：

```text
outputs/reference-local/dashboard.html
studio/index.html
```

`studio/index.html` 是不联网、不自动评分的离线学习者工作台；`pilot/` 提供预注册、学习者宪约、探针模板、盲评量表和会话数据结构。

## 主要目录

```text
src/dikwp_mesh57_noesis/   运行时源码
schemas/                   19 个 JSON Schema
examples/reference/        可复现参考制品
outputs/reference/         完整参考运行
protocols/                 宪约与证据协议
scripts/                   构建和验证工具
docs/                      理论、架构、实验和边界文档
dashboard/index.html       离线证据驾驶舱
studio/index.html          离线学习者工作台
pilot/                     人类试验预注册与数据模板
dist/                      MESH 5.7 与 NOESIS 可安装 wheel
```

## 已验证

- NOESIS pytest：67/67；
- NOESIS conformance：81/81；
- 上游 MESH 5.7 pytest：73/73；
- 上游 MESH 5.7 conformance：60/60；
- 输出结构与引用完整性：61/61；
- JSON Schema：11 个输出制品分别通过 Draft 2020-12 与内置离线子集验证，19 个 Schema 可用；
- SQLite 原子提交、幂等重试、崩溃回滚和篡改检测：通过；
- clean-wheel 无源码路径安装、完整 demo、fallback Schema 和人类试验模板：通过；
- 离线驾驶舱与学习者工作台 Chromium 渲染、工作台否决/预览/JSON 导出：通过。

## 明确不作出的主张

本版本不证明：真实人类理解得到提升；段玉聪的理解理论已被经验验证；发送者意图永远是正确目标；十二个能力穷尽全部理解；拒绝内容已被理解；局部阻碍具有形而上学必然性；一次合成延迟任务证明长期保持；本系统适用于临床、法律、就业、教育淘汰或其他高风险人格评估。

更多内容见：

- `docs/UNDERSTANDING_ESSENCE_CN_EN.md`
- `docs/DUAN_THEORY_AUDIT_AND_EXTENSION_CN_EN.md`
- `docs/ARCHITECTURE_CN_EN.md`
- `docs/HUMAN_EVALUATION_PROTOCOL_CN_EN.md`
- `docs/LEARNER_STUDIO_GUIDE_CN_EN.md`
- `docs/SCIENTIFIC_BOUNDARY_CN_EN.md`
