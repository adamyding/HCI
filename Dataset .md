# Dataset notes — Human-to-AI knowledge transfer

## Conversation datasets

### 1. StudyChat https://huggingface.co/datasets/wmcnicho/StudyChat

- Student conversations with an AI assistant in an undergraduate AI course. Our download contains 203 students, 2,214 chats, and 16,851 exchanges.
- Found cases where students provide column names, code, constraints, or corrections, and the assistant uses them.
- Much of the dataset involves students asking for explanations. We need to identify cases where knowledge comes from the human.

### 2. RealCompanion https://huggingface.co/datasets/Quislab/RealCompanion

- Contains 27,218 messages from 10 participants, spanning roughly 36–120 days per person.
- Suitable for studying whether AI remembers earlier information and uses later corrections.
- Two participants account for 73% of messages. Released text was rewritten, and the terms prohibit training and redistribution.

### 3. WildChat-4.8M https://huggingface.co/datasets/allenai/WildChat-4.8M

- Large multilingual collection of real ChatGPT conversations. The linked filtered version contains about 3.2 million conversations.
- Could provide examples of users supplying information, instructions, and corrections across many subjects.
- Needs sampling and annotation. We also need to check how reliably conversations can be linked to the same participant.

### 4. ChatGPT-RealUser-2.2M https://huggingface.co/datasets/Gata-community/ChatGPT-RealUser-2.2M-preview

- Authors report 2.24 million conversations from 15,316 users. The public preview contains 600 conversations.
- Includes user IDs and conversations with GPT-3.5, GPT-4, and o1.
- Full access requires contacting the authors. Users received incentives to contribute, which may affect the sample.

### 5. CoAuthor https://coauthor.stanford.edu/

- Contains 1,445 writing sessions from 63 writers working with GPT-3.
- Records text entry, AI suggestions, accepted and rejected suggestions, and edits.
- Could support studying whether AI follows information and revisions supplied by a writer. Limited to creative and argumentative writing.

### 6. ThoughtTrace https://huggingface.co/datasets/SCAI-JHU/ThoughtTrace

- Contains 2,155 conversations from 1,058 participants, plus 10,174 annotations explaining users’ reasons and reactions.
- Helps identify what users wanted, which constraints mattered, and where responses missed their expectations.
- Some annotations were recorded outside the conversation. We need to check what the AI actually saw before treating them as evidence of knowledge transfer.

## Evaluation benchmarks

### 7. MemoryArena https://memoryarena.github.io/

- Tests agents on connected tasks across multiple sessions, including shopping, travel planning, search, and formal reasoning.
- Later tasks require information or experience from earlier tasks.
- Relevant to testing whether acquired knowledge helps an AI complete a new task.

### 8. MemoryAgentBench https://github.com/HUST-AI-HYZ/MemoryAgentBench

- Tests retrieval, test-time learning, understanding across long contexts, and conflict resolution.
- Supplies information incrementally and asks questions that depend on it.
- Relevant to testing how AI acquires information, combines it, and handles conflicting updates.

### 9. LongMemEval https://github.com/xiaowu0162/LongMemEval

- Contains 500 questions about information in earlier conversations.
- Tests recall, reasoning across sessions, knowledge updates, temporal reasoning, and abstention.
- Provides reference answers and evidence locations. Useful for designing retention tests.