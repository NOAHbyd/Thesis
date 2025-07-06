# Thesis

|论文标题|Towards Conversational AI for Disease Management|
|---|---|
|论文链接|https://arxiv.org/pdf/2503.06074|
|模型任务|通过对话收集病史，生成鉴别诊断（DDx）;根据RxQA 基准测试 + BNF/OpenFDA 知识库,生成安全处方|
|数据集|MIMIC-III + Google 内部脱敏数据;Gemini 1.5 Pro 生成;NICE Guidance + BMJ Best Practice;OpenFDA + 英国国家处方集;虚拟 OSCE 病例 + RxQA|
|改进方向|Gemini 1.5 直接处理完整指南，避免传统 RAG 的信息丢失，提升多文档推理能力|
|创新点|JSON Schema 约束管理计划，确保临床可解释性，每条建议关联权威依据|
|不足之处|RxQA 准确率仅 65.3%，高难度问题仍有提升空间|

<br>
<p>
    
|论文标题|Development and Testing of a Novel Large Language Model-Based Clinical Decision Support Systems for Medication Safety in 12 Clinical Specialties|
|---|---|
|论文链接|https://arxiv.org/pdf/2402.01741|
|模型任务|开发基于 RAG-LLM（检索增强生成）的临床决策支持系统（CDSS），用于识别药物处方错误|
|数据集|基于本地药房干预数据库构建的 61个模拟处方错误场景，嵌入 23个复杂临床案例。|
|改进方向|跨 12个临床专科 验证模型普适性，并首次对比 GPT-4/Gemini Pro/Med-PaLM 2 在医疗场景的性能。|
|创新点|设计 "Co-pilot"协同模式：初级药师与LLM协作，显著提升中重度DRP识别率|
|不足之处|Co-pilot模式在 剂量调整 和 无适应症用药 场景表现下降|

<br>
<p>


|论文标题|MedRAG: Enhancing Retrieval-Augmented Generation with Knowledge Graph-Elicited Reasoning for Healthcare Copilot|
|---|---|
|论文链接|https://arxiv.org/pdf/2502.04413|
|模型任务|提出MedRAG框架，通过知识图谱（KG）引导的推理机制提升诊断精度，降低误诊率，并主动生成随访问题以优化决策。|
|数据集|DDXPlus；CPDD，包含551名患者、33种慢性疼痛相关诊断|
|改进方向|利用四层诊断知识图谱（KG）推理RAG，将患者主诉拆解为临床特征并与图谱匹配，融合相似EHR与KG，驱动LLM生成诊断|
|创新点|主动问诊机制，基于特征节点在KG中的区分度评分，主动提问高区分度问题。有效解决信息模糊导致的误诊，提升问诊效率。|
|不足之处|知识图谱增强过程对LLM的依赖与潜在误差，大语言模型仍存在“幻觉”现象，即可能生成看似合理但实际不准确的信息|


<br>
<p>
    
|论文标题|GAP: Graph-Assisted Prompts for Dialogue-based Medication Recommendation|
|---|---|
|论文链接|https://arxiv.org/abs/2505.12888|
|模型任务|DialMed：基于对话的药物推荐；LLM as Patients：动态诊断访谈，评估MDS的主动问诊能力|
|数据集|从医疗平台“春雨医生”（Chunyu-Doctor）和“丁香园药品数据库”（DXY Drugs Database）构建 |
|改进方向|提出GAP框架：一个新颖的基于LLM的药物推荐框架，通过构建以患者为中心的图来捕获和维护细粒度的医疗信息，包括医学概念和状态|
|创新点|三重提示机制：邻域提示（基于图谱邻域关系检索关键知识）；路径提示（通过预定义医疗路径模板生成查询并结合多源验证）；图谱线性化（将图谱三元组转为文本，与对话历史共同输入LLM）|
|不足之处|忽略对话历史中的医疗因素；LLM有时过度关注非必要的医疗信息，导致无用的推荐|

<br>
<p>


|论文标题|Ask Patients with Patience: Enabling LLMs forHuman-Centric Medical Dialogue with GroundedReasoning|
|---|---|
|论文链接|https://arxiv.org/abs/2502.07143|
|模型任务|通过多轮对话实现渐进式医疗诊断，基于患者反馈迭代优化诊断结果|
|数据集|ReMeDi-base|
|改进方向|医学指南驱动的多轮对话框架，整合MSD医学手册，确保问题可靠性与可解释性|
|创新点|利用熵最小化实现最大化信息增益，主动选择信息性价比最高的问题，直接优化诊断效率|
|不足之处|知识依赖单一，完全基于MSD手册，未整合其他医学知识源|

<br>
<p>