# Mock iPhD Candidate Assessment

Oct 26, 2026 · @Alex

A mock assessment for the UNSW–CSIRO Industry PhD in collaborative cyber defence, written as the supervisory panel would set it to vet candidates. It has two components: a 155-mark written exam (multiple choice, fill in the blanks, short and extended response, code reading, programming and debugging) and a 60-minute panel interview, which is in its own tab.

## Instructions

You are a shortlisted candidate. The panel wants to see how you think, not just whether you know the answer, so show your working and state your assumptions. Answers and marking criteria are in the separate **Marking guide** tab; attempt each part before opening it.

| Paper | Part | Question types | Time | Marks |
| --- | --- | --- | --- | --- |
| 1. Handwritten | M. Multiple choice | 25 multiple-choice questions | 25 min | 25 |
| 1. Handwritten | Q. Fill in the blanks | 15 short completions | 15 min | 15 |
| 1. Handwritten | A. Theory | Calculations, short and extended response | 90 min | 40 |
| 1. Handwritten | C. Applied cyber security | Scenario, short and extended response | 25 min | 10 |
| 1. Handwritten | D. Research skills | Extended response, critique | 45 min | 15 |
| 1. Handwritten | R. Code reading | Trace output by hand, explain | 20 min | 10 |
| 2. In code | B. Programming | Implement, test, analyse | 6 hrs over a week | 30 |
| 2. In code | F. Debugging | Find and fix bugs, add tests | 2 hrs | 10 |
|  | **Exam total** |  |  | **155** |
| Panel interview | See the *Panel interview* tab | Presentation, technical, research, behavioural | 60 min | 30 |

