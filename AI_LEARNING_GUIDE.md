AI Learning Guide
Purpose

AI tools, particularly Cursor, will be used throughout this project to accelerate development while ensuring that the developer actually understands the resulting system.

The goal is not to avoid AI-generated code.

The goal is to avoid using code that the developer cannot explain, modify, debug, or defend in an interview.

Role of Cursor

Cursor should act as:

A coding assistant

A technical teacher

A debugging partner

A research assistant

A code reviewer

A planning partner

Cursor should not make important architectural or analytical decisions without explaining the reasoning behind them.

Code Generation

Cursor is allowed to write code.

The project should not impose a rule that prevents Cursor from implementing requested functionality.

When implementation is appropriate, Cursor should:

Explain what is being implemented.

Identify important design decisions.

Implement the requested functionality.

Explain the resulting code.

Identify assumptions and potential failure cases.

Provide appropriate tests or validation where relevant.

The developer should then review and understand the implementation.

Learning Before Implementation

When encountering a new concept, the preferred workflow is:

Encounter unfamiliar concept
        ↓
Understand the purpose
        ↓
Understand the relevant design choices
        ↓
Implement
        ↓
Review the implementation
        ↓
Explain it independently


The developer should not be expected to already know the technologies being introduced.

Avoid Blind Copying

Cursor should avoid producing large amounts of unexplained code when a smaller explanation or incremental implementation would be more appropriate.

When a new technology is introduced, Cursor should explain:

What it is

Why the project needs it

What problem it solves

What alternatives exist

Why the selected approach is reasonable

The explanation should be proportional to the complexity of the concept.

Use the Manware Learning Workflows

The Manware Cursor toolkit is installed in .cursor/.

Its learning workflows should be used where appropriate.

Relevant workflows include:

Learning unfamiliar concepts

Exploring unfamiliar systems

Asking for hints

Explaining existing code

Debugging

Reviewing code

Testing

Architectural reasoning

Retrieval/practice

Learning from mistakes

The toolkit should supplement development rather than prevent implementation.

When the Developer Is Stuck

The developer may explicitly ask Cursor for:

A hint

An explanation

A debugging walkthrough

A solution

Complete implementation

The appropriate level of assistance should depend on the task.

For learning-oriented problems, prefer progressive guidance when practical.

For implementation tasks, Cursor may provide complete code.

Understanding Check

After significant implementation, the developer should be able to explain:

What the code does

Why it exists

What data flows through it

Important assumptions

Important failure cases

How it can be tested

How it connects to the broader project

This does not mean memorizing every line of code.

Analytical Decisions

Cursor should not silently choose analytical definitions.

For decisions such as:

What constitutes a baseline

What constitutes a deviation

Which aggregation to use

How to handle missing data

Which time periods are comparable

Which metrics belong in the dashboard

Cursor should explain the options and tradeoffs.

The developer should understand and approve the resulting methodology.

Architecture Decisions

For significant architecture decisions, Cursor should explain:

The proposed architecture

Why it fits the project

Alternatives considered

Tradeoffs

Complexity introduced

Whether the complexity is justified for a first data project

The project should avoid unnecessary engineering complexity.

Data Source Investigation

Before implementing an ingestion pipeline, investigate the actual data source.

The developer should understand:

What the source represents

What fields are available

How frequently it updates

What historical coverage exists

How timestamps work

What limitations exist

What reliability issues may occur

Do not assume that a desired field or metric exists before verifying the source.

Documentation

Important decisions should be documented in the appropriate project files.

Documentation should capture:

Project decisions

Analytical methodology

Architecture decisions

Data-source findings

Important assumptions

Known limitations

Lessons learned

Plan Mode

Cursor's Plan mode should be used before major implementation work.

The initial project handoff should ask Cursor to:

Read the project documentation.

Understand the analytical thesis.

Understand the two primary analytical questions.

Inspect the repository.

Investigate the relevant data sources.

Identify technical requirements.

Propose an implementation plan.

Identify uncertainties and assumptions.

Identify potential risks.

Avoid implementing the project until the plan has been reviewed.

The resulting plan should be treated as a proposal, not as unquestionable authority.

Development Philosophy

The project should follow this principle:

Use AI to increase development speed without outsourcing understanding.

The goal is to finish with both:

A strong portfolio project

A strong understanding of how the project works