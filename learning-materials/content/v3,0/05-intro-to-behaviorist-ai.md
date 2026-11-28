> **Part 3: Behaviorist AI**  
> **Chapter 3.1: Intro to Behaviorist AI & RL**

## Prerequisites

No advanced knowledge of artificial intelligence or machine learning is required. Before starting, you should be able to:

- Understand the basic idea of an algorithm as a sequence of instructions used to solve a problem.
- Recognize that a computer program receives input, processes information, and produces output.
- Understand basic cause-and-effect relationships (for example, an action followed by a positive or negative consequence).
- Interpret simple numerical values, including positive and negative numbers.
- Follow simple step-by-step processes and understand basic flowcharts.

No previous knowledge of psychology, neuroscience, or reinforcement learning is required.

# Overview & Prediction

Imagine you are teaching a dog a new trick, like rolling over. You do not hand the dog a 300-page manual on canine anatomy, nor do you write out code for its brain to execute. Instead, you wait for the dog to make a move. When it gets closer to what you want, you give it a treat. When it barks or runs away, you withhold the treat. Over time, without reading a single word, the dog learns a complex sequence of physical movements purely through trial, error, and incentives.

**Predict:** If an artificial intelligence is placed in a digital maze without a map, rules, or instructions, how might it figure out the shortest path to the exit using only a score counter that goes up when it reaches the exit and down every time it hits a wall?

---

# Learning Goals

By the end of this chapter, you will be able to:
* Define behaviorist AI and explain its connection to psychology and neuroscience.
* Diagram the core interaction loop between an agent and its environment.
* Identify the four key components of Reinforcement Learning (Agent, Environment, Actions, and Rewards).
* Contrast Model-Based learning with Model-Free learning using real-world analogies.

---

# The Explanation

## 1. What is Behaviorist AI?

**Behaviorist AI** is a branch of artificial intelligence inspired by psychological behaviorism, where an artificial system learns how to act by interacting with its surroundings and receiving feedback rather than following pre-programmed rules.

In classical psychology, behaviorism (popularized by figures like B.F. Skinner) suggests that actions followed by positive outcomes tend to be repeated, while actions followed by negative outcomes tend to decline. Neuroscience shows a similar pattern in living brains, where neurotransmitters like dopamine reinforce neural pathways associated with successful choices. 

Behaviorist AI translates this biological concept into mathematics. Instead of giving a machine step-by-step instructions (Symbolic AI) or showing it millions of labeled photos (Supervised Learning), we place the machine in an environment and let it learn through trial and error.

> **Check Your Understanding:** In your own words, explain how Behaviorist AI differs from traditional software programming where a developer writes strict "if/then" rules.

---

## 2. The Core Process: Reinforcement Learning

The primary framework used to implement Behaviorist AI is **Reinforcement Learning**, a machine learning paradigm where a computer program learns to make decisions by performing actions and receiving rewards or penalties.

To understand Reinforcement Learning, we divide any system into four primary components:

```
                  +-------------------+
                  |    Environment    |
                  +-------------------+
                     /             \
       State / Reward               Action
                   /                 \
                  v                   v
                  +-------------------+
                  |       Agent       |
                  +-------------------+
```

1. **Agent**: The autonomous decision-maker or AI learner that perceives the environment and takes actions.
2. **Environment**: Everything outside the agent with which the agent interacts, responds to actions, and presents new situations.
3. **Action**: The set of all possible moves, decisions, or behaviors that the agent can execute at any given moment.
4. **Reward**: A numeric scalar feedback signal sent from the environment to the agent indicating how successful or desirable the previous action was.

The agent's goal is not just to get an immediate reward, but to maximize its total cumulative reward over time.

> **Check Your Understanding:** Imagine an AI learning to play chess. Identify the **Agent**, **Environment**, **Action**, and **Reward** in this specific context.

---

## 3. Model-Based vs. Model-Free Learning

When an agent learns within an environment, it generally takes one of two strategic approaches:

**Model-Based Learning** is a reinforcement learning approach where the agent builds an internal mental representation or map of how the environment works to predict future outcomes before taking an action. Think of this like playing a game of chess while carefully planning five moves ahead in your head, predicting how your opponent will react to each choice.

**Model-Free Learning** is a reinforcement learning approach where the agent learns directly from trial-and-error experience without attempting to build an explicit model or map of the environment. Think of this like learning to ride a bicycle. You do not calculate physics equations or model gravity in your head; you simply adjust your balance based on immediate feedback until muscle memory takes over.

| Feature | Model-Based | Model-Free |
| :--- | :--- | :--- |
| **Internal Map** | Builds a detailed map/rules of the environment | Operates purely on experience |
| **Planning Ability** | High (can simulate future states) | Low (reacts based on past learned values) |
| **Computational Needs**| High memory and processing for planning | Faster execution once trained |

> **Check Your Understanding:** Predict which approach (Model-Based or Model-Free) a fast-moving reflex system in a self-driving car might rely on when deciding to slam on the brakes for an unexpected obstacle.

---

# Hands-On Activity (Apply)

## Goal
Design a complete Reinforcement Learning feedback framework for a real-world task on paper.

## Preparation
Grab a sheet of paper and a pen (or open a blank text document).

## Task
Select **one** of the following scenarios:
1. An AI system learning to optimize household thermostat temperatures to lower electricity bills.
2. An AI vacuum cleaner learning to clean a room as quickly as possible.
3. An AI character in a video game learning to dodge incoming projectiles.

For your chosen scenario, write out explicit definitions for each of the following:
* **The Agent**
* **The Environment**
* **At least 3 distinct Actions**
* **A specific Reward (+ points) condition**
* **A specific Penalty (- points) condition**

## Observation
Look closely at your reward and penalty conditions. Ask yourself: Is there any way the AI could "cheat" your reward system to get points without actually completing the real-world goal? (For example, could the vacuum just run around in circles over a clean spot to gain movement points?)

## Reflection
How might changing the penalty value (making it much harsher or much milder) affect how cautiously or aggressively your AI agent behaves?

## Feedback
Check your setup against these standard guidelines:
* The **Agent** must be the software making choices, not the human user.
* The **Environment** must include the physical or virtual space the agent interacts with.
* The **Reward/Penalty** must directly encourage the desired outcome while preventing unintended loopholes.

---

# Summary & Glossary

Behaviorist AI turns the challenge of programming complex behaviors into a process of trial, error, and feedback. Rooted in psychological conditioning and neuroscience, this branch of AI relies heavily on Reinforcement Learning. An autonomous agent constantly observes its environment, takes actions, and receives numerical rewards or penalties. Depending on whether the agent constructs an internal map of its surroundings, it utilizes either Model-Based or Model-Free learning strategies to continuously improve its decision-making capabilities.

## Glossary
* **Behaviorist AI**: A branch of artificial intelligence inspired by psychological behaviorism, where an artificial system learns how to act by interacting with its surroundings and receiving feedback rather than following pre-programmed rules.
* **Reinforcement Learning**: A machine learning paradigm where a computer program learns to make decisions by performing actions and receiving rewards or penalties.
* **Agent**: The autonomous decision-maker or AI learner that perceives the environment and takes actions.
* **Environment**: Everything outside the agent with which the agent interacts, responds to actions, and presents new situations.
* **Action**: The set of all possible moves, decisions, or behaviors that the agent can execute at any given moment.
* **Reward**: A numeric scalar feedback signal sent from the environment to the agent indicating how successful or desirable the previous action was.
* **Model-Based Learning**: A reinforcement learning approach where the agent builds an internal mental representation or map of how the environment works to predict future outcomes before taking an action.
* **Model-Free Learning**: A reinforcement learning approach where the agent learns directly from trial-and-error experience without attempting to build an explicit model or map of the environment.

# Comprehensive RL Study Questions & Answers
**Source:** Test Banks for Chapter 3.1 & 3.2

---

## Chapter 5: Behaviorist AI and RL Basics

### Question 1 (Open-Ended)
**Explain what Behaviorist AI is. Describe its connection to psychology (behaviorism) and neuroscience, and explain how it differs from Symbolic AI and from Supervised Learning.**

**Answer:**
*   **Definition:** Behaviorist AI is a branch of artificial intelligence inspired by psychological behaviorism. An artificial system learns how to act by interacting with its surroundings and receiving feedback, rather than by following pre-programmed rules.
*   **Psychology:** In behaviorism (popularized by B.F. Skinner), actions followed by positive outcomes tend to be repeated, while actions followed by negative outcomes tend to decline. 
*   **Neuroscience:** In living brains, neurotransmitters such as dopamine reinforce the neural pathways connected with successful choices. Behaviorist AI translates this biological idea into mathematics.
*   **Difference from Symbolic AI:** In Symbolic AI, a developer gives the machine step-by-step instructions (strict if/then rules). 
*   **Difference from Supervised Learning:** A supervised system is shown millions of labeled examples (like labeled photos). In Behaviorist AI, the machine is placed in an environment and learns through trial and error, using feedback in the form of rewards and penalties.

### Question 2 (Open-Ended)
**Compare Model-Based and Model-Free learning. Define each, give an analogy for each, compare them on internal map, planning ability and computational needs, and say which one you would choose for (a) a program that plans several moves ahead in a board game and (b) a car's emergency braking reflex.**

**Answer:**
*   **Model-Based Learning:** The agent builds an internal mental representation or map of how the environment works and uses it to predict future outcomes before acting. 
    *   *Analogy:* Playing chess while planning five moves ahead and predicting how the opponent will react to each choice.
*   **Model-Free Learning:** The agent learns directly from trial-and-error experience without building an explicit model of the environment. 
    *   *Analogy:* Learning to ride a bicycle by adjusting your balance from immediate feedback, without calculating physics, until muscle memory takes over.
