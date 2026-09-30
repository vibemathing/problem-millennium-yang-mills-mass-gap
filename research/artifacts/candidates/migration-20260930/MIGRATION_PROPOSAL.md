# yang-mills-mass-gap: blocked migration and archived research proposal

Status: proposal_only / not admitted. Date: 2026-09-30 UTC.
Base revision: 5dfe77eca549490025f1ab5f21ddf9abdd1f91f0. Problem: problem:millennium-yang-mills-mass-gap.
Contract digest: 8d261ef6372623ce357fc61c2bbc566d89163ca53366fe7c6e0ea983f9bae85c. Harness: 1.2.6.

## Bootstrap and migration boundary

Fresh default branch has verified repository identity, active canonical-admitted ProblemContract, but empty attempts and obligation-graphs. No admitted Attempt/Route/Graph/target Obligation exists. Therefore no new mathematical research was started. This PR archives the relevant previously written exploratory derivations for review and proposes admission work. Proposed node labels and IDs are not admitted records. No canonical record, Harness file, schema, script, workflow, EvidenceLink, Result, verifier receipt, or Solution view is changed.

The profile remains candidate_generator_and_transport_writer, even under an owner GitHub principal. Harness maintenance cannot include candidate artifacts or change canonical truth. Source repair below is a proposed input for a trusted migration, not a changed ProblemContract. Baseline make check-full passed (8 tests, 1 skipped); this does not establish current-template compatibility. Current template requires source revision/content_sha256/quote/license fields missing from canonical records.

The existing PR diff gate requires exactly one valid web-attempt packet. None is fabricated here because pre-admission objects are absent. Expected exact failure: `candidate PR must add exactly one web attempt packet, found 0`. Do not merge this proposal-only draft or weaken the gate to make it pass. A trusted operator must review and admit the Attempt and graph, confirm source provenance/license treatment, and then produce a correctly bound packet.

## Archived local research (not new repository execution)

The following text was developed before this migration and has candidate-only scope. Its references to executed assertions concern the earlier local exploration, not a verifier receipt or this repository's CI. Original combined draft SHA-256: d05ccad5b75594a1380c2e3c9d4f7405c90885c0c83a2be6a85935309d266e84. Original script SHA-256: 4fadc66faf3e39dfdb616d8316412f67ef516b297ff0b93f32783f1d64bbf4da. No full third-party paper is republished.

## 3. Yang–Mills 根与六个子问题

### 3.1 冻结目标

