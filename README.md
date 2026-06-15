# SureBo?

**SureBo?** is a statistics proof-of-understanding AI agent designed to determine whether students truly understand a concept rather than merely recognise or repeat an AI-generated answer.

Built for the **Microsoft Buildathon**, the agent is grounded in verified learning materials and worked questions from **NUS ST2334: Probability and Statistics**.

Instead of immediately providing solutions, SureBo? conducts an adaptive, oral-style assessment that asks students to explain their reasoning, apply concepts, distinguish between similar ideas, and interpret statistical results.

## The Problem

Generative AI can provide students with correct answers almost instantly. However, receiving or recognising a correct answer does not necessarily mean that the student understands the underlying concept.

Traditional quizzes may also overestimate understanding because students can:

* Guess the correct option
* Memorise formulas without understanding them
* Follow worked solutions mechanically
* Recognise familiar answer patterns
* Use AI-generated responses without being able to explain the reasoning

SureBo? addresses this gap by testing whether students can independently demonstrate ownership of a statistical concept.

## How It Works

The agent begins with a target concept or worked statistics question and conducts an adaptive assessment based on the student's responses.

Rather than following a fixed list of questions, SureBo? changes its questioning strategy depending on the evidence collected.

The agent may ask the student to:

* Explain a concept in their own words
* Justify why a method or formula is appropriate
* Apply the concept to a new situation
* Distinguish between commonly confused concepts
* Interpret a statistical result in context
* Identify and correct an incorrect line of reasoning
* Explain what would change if the conditions of a question were modified

When the agent detects uncertainty or a misconception, it asks targeted follow-up questions to identify the exact source of the misunderstanding.

## Key Features

### Adaptive Oral-Style Assessment

SureBo? simulates the questioning style of a tutor or oral examiner. Each follow-up question is selected based on the student's previous response rather than being taken from a fixed question bank.

### Precise Misconception Detection

The agent does not simply label an answer as correct or incorrect. It identifies specific misconceptions, such as:

* Confusing mutually exclusive and independent events
* Misinterpreting a confidence interval
* Using a statistical test without checking its assumptions
* Treating correlation as evidence of causation
* Applying the wrong probability distribution
* Performing calculations correctly while interpreting the result incorrectly

### Verified Course Grounding

The agent is grounded in verified **NUS ST2334** course materials and worked questions. This helps keep its explanations, terminology, and assessment criteria aligned with the module's learning objectives.

### Dynamic Questioning Strategy

SureBo? adjusts the type and difficulty of its questions depending on the student's demonstrated understanding.

For example, it may move from:

1. Definition and recall
2. Explanation and reasoning
3. Application to a new scenario
4. Comparison with a similar concept
5. Interpretation of results

A student who gives a partially correct response may receive a diagnostic follow-up, while a student who demonstrates strong understanding may be given a transfer or edge-case question.

### Evidence-Based Concept Passport

At the end of the assessment, SureBo? generates a **Concept Passport** that summarises what the student has demonstrated.

The passport evaluates whether the student can:

* **Explain** the concept in their own words
* **Apply** it to unfamiliar questions
* **Distinguish** it from related or commonly confused concepts
* **Interpret** results within the context of a problem

It also records:

* Evidence from the student's responses
* Misconceptions detected
* Areas of uncertainty
* Recommended topics for revision
* The current level of demonstrated concept ownership

## Example Assessment Flow

```text
Agent:
Why is the normal distribution appropriate for this question?

Student:
Because the sample size is large.

Agent:
A large sample size may allow the sampling distribution of the mean
to be approximated as normal. Is that the same as saying the original
population is normally distributed?

Student:
No. The population itself may still be non-normal.

Agent:
Good. What theorem supports the approximation, and what exactly does
it tell us becomes approximately normal?
```

The agent uses the student's responses as evidence rather than relying only on whether the final numerical answer is correct.

## Concept Passport Example

```text
Concept: Central Limit Theorem

Explain:
Demonstrated. The student explained that the theorem concerns the
sampling distribution rather than the original population.

Apply:
Partially demonstrated. The student applied the theorem correctly
when the sample size was large but was uncertain about small-sample
conditions.

Distinguish:
Demonstrated. The student distinguished population normality from
the approximate normality of the sampling distribution.

Interpret:
Needs improvement. The student had difficulty interpreting standard
error in context.

Misconception Detected:
Initially assumed that a large sample size makes the population
normally distributed.

Recommended Revision:
Review the difference between population distributions, sample
distributions and sampling distributions.
```

## Intended Users

SureBo? is designed for:

* University students studying probability and statistics
* Students revising for tutorials, tests or examinations
* Educators who want stronger evidence of conceptual understanding
* Tutors conducting formative assessments
* Institutions exploring responsible uses of AI in education

## Why SureBo? Is Different

Most educational AI tools focus on helping students obtain answers.

SureBo? focuses on verifying whether students can defend and transfer their understanding.

| Conventional AI Tutor              | SureBo?                                      |
| ---------------------------------- | -------------------------------------------- |
| Provides explanations and answers  | Requires the student to produce explanations |
| Focuses on answer correctness      | Focuses on evidence of understanding         |
| Uses a mostly fixed response style | Adapts its questioning strategy              |
| May allow passive learning         | Encourages active retrieval and reasoning    |
| Ends after solving the question    | Produces a Concept Passport                  |
| Identifies that an answer is wrong | Identifies why the reasoning is wrong        |

## Technology

The prototype was developed using Microsoft AI technologies for the Microsoft Buildathon.

The project uses:

* Microsoft Copilot Studio
* Grounded course knowledge sources
* Adaptive conversational logic
* Structured misconception tracking
* Evidence-based assessment generation
* Shareable agent deployment through a Microsoft-managed environment

> The live agent is hosted under an institution-managed Microsoft account. As a result, the full solution package may not be available for public distribution. This repository documents the agent's design, workflow, features and evaluation approach.

## Responsible AI Considerations

SureBo? is intended as a formative learning and assessment-support tool rather than a replacement for instructors or formal examinations.

Its design includes several safeguards:

* Uses verified module materials as its primary knowledge source
* Requests reasoning instead of accepting unsupported answers
* Separates demonstrated understanding from uncertain understanding
* Records evidence supporting each assessment
* Avoids awarding concept mastery based on a single correct response
* Highlights uncertainty when the available evidence is insufficient
* Provides revision recommendations rather than only a final score

## Project Structure

```text
SureBo/
├── README.md
├── docs/
│   ├── agent-workflow.md
│   ├── assessment-framework.md
│   └── responsible-ai.md
├── screenshots/
├── sample-assessments/
├── concept-passport-examples/
└── demo/
```

## Demo

A project demonstration can be added here:

* **Live agent:** [Add shareable agent link]
* **Demo video:** [Add video link]
* **LinkedIn project post:** [Add LinkedIn link]

## Project Status

SureBo? was developed as a prototype for the Microsoft Buildathon.

Possible future developments include:

* Supporting additional NUS statistics modules
* Allowing educators to define their own concept rubrics
* Tracking concept growth across multiple assessment sessions
* Generating personalised revision plans
* Providing an educator dashboard for class-level misconception trends
* Comparing confidence with demonstrated understanding
* Supporting diagrams, equations and handwritten working
* Validating the assessment framework through student testing

## Team

Developed by **Ryan Tan** as part of the Microsoft Buildathon.

* GitHub: [Add GitHub profile]
* LinkedIn: [Add LinkedIn profile]
* Portfolio: [Add portfolio link]

## Acknowledgements

This project was created using learning materials and worked questions associated with **NUS ST2334: Probability and Statistics**.

Course materials are used only as grounded educational references and are not redistributed in this public repository unless permission has been granted.

