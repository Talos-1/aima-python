# PhD Prep Reading Schedule

## Week 1 (26 Oct – 1 Nov): agents, uncertainty and incident response

Foundations, set-up and a first look at real SOC data.

- **Mon 26 Oct**
  - [x] Read: AIMA 2.1 *Agents and Environments*, 2.2 *Good Behavior: The Concept of Rationality* (pp. 54–60)
  - [x] Do: set up a Python environment; clone aima-python and aima-data; run the `agents` notebook
- **Tue 27 Oct**
  - [ ] Read: AIMA 2.3 *The Nature of Environments*, 2.4 *The Structure of Agents*, Summary (pp. 60–78)
  - [ ] Do: aima-exercises, *Intelligent Agents*: a PEAS description for a SOC triage agent (2.3); then use the aima-python agent classes to sketch a simple reflex agent and a model-based agent for alert triage (2.4)
- **Wed 28 Oct**
  - [ ] Read: AIMA 12.1 *Acting under Uncertainty* to 12.4 *Independence* (pp. 403–417)
  - [ ] Do: first part of the `probability` notebook (distributions, joint probability); two aima-exercises from *Quantifying Uncertainty* on full joint distributions and independence (12.3–12.4)
- **Thu 29 Oct**
  - [ ] Read: AIMA 12.5 *Bayes' Rule and Its Use* to 12.7, Summary (pp. 417–426); MAS Appendix A *Probability Theory* (A.1–A.4) as a refresher
  - [ ] Do: two Bayes' rule exercises (12.5); write a short script showing how P(true positive | alert) changes with the base rate, the classic alert-fatigue problem
- **Fri 30 Oct**
  - [ ] Read: NIST SP 800-61 Rev. 3, *Incident Response Recommendations and Considerations for Cybersecurity Risk Management* (whole)
  - [ ] Do: download GUIDE from Kaggle and explore it in pandas: the share of TP/BP/FP grades, alerts per incident, the most common detectors and MITRE techniques. Save it as a notebook in a new repo
- **Sat 31 Oct**
  - [ ] Read: Freitas et al. (2024), "AI-Driven Guided Response for Security Operation Centers with Microsoft Copilot for Security" (the GUIDE paper, arXiv 2407.09017)
  - [ ] Do: half a page of notes mapping NIST's incident response activities to the fields in GUIDE; catch up on anything missed
- **Sun 1 Nov** — Rest

## Week 2 (2 – 8 Nov): Bayesian networks, causality and decisions

The most important week. Bayesian and causal reasoning are named directly in the project.

- **Mon 2 Nov**
  - [ ] Read: AIMA 13.1 *Representing Knowledge in an Uncertain Domain*, 13.2 *The Semantics of Bayesian Networks* (pp. 430–445)
  - [ ] Do: in the `probability` notebook, build the burglary network and query it with `enumeration_ask`; aima-exercises, *Probabilistic Reasoning*: one exercise on building a network and counting its parameters (13.2)
- **Tue 3 Nov**
  - [ ] Read: AIMA 13.3 *Exact Inference in Bayesian Networks* (pp. 445–453)
  - [ ] Do: implement variable elimination yourself from the 13.3 pseudocode and test it against `elimination_ask`; one exact-inference exercise
- **Wed 4 Nov**
  - [ ] Read: AIMA 13.4 *Approximate Inference for Bayesian Networks* (pp. 453–467)
  - [ ] Do: run the notebook's sampling methods (e.g. likelihood weighting, Gibbs sampling) on the burglary network and plot how their estimates converge to the exact answer
- **Thu 5 Nov**
  - [ ] Read: AIMA 13.5 *Causal Networks*, Summary (pp. 467–472); Pearl, Glymour & Jewell, *Primer*, Ch 1–2
  - [ ] Do: pgmpy: build a Bayesian network on GUIDE that outputs P(true positive | alert category, MITRE tactic, number of alerts, detector), queried with variable elimination
- **Fri 6 Nov**
  - [ ] Read: AIMA 15.1 to 15.4 *Multiattribute Utility Functions* (pp. 518–534); Pearl *Primer* Ch 3 *The Effects of Interventions*
  - [ ] Do: DoWhy's four steps (model, identify, estimate, refute) to test whether one GUIDE feature *causes* a TP grade or only correlates with it, e.g. because of the organisation
- **Sat 7 Nov**
  - [ ] Read: AIMA 15.5 *Decision Networks*, 15.6 *The Value of Information*, 15.7 *Unknown Preferences*, Summary (pp. 534–547)
  - [ ] Do: add an escalate-or-close decision on top of your network, with utilities for a missed true positive vs. wasted analyst time; check calibration with `calibration_curve` and the Brier score; write the README
- **Sun 8 Nov** — Rest

## Week 3 (9 – 15 Nov): logic, rule-based agents and multi-agent decisions

Rule-based reasoning becomes your first triage agent; then how several agents decide together.

- **Mon 9 Nov**
  - [ ] Read: AIMA 7.1 *Knowledge-Based Agents* to 7.4 *Propositional Logic: A Very Simple Logic* (pp. 227–240)
  - [ ] Do: the propositional parts of the `logic` notebook; aima-exercises, *Logical Agents*: one exercise on converting rules to Horn clauses
- **Tue 10 Nov**
  - [ ] Read: AIMA 7.5 *Propositional Theorem Proving* (pp. 240–250); *skim* 7.7 *Agents Based on Propositional Logic*
  - [ ] Do: run `pl_fc_entails`; then write your own forward-chaining engine (\~100 lines) following 7.5, with tests
- **Wed 11 Nov**
  - [ ] Read: AIMA 8.1 *Representation Revisited* to 8.3 *Using First-Order Logic* (pp. 269–289); 9.3 *Forward Chaining*, 9.4 *Backward Chaining* (pp. 304–316)
  - [ ] Do: run `fol_fc_ask` and `fol_bc_ask`; encode 10–15 triage rules over GUIDE alert features (e.g. combinations of MITRE techniques and categories) that output TP, BP or FP. This is **Agent 1**; score it against the analysts' grades
- **Thu 12 Nov**
  - [ ] Read: AIMA 10.6 *Reasoning with Default Information* (pp. 351–355); 17.1 *Properties of Multiagent Environments* and the first half of 17.2 *Non-Cooperative Game Theory* (pp. 589–605)
  - [ ] Do: add default and exception rules to Agent 1 (e.g. "admin tooling is benign unless it touches a sensitive host"); optionally re-express the rules in clingo
