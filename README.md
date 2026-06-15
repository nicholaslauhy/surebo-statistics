# SureBo Statistics Knowledge Base

The **SureBo Statistics Knowledge Base** is a structured collection of verified statistics concepts, worked questions, misconception patterns, and assessment criteria used to support the SureBo? proof-of-understanding AI agent.

It is designed to help the agent assess whether a student genuinely understands a statistical concept rather than merely recognising or repeating a correct answer.

The knowledge base is primarily aligned with concepts covered in **NUS ST2334: Probability and Statistics**.

## Purpose

The knowledge base provides SureBo? with reliable and structured reference material for:

* Generating concept-focused assessment questions
* Checking whether student explanations are accurate
* Detecting common statistical misconceptions
* Creating targeted follow-up questions
* Distinguishing partial understanding from genuine concept ownership
* Producing evidence-based Concept Passports
* Reducing unsupported or hallucinated explanations

Unlike a standard collection of lecture notes, the knowledge base is organised around how understanding can be demonstrated and assessed.

## What the Knowledge Base Contains

The repository may include the following types of content:

### Concept Summaries

Clear explanations of important statistics concepts, including:

* Core definitions
* Mathematical intuition
* Assumptions
* Conditions for use
* Common interpretations
* Related concepts
* Common points of confusion

### Worked Questions

Worked examples that demonstrate:

* How to identify the appropriate statistical method
* How to apply formulas correctly
* How to justify each step
* How to interpret results in context
* How to recognise incorrect approaches

### Misconception Library

A collection of common mistakes and misunderstandings, such as:

* Confusing independent and mutually exclusive events
* Treating correlation as causation
* Misinterpreting p-values
* Assuming a large sample makes the population normally distributed
* Confusing population parameters with sample statistics
* Applying a probability distribution without checking its assumptions
* Interpreting confidence intervals incorrectly
* Using the correct calculation but giving the wrong contextual interpretation

Each misconception entry can include:

* The incorrect belief
* Why it is incorrect
* Indicators that a student may hold the misconception
* Diagnostic questions
* Corrective follow-up questions
* Evidence required to demonstrate corrected understanding

### Assessment Rubrics

Rubrics define what counts as evidence that a student can:

* **Explain** a concept
* **Apply** it to a problem
* **Distinguish** it from related concepts
* **Interpret** results correctly

These rubrics help SureBo? evaluate understanding consistently instead of relying only on answer correctness.

### Diagnostic Questions

Questions designed to reveal how a student is reasoning.

Examples include:

```text
Why is this probability distribution appropriate for the situation?

What assumption must hold before this method can be used?

How would your answer change if the sample size were smaller?

What is the difference between the population distribution and the
sampling distribution?

Can the final numerical answer be correct even if the method used was
inappropriate? Explain.
```

### Transfer Questions

Transfer questions test whether students can apply a concept in a new or unfamiliar context rather than repeating a memorised procedure.

These questions may involve:

* Changing the context of a familiar problem
* Modifying an assumption
* Comparing two possible methods
* Identifying an edge case
* Explaining why a method fails
* Interpreting the same result for different audiences

## Knowledge Structure

Each concept can be stored using a consistent format.

```text
Concept Name

1. Definition
2. Intuition
3. Key Formulae
4. Assumptions
5. Conditions for Use
6. Worked Example
7. Common Misconceptions
8. Diagnostic Questions
9. Application Questions
10. Distinction Questions
11. Interpretation Questions
12. Mastery Criteria
13. Related Concepts
```

A structured concept entry may look like this:

```yaml
concept: Central Limit Theorem

definition:
  The sampling distribution of the sample mean approaches a normal
  distribution as the sample size increases, under suitable conditions.

key_distinctions:
  - Population distribution
  - Sample distribution
  - Sampling distribution

common_misconceptions:
  - A large sample size makes the population normally distributed.
  - The theorem applies to every statistic.
  - The sample observations themselves become normally distributed.

diagnostic_questions:
  - What exactly becomes approximately normal?
  - Does the original population need to be normally distributed?
  - How does sample size affect the approximation?

mastery_criteria:
  explain:
    Student explains that the theorem concerns the sampling distribution.

  apply:
    Student identifies when the approximation is reasonable.

  distinguish:
    Student distinguishes population normality from sampling distribution
    normality.

  interpret:
    Student interprets the sample mean and standard error in context.
```

## Suggested Topic Coverage

The knowledge base may cover areas such as:

### Probability

