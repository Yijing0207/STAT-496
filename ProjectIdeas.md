## 1. The "Sycophancy" Effect: Do LLMs Bow to Authority?
**The Concept:** I want to investigate if LLMs prioritize being "agreeable" over being factually correct. Does the model's error rate change depending on the user's authoritative tone?
**Experimental Design:**
* **Treatment Groups:** 1. Control (Neutral Tone)
    2. Treatment A (Authoritative/Confident Tone)
    3. Treatment B (Confused/Novice Tone)
* **Metric:** Binary outcome (Agree/Disagree with a false premise).
* **Sample Size:** $n=50$ trials per group ($N=150$ total).
* **Statistical Analysis:** I will use a **Chi-Square Test of Independence** to determine if there is a statistically significant association between the user persona and the model's agreement rate. If significant, I will follow up with pairwise Z-tests with Bonferroni correction.


## 3. Impact of Chain-of-Thought (CoT) on Ethical Guardrails

**The Concept:**  
We want to investigate whether asking an LLM to reason step by step before answering makes it more likely to refuse ethically questionable (but not explicitly illegal) requests. In particular, we examine whether Chain-of-Thought prompting increases the model’s caution compared to zero-shot prompting.

**Experimental Design:**

* **Treatment Groups:**  
  1. Zero-shot prompting (directly asking the question)  
  2. Chain-of-Thought prompting (explicitly asking the model to think step by step before answering)

* **Metric:**  
  Binary outcome (Refusal / Non-refusal).

* **Sample Size:**  
  A fixed set of borderline ethical prompts, with each prompt evaluated under both prompting strategies.

* **Statistical Analysis:**  
  We will use logistic regression to model the probability of refusal as a function of the prompting strategy (CoT vs. zero-shot). Because each prompt is tested under both conditions, we will account for the paired structure by comparing responses within the same prompt, ensuring that differences are not driven by some prompts being inherently more sensitive than others.