- **Fri 13 Nov**
  - [ ] Read: AIMA rest of 17.2 (pp. 605–616), 17.3 *Cooperative Game Theory* (pp. 616–622)
  - [ ] Do: Nashpy: model a simple attacker–defender game (attack vs. wait, monitor vs. don't) as a normal-form game, find its Nash equilibria with support enumeration, and see how they shift as you change the payoffs
- **Sat 14 Nov**
  - [ ] Read: AIMA 17.4 *Making Collective Decisions*, Summary (pp. 622–636)
  - [ ] Do: write the voting rules from 17.4 (plurality, Borda and one other) as reusable Python functions for Week 4; catch up
- **Sun 15 Nov** — Rest

**Deep learning track: PyTorch basics**

- [ ] Mon–Tue: AIMA 22.1 *Simple Feedforward Networks*, 22.2 *Computation Graphs for Deep Learning* (pp. 802–811); PyTorch *Learn the Basics*: Tensors, Datasets & DataLoaders, Transforms
- [ ] Wed–Thu: PyTorch *Learn the Basics*: Build the Neural Network, Automatic Differentiation, Optimization Loop, Save & Load Model
- [ ] Fri–Sat: write a GUIDE `Dataset` and `DataLoader` for incident-level features, ready for Week 4; train a tiny model end to end to check the pipeline works

## Week 4 (16 – 22 Nov): Multiagent Systems and more agents

Deeper theory from Shoham & Leyton-Brown (focus on intuition, *skim* proofs) while you build Agents 2 and 3.

- **Mon 16 Nov**
  - [ ] Read: MAS 3.1 *Self-interested agents*, 3.2 *Games in normal form*; Wooldridge, *An Introduction to MultiAgent Systems*, chapter *Practical Reasoning Agents* (BDI)
  - [ ] Do: train a gradient-boosted classifier on incident-level GUIDE features (aggregate alerts per incident); use SHAP to see what drives it. This is **Agent 2**
- **Tue 17 Nov**
  - [ ] Read: MAS 3.3.1 *Pareto optimality* to 3.3.3 *Finding Nash equilibria* (skip the 3.3.4 proof); MAS 6.3.1–6.3.2 on Bayesian games (defending when you're unsure of the attacker's type)
  - [ ] Do: build an LLM agent with LangGraph that reads an incident summary (alert titles, categories, MITRE techniques) and returns a grade, a confidence and its reasoning. Run it on a few hundred incidents to keep costs down. This is **Agent 3**
- **Wed 18 Nov**
  - [ ] Read: MAS 3.4.1 *Maxmin and minmax strategies* to 3.4.3 *Removal of dominated strategies* (*skim* 3.4.4–3.4.7); MAS 2.3.1 *From contract nets to auction-like optimization* (how agents split up tasks)
  - [ ] Do: run all three agents on a shared test set; measure pairwise Cohen's kappa and Fleiss' kappa, broken down by alert category and against the analysts' grades
- **Thu 19 Nov**
  - [ ] Read: MAS 9.1 *Introduction*, 9.2 *A formal model*, 9.3 *Voting* (9.3.1 *Voting methods*, 9.3.2 *Voting paradoxes*)
  - [ ] Do: reconcile the three agents with your plurality and Borda functions; look for a voting paradox in the results
- **Fri 20 Nov**
  - [ ] Read: MAS 9.4 *Existence of social functions* (9.4.1 Arrow, 9.4.2 Muller–Satterthwaite; know what they rule out); *skim* 9.5; Wooldridge, chapter *Making Group Decisions*
  - [ ] Do: compare the voted verdicts with each single agent and with the analysts; write up the results so far
- **Sat 21 Nov**
  - [ ] Read: MAS 13.1 *The partition model of knowledge*, 13.4 *Common knowledge…*, 13.6 *From knowledge to belief*, 13.7 *Combining knowledge and belief*; *skim* 13.2–13.3
  - [ ] Do: document Agents 1–3 in the project README; catch up
- **Sun 22 Nov** — Rest

**Deep learning track: neural and graph-based Agent 2**

- [ ] Mon–Tue: AIMA 22.3–22.5 (*Convolutional Networks*, *Learning Algorithms*, *Generalization*, pp. 811–823); d2l.ai, chapter *Multilayer Perceptrons*. Train a PyTorch MLP version of Agent 2 and compare it with the gradient-boosted one
- [ ] Wed–Thu: d2l.ai, chapter *Builders' Guide* (custom layers, parameters, saving); PyTorch Geometric *Introduction by Example*. Turn GUIDE incidents into graphs (alerts and entities as nodes, shared entities as edges) with networkx, then convert them to PyG
- [ ] Fri–Sat: train a graph neural network that classifies whole incidents (graph classification) and compare it with the MLP and gradient-boosted versions; keep the best as Agent 2. Optional: AIMA 25.4 *The Transformer Architecture* (pp. 919–922), to understand what's inside your LLM agent

## Week 5 (23 – 29 Nov): belief change, trust and counterfactuals

How agents merge conflicting beliefs, how humans trust automation, and how to explain what would have changed a decision. The project comes together this week.

- **Mon 23 Nov**
  - [ ] Read: MAS 14.2 *Dynamics of knowledge and belief* (14.2.1 *Belief revision*, 14.2.2 *Beyond AGM: update, arbitration, fusion, and friends*, 14.2.3). Read 14.2.2 closely
  - [ ] Do: calibrate each agent: `CalibratedClassifierCV` for Agent 2, and a reliability table (stated confidence vs. actual accuracy) for Agents 1 and 3
- **Tue 24 Nov**
  - [ ] Read: MAS 14.4 *Towards a logic of "intention"* (14.4.1–14.4.3); *skim* 14.1; Wooldridge, chapter *Arguing*
  - [ ] Do: Bayesian combination (AIMA 13.2): in pgmpy, make the true grade a parent node and each agent's verdict a child, so the learned CPTs encode each agent's reliability; query P(grade | all three verdicts)
- **Wed 25 Nov**
  - [ ] Read: Parasuraman & Riley (1997), "Humans and Automation: Use, Misuse, Disuse, Abuse", *Human Factors*
  - [ ] Do: implement Dempster–Shafer combination (\~50 lines) as a belief-fusion method (MAS 14.2.2); compare it with voting and the Bayesian method on high-conflict incidents
- **Thu 26 Nov**
  - [ ] Read: Lee & See (2004), "Trust in Automation: Designing for Appropriate Reliance", *Human Factors*
  - [ ] Do: human–AI conflict analysis: find incidents where the agents agree but the analyst disagrees, and vice versa; use networkx to look at the entity graphs of a few
- **Fri 27 Nov**
  - [ ] Read: Pearl, Glymour & Jewell, *Primer*, Ch 4 *Counterfactuals and Their Applications*
  - [ ] Do: DiCE: generate counterfactual explanations for Agent 2's decisions ("this incident would have been graded benign if…")
- **Sat 28 Nov**
  - [ ] Read: Molnar, *Interpretable Machine Learning* (free online), chapter *Counterfactual Explanations*; *skim* its SHAP chapter
  - [ ] Do: write the project README: the problem, the three agents, the reconciliation methods, agreement with analysts, results and limitations. This is your interview piece
- **Sun 29 Nov** — Rest

**Deep learning track: uncertainty in neural agents**

- [ ] Mon–Tue: read Gal & Ghahramani (2016), "Dropout as a Bayesian Approximation"; add MC dropout to the neural Agent 2 so each verdict comes with an uncertainty estimate
- [ ] Wed–Thu: read Lakshminarayanan et al. (2017), "Simple and Scalable Predictive Uncertainty Estimation using Deep Ensembles"; train a small ensemble and compare its uncertainty and calibration with MC dropout
- [ ] Fri–Sat: feed Agent 2's uncertainty into the Bayesian and Dempster–Shafer reconciliation, and check whether high-uncertainty incidents are where the agents and analysts disagree most

## Week 6 (30 Nov – 6 Dec): human–AI teaming, systems and review

The most on-topic reading, the systems side of the project (distributed and self-adaptive systems), CybORG, and turning it all into interview material.

- **Mon 30 Nov**
  - [ ] Read: National Academies, *Human-AI Teaming: State-of-the-Art and Research Needs* (2022, free online): summary, plus the chapters on situation awareness and on transparency and explainability
  - [ ] Do: install CybORG with the CAGE Challenge 4 scenario (or CybORG++ MiniCAGE for faster runs) and run the baseline defender agents
- **Tue 1 Dec**
  - [ ] Read: *Human-AI Teaming* report: the chapters on trust and on reducing human and AI bias
  - [ ] Do: log the steps where CybORG's defending agents choose conflicting actions
- **Wed 2 Dec**
  - [ ] Read: van Steen & Tanenbaum, *Distributed Systems* (free PDF), chapters *Coordination* and *Fault Tolerance*, focusing on consensus and Byzantine failures
  - [ ] Do: plug one of your Week 5 reconciliation methods into the CybORG defenders' action choices and compare outcomes with the baseline
- **Thu 3 Dec**
  - [ ] Read: Weyns, *An Introduction to Self-Adaptive Systems*, the early chapters on core principles and MAPE-K; Kephart & Chess (2003), "The Vision of Autonomic Computing"
  - [ ] Do: draw your disagreeing-agents system as a MAPE-K loop (monitor, analyse, plan, execute, shared knowledge) and add the diagram to the README
- **Fri 4 Dec**
  - [ ] Read: AIMA 28.3 *The Ethics of AI* (pp. 1037–1056), *skimming* for trust, transparency and safety; two or three recent papers by Professor Kanhere
  - [ ] Do: draft a one-page note with three research ideas, each pairing a method (Bayesian, voting, belief fusion, argumentation, counterfactual) with a human–AI conflict in incident response, using your project results as evidence
- **Sat 5 Dec**
  - [ ] Read: review AIMA 13.2, 13.5 and 17.4, and MAS 9.3 and 14.2.2
  - [ ] Do: tighten the note so you can talk through it in two minutes; tidy and pin your repos on GitHub and link them from your CV
- **Sun 6 Dec** — Rest

**Deep learning track: reinforcement-learning defender**

- [ ] Mon–Tue: AIMA 23.1 *Learning from Rewards* to 23.3 *Active Reinforcement Learning* (pp. 840–854)
- [ ] Wed–Thu: AIMA 23.5 *Policy Search* (pp. 861–863), the idea behind PPO; Stable-Baselines3's getting-started guide. Train a PPO defender on CybORG++ MiniCAGE
- [ ] Fri–Sat: compare your trained defender with the baseline agents, and log where it disagrees with them. Add the results to your CybORG repo

If you have time afterwards: repeat one agent on the LANL multi-source dataset, giving each agent a different log source (auth, process, DNS or flows) to study disagreement caused by different evidence; and read MAS Ch 8 *Communication* and Ch 12 (the Shapley value, useful for attributing credit across agents).