* Sample spaces and events
* Conditional probability
* Independence
* Bayes' theorem
* Counting methods
* Law of total probability

### Random Variables

* Discrete random variables
* Continuous random variables
* Expected value
* Variance
* Covariance
* Transformations

### Probability Distributions

* Bernoulli distribution
* Binomial distribution
* Geometric distribution
* Poisson distribution
* Uniform distribution
* Exponential distribution
* Normal distribution

### Sampling Distributions

* Sample mean
* Sample proportion
* Standard error
* Central Limit Theorem
* Chi-square distribution
* Student's t-distribution

### Estimation

* Point estimators
* Bias
* Consistency
* Efficiency
* Maximum likelihood estimation

### Confidence Intervals

* Confidence intervals for means
* Confidence intervals for proportions
* Interpretation of confidence levels
* Margin of error
* Sample size considerations

### Hypothesis Testing

* Null and alternative hypotheses
* Test statistics
* Rejection regions
* p-values
* Type I and Type II errors
* Statistical power
* One-tailed and two-tailed tests

## How SureBo? Uses the Knowledge Base

SureBo? retrieves relevant knowledge based on the concept being assessed.

The agent uses the knowledge base to:

1. Identify the target concept
2. Retrieve verified explanations and assumptions
3. Select an appropriate diagnostic question
4. Analyse the student's reasoning
5. Match the response against known misconceptions
6. Choose a targeted follow-up question
7. Collect evidence across multiple dimensions
8. Generate a Concept Passport

The agent is not intended to simply repeat content from the knowledge base. It uses the content as a reference for adaptive assessment.

## Concept Passport Alignment

Each concept is assessed across four dimensions:

| Dimension   | Evidence Required                                           |
| ----------- | ----------------------------------------------------------- |
| Explain     | Student describes the concept accurately in their own words |
| Apply       | Student uses the concept correctly in a new problem         |
| Distinguish | Student separates the concept from similar ideas            |
| Interpret   | Student explains the statistical meaning in context         |

A student should not be marked as having mastered a concept based on one correct final answer alone.

## Content Quality Guidelines

Every knowledge entry should:

* Use accurate statistical terminology
* Clearly state assumptions and limitations
* Separate formulas from interpretation
* Avoid presenting shortcuts as universal rules
* Include at least one misconception
* Include diagnostic and transfer questions
* Define what mastery looks like
* Be understandable without relying on unexplained notation
* Be reviewed before being used for assessment

## Responsible Use

The SureBo Statistics Knowledge Base is intended for educational and formative assessment purposes.

It should not be used to:

* Replace formal grading without educator oversight
* Automatically assign high-stakes academic results
* Redistribute copyrighted course material without permission
* Claim that a student has mastered a concept based on limited evidence
* Generate unsupported explanations outside the verified content

The agent should clearly indicate uncertainty when the available evidence is insufficient.

## Copyright and Access

This repository does not publicly include copyrighted NUS teaching materials and is based on my own knowledge of NUS ST2334.

## Project Status

The knowledge base was developed as part of the **SureBo?** prototype for the Microsoft Buildathon.

Future improvements may include:

* Expanding coverage across all ST2334 topics
* Creating machine-readable concept schemas
* Adding misconception severity levels
* Linking concepts through a knowledge graph
* Adding prerequisite relationships
* Introducing confidence scores for retrieved content
* Supporting educator review and approval workflows
* Tracking version history for each concept
* Adding benchmark student responses
* Evaluating misconception detection accuracy

## Related Project

**SureBo?** is the AI assessment agent that uses this knowledge base to conduct adaptive oral-style assessments and generate evidence-based Concept Passports.

* Main agent repository: [Click Me!](https://github.com/nicholaslauhy/ai-agent-surebo)
* Live agent link: [Click Me! (only for NUS students)](https://m365.cloud.microsoft/chat/?titleId=T_8de55795-d602-4752-1024-6bdf20dfde4b&source=embedded-builder)
* Demo video: [Click Me!](https://youtu.be/HHv0G7ei1vM)

## Author

Developed by **Nicholas Lau** for the Microsoft Buildathon.

* GitHub: [Click Me!](https://github.com/nicholaslauhy)
* LinkedIn: [Click Me!](https://www.linkedin.com/in/nicholas-lau-688509292/)

## Acknowledgements

This project draws on concepts associated with **NUS ST2334: Probability and Statistics**, but is in no way associated with the National University of Singapore.

All original course materials remain the property of their respective authors and institutions. Please use the knowledge in this website with discretion.
