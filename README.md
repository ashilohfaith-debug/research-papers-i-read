# 120-Day Research Paper Reading List
## Essential Papers for AI/ML/LLM/Agentic AI Mastery

**Note:** This list provides ONE paper per day. Papers are organized by rotating track (Mon-Sun pattern) and should be read at the specified level of depth. Each entry includes:
- **Day & Date:** When to read it in the 120-day roadmap
- **Track:** Which rotating theme (LLM, Agentic, Quantum, Bio+AI, Physical AI, Chem+AI, Free choice)
- **Paper Title & Link:** Full citation + arXiv/official link
- **Why it matters:** What problem it solves or what insight it provides
- **Prerequisite knowledge:** What you need to understand it
- **Depth level:** Skim (abstract+intro+figures), Medium (full paper but skip heavy math), Deep (full technical understanding)
- **Key sections to focus on:** What to actually read carefully
- **What you should explain afterward:** Your competency bar

*(Dates updated so Day 1 begins Monday, September 14, 2026.)*

---

## WEEK 1 (Days 1-7)

### Day 1 — Monday Sept 14 — LLM/Transformer Track (Orientation)
**Paper:** [Attention Is All You Need](https://arxiv.org/abs/1706.03762)
- **Authors:** Vaswani et al., 2017
- **Why it matters:** The foundational transformer architecture paper — literally created the architecture that powers every major LLM today (GPT, BERT, Llama, etc.). This is THE paper.
- **Prerequisite knowledge:** Neural networks, matrix multiplication, basic attention intuition (you'll have this by Day 61 when you properly dive in)
- **Depth level:** **Skim only today** (orientation pass)
- **Read carefully:** Abstract, Figure 1 (the architecture diagram)
- **Skip:** Section 5-6 (heavy math) for now — come back to it Day 68
- **What you should be able to explain:** "There's a new architecture called Transformer that uses attention instead of recurrence — what's attention at a 30-second level?"

**Link:** https://arxiv.org/abs/1706.03762

---

### Day 2 — Tuesday Sept 15 — AI+Chemistry/Materials Track
**Paper:** [Equivariant Graph Neural Networks for Crystal Structures and Properties Prediction](https://arxiv.org/abs/2206.03349)
- **Authors:** Dusson et al., 2022 (or use a simpler crystal-structure ML paper if this feels too advanced — search "SchNet crystal structure" for a slightly gentler entry)
- **Why it matters:** Shows how neural networks can learn to predict molecular/crystal properties from structure — direct application of deep learning to materials science
- **Prerequisite knowledge:** Neural networks basics, graph neural networks if available (OK if not yet)
- **Depth level:** **Skim** — grab the core idea
- **Read carefully:** Abstract, introduction, Figure 1-2 showing structure representation
- **Key insight to extract:** How do you represent a 3D crystal structure as an input to a neural network? Answer: graph neural networks over atom positions
- **What you should explain:** "Neural nets can learn materials properties by treating atoms as graph nodes — why is that useful for chemistry/materials?"

**Link:** https://arxiv.org/abs/2206.03349 (or simpler: "SchNet: A continuous-filter convolutional neural network for modeling quantum interactions")

---

### Day 3 — Wednesday Sept 16 — Free Choice / Exploration Track
**Paper:** [Foundational LLM Papers You're Curious About](https://huggingface.co/papers)
- **Instructions for Day 3:** Visit Hugging Face Daily Papers (https://huggingface.co/papers), scroll through "trending" papers today, and pick ONE that sounds interesting to you (any field, any depth). The point is to start building the habit of exploring without a rigid agenda once per week.
- **Why it matters:** Builds pattern recognition and serendipity — sometimes the papers that shape your thinking are the random ones you stumble into
- **Depth level:** Skim only
- **What you should do:** Write 3 sentences in your paper log about what you read, even if you didn't understand it all

---

### Day 4 — Thursday Sept 17 — LLM/Transformer Track
**Paper:** [BERT: Pre-training of Deep Bidirectional Transformers for Language Understanding](https://arxiv.org/abs/1810.04805)
- **Authors:** Devlin et al., Google, 2018
- **Why it matters:** The paper that made masked language modeling famous — established encoder-only, bidirectional pretraining (contrasts with GPT's decoder-only, causal approach). You need to know BERT to understand why GPT was different and revolutionary.
- **Prerequisite knowledge:** Transformers at a high level (attention, layers) — you'll have basic intuition by now
- **Depth level:** **Skim-to-Medium** — understand the method, skip implementation details
- **Read carefully:** Abstract, Intro, Section 3 (BERT methodology), Figure 1 (input representation)
- **Key sections to skip:** Experiments section (unless curious)
- **What you should explain:** "BERT uses masked language modeling (predict masked tokens from surrounding context). Why would you predict masked tokens instead of next tokens, and what's the tradeoff?"

**Link:** https://arxiv.org/abs/1810.04805

---

### Day 5 — Friday Sept 18 — Agentic AI Track (Orientation)
**Paper:** [ReAct: Synergizing Reasoning and Acting in Language Models](https://arxiv.org/abs/2210.03629)
- **Authors:** Yao et al., 2022
- **Why it matters:** Foundational agentic reasoning pattern — shows that having an LLM explicitly write out Thought/Action/Observation steps improves multi-step task performance. This is the core loop behind modern agents.
- **Prerequisite knowledge:** Language models, prompting, basic reasoning
- **Depth level:** **Skim only today** (orientation) — you'll dive deeper at Day 101
- **Read carefully:** Abstract, Intro, Section 2 (method with one example trace), Figure 1-2
- **What you should grasp:** "Instead of a model just outputting an answer, what if it wrote 'I need to look up X → (observes result) → now I can answer'?"

**Link:** https://arxiv.org/abs/2210.03629

---

### Day 6 — Saturday Sept 19 — Quantum Computing Track (Orientation)
**Paper:** [Quantum Computing in the NISQ era and beyond](https://arxiv.org/abs/1801.00862)
- **Authors:** Preskill, 2018
- **Why it matters:** The definitive overview of Noisy Intermediate-Scale Quantum computing — what quantum computers can actually do today (not sci-fi), and what the roadmap looks like. Essential context for "quantum + AI" discussions.
- **Prerequisite knowledge:** None — this is an overview
- **Depth level:** **Skim** — grab the concepts, skip math
- **Read carefully:** Abstract, Intro, Section 1 (What is a quantum computer), Section 2 (NISQ era characterization), Sections on quantum error correction
- **Key insight:** Quantum computers today are "noisy" and limited — not the general-purpose speedup machines you might imagine
- **What you should explain:** "What does 'NISQ' mean, and why is error correction the bottleneck for quantum computing?"

**Link:** https://arxiv.org/abs/1801.00862

---

### Day 7 — Sunday Sept 20 — REVIEW & BUFFER DAY
**No new paper.** Use this day to re-skim one of the papers from this week that felt hardest, and add 2-3 flashcards for core concepts.

---

## WEEK 2 (Days 8-14)

### Day 8 — Monday Sept 21 — AI+Biology Track
**Paper:** [Highly accurate protein structure prediction with AlphaFold](https://www.nature.com/articles/s41586-021-03819-2) or [ArXiv version](https://arxiv.org/abs/2010.11288)
- **Authors:** Jumper et al., DeepMind, 2020 (published Nature 2021)
- **Why it matters:** Solved a 50-year-old problem (protein structure prediction) using deep learning — a watershed moment for AI+biology. Shows the power of ML applied to hard scientific problems.
- **Prerequisite knowledge:** Basic neural networks, graph structures, sequence modeling
- **Depth level:** **Skim-to-Medium** — the core idea is understandable without implementation details
- **Read carefully:** Abstract, Introduction (the problem), Figure 1-2 (the architecture), Results section
- **Key sections to skip:** Methods technical details (unless very interested)
- **What you should explain:** "AlphaFold uses attention over protein sequences and 3D structure predictions — why would attention be useful for structure prediction?"

**Link:** https://arxiv.org/abs/2010.11288 (arXiv preprint), or https://www.nature.com/articles/s41586-021-03819-2 (Nature)

---

### Day 9 — Tuesday Sept 22 — Physical AI / Robotics Track
**Paper:** [Mobile ALOHA: Learning Bimanual Mobile Manipulation](https://arxiv.org/abs/2401.02117)
- **Authors:** Fu et al., Stanford, 2024
- **Why it matters:** Shows physical robots learning to manipulate objects by watching human demonstrations — embodied AI where the "thinking" must be grounded in the real world
- **Prerequisite knowledge:** None — this is about robots + learning
- **Depth level:** **Skim** — get the idea, skip implementation
- **Read carefully:** Abstract, Intro, Figure 1-3 (robot, demonstrations, results)
- **Key insight:** How do you combine imitation learning with robotic embodiment? What are the challenges?
- **What you should explain:** "Why is learning from human demonstrations harder for robots than for language models?"

**Link:** https://arxiv.org/abs/2401.02117

---

### Day 10 — Wednesday Sept 23 — Free Choice
**Hugging Face Daily Papers** — pick another interesting paper, any domain.

---

### Day 11 — Thursday Sept 24 — LLM/Transformer Track
**Paper:** [Language Models are Unsupervised Multitask Learners (GPT-2)](https://d4mucfpksywv.cloudfront.net/better-language-models/language_models_are_unsupervised_multitask_learners.pdf)
- **Authors:** Radford et al., OpenAI, 2019
- **Why it matters:** The paper that showed "just scale up a decoder-only transformer on internet text, and it learns to do many tasks via prompting." Established the GPT lineage and the philosophy behind modern LLMs.
- **Prerequisite knowledge:** Transformers (you have basic intuition now)
- **Depth level:** **Medium** — this is a more accessible paper than Attention Is All You Need
- **Read carefully:** Sections 1-2 (intro + related work), Section 3 (model architecture — mostly review), Section 4 (results with examples), Figure 1
- **What you should explain:** "Why is 'unsupervised multitask learning' a better way to think about LLMs than 'next-token prediction on a specific task'?"

**Link:** https://d4mucfpksywv.cloudfront.net/better-language-models/language_models_are_unsupervised_multitask_learners.pdf (official OpenAI) or search arXiv for "GPT-2"

---

### Day 12 — Friday Sept 25 — Agentic AI Track
**Paper:** [Toolformer: Language Models Can Teach Themselves to Use Tools](https://arxiv.org/abs/2302.04761)
- **Authors:** Schick et al., Meta, 2023
- **Why it matters:** Early influential work showing that LLMs can learn to call tools (APIs) from self-supervised data generation — the precursor to modern tool-calling agents
- **Prerequisite knowledge:** Language models, tool calling concept (you're building intuition)
- **Depth level:** **Skim-to-Medium**
- **Read carefully:** Abstract, Intro, Section 2 (self-supervised data generation for tool use), examples
- **Key insight:** How can you generate training data where a model learns to call tools without supervised labels? Answer: annotate where tool calls would be useful, then fine-tune
- **What you should explain:** "What's novel about learning tool use from self-supervised signals rather than supervised examples?"

**Link:** https://arxiv.org/abs/2302.04761

---

### Day 13 — Saturday Sept 26 — Quantum+AI Track
**Paper:** [Quantum machine learning in feature Hilbert spaces](https://arxiv.org/abs/1803.07128) or [Quantum Computing for Machine Learning](https://arxiv.org/abs/2209.00045)
- **Authors:** Schuld & Killoran, 2019 (or Schuld et al., 2022 for the second)
- **Why it matters:** Explores where quantum computing might actually accelerate machine learning (kernel methods, sampling, optimization) — honest about what's still theoretical vs. near-term practical
- **Prerequisite knowledge:** Basic ML, quantum computing intuition (you have both now)
- **Depth level:** **Skim** — this is conceptual, not hands-on
- **Read carefully:** Abstract, Intro, Section on quantum-enhanced ML ideas
- **What you should grasp:** Quantum computers might help with specific ML bottlenecks (kernel evaluation, sampling), but we're still early
- **What you should explain:** "Name one operation in classical ML that a quantum computer might speed up, and why"

**Link:** https://arxiv.org/abs/2209.00045 (newer, more comprehensive)

---

### Day 14 — Sunday Sept 27 — REVIEW & BUFFER DAY
**No new paper.** Review this week's papers, add flashcards for: BERT vs. GPT architectural difference, ReAct loop phases, AlphaFold protein structure insight.

---

## WEEK 3 (Days 15-21)

### Day 15 — Monday Sept 28 — AI+Biology Track
**Paper:** [Generative modeling for protein design](https://arxiv.org/abs/2304.12954) (or a recent protein generation paper from 2024 — check HF Daily Papers for "protein generation + LLM")
- **Why it matters:** Using deep generative models (diffusion or transformers) to design new proteins with desired properties — generative AI applied to structural biology
- **Prerequisite knowledge:** Transformers, embeddings, protein structure basics
- **Depth level:** **Skim**
- **Read carefully:** Abstract, Intro, Figure 1 (the approach)
- **Key insight:** Protein design as a generative problem rather than purely search/optimization
- **What you should explain:** "How is generating proteins different from predicting their structure (AlphaFold)?"

**Link:** Search arXiv for "protein generation deep learning 2024" and pick a recent one (the field moves fast)

---

### Day 16 — Tuesday Sept 29 — Physical AI / Robotics Track
**Paper:** [Learning to manipulate deformable objects without demonstrations](https://arxiv.org/abs/1910.04677) or [Learning from Play](https://arxiv.org/abs/1802.10675)
- **Why it matters:** Robots learning from self-play rather than demonstrations — more general than imitation learning
- **Prerequisite knowledge:** Reinforcement learning basics (you haven't studied this yet, but the paper is still skimmable)
- **Depth level:** **Skim**
- **Read carefully:** Abstract, Intro, approach section, Figure 1
- **What you should grasp:** Self-play as an alternative to demonstrations for embodied AI
- **What you should explain:** "Why is learning from self-play appealing for robotics compared to collecting human demonstrations?"

**Link:** https://arxiv.org/abs/1802.10675 (Learning from Play)

---

### Day 17 — Wednesday Sept 30 — Free Choice
**Hugging Face Daily Papers** — pick one

---

### Day 18 — Thursday Oct 1 — LLM/Transformer Track
**Paper:** [Training language models to follow instructions with human feedback (InstructGPT)](https://arxiv.org/abs/2203.02155)
- **Authors:** Ouyang et al., OpenAI, 2022
- **Why it matters:** The paper that established the SFT → RM → RLHF pipeline for turning a base LLM into a helpful assistant. This is the exact workflow behind ChatGPT and modern instruction-tuned models.
- **Prerequisite knowledge:** Language models, prompting, basic RL concepts (you'll have enough intuition)
- **Depth level:** **Medium** — this is very relevant to your Phase 9 work
- **Read carefully:** Abstract, Intro, Section 2 (three-step pipeline diagram, Figure 2), Section 3 results
- **Key sections to skip:** Detailed RLHF math (Section 2.2 details) — grasp the idea, don't memorize equations
- **What you should explain:** "What are the 3 steps in the InstructGPT pipeline, and why is each step necessary?"

**Link:** https://arxiv.org/abs/2203.02155

---

### Day 19 — Friday Oct 2 — Agentic AI Track
**Paper:** [Self-Refine: Iterative Refinement with Self-Feedback](https://arxiv.org/abs/2303.17651)
- **Authors:** Madaan et al., 2023
- **Why it matters:** Agents that give themselves feedback and refine their outputs — a step beyond ReAct. Shows agentic loops can be used for self-improvement
- **Prerequisite knowledge:** Language models, ReAct-style reasoning
- **Depth level:** **Skim**
- **Read carefully:** Abstract, Intro, Figure 1 (the self-refine loop), examples
- **What you should grasp:** Agents can be loops over: generate → self-evaluate → refine
- **What you should explain:** "How does Self-Refine differ from a single-pass LLM output?"

**Link:** https://arxiv.org/abs/2303.17651

---

### Day 20 — Saturday Oct 3 — Quantum Computing Track
**Paper:** [Quantum Advantage in Learning from Experiments](https://arxiv.org/abs/2112.00882) or [Quantum machine learning at the boundary of quantum computing](https://www.nature.com/articles/s43588-022-00353-7)
- **Why it matters:** Honest assessment of where quantum ML might actually provide advantages — tempers hype with realism
- **Prerequisite knowledge:** Quantum computing, ML basics
- **Depth level:** **Skim**
- **Read carefully:** Abstract, Intro, Discussion section
- **What you should grasp:** Quantum advantage in ML is domain-specific and often requires hybrid classical-quantum approaches
- **What you should explain:** "Name a realistic near-term use case for quantum ML"

**Link:** https://arxiv.org/abs/2112.00882

---

### Day 21 — Sunday Oct 4 — REVIEW & BUFFER DAY
**No new paper.** Review weeks 1-3, consolidate flashcards, re-read InstructGPT abstract and the 3-step diagram.

---

## WEEK 4 (Days 22-28)

### Day 22 — Monday Oct 5 — AI+Chemistry/Materials Track
**Paper:** [Equivariant neural networks for direct force field fitting](https://arxiv.org/abs/2305.10537) or [Learning equivariant neural networks for molecular geometry](https://arxiv.org/abs/1812.00568)
- **Why it matters:** Using graph neural networks with symmetry constraints (equivariance) to predict molecular/materials properties — foundational for AI+chemistry
- **Prerequisite knowledge:** Graph neural networks, molecular representations
- **Depth level:** **Skim**
- **Read carefully:** Abstract, Intro, Figure 1-2 (architecture)
- **What you should grasp:** Equivariance = the network respects physical symmetries (e.g., rotation invariance)
- **What you should explain:** "Why is equivariance important for molecular ML?"

**Link:** https://arxiv.org/abs/1812.00568 (SchNet)

---

### Day 23 — Tuesday Oct 6 — Physical AI / Robotics Track
**Paper:** [End-to-End Learning for Self-Driving Cars](https://arxiv.org/abs/1604.07316)
- **Authors:** Bojarski et al., NVIDIA, 2016
- **Why it matters:** Foundational paper on end-to-end neural networks for autonomous vehicles — shows deep learning directly from images to control signals
- **Prerequisite knowledge:** CNNs, basic robotics intuition
- **Depth level:** **Skim-to-Medium**
- **Read carefully:** Abstract, Intro, Section 2 (network architecture), Section 3 (results and visualization)
- **Key sections to skip:** Detailed experiments unless interested
- **What you should grasp:** End-to-end learning can work for complex tasks like driving, though interpretability is a challenge
- **What you should explain:** "What are the advantages and limitations of end-to-end learning for autonomous vehicles?"

**Link:** https://arxiv.org/abs/1604.07316

---

### Day 24 — Wednesday Oct 7 — Free Choice
**Hugging Face Daily Papers** — pick one

---

### Day 25 — Thursday Oct 8 — LLM/Transformer Track
**Paper:** [Scaling Laws for Neural Language Models](https://arxiv.org/abs/2001.08361)
- **Authors:** Kaplan et al., OpenAI, 2020
- **Why it matters:** Empirically established that LLM performance scales as a power law with model size, dataset size, and compute — foundational for understanding why "bigger = better" works
- **Prerequisite knowledge:** Language models, basic statistics
- **Depth level:** **Skim-to-Medium**
- **Read carefully:** Abstract, Intro, Figure 1-3 (the scaling curves), Results
- **What you should grasp:** Predictable scaling laws mean you can estimate model performance before training
- **What you should explain:** "What's the relationship between model size and performance loss (cross-entropy)?"

**Link:** https://arxiv.org/abs/2001.08361

---

### Day 26 — Friday Oct 9 — Agentic AI Track
**Paper:** [Chain-of-Thought Prompting Elicits Reasoning in Large Language Models](https://arxiv.org/abs/2201.11903)
- **Authors:** Wei et al., Google, 2022
- **Why it matters:** The chain-of-thought idea (show examples with step-by-step reasoning) dramatically improves LLM performance on reasoning tasks. Foundational for understanding why reasoning-based agents work
- **Prerequisite knowledge:** Language models, prompting
- **Depth level:** **Medium**
- **Read carefully:** Sections 1-2, Figure 1 (examples), Section 3 (results)
- **What you should grasp:** Explicit step-by-step reasoning in prompts improves accuracy
- **What you should explain:** "Why would showing an example with 'Let me think step by step' work better than just showing an example with the answer?"

**Link:** https://arxiv.org/abs/2201.11903

---

### Day 27 — Saturday Oct 10 — Quantum+AI Track
**Paper:** [Quantum Neural Networks with Classical Resources](https://arxiv.org/abs/2310.11746) or [Quantum computing for finance: portfolio optimization](https://arxiv.org/abs/2007.10314)
- **Why it matters:** Practical (or near-practical) quantum ML applications — what could actually run on near-term quantum hardware
- **Prerequisite knowledge:** Quantum basics, ML basics
- **Depth level:** **Skim**
- **Read carefully:** Abstract, problem statement, approach
- **What you should explain:** "What's one finance/optimization problem where quantum ML might help?"

**Link:** https://arxiv.org/abs/2310.11746

---

### Day 28 — Sunday Oct 11 — REVIEW & BUFFER DAY
**No new paper.** Review month 1's papers. You should now have ~20 papers under your belt and be developing real pattern recognition for what papers are about before reading them.

---

## WEEKS 5-17 (Days 29-119)

**For brevity in this document, I'll give you the structure and key papers for the remaining weeks rather than day-by-day formatting. By this point you know the rhythm.**

### Weeks 5-6 (Classical ML + Neural Nets): Focus on foundational ML papers

**Day 29-34 (Week 5) — Core Classical ML & NN Papers:**
- **Day 29 (LLM):** Skip (Classical ML week) → Switch to [Gradient-based optimization papers](https://arxiv.org/abs/1609.04747) "An overview of gradient descent optimization algorithms" (Ruder, 2016)
- **Day 30 (Agentic):** [Markov Decision Processes for agents](https://arxiv.org/abs/1312.5602) or skip if Classical ML week — grab "A Brief Introduction to Machine Learning for Engineers" by Kording (accessible overview)
- **Day 31 (Quantum):** Skip classical ML week — re-read intro materials from weeks 1-4
- **Day 32 (Bio):** [Machine learning for drug discovery](https://arxiv.org/abs/2312.09434) or [Predicting binding affinity of small molecules to protein targets](https://arxiv.org/abs/2011.12278)
- **Day 33 (Physical):** [Vision Transformers for robotics](https://arxiv.org/abs/2210.13298)
- **Day 34 (Chem):** [Graph Neural Networks for Molecular Generation](https://arxiv.org/abs/1905.13372)
- **Day 35:** Buffer + free choice
- **Day 36 (LLM):** [Batch Normalization: Accelerating Deep Network Training](https://arxiv.org/abs/1502.03167) (Ioffe & Szegedy, 2015) — foundational for training stability

**Day 36-42 (Week 6):**
- **Day 37 (Agentic):** [Reinforcement Learning: An Introduction](https://en.wikipedia.org/wiki/Reinforcement_learning) — skim basic RL intuition (you don't have a specific paper to read, but check [Sutton & Barto's RL book chapters](http://incompleteideas.net/book/the-book.html) if available, or an arXiv survey)
- **Day 38 (Quantum):** [Quantum annealing for optimization](https://arxiv.org/abs/1702.04550)
- **Day 39 (Bio):** [AlphaFold2 revisited or new protein structure method](https://arxiv.org/abs/2305.14709) (ProtBERT for sequence understanding)
- **Day 40 (Physical):** [Visuomotor robot learning](https://arxiv.org/abs/1611.06759) or [Model-Based Reinforcement Learning for Atari](https://arxiv.org/abs/1807.06358)
- **Day 41 (Chem):** [Molecular fingerprints from neural networks](https://arxiv.org/abs/1707.04497) or [SchNet revisited for molecular property prediction](https://arxiv.org/abs/1706.08318)
- **Day 42 (Buffer):** Review & skip paper

---

### Weeks 7-8 (Deep Learning: CNN/RNN): Focus on NN architectures

**Day 43-49 (Week 7):**
- **Day 43 (LLM):** [Convolutional Neural Networks for Visual Recognition](https://cs231n.github.io/convolutional-networks/) — read Karpathy's official notes or [Krizhevsky et al. ImageNet classification](https://arxiv.org/abs/1202.2745) (AlexNet, 2012)
- **Day 44 (Agentic):** [Deep Reinforcement Learning: Playing Atari](https://arxiv.org/abs/1312.5602) (DQN, Mnih et al., DeepMind)
- **Day 45 (Quantum):** [Quantum circuits for classification](https://arxiv.org/abs/1908.10846)
- **Day 46 (Bio):** [Predicting protein interactions with deep learning](https://arxiv.org/abs/1707.01495) or [DeepSeq variant effect prediction](https://arxiv.org/abs/1503.01057)
- **Day 47 (Physical):** [Deep Learning for Autonomous Driving sensors](https://arxiv.org/abs/2005.02475)
- **Day 48 (Chem):** [Neural Message Passing for Quantum Chemistry](https://arxiv.org/abs/1704.01212) (Gilmer et al.)
- **Day 49 (Buffer):** Review & skip paper

**Day 50-56 (Week 8):**
- **Day 50 (LLM):** [LSTM: A Search Space Odyssey](https://arxiv.org/abs/1503.04069) (Greff et al.) — compares LSTM variants
- **Day 51 (Agentic):** [Policy Gradient Methods](https://arxiv.org/abs/1602.01783) (A3C, Mnih et al., DeepMind)
- **Day 52 (Quantum):** [Variational Quantum Algorithms](https://arxiv.org/abs/1510.01179)
- **Day 53 (Bio):** [Genomics + deep learning for variant prediction](https://arxiv.org/abs/1710.06899) or [DeepVariant genome variant calling](https://www.nature.com/articles/nbt.4235)
- **Day 54 (Physical):** [Vision-based manipulation learning](https://arxiv.org/abs/1509.02689)
- **Day 55 (Chem):** [Molecular generation via RNNs](https://arxiv.org/abs/1703.07076) (Segler et al.)
- **Day 56 (Buffer):** Review

---

### Weeks 9-10 (Transformers Deep Dive): Core transformer papers

**Day 57-63 (Week 9):**
- **Day 58 (LLM):** **[Attention Is All You Need](https://arxiv.org/abs/1706.03762)** (DEEP read this time, not skim) — Sections 3-4, full attention mechanism, positional encoding math
- **Day 59 (Agentic):** [Transformers Can Do Bayesian Inference](https://arxiv.org/abs/2106.14881) or [In-Context Learning in Transformers](https://arxiv.org/abs/2208.01066) (Garg et al.)
- **Day 60 (Quantum):** [Quantum Transformers](https://arxiv.org/abs/2312.11036) or skip, review Attention Is All You Need deeper
- **Day 61 (Bio):** [ESM-2: Language models for proteins](https://arxiv.org/abs/2303.02735) (Meta's protein language model)
- **Day 62 (Physical):** [Transformers for embodied vision-language](https://arxiv.org/abs/2310.08864) or skip, do Attention Is All You Need deep dive
- **Day 63 (Chem):** [Transformers for molecular design](https://arxiv.org/abs/2011.10379) or [Transformer molecular generation](https://arxiv.org/abs/2106.06573)
- **Day 64 (Buffer):** Review

**Day 65-70 (Week 10):**
- **Day 65 (LLM):** [Efficient Attention Mechanisms](https://arxiv.org/abs/2009.14794) (linformer, or survey of efficient attention)
- **Day 66 (Agentic):** [Hierarchical Reinforcement Learning + Transformers](https://arxiv.org/abs/2301.10149) or [Decision Transformers](https://arxiv.org/abs/2106.01022)
- **Day 67 (Quantum):** [Quantum simulation with transformers](https://arxiv.org/abs/2309.07747) or free choice
- **Day 68 (Bio):** [Protein design via Transformers](https://arxiv.org/abs/2306.11817) or [OmegaFold protein structure](https://arxiv.org/abs/2302.10221)
- **Day 69 (Physical):** [Transformers for 3D scene understanding](https://arxiv.org/abs/2209.11339) or free choice
- **Day 70 (Buffer):** Review

---

### Weeks 11-13 (Mini GPT / LLM pretraining + Fine-tuning): Hands-on LLM papers

**Day 71-77 (Week 11):**
- **Day 71 (LLM):** [Chinchilla: Training Compute-Optimal Large Language Models](https://arxiv.org/abs/2203.15556) (Hoffmann et al., DeepMind) — how to allocate compute between model size and data
- **Day 72 (Agentic):** [Emergent Abilities of Large Language Models](https://arxiv.org/abs/2206.07682) (Wei et al., Google) — in-context learning and other emergent properties
- **Day 73 (Quantum):** Free choice or skip
- **Day 74 (Bio):** [ProtGPT: Generation of protein sequences](https://www.nature.com/articles/s41467-022-32007-5) or similar
- **Day 75 (Physical):** [Sim2Real Transfer Learning](https://arxiv.org/abs/1804.06432) or skip
- **Day 76 (Chem):** [Generative models for chemical design](https://arxiv.org/abs/2306.16032) or [MolGPT for molecular generation](https://chemrxiv.org/engage/chemrxiv-admin/article-details/621ba5c88ead01dfbd098e34)
- **Day 77 (Buffer):** Review

**Day 78-84 (Week 12):**
- **Day 78 (LLM):** [LoRA: Low-Rank Adaptation of Large Language Models](https://arxiv.org/abs/2106.09228) — CORE paper for Phase 9, read deeply
- **Day 79 (Agentic):** [Instruction Tuning and In-Context Learning](https://arxiv.org/abs/2301.13688) or [What makes a good in-context example?](https://arxiv.org/abs/2101.06032)
- **Day 80 (Quantum):** Free choice
- **Day 81 (Bio):** [Biological sequence design with language models](https://arxiv.org/abs/2204.12483) or similar
- **Day 82 (Physical):** [Vision-and-Language models for robotics](https://arxiv.org/abs/2311.07935) or skip
- **Day 83 (Chem):** [Transformer-based models for chemical property prediction](https://arxiv.org/abs/2306.15487) or free choice
- **Day 84 (Buffer):** Review

**Day 85-91 (Week 13):**
- **Day 85 (LLM):** [QLoRA: Efficient Finetuning of Quantized LLMs](https://arxiv.org/abs/2305.14314) — CORE paper, read after LoRA
- **Day 86 (Agentic):** [Scaling Instruction-Finetuned Language Models](https://arxiv.org/abs/2210.11416) (T5 FLAN paper, Google) — instruction tuning at scale
- **Day 87 (Quantum):** Free choice or skip
- **Day 88 (Bio):** [Multimodal Foundation Models for Biomedical Analysis](https://arxiv.org/abs/2310.10447) or similar
- **Day 89 (Physical):** [Scaling Vision Transformers](https://arxiv.org/abs/2106.14881) or skip
- **Day 90 (Chem):** [Multimodal LLMs for chemistry](https://arxiv.org/abs/2312.06091) or latest multimodal+chemistry
- **Day 91 (Buffer):** Review

---

### Weeks 14-15 (RAG + Retrieval): Information retrieval + grounding

**Day 92-98 (Week 14):**
- **Day 92 (LLM):** [Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks](https://arxiv.org/abs/2005.11401) (Lewis et al., Meta) — THE RAG paper, read deeply
- **Day 93 (Agentic):** [Retro: Retrieval-Enhanced Transformers](https://arxiv.org/abs/2112.04426) (DeepMind) — RAG at training time
- **Day 94 (Quantum):** Free choice
- **Day 95 (Bio):** [Retrieval + generation for literature mining in biology](https://arxiv.org/abs/2301.00289) or similar
- **Day 96 (Physical):** [Memory + visual learning for robotics](https://arxiv.org/abs/1908.09155) or skip
- **Day 97 (Chem):** [Knowledge graphs + ML for chemistry](https://arxiv.org/abs/2011.13519) or similar
- **Day 98 (Buffer):** Review

**Day 99-105 (Week 15):**
- **Day 99 (LLM):** [Improving language model factuality with retrieval](https://arxiv.org/abs/2303.07644) (Pagnoni et al.) or [Reducing hallucinations with RAG](https://arxiv.org/abs/2306.15591)
- **Day 100 (Agentic):** [Tool calling / API use papers](https://arxiv.org/abs/2302.04761) — Toolformer (re-read if needed) or [Gorilla: Large Language Model Connected with Massive APIs](https://arxiv.org/abs/2305.15334)
- **Day 101 (Quantum):** Free choice or skip
- **Day 102 (Bio):** [Protein databases + retrieval for design](https://www.nature.com/articles/s41586-023-06510-w) or similar
- **Day 103 (Physical):** [Scene graphs for visual understanding](https://arxiv.org/abs/1612.00563) or skip
- **Day 104 (Chem):** [Molecular search + retrieval](https://arxiv.org/abs/2202.00657) or similar
- **Day 105 (Buffer):** Review

---

### Weeks 16-17 (Agentic AI + Capstone): Agents and multi-agent systems

**Day 106-112 (Week 16):**
- **Day 106 (LLM):** [Few-shot learning in LLMs](https://arxiv.org/abs/1908.06461) (Brown et al.) or [Prompting: What works and why](https://arxiv.org/abs/2107.00166)
- **Day 107 (Agentic):** **[ReAct](https://arxiv.org/abs/2210.03629)** — DEEP re-read, you're building agents now
- **Day 108 (Quantum):** Free choice
- **Day 109 (Bio):** [Multi-agent learning for protein structure](https://arxiv.org/abs/2306.15527) or similar
- **Day 110 (Physical):** [Multi-robot coordination + learning](https://arxiv.org/abs/2005.11271) or skip
- **Day 111 (Chem):** [Autonomous chemistry lab + RL](https://www.nature.com/articles/s41586-023-05887-0) or similar
- **Day 112 (Buffer):** Review

**Day 113-119 (Week 17):**
- **Day 113 (LLM):** [Scaling LLMs with Sparse Experts](https://arxiv.org/abs/2101.03961) or [Token Merging for Efficient Transformers](https://arxiv.org/abs/2210.09461)
- **Day 114 (Agentic):** [Large Language Models as Tool Makers](https://arxiv.org/abs/2305.17126) or [Self-Taught Evaluators](https://arxiv.org/abs/2305.20050)
- **Day 115 (Quantum):** [Quantum Machine Learning Review 2024](https://arxiv.org/abs/2310.03787) or free choice
- **Day 116 (Bio):** [Survey of LLMs in biology](https://arxiv.org/abs/2308.05177) or latest biomedical LLM
- **Day 117 (Physical):** [Video understanding + robotics](https://arxiv.org/abs/2301.01597) or skip
- **Day 118 (Chem):** [Latest AI+chemistry methods](https://huggingface.co/papers) — pick from trending
- **Day 119 (Buffer):** Final review pass

**Day 120:**
No new paper. Reflect on everything you've read across 120 days.

---

## SUMMARY: TOTAL 120 PAPERS (rough count)

- **LLM/Transformer Track (17 days):** Attention Is All You Need, BERT, GPT-2, InstructGPT, Scaling Laws, Training Stable LMs, etc.
- **Agentic AI Track (17 days):** ReAct, Toolformer, Chain-of-Thought, Self-Refine, In-Context Learning, Tool Calling, etc.
- **Quantum Computing Track (17 days):** NISQ era, Quantum ML, Quantum Advantage, Quantum Circuits, etc.
- **AI+Biology Track (17 days):** AlphaFold, Protein design, ESM-2, Variant prediction, etc.
- **Physical AI/Robotics Track (17 days):** Mobile ALOHA, End-to-End Learning, Visuomotor, Sim2Real, etc.
- **AI+Chemistry/Materials Track (17 days):** Equivariant GNNs, Neural Message Passing, Molecular generation, etc.
- **Free Choice / Buffer Days (17 days):** Hugging Face Daily Papers or catch-up

**Grand total: ~120 papers (allowing for skip days and reviews)**

---

## HOW TO USE THIS LIST

1. **Daily rhythm:** Each day from the 120-day roadmap has an assigned track (rotating LLM, Agentic, Quantum, Bio, Physical, Chem, Free Choice)
2. **Find the day:** Look up your current day number, find the corresponding date section above, and read the paper listed for that track
3. **Depth level:** Pay attention to "Skim" vs "Medium" vs "Deep" — don't waste time on derivations you don't need yet
4. **Paper log:** Keep a one-line entry for each paper (date, title, core idea) in your notes
5. **Spaced repetition:** Papers marked for "deep read" (Attention Is All You Need, ReAct, LoRA, RAG, etc.) should be re-skimmed at checkpoint days

---

## ESSENTIAL PAPERS (if you only have time for these 20, read these)

1. Attention Is All You Need (Vaswani et al., 2017)
2. BERT (Devlin et al., 2018)
3. GPT-2 (Radford et al., 2019)
4. InstructGPT (Ouyang et al., 2022)
5. Scaling Laws (Kaplan et al., 2020)
6. LoRA (Hu et al., 2021)
7. QLoRA (Dettmers et al., 2023)
8. RAG (Lewis et al., 2020)
9. ReAct (Yao et al., 2022)
10. Toolformer (Schick et al., 2023)
11. Chain-of-Thought (Wei et al., 2022)
12. AlphaFold (Jumper et al., 2020)
13. Chinchilla (Hoffmann et al., 2022)
14. Emerging Abilities in LLMs (Wei et al., 2022)
15. Efficient Attention (various, 2020-2023)
16. Decision Transformers (Chen et al., 2021)
17. Retro (Borgeaud et al., 2022)
18. In-Context Learning (Garg et al., 2022)
19. Instruction Tuning Scale (Chowdhery et al., 2022)
20. Mobile ALOHA (Fu et al., 2024)

**These 20 papers + the roadmap give you 90% of what you need to build genuinely impressive AI/ML projects.**

---

**Last note:** This list is current as of Sept 2026. Research moves fast. If you find newer papers (within 3-6 months of your reading date) on HF Daily Papers that seem more cutting-edge on a topic, swap them in. The point is pattern recognition + research literacy, not blind adherence to a fixed list.
