# Human-to-AI Knowledge Transfer — Oct 30

## 1. Background Info

### 1.1 Types of Knowledge

| Type | Description | Example |
|-|-|-|
| Factual | Knowing specific information | Knowing a scientific formula |
| Conceptual | Understanding principles and relationships | Understanding cause and effect |
| Procedural | Knowing how to perform a task | Writing a research paper |
| Strategic | Knowing approaches to solving problems | Comparing alternative explanations |
| Conditional | Knowing when and why to use a strategy | Recognizing when causal analysis is appropriate |
| Metacognitive | Monitoring and adjusting one's thinking | Recognizing a mistake and changing approach |

- factual knowledge may be domain-specific, higher-level reasoning and problem-solving strategies may be reusable across different tasks and domains
- transferring a strategy requires more than remembering its steps
- learner must recognize the underlying principle and determine when to use it

### 1.2 Successful Knowledge Transfer

Transfer depends not only on task or domain similarity, but also on whether the underlying strategy is applicable.


| Dimension | Key Question |
|-|-|
| Acquisition | Can AI identify the knowledge or strategy being taught? |
| Application | Can it use the strategy to solve a problem? |
| Generalization | Can it apply the strategy to unfamiliar tasks? |
| Appropriate use | Can it recognize when the strategy should or should not be used? |
| Retention | Can it reuse or adapt the strategy across interactions? |

**Near, far, and negative transfer**

Example: Someone writing a scientific paper.

- Near transfer -> write another paper in a related field
- Far transfer -> apply scientific reasoning and evidence-based arguments to a policy proposal (different domain)
- Negative transfer -> apply an inappropriate strategy that reduces performance

**Main measurement challenge**

- Better AI performance after human teaching doesn't mean it learned something reusable
- AI can just be following instructions, remembering examples, or using knowledge it already had
- The challenge is distinguishing actual learning and transfer from these other explanations.

### 1.3 Reverse KITE — Human-to-AI Knowledge Transfer

[KITE](https://arxiv.org/pdf/2506.05579) investigates whether humans can independently apply knowledge gained through AI collaboration.

**Proposed Reversal:** Human teaches AI -> AI independently applies the learned knowledge
- key is are we able to determine if AI can acquire knowledge from humans and apply it to new tasks
- is AI able to generalize human-taught reasoning strategies across domains and recognize when those strategies should or should not be used.

## 2. Research Directions

### 2.1 Research Questions

Study 1 — Measuring Human-to-AI Transfer

- RQ1 — Extraction: What knowledge, reasoning strategies, and learning plans can AI extract from human teaching?
- RQ2 — Transfer: Can AI apply what it learned to new tasks (including near and far transfer, while avoiding inappropriate transfer)?
- RQ3 — Retention: Can AI retain and update learned strategies across interactions and sessions?

Study 2 — Human Teaching and Learning Strategies

- RQ4 — Teaching Methods: Which human teaching methods are more effective for AI knowledge transfer?
- RQ5 — Learning to Learn: Can human-taught learning strategies improve how AI learns unfamiliar tasks?

### 2.2 Study 1 — Measuring Human-to-AI Transfer

- develop a framework or benchmark to measure whether AI acquires knowledge from humans and transfers it independently.
- start with a small set of reasoning, procedural, and learning strategies. Each would have teaching examples and separate tasks for evaluation.

#### Extraction / Measure

Possible task settings:
- Controlled reasoning problems with known answers, to better isolate transfer.
- Real-world tasks such as research, data analysis, and decision-making.
- Example: human teaches AI to consider alternative explanations before drawing conclusions -> can test whether AI uses that reasoning in new problems (including cases where it does not apply)
- Teaching conditions could include:
    - No teaching (baseline).
    - Demonstrations using worked examples.
    - Explanations of how, why, and when a strategy works.
    - Interactive teaching with practice, questions, and feedback.

#### Measuring Transfer

After teaching, remove original transcript and test AI on unfamiliar tasks without explicitly telling it to use the strategy and compare performance
- Near transfer — Same domain and reasoning structure, different problem.
- Far transfer — Different domain, same underlying strategy.
- Misleading similarity — Looks similar, but the strategy should not be used.
- Unrelated task — Neither the task nor the strategy matches.

#### Retention

Test whether AI still uses the strategy in new sessions, with unrelated tasks in between. 
- can also create exceptions or new information and see whether it updates the strategy without losing what was previously useful.

### 2.3 Study 2 — Human Teaching and Learning Strategies

Determine whether methods from education and cognitive psychology help AI learn more effectively -> focus on how AI is taught and how it learns, rather than developing a new memory architecture.

#### A — Comparing Examples and Explanations

- human learning process includes comparing examples can help reveal underlying principles
- talking out loud / Self-explanation may also help learners understand why a strategy works.

Compare:
- One example vs. multiple contrasting examples.
- Observing examples vs. generating and checking explanations.
- Both methods separately and together.

####  B — Guided Practice and Feedback

- Compare direct explanations, worked examples, practice with feedback, and practice where guidance is gradually removed.
- After teaching, test AI on new problems without support.
- testing to see if practice and feedback improve independent transfer compared with simply explaining a strategy
- does gradually removing guidance makes a difference.

####  C — Learn Learning

- teach the appracoh of learning instead of specific problem solving stragtey
- Example
    1. Identify what it doesn't understand.
    2. Decide what to learn or practice next.
    3. Attempt the task.
    4. Check the result.
    5. Adjust the learning plan.
- compare an agent with speciifc problem solving plan vs agent taught above method
- same resources and an unfamiliar domain, then compare how they improve over several attempts

