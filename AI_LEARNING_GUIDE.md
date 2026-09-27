AI Learning Guide
Purpose

This project uses AI as an implementation and learning partner.

The goal is not to avoid using AI-generated code.

The goal is to use AI to accelerate development while ensuring the developer understands the resulting system well enough to explain, modify, debug, and defend it.

How AI Should Be Used

AI may:

Write code

Suggest architecture

Research implementation approaches

Explain concepts

Debug problems

Write tests

Review code

Refactor code

Help interpret data

Suggest analytical methods

Help document the project

AI should not silently make important analytical or architectural decisions.

Learning Principle

When introducing an important new concept, explain:

What it is.

Why this project needs it.

How it fits into the system.

What alternatives exist.

Why the proposed approach is appropriate.

What the implementation is doing.

Explanations should be proportional to the difficulty of the concept.

Do not explain basic programming concepts the developer already understands unless requested.

Code Generation

The AI is explicitly allowed to generate complete code.

Do not intentionally withhold code when code is the appropriate solution.

However, generated code should be accompanied by enough explanation for the developer to understand:

what it does

why it exists

important implementation decisions

assumptions

potential failure cases

For significant pieces of code, explain the structure before or after implementation.

Do Not Fake Understanding

The developer should not blindly copy code.

After implementing a significant component, the developer should be able to answer questions such as:

What does this component do?

What data enters it?

What data leaves it?

Why was it designed this way?

What happens when the input is invalid?

What assumptions does it make?

How would I modify it?

AI should help the developer reach that understanding.

Analytical Decisions

AI must distinguish between:

Fact

Directly supported by the data or an authoritative source.

Derived result

Calculated from available data.

Interpretation

An explanation supported by evidence but not directly observed.

Assumption

Something that has not yet been verified.

Never present an assumption as a fact.

Data Investigation

When working with a new dataset:

Inspect the actual data.

Determine its grain.

Inspect its schema.

Check data quality.

Identify relevant fields.

Determine what can actually be measured.

Only then design transformations and analysis.

Do not design an analytical metric first and assume the dataset supports it.

Debugging

When something breaks:

Reproduce the problem.

Identify the error.

Determine the root cause.

Explain the cause.

Fix it.

Test the fix.

Explain why the fix works.

Do not repeatedly change code without understanding the failure.

Architecture

Prefer the simplest architecture that satisfies the requirements.

Do not introduce technologies solely because they appear impressive on a resume.

Every major component should have a reason to exist.

Research

When external information is required:

Prefer primary/official sources.

Verify current information.

Record important sources.

Distinguish documented facts from interpretation.

Do not invent unavailable information.

AI Output Review

Before accepting a significant AI-generated implementation, check:

Does it match the project requirements?

Does it use the actual data schema?

Are assumptions documented?

Is error handling appropriate?

Is the implementation unnecessarily complex?

Can the developer explain it?

Developer Responsibility

The developer remains responsible for understanding and validating the project.

AI assistance does not replace:

testing

data validation

source verification

analytical reasoning

code review

documentation

understanding the final system