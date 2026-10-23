# Education Notes

## Summary

### Learning a strategy != knowing when to use it

**Gick & Holyoak (1983), Lobato (2006)**

- People can understand a strategy but fail to recognize when it applies to another problem.
- Comparing multiple examples helps people identify common patterns.
- Transfer requires both learning the underlying principle and recognizing its relevance in a new situation.
- For AI, An agent might have the correct skill stored but fail to retrieve it when needed.

### Understanding Why matters, not just how

**Chi et al. (1989)**

- Students who explained why solution steps worked tended to perform better.
- Simply memorizing the steps doesn't necessarily produce transferable understanding.
- Explanations can help reveal the principles and conditions behind a strategy.
- AI or agents may need to also capture the reasoning behind decisions instead of recording only successful workflows

### How we teach affects what gets learned

**Shafto et al. (2014), Chi et al. (2001), Csibra & Gergely (2009)**

- Carefully selected examples can communicate concepts more effectively than arbitrary examples.
- Learners benefit from actively working through problems rather than just receiving explanations.
- People interpret deliberate teaching differently from simply observing someone's behavior.
- Could comparing examples, explaining decisions, and receiving feedback help agents learn transferable strategies?

### Knowledge transfer is more than solving a new problem correctly

**Bransford & Schwartz (1999)**

- Traditional transfer tests measure whether someone can immediately solve a new problem.
- Prior knowledge can also prepare someone to learn faster when new information becomes available.
- This is called **Preparation for Future Learning (PFL)**.
- Experimentally, we can evaluate both whether an agent solves a new task independently and whether it adapts faster after feedback.

### Observing behavior doesn't reveal the full reasoning behind it

**Malle & Knobe (1997), Meltzoff (1995)**

- People distinguish between someone's actions, goals, intentions, and abilities.
- Children can sometimes infer what someone intended to accomplish even after watching them fail.
- But inferring a goal is different from recovering the actual reasoning strategy.
- Can we reliably extract someone's strategy from their actions alone, or do we need explanations, multiple examples, and additional context?


## 1. Gick & Holyoak (1983) — *Schema Induction and Analogical Transfer*

