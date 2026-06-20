# Questionnaire Design

## Design Goal

The questionnaire should help users understand how they behave in romantic
relationships. It should feel lighter than a clinical scale and more specific
than an entertainment quiz.

## Why Use Questions Instead Of Pure Chat

Open conversation is flexible, but it creates unstable inputs. A questionnaire
gives the system comparable signals across users.

The product advantages are:

- lower user effort,
- more consistent analysis,
- easier scoring,
- easier result comparison,
- less dependence on the LLM inventing structure.

## Stage Structure

The full product concept can be organized into five emotional stages:

| Stage | What it observes |
| --- | --- |
| Heartbeat origin | What first attracts the user. |
| Closeness style | How the user moves toward intimacy. |
| Conflict and defense | What happens when pressure appears. |
| Security needs | What makes the user feel safe or unsafe. |
| Long-term connection | What kind of lasting relationship the user imagines. |

The portfolio README describes a richer version with 18 questions. The current
single-file skill keeps a lighter questionnaire in `SKILL.md`, but this staged
structure is the direction for deeper productization.

## Question Design Rules

Good questions should:

- describe specific relationship scenes,
- avoid obviously correct answers,
- make every option emotionally recognizable,
- map each option to one or more dimensions,
- avoid moral judgment.

Weak questions ask abstractly:

```text
Are you secure or insecure in love?
```

Stronger questions ask through a scene:

```text
If someone you like suddenly replies much slower than usual, what do you most
likely do first?
```

## Progressive Disclosure

The product should present questions one at a time rather than showing a long
form. This lowers psychological pressure and makes the assessment feel like a
guided experience instead of an exam.

## Interview Talking Point

The questionnaire is not just a data collection form. It is the product
interface that turns abstract emotional patterns into observable choices.