**Difficulty key:** ★ foundational (any strong master's graduate) · ★★ intermediate (expected of a PhD candidate) · ★★★ advanced (distinguishes the top candidate).

**Bonus questions** (marked **Extension**) are optional and scored separately, up to 15 bonus marks in total. They can lift a borderline result but can't replace core marks.

**When to sit it:** Parts A and C after Week 3 of your reading plan as a checkpoint, then the full assessment after Week 6.

**Sittings:** Paper 1 takes about 3 hours 40 minutes, so sit it in two blocks with a short break: Parts M, Q and A (130 min), then Parts C, D and R (90 min). Do Paper 2 over the following week, and the panel interview last.

**Printing:** export the doc as a PDF and print the **Written exam** and **Answer booklet** tabs only. Never print the Marking guide or read it beforehand. Answer Paper 1 by hand in the booklet under timed conditions. Do Paper 2 in code. For the panel interview, have someone use the *Panel interview* tab to question you, or record yourself.

## Paper 1 — Handwritten, closed book

Parts M, Q, A, C, D and R. Answer in the Answer booklet. Calculator allowed; no notes or devices.

## Part M — Multiple choice (25 marks, 25 min)

One mark each; choose the single best answer. No negative marking.

1. **MC1** ★ In a Bayesian network, each node is conditionally independent of its non-descendants given: (a) its children (b) its parents (c) its children's other parents (d) all other nodes
2. **MC2** ★ Which structure produces "explaining away"? (a) a chain A → B → C with B observed (b) a fork A ← B → C with B observed (c) a collider A → B ← C with B observed (d) none of these
3. **MC3** ★★ The worst-case cost of variable elimination is exponential in: (a) the size of the largest intermediate factor (b) the number of evidence variables (c) the number of query variables (d) the number of entries in the original CPTs
4. **MC4** ★ Likelihood weighting: (a) rejects samples that contradict the evidence (b) samples the evidence from its prior (c) is an exact method (d) fixes the evidence variables and weights each sample by the evidence likelihood
5. **MC5** ★★ P(Y | do(X)) equals P(Y | X) when: (a) X and Y are correlated (b) Y causes X (c) there are no open back-door paths from X to Y (d) X is binary
6. **MC6** ★ A Horn clause has: (a) at most one positive literal (b) exactly two literals (c) no negative literals (d) at least two positive literals
7. **MC7** ★ Forward chaining is best described as: (a) goal-driven (b) data-driven (c) only usable in first-order logic (d) incomplete for Horn clauses
8. **MC8** ★ A Nash equilibrium is a strategy profile in which: (a) total payoff is maximised (b) every player gets their best possible outcome (c) all strategies are pure (d) no player gains by deviating alone
9. **MC9** ★★ Nash's theorem guarantees that every finite game has: (a) a pure-strategy equilibrium (b) a unique equilibrium (c) at least one equilibrium, possibly mixed (d) a Pareto-optimal equilibrium
10. **MC10** ★★ In two-player zero-sum games, the minimax theorem states that: (a) the maxmin and minmax values are equal in mixed strategies (b) a pure equilibrium always exists (c) players should cooperate (d) the Pareto-optimal outcome is unique
11. **MC11** ★★ Arrow's impossibility theorem applies to ranked voting with: (a) exactly two alternatives (b) three or more alternatives (c) cardinal utilities only (d) plurality voting only
12. **MC12** ★ With three options, the Borda count awards (first, second, third): (a) 1, 1, 0 (b) 3, 2, 0 (c) 1, 0, 0 (d) 2, 1, 0
13. **MC13** ★★ In Dempster–Shafer theory, mass on the whole frame m(Θ) represents: (a) belief in the empty set (b) the conflict between sources (c) belief that is uncommitted, i.e. ignorance (d) the probability of the most likely hypothesis
14. **MC14** ★★ For any set A, belief Bel(A) and plausibility Pl(A) satisfy: (a) Bel(A) ≤ Pl(A) (b) Bel(A) ≥ Pl(A) (c) Bel(A) + Pl(A) = 1 (d) no fixed relationship
15. **MC15** ★ Automation bias is: (a) refusing to use automation (b) bias in a model's training data (c) a model favouring certain classes (d) over-relying on automated advice, even when it's wrong
16. **MC16** ★★ A Cohen's kappa of 0 between two triage agents means: (a) they always disagree (b) they agree no more than chance would predict (c) they always agree (d) kappa is undefined
17. **MC17** ★★ A well-calibrated classifier is one where: (a) accuracy is maximised (b) outputs are always 0 or 1 (c) of predictions made with 80% confidence, about 80% are correct (d) training loss is zero
18. **MC18** ★★ MC dropout estimates uncertainty by: (a) disabling dropout at test time (b) retraining the model several times (c) using a batch size of 1 (d) keeping dropout on and averaging many forward passes
19. **MC19** ★ In PyTorch, `optimizer.zero_grad()` is needed because: (a) gradients accumulate by default (b) it resets the weights (c) it frees GPU memory (d) it sets the learning rate to zero
20. **MC20** ★★ PyTorch's `F.cross_entropy` expects its input to be: (a) probabilities after softmax (b) one-hot vectors (c) raw logits (d) class indices
21. **MC21** ★★ PPO is best described as: (a) a value-iteration method (b) model-based planning (c) supervised learning (d) a policy-gradient method with a clipped objective
22. **MC22** ★ In incident response, containment aims to: (a) limit the spread and damage of an incident (b) remove the root cause (c) write the post-incident report (d) procure new tools
23. **MC23** ★ MITRE ATT&CK technique T1059 is: (a) Phishing (b) Command and Scripting Interpreter (c) Valid Accounts (d) Data Encrypted for Impact
24. **MC24** ★★ Without signed messages, Byzantine agreement among n agents with f faulty ones requires: (a) n ≥ 2f + 1 (b) n ≥ f + 1 (c) n ≥ 3f + 1 (d) n ≥ 4f
25. **MC25** ★ In the MAPE-K loop, K stands for: (a) Kernel (b) Key (c) Kalman (d) Knowledge

## Part Q — Fill in the blanks (15 marks, 15 min)

One mark each. Where a question has two blanks, both must be right for the mark.

1. **FB1** ★ Bayes' rule: P(A | B) = P(B | A) P(A) / \_\_\_\_\_\_\_\_.
2. **FB2** ★ A full joint distribution over *n* binary variables needs \_\_\_\_\_\_\_\_ independent parameters.
3. **FB3** ★★ The three steps of computing a counterfactual are abduction, \_\_\_\_\_\_\_\_ and prediction.
4. **FB4** ★★ A valid back-door adjustment set must not contain any \_\_\_\_\_\_\_\_ of the treatment variable.
5. **FB5** ★ An inference procedure that derives only entailed sentences is \_\_\_\_\_\_\_\_; one that derives every entailed sentence is \_\_\_\_\_\_\_\_.
6. **FB6** ★★ In Dempster's rule, combined masses are normalised by dividing by 1 − \_\_\_\_\_\_\_\_, the total conflict mass.
7. **FB7** ★ The Condorcet paradox occurs when pairwise majority preferences form a \_\_\_\_\_\_\_\_.
8. **FB8** ★★ Expected calibration error is a weighted average, over confidence bins, of the gap between accuracy and \_\_\_\_\_\_\_\_.
9. **FB9** ★ In PyTorch, gradients are computed by calling \_\_\_\_\_\_\_\_ on the loss tensor.
10. **FB10** ★★ To keep alerts from the same incident out of both the training and test sets, use a \_\_\_\_\_\_\_\_ split, such as scikit-learn's `GroupShuffleSplit`.
11. **FB11** ★ Parasuraman and Riley call over-reliance on automation \_\_\_\_\_\_\_\_ and under-reliance \_\_\_\_\_\_\_\_.
12. **FB12** ★★ In a mixed-strategy equilibrium, each player randomises so that the other player is \_\_\_\_\_\_\_\_ between their actions.
13. **FB13** ★ MITRE ATT&CK sub-technique T1059.001 is \_\_\_\_\_\_\_\_.
14. **FB14** ★ High predictive entropy in a classifier's output indicates high \_\_\_\_\_\_\_\_.
15. **FB15** ★ The three triage grades in the GUIDE dataset are true positive, \_\_\_\_\_\_\_\_ and false positive.

## Part A — Theory (40 marks, 90 min)

**A1. Base rates and alert fatigue** ★ · 3 marks

An endpoint detector fires on 95% of genuinely malicious events and on 2% of benign events. 1% of events it inspects are malicious.

1. What is P(malicious | alert)? Show your working. (2)
2. What does this mean for the analysts receiving these alerts? (1)

**A2. A small Bayesian network** ★★ · 5 marks

All variables are binary. A host compromise *C* can trigger an endpoint alert *E* and a network alert *N*. Legitimate admin activity *M* can also trigger *E*. There are no other edges.

1. Draw the network and count the independent parameters needed. Compare this with the full joint distribution. (2)
2. Are *E* and *N* independent? Are they independent given *C*? Justify using d-separation. (1)
3. Explain "explaining away" between *C* and *M* when *E* is observed, and why it matters for triage. (2)

**A3. Exact vs. approximate inference** ★★ · 3 marks

Explain how variable elimination works, what determines its cost, and when you would switch to a sampling method instead.

**A4. Causation and counterfactuals** ★★★ · 5 marks

1. Explain the difference between P(TP | many alerts) and P(TP | do(many alerts)) using a SOC example with a plausible confounder. (2)
2. Write the back-door adjustment formula for your example and state when it is valid. (2)
3. Name the three steps for computing a counterfactual. (1)

**A5. Rule-based reasoning** ★ · 3 marks

Rules: (R1) a new-country login to a privileged account is suspicious; (R2) suspicious activity plus a large outbound transfer is an incident; (R3) any incident requires escalation. Facts: account *a* is privileged; *a* logged in from a new country; there was a large outbound transfer from *a*'s host.

1. Write R1–R3 as Horn clauses. (1)
2. Show how forward chaining derives the escalation, and say when backward chaining would suit a SOC better. (2)

**A6. An attacker–defender game** ★★ · 5 marks

Payoffs are (Defender, Attacker).

|  | Attack | Wait |
| --- | --- | --- |
| **Monitor** | (2, −2) | (−1, 0) |
| **Don't monitor** | (−5, 5) | (0, 0) |

1. Show there is no pure-strategy Nash equilibrium. (1)
2. Find the mixed-strategy equilibrium. (3)
3. Interpret the defender's equilibrium strategy in plain words. (1)

**A7. Reconciling agents by voting** ★★ · 4 marks

Three triage agents rank the verdicts: Agent 1: TP > BP > FP; Agent 2: BP > FP > TP; Agent 3: FP > TP > BP.

1. Show that pairwise majority voting produces a cycle. (2)
2. Apply plurality and Borda counting. What happens? (1)
3. What does Arrow's theorem imply for anyone designing a reconciliation rule? (1)

**A8. Belief fusion** ★★★ · 5 marks

On the frame {Malicious, Benign}, Agent A assigns m({M}) = 0.7, m({B}) = 0.1, m(Θ) = 0.2. Agent B assigns m({M}) = 0.2, m({B}) = 0.6, m(Θ) = 0.2.

1. Combine them with Dempster's rule. Show the conflict mass *K*. (3)
2. Explain the main criticism of Dempster's rule when conflict is high, and name one alternative. (2)

**A9. Trust in automation** ★★ · 3 marks

Define misuse and disuse of automation, explain what calibrated trust means, and suggest one way to measure it in a SOC study.

**A10. Uncertainty in neural networks** ★★ · 4 marks

1. Why is a classifier's softmax output not a reliable confidence? (1)
2. Compare MC dropout and deep ensembles as ways to estimate uncertainty. (2)
3. Define expected calibration error (ECE). (1)

### Extension (bonus)

- **A-X1** ★★★ (3 bonus) In a team of *n* agents, how many can be Byzantine (arbitrarily faulty) while the honest agents still reach agreement? Relate this to triage agents that may be compromised or manipulated.
- **A-X2** ★★★ (3 bonus) Your Bayesian reconciler assumes the agents' errors are independent given the true grade. Why is that unrealistic, and how would you model correlated errors?
- **A-X3** ★★★ (2 bonus) Give Zadeh's example showing Dempster's rule producing a counterintuitive result.

## Part C — Applied cyber security (10 marks, 25 min)

**C1. Triage grades** ★ · 2 marks

Define true positive, benign positive and false positive in SOC triage, with a realistic example of each.

**C2. Disagreeing agents at 2 a.m.** ★★ · 4 marks

On a finance workstation, the endpoint agent flags an encoded PowerShell command as high severity. The network agent sees no unusual outbound traffic. The LLM agent concludes it's a benign admin script, citing a similar ticket from last month. The on-call analyst can't be reached for two hours.

1. Which MITRE ATT&CK techniques are plausibly involved? (1)
2. What would you do in the next 15 minutes, and what extra evidence would you collect to resolve the disagreement? (2)
3. How should the system present this disagreement to the analyst when they arrive? (1)

**C3. Limits of automation** ★★ · 4 marks

1. Give two response actions that should never be fully automated and explain why. (2)
2. Distinguish human-in-the-loop from human-on-the-loop, and say which suits each action you named. (2)

### Extension (bonus)

- **C-X1** ★★★ (3 bonus) An attacker knows your SOC uses an LLM triage agent that reads raw log fields. Describe two ways they could manipulate it, or exploit disagreement between the agents, and how you would defend against each.

## Part D — Research skills (15 marks, 45 min)

**D1. Research questions** ★★ · 4 marks

Write two research questions for this PhD project. For each, give a testable hypothesis and the evidence that would support or refute it.

**D2. Designing a user study** ★★★ · 5 marks

You want to know whether showing analysts *why* the agents disagree (explanations and counterfactuals) leads to better triage decisions than showing a single reconciled verdict. Design the study: the participants, conditions, task, independent and dependent variables, measures (including trust and workload), within- or between-subjects design, how you'd handle order effects, sample size reasoning, and the ethics approvals you'd need.

**D3. Critiquing a claim** ★★ · 3 marks

A paper's abstract says: "Our multi-agent triage system achieves 99% accuracy on the GUIDE dataset, outperforming human analysts." List the questions you'd ask before believing it.

**D4. Positioning the work** ★ · 3 marks

Name three research communities or venues where this project's work could be published, and say what each would expect from a paper. Then state, in two sentences, the gap this project would fill.

### Extension (bonus)

- **D-X1** ★★ (2 bonus) Write a 150-word abstract for a first-year paper from this project, based on your disagreeing-agents build.
- **D-X2** ★★★ (3 bonus) Sketch a four-year plan with milestones tied to confirmation of candidature, the annual reviews and the 60-day industry placement.

## Part R — Code reading (10 marks, 20 min)

Read each snippet by hand without running it. Write the exact output and answer the follow-up question.

**R1** ★ · 2 marks

```python
from collections import Counter
votes = ["TP", "FP", "TP", "BP", "FP"]
print(Counter(votes).most_common(1))
```

What is printed? Why is this a risky way for a reconciler to break ties?

**R2** ★★ · 3 marks

```python
def fc(facts, rules):
    agenda, known = list(facts), set()
    while agenda:
        p = agenda.pop(0)
        if p in known:
            continue
        known.add(p)
        for premises, conclusion in rules:
            if conclusion not in known and all(q in known for q in premises):
                agenda.append(conclusion)
    return known

rules = [({"A", "B"}, "C"), ({"C"}, "D"), ({"D", "E"}, "F")]
print(sorted(fc(["A", "B"], rules)))
```

What is printed? Why isn't F derived? How does AIMA's forward-chaining algorithm (7.5) avoid rescanning every rule each time?

**R3** ★★ · 2 marks

```python
import torch
x = torch.randn(32, 10)
W = torch.randn(10, 3)
probs = torch.softmax(x @ W, dim=0)
print(probs.shape)
print(probs.sum(dim=1)[:3])
```

What shape is printed? Will the three printed sums be 1? Explain, and give the fix.

**R4** ★★★ · 3 marks

```python
def cohen_kappa(a, b):
    labels = sorted(set(a) | set(b))
    n = len(a)
    po = sum(x == y for x, y in zip(a, b)) / n
    pe = sum((a.count(l) / n) * (b.count(l) / n) for l in labels)
    return (po - pe) / (1 - pe)

print(cohen_kappa(["TP", "TP", "FP", "FP"], ["TP", "FP", "TP", "FP"]))
```

What is printed? Interpret the result, and name an input that makes the function crash.

## Paper 2 — In code, take-home

Parts B and F. Submit one GitHub repo with a folder per question. Any documentation is allowed; AI coding assistants are not, since the panel wants to see your own work.

## Part B — Programming (30 marks, take-home)

Submit a GitHub repo with one folder per task, tests where asked, and a short README per task. Code quality, tests and clarity count, not just correct output. Use the GUIDE dataset where data is needed.

**B1. Voting rules** ★ · 4 marks

Implement `plurality(rankings)` and `borda(rankings)`, where `rankings` is a list of rankings over the verdicts {TP, BP, FP}. Handle ties with a documented, deterministic rule. Include unit tests, one of which reproduces the cycle from A7.

**B2. Variable elimination** ★★ · 6 marks

Implement exact inference for discrete Bayesian networks: a `Factor` class with product and sum-out, and `variable_elimination(network, query, evidence, order)`. Encode the A2 network with CPTs of your choice, and test your answers against brute-force enumeration (or aima-python's `enumeration_ask`). Report how the size of the largest intermediate factor changes with two different elimination orders.

**B3. Explainable forward chaining** ★★ · 5 marks

Write a forward-chaining engine for propositional Horn clauses that records *why* each fact was derived, and can print the derivation tree for any conclusion. Load the A5 rules and facts, and print the explanation for the escalation.

**B4. Measuring disagreement** ★★ · 5 marks

Given a CSV with columns `incident_id, category, agent1, agent2, agent3, analyst` (verdicts in {TP, BP, FP}), produce:

1. pairwise Cohen's kappa between all agents and with the analyst, and Fleiss' kappa across the three agents;
2. a confusion matrix for each agent against the analyst;
3. disagreement rates by category, with a short written interpretation.

Create this CSV yourself by running three simple agents on GUIDE.

**B5. Uncertainty in PyTorch** ★★★ · 6 marks

Train a PyTorch MLP that classifies GUIDE incidents into TP, BP or FP. Then:

1. add MC dropout and report each prediction's mean probabilities and predictive entropy;
2. train a deep ensemble of 5 models and report the same;
3. compare accuracy, macro-F1, ECE and a reliability diagram for the single model, MC dropout and the ensemble;
4. show whether high-uncertainty incidents are more often misclassified.

Split by incident or organisation, not at random by row, and justify your choice.

**B6. Code review** ★★ · 4 marks

A research assistant submits this baseline for alert-level triage. Find at least four problems, explain why each matters, and give a corrected version.

```python
import pandas as pd
from sklearn.preprocessing import StandardScaler
from sklearn.model_selection import train_test_split
from sklearn.ensemble import GradientBoostingClassifier
from sklearn.metrics import accuracy_score

df = pd.read_csv("guide_alerts.csv")   # one row per alert
X = df.drop(columns=["IncidentGrade"])  # includes IncidentId, OrgId, Category
y = df["IncidentGrade"]

X = StandardScaler().fit_transform(X)
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2)

model = GradientBoostingClassifier().fit(X_train, y_train)
print("Accuracy:", accuracy_score(y_test, model.predict(X_test)))
```

### Extension (bonus)

- **B-X1** ★★★ (3 bonus) Implement Dempster's rule for any frame of discernment (focal sets as `frozenset`s), plus Yager's rule, and reproduce your A8 answer with both.
- **B-X2** ★★★ (4 bonus) Train a PPO defender with Stable-Baselines3 on CybORG++ MiniCAGE. Compare it with a baseline agent over at least 30 episodes, with confidence intervals.

## Part F — Debugging (10 marks, in code)

Each snippet runs but gives wrong results, or fails on some inputs. Copy it into a file, find every bug, fix it, add a comment on each fix explaining why, and write a test that would have caught it. The number of bugs isn't given.

**F1. A posterior that doesn't add up** ★★ · 3 marks

This should return P(C = True | E = e) for the network C → E ← M from A2.

```python
def posterior_compromise(p_c, p_m, p_e_given, e_observed=True):
    """p_c = P(C=True), p_m = P(M=True),
    p_e_given[(c, m)] = P(E=True | C=c, M=m)."""
    scores = {}
    for c in (True, False):
        total = 0.0
        for m in (True, False):
            pe = p_e_given[(c, m)]
            if not e_observed:
                pe = 1 - pe
            total += p_c * p_m * pe
        scores[c] = total
    return scores[True]
```

**F2. A Borda count that picks the loser** ★ · 2 marks

```python
def borda(rankings):
    """rankings: list of lists, best first, e.g. [["TP", "BP", "FP"], ...]"""
    scores = {}
    for ranking in rankings:
        for position, verdict in enumerate(ranking):
            scores[verdict] = scores.get(verdict, 0) + position
    return max(scores, key=scores.get)
```

**F3. A training loop that won't learn properly** ★★ · 2 marks

```python
import torch.nn.functional as F

for epoch in range(epochs):
    for xb, yb in train_loader:
        logits = model(xb)
        loss = F.cross_entropy(torch.softmax(logits, dim=1), yb)
        loss.backward()
        optimizer.step()
    val_acc = evaluate(model, val_loader)   # evaluate() leaves the model as it found it
    print(epoch, val_acc)
```

**F4. MC dropout that reports no uncertainty** ★★★ · 3 marks

`x` is a batch of shape (batch, features); the model contains dropout layers and no batch normalisation.

```python
def mc_dropout_predict(model, x, T=50):
    model.eval()
    preds = []
    with torch.no_grad():
        for _ in range(T):
            preds.append(model(x))
    mean_logits = torch.stack(preds).mean(dim=0)
    probs = torch.softmax(mean_logits, dim=0)
    entropy = -(probs * probs.log()).sum(dim=-1)
    return probs, entropy
```

### Extension (bonus)

- **F-X1** ★★★ (3 bonus) This should implement Dempster's rule, with focal sets as `frozenset`s. Fix it and check it against your A8 answer.

```python
def dempster(m1, m2):
    combined, conflict = {}, 0.0
    for a, wa in m1.items():
        for b, wb in m2.items():
            inter = a | b
            if not inter:
                conflict += wa * wb
            else:
                combined[inter] = combined.get(inter, 0) + wa * wb
    return combined
```

## Scoring

Add up the exam's core marks out of 155 and convert to a percentage; bonus marks (up to 15) are added to the raw score first. Score the panel interview out of 30 using the rubric in its tab. For an overall result, weight the exam 60% and the interview 40%.

| Score (%) | Panel's view |
| --- | --- |
| 85+ | Top candidate: ready to start, likely to publish early |
| 70–84 | Strong: shortlist and interview with confidence |
| 55–69 | Promising: clear gaps, but trainable in year one |
| Below 55 | Not yet ready for this project |

Beyond the numbers, the panel looks for: honest reasoning when you're unsure; linking theory to the cyber setting rather than reciting definitions; clean, tested code; and research judgement, such as spotting leakage, weak baselines or overclaiming. If one part scores well below the others, that's the area to focus on in your reading plan.