[PDF](https://gwern.net/doc/psychology/1983-gick.pdf)

- **Research question**
  - How do people learn a general strategy from examples and recognize when it applies to a different problem?
- **Experiment**
  - Participants read problem-solving stories, then tried to solve a medical problem: destroy a tumor without damaging surrounding tissue.
  - A relevant military story described forces approaching a target from several directions. Both problems involved **converging several weaker forces on one target**.
  - Across six experiments, researchers varied the number and type of examples, comparisons, explanations of the principle, diagrams, and hints.
  - They measured whether participants used the strategy on their own or only after receiving a hint.
- **Findings**
  - A relevant example helped, but people did not always notice the connection without prompting.
  - Comparing two related examples improved spontaneous transfer: **45%** solved the new problem, versus **21%** with one relevant and one irrelevant example.
  - With two relevant examples, adding an explicit principle raised spontaneous solutions from **40% to 62%**.
  - Adding diagrams that highlighted the shared structure raised spontaneous solutions from **37% to 57%**.
  - Hints improved performance, showing that having learned a strategy does not mean people will think to use it.
- **Takeaway**
  - Transfer involves both **learning the underlying pattern** and **recognizing it in a new task**.
  - Comparing examples can make that pattern easier to see, even when the examples look different on the surface.

## 2. Chi et al. (1989) — *Self-Explanations: How Students Study and Use Examples in Learning to Solve Problems*

[PDF](https://doi.org/10.1207/s15516709cog1302_1)

- **Research question**
  - Why do some students learn much more than others from the same worked examples?
- **Experiment**
  - Ten university students studied three worked physics examples while thinking aloud.
  - Researchers recorded whether they explained principles, justified solution steps, or noticed things they did not understand.
  - Students then solved new physics problems. The detailed comparison focused on four stronger and four weaker performers.
- **Findings**
  - Stronger performers explained **why** steps worked and connected them to physics principles more often.
  - They averaged **15.3 self-explanations per example**, compared with **2.8** for weaker performers.
  - They solved **82%** of test problems correctly, compared with **46%** for weaker performers.
  - They also identified more gaps in their understanding instead of skipping over confusing steps.
- **Takeaway**
  - Following a worked solution is not the same as understanding the reasoning behind it.
  - Explaining why a step makes sense may help build knowledge that carries over to other problems.
  - This was an observational study; it does not prove that self-explanation alone caused the performance difference.

## 3. Shafto, Goodman & Griffiths (2014) — *A Rational Account of Pedagogical Reasoning: Teaching by, and Learning from, Examples*

[PDF](https://web.stanford.edu/~ngoodman/papers/shaftogg14.pdf)

- **Research question**
  - How do teachers choose useful examples, and how do learners interpret examples that were deliberately chosen to teach them something?
- **Experiment**
  - The authors built a model in which teachers choose informative examples and learners reason about why those examples were selected.
  - **Experiment 1:** Examined teaching and learning of rule-based concepts.
  - **Experiment 2:** Examined concepts organized around typical or representative examples (prototypes).
  - **Experiment 3:** Examined concepts involving cause-and-effect relationships.
  - Across the experiments, they compared people's teaching choices and interpretations with the model's predictions.
- **Findings**
  - People's responses broadly matched the model across all three kinds of concepts.
  - Learners can draw information from **why a teacher chose a particular example**, not just from the example itself.
- **Takeaway**
  - Good teaching is not just about showing more correct examples.
  - Choosing examples carefully can help learners distinguish the intended idea from other possible interpretations.
  - The same example may be interpreted differently when it is presented as teaching rather than as an ordinary observation.

## 4. Bransford & Schwartz (1999) — *Rethinking Transfer: A Simple Proposal with Multiple Implications*

[PDF](https://aaalab.stanford.edu/assets/papers/earlier/Rethinking_transfer_a_simple_proposal_with_multiple_implications.pdf)

- **Research question**
  - How should we measure whether previous learning helps in a new situation?
- **Experiment / evidence**
  - This paper proposes a broader way to evaluate transfer, drawing on earlier research rather than reporting one new experiment.
  - Traditional tests ask whether someone can solve a new problem immediately, without help.
  - The authors also consider **preparation for future learning**: whether earlier experience helps someone learn from later instruction or feedback.
  - In one study discussed, learners either compared contrasting memory cases or completed a summarizing activity.
  - Some then received a lecture explaining the relevant principle before making predictions.
- **Findings**
  - After the lecture, learners who had compared contrasting cases made better predictions than those who had summarized.
  - Comparing cases alone did not guarantee strong performance without that later instruction.
- **Takeaway**
  - Failing to solve a new task immediately does not necessarily mean earlier learning was useless.
  - Previous experience may instead help someone **learn faster once new information is available**.
  - It is useful to measure independent problem-solving and learning after feedback separately.

## 5. Lobato (2006) — *Alternative Perspectives on the Transfer of Learning*

[PDF](https://www.researchgate.net/publication/228621766_Alternative_Perspectives_on_the_Transfer_of_Learning_History_Issues_and_Challenges_for_Future_Research)

- **Research question**
  - Should transfer be judged only by whether learners use the strategy researchers expect, or also by the connections learners actually make?
- **Research approach**
  - This is a review of previous research, not a new experiment.
  - **Traditional approach:**
    - Researchers identify two tasks that share an underlying strategy.
    - They test whether learners use that strategy on the second task, often scoring the expected answer.
  - **Actor-oriented approach:**
    - Researchers look at what learners themselves notice, say, and do when facing the new task.
    - A learner might make a meaningful connection but use it incompletely or incorrectly.
    - Two tasks may seem similar to researchers but not to the learner.
- **Findings**
  - The review argues that a correct-or-incorrect score can miss how learners connect past experience to a new situation.
  - A connection can be meaningful without producing the expected answer; it can also lead to a mistake.
- **Takeaway**
  - Transfer depends partly on **what the learner notices**, not just on similarities between tasks.
  - To understand a transfer failure, examine the connection the learner tried to make, not only the final answer.

## 6. Chi et al. (2001) — *Learning from Human Tutoring*

[PDF](https://education.asu.edu/sites/g/files/litvpz656/files/lcl/image3_2.pdf)

- **Research question**
  - Why does one-to-one tutoring help students learn? Is it mainly the tutor's explanations or the student's own activity during tutoring?
- **Experiment**
  - **Study 1:** Researchers analyzed tutoring conversations, including what tutors explained, how students responded, and how the two interacted.
  - They considered tutor-centered, student-centered, and interaction-based explanations of learning.
  - **Study 2:** Tutors were restricted from giving direct explanations and feedback and were encouraged to prompt students instead.
  - Researchers compared learning in this condition with less restricted tutoring.
- **Findings**
  - The conversation analysis highlighted students' active contributions and the support they received during interaction.
  - In the second study, students learned **just as effectively** when tutors gave fewer direct explanations and prompts played a larger role.
- **Takeaway**
  - Tutoring is not just a tutor delivering a complete explanation.
  - Students also need to work through ideas, respond, and build understanding themselves.
  - This does not mean explanations are unhelpful; more explanation was simply not always better in these conditions.

## 7. Csibra & Gergely (2009) — *Natural Pedagogy*

[PDF](https://www.icts.res.in/sites/default/files/csibra_gergely_2009.pdf)

- **Research question**
  - How do humans learn general knowledge from another person's demonstration instead of treating it as just one event?
- **Experiment / evidence**
  - This is a theoretical review of earlier developmental and imitation research; it reports no new experiment.
  - The authors propose that communicative cues, such as direct eye contact or speech addressed to a child, signal that someone is teaching.
  - Learners may then treat the demonstration as information that applies beyond that particular situation.
  - In earlier studies discussed by the authors, children sometimes copied an unusual action even when it was not needed to reach the goal.
- **Findings**
  - The authors interpret this evidence as suggesting that **being taught** can change what learners think is important to copy or generalize.
  - A demonstrated action may communicate something about *how* to act, not just the final outcome.
- **Takeaway**
  - Watching someone act and being deliberately taught are not necessarily the same learning experience.
  - Communication can affect which parts of a demonstration the learner treats as important.

## 8. Malle & Knobe (1997) — *The Folk Concept of Intentionality*

[PDF](https://research.clps.brown.edu/SocCogSci/Publications/Pubs/Malle_Knobe_%281997%29_folk_concept_JESP.pdf)

- **Research question**
  - What makes people judge an action as intentional rather than accidental or merely attempted?
- **Experiment**
  - **Experiment 1:** 104 participants rated 20 short actions for intentionality.
  - **Experiment 2:** 159 participants described what they thought made an action intentional.
  - **Experiment 3:** 132 participants judged scenarios that varied an actor's desire, belief, and skill.
  - **Experiment 4:** 225 participants judged scenarios that also varied whether the actor was aware of the action.
- **Findings**
  - Participants showed broad agreement about which actions counted as intentional.
  - Their judgments drew on several factors: **desire, belief, decision, skill, and awareness**.
  - Without the necessary skill, **81%** judged an actor to be *trying*, but only **3%** judged the completed action to be *intentional*.
  - Skill and awareness changed judgments even when the outward behavior was similar.
- **Takeaway**
  - Observing an action does not tell us everything about the person's intention.
  - Goals, abilities, awareness, and behavior are related but should not be treated as the same thing.
  - The experiments measured people's **judgments** of intention, not whether those judgments revealed someone's actual thoughts.

## 9. Meltzoff (1995) — *Understanding the Intentions of Others: Re-Enactment of Intended Acts by 18-Month-Old Children*

[PDF](https://ilabs.uw.edu/wp-content/uploads/95Meltzoff_DevPsy.pdf)

- **Research question**
  - Can young children understand what someone intended to do, even if that person failed?
- **Experiment**
  - **Experiment 1:** 40 infants (18 months old) watched an adult succeed or fail at five object tasks, such as pulling an object apart.
  - Children then received the objects. Control groups saw no demonstration or unrelated handling.
  - **Experiment 2:** 60 infants watched failed actions performed by a person or comparable movements produced by a mechanical device.
- **Findings**
  - After watching failed attempts, children completed an average of **4.0 out of 5** target actions; after successful demonstrations, **3.8**.
  - Control groups averaged about one target action.
  - In Experiment 2, **60%** completed the target action after a human demonstration, versus **10%** after the mechanical-device condition.
- **Takeaway**
  - Learning from behavior is not always simple imitation.
  - Children can sometimes infer **what someone was trying to achieve** even when the observed action failed.
  - These were simple physical tasks, not evidence that children could reconstruct complex reasoning strategies.