[Clay/Jaffe–Witten 官方陈述](https://www.claymath.org/wp-content/uploads/2022/06/yangmills.pdf)：对每个紧致简单规范群 G，在 R⁴ 构造非平凡量子 Yang–Mills 理论，满足至少官方所要求公理强度，且 Hamiltonian 的真空之上有正谱隙。还应存在有限正能谱，排除“只有真空”的空洞构造。否定形式为存在一个此类 G，使所有满足目标公理且非平凡的构造都不能同时有规定质量隙（包括不存在这样的理论）。

[Clay 当前问题页](https://www.claymath.org/millennium/yang-mills-the-maths-gap/) 仍标为 Unsolved；不能用单个网上“已证明”文稿覆盖该状态。规范不变可观测量的量子构造与四维连续极限是对象；经典 Yang–Mills PDE、单个有限格点、低维模型都不能代替。

### 3.2 DAG：一个可选的欧氏重构路线，不是唯一可能分解

- Y1 `definition`：规定 G、规范不变可观测量、连续极限/重整化方案及公理对象；定义任务，尚无本包具体完整构造
- Y2 `lemma`：给定有限格点与正参数，归一化测度存在及合适反射正性；有经典严格格点框架，不等于连续理论。[Osterwalder–Seiler 原始论文](https://doi.org/10.1016/0003-4916(78)90039-8) 建立格点 Schwinger 正性/正转移矩阵
- Y3 `theorem`：在移除 UV cutoff 并扩张体积时控制所需全部 Schwinger 分布，保留非平凡性、欧氏不变性、正性、正则性、聚类及一致兼容性；本包未完成，是本路线实质缺口
- Y4 `theorem`：由已满足完整假设的欧氏对象重构具有唯一真空、正能及局域性的量子理论；重构是已知条件框架，输入假设的证明未完成
- Y5 `lemma`：真空正交空间一个稠密向量族上共同正指数率的时间相关衰减 ⇒ 谱隙；本包完整证明并测试边界。未知的是构造 YM 后能否建立此前提，特别是 cutoff/体积一致性
- Y6 `theorem`：在真实四维连续理论中验证 Y5 的共同衰减率与稠密性、非零有限能激发，并覆盖任意紧致简单 G；本包未完成

边：Y1→Y2；Y1+Y2→Y3（构造路线依赖，不是自动蕴含）；Y3+完整重构定理前提→Y4；Y4+Y6→Y5可应用；Y4+Y5应用+Y6非平凡性/群全称量词→根。图为无环；Y5 是抽象桥，Y6 的内容是检验桥的前提而不是先假设谱隙。证明 SU(2) 不能自动完成“任意 G”。

## 4. YM 已执行数学：条件谱隙桥与负控

### 4.1 定理、所有量词与证明

设 ℋ 为 Hilbert 空间，H≥0 自伴，ker H=span{Ω}，||Ω||=1。设 D⊂Ω⊥ 稠密。假设存在共同 m>0，使每个 v∈D 都存在有限 Cv≥0，且对所有 t≥0，

0≤⟨v,e^(−tH)v⟩≤Cv e^(−mt)。

则 H|Ω⊥ 的谱包含于 [m,∞)，即真空之上至少有 m 的能隙。这里 Cv 可依赖 v，m 必须共同；不需 Cv=||v||²，也不需对所有向量预先成立。

证明：谱定理给 μv(B)=||E_H(B)v||²≥0，相关函数=∫_[0,∞)e^(−tλ)dμv(λ)。固定0<a<m，

e^(−at) μv([0,a]) ≤相关函数≤Cv e^(−mt)，

故 μv([0,a])≤Cv e^(−(m−a)t)→0。因而 E_H([0,a])v=0。该谱投影有界，且 D 在 Ω⊥ 稠密，所以它在整个 Ω⊥ 上为零。取有理 a↑m 得 E_H([0,m))|Ω⊥=0。结合真空与正交补的约化分解得到结论。端点 m 允许有谱。

反向：若上述谱隙已知，则对任意 v∈Ω⊥，积分直接给出相关函数≤||v||² e^(−mt)。所以在已构造自伴 Hamiltonian 的层次，这是可用的等价判据；它不构造 H，也不证明 YM 公理。

反例目标/否定：若正谱落入(0,m)但所有稠密测试向量仍满足共同率 m，则其对应非零谱投影应同时在稠密集上为零，矛盾。这正是上面证明排除的情形。

### 4.2 三个不可省条件：已执行负控

1. **单个观测量不够。** H=diag(0,1/100,1)，Ω=e₁，v=e₃。相关函数精确为 e^(−t)，但整体谱隙仅1/100。看到一条曲线斜率1不能推出整体 gap≥1
2. **体积一致性不够就不能取极限。** H_L=diag(0,L⁻²)。每个有限 L 都有正隙，L→∞ 却趋于0。脚本精确列出1,1/4,1/16,1/64,1/256；这不是 YM 格点模型，只是对逻辑推断的反例
3. **每个向量都有自己的率也不够。** 在 ℂΩ⊕ℓ²(N) 上令 HΩ=0，He_n=n⁻¹e_n。有限支撑向量稠密，每个向量的相关函数以某正率衰减，但正谱1/n聚向0，没有共同隙。故不能交换“∀v∃m_v”与“∃m∀v”

一个额外负控：在第二个低能模上 t=100，e^(−1)>e^(−50)，精确击穿错误共同率1/2。脚本全部断言通过。

### 4.3 连续极限转移的精确待证项

若在同一测试代数上有 cutoff 参数 a、体积 L 的相关函数 C_a,L(v,t)，并对每个固定 v,t 已证明 C_a,L→C(v,t)，且统一有 0≤C_a,L(v,t)≤Cv e^(−mt)，其中 Cv 和 m 与 a,L 无关，则极限逐点继承该界。随后还必须证明这些测试向量在重构的 Ω⊥ 中稠密并证明其相关函数确实为 ⟨v,e^(−tH)v⟩。不需擅自交换 t→∞ 与 cutoff 极限；先在每个固定 t 传递界，再用4.1即可。若常数随 cutoff 发散、归一化改变、真空正交条件失效或极限变平凡，桥失效。

这一段完成了一个有用的条件化简与失败准则，但没有产生未知的四维一致估计。无新颖性、根证明或独立准入声称。