*   **Comparison:**
    *   *Internal Map:* Model-Based builds a detailed map; Model-Free works purely on experience.
    *   *Planning Ability:* High for Model-Based (can simulate future states); Low for Model-Free (reacts from past learned values).
    *   *Computational Needs:* High memory/processing for Model-Based planning; faster execution once trained for Model-Free.
*   **Choices:** 
    *   (a) A board-game planner suits **Model-Based** learning because it benefits from simulating several moves ahead. 
    *   (b) An emergency braking reflex suits **Model-Free** learning because it needs a fast reaction from learned experience.

### Question 3 (Open-Ended)
**Design a Reinforcement Learning setup for an AI thermostat that lowers electricity bills. Define the agent, the environment, at least three actions, one reward condition and one penalty condition. Then describe one way the AI could "cheat" your reward system, and how making the penalty harsher or milder would change its behavior.**

**Answer:**
*   **Agent:** The software that controls the heating and cooling (not the homeowner).
*   **Environment:** The house, including its rooms, the weather, the occupants, and the electricity meter, which respond to the thermostat's decisions.
*   **Actions (at least 3):** Raise the target temperature, lower the target temperature, switch the heating off, switch the heating on, or keep the setting unchanged.
*   **Reward:** +points when the house stays at a comfortable temperature while electricity use is lower than before.
*   **Penalty:** −points when the house is outside the comfortable range, or when electricity use is high.
*   **Loophole:** If the reward is only for low electricity use, the AI could cheat by switching everything off and letting the house get uncomfortable. The reward must be tied to comfort as well as saving energy.
*   **Penalty Strength:** A much harsher penalty usually makes the agent more cautious and quick to avoid discomfort, even if it costs more electricity. A much milder penalty lets it take more aggressive risks to save energy.

### Question 4 (Multiple Choice)
**A chess AI gives up a pawn now because this leads to winning the game later. Which idea does this show?**
A) Maximizing only the immediate reward
B) Memorizing labeled examples
C) Following fixed if/then rules
D) Maximizing the total cumulative reward over time

**Answer:** **D) Maximizing the total cumulative reward over time.**
*Reasoning:* The agent's goal is the total reward over time, so it can accept a small loss now for a bigger reward later.

### Question 5 (Multiple Choice)
**A vacuum agent earns points for movement, so it runs in circles over a clean spot. What does this show?**
A) The agent is using model-based planning
B) The environment is too small
C) The penalty is too mild
D) The reward has a loophole that lets the agent score points without doing the real task

**Answer:** **D) The reward has a loophole that lets the agent score points without doing the real task.**
*Reasoning:* The agent exploits the reward system. A reward must encourage the desired outcome while preventing unintended loopholes.

---

## Chapter 3.2: MDPs and RL Algorithms

### Question 6 (Multiple Choice)
**What does the word "Markov" mean in a Markov Decision Process?**
A) The agent always picks the same action
B) The next state depends only on the current state and the action taken, not on everything that happened before
C) Every reward must be positive
D) The agent knows the whole future in advance

**Answer:** **B) The next state depends only on the current state and the action taken, not on everything that happened before.**
*Reasoning:* This is the "Markov property," a foundational assumption that makes MDPs computationally feasible by removing the need to track all historical states.

### Question 7 (Multiple Choice)
**A robot gets rewards of 5, 10 and 20 over three steps. With a discount factor of 0.8, what is the return?**
A) 35
B) 25.8
C) 29
D) 20

**Answer:** **B) 25.8**
*Reasoning:* The return is calculated as \(R = r_1 + \gamma r_2 + \gamma^2 r_3\).
* \(R = 5 + (0.8 \times 10) + (0.8^2 \times 20)\)
* \(R = 5 + 8 + (0.64 \times 20)\)
* \(R = 5 + 8 + 12.8 = 25.8\)

### Question 8 (Multiple Choice)
**Which description fits policy iteration?**
A) It updates every state value until the values stop changing and then picks the best actions
B) It picks only random actions
C) It switches between evaluating the current policy and improving it, until the policy cannot be improved
D) It builds a Q-table of rewards

**Answer:** **C) It switches between evaluating the current policy and improving it, until the policy cannot be improved.**
*Reasoning:* Policy iteration is a dynamic programming algorithm that alternates between policy evaluation (calculating the value of the current policy) and policy improvement (making the policy greedy with respect to those values).

### Question 9 (Multiple Choice)
**What does the Q-table store?**
A) Only the best action for each state
B) The labels of the training data
C) The transition probabilities
D) A Q-value for every (state, action) pair

**Answer:** **D) A Q-value for every (state, action) pair.**
*Reasoning:* The Q-table is the "memory" of a Q-learning agent. It stores the expected future rewards for taking a specific action in a specific state.

### Question 10 (True/False)
**With the ε-greedy method and ε = 0.1, the agent picks a random action about 10% of the time.**

**Answer:** **True.**
*Reasoning:* The epsilon (\(\epsilon\)) in \(\epsilon\)-greedy represents the exploration rate. If \(\epsilon = 0.1\), the agent will explore (pick a random action) 10% of the time and exploit (pick the best known action) the remaining 90% of the time.