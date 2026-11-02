# PRD for WoW Forever Class Chooser

## Primary Persona

WoW Forever players that want to learn about the different classes.

## Use Cases

Primary use case:

1. A player wants help deciding which class to play.

Secondary use cases and side effects:

2. A player wants to explore and learn about the classes from different perspectives.

## Scope

The app should cover:

- all classes
- each class's defining niches and tradeoffs (see `class-niches-and-tradeoffs.md`)
- all specializations of each class

The app does *not* need to cover:

- every single ability of the class

## User Journey

The UI shows three sections:

- "Question" section
- "Result" section
- "Best matches so far" section

1. In the "Question" section, the app displays a new multiple-choice question,
and underneath that, a [Skip this question] button.
If the user clicks [Skip this question], replace it with a different question.

2. The user answers the question.

3. In the "Result" section, the app displays
the classes, sorted according to how closely
the class matches the user's answer.

In the "Best matches so far" section, the app displays:
- all of the user's answers so far, with a [Change] button for each
- a list of the classes, sorted according to how closely
the class matches ALL of the user's answers to all questions so far

At the bottom, the app displays a button:
[Ask me another question]

If the user clicks [Change] for a question,
it re-asks the question in the "Question" section,
clears the "Result" section, and modifies the
"Best matches so far" section as if the question
has not been answered.

4. The user clicks [Ask me another question].
It clears the "Question" and "Result" section
and goes back to Step 1.

### User Journey Example

1. In the "Question" section, the app asks the player:

"How do you feel about tanking?"
[ ] I definitely want the ability to tank.
[ ] I definitely do not want to tank.
[ ] Skip this question

2. The player chooses the option: I definitely want the ability to tank.

3. In the "Result" section, the app displays the following classes:

Answer:
| "I definitely want the ability to tank." |

Classes:
| **Warrior** | (10/10) Designed to tank with Protection spec |
| **Paladin** | (9/10) Designed to tank with Protection spec |
| **Druid** | (8/10) Designed to tank with Feral Combat spec |
| **Shaman** | (5/10) Not designed to tank, but can tank to some degree, with Enhancement spec |

In the "Best matches so far" section, the app displays:

Answers:
| "I definitely want the ability to tank." | [Change] |

Classes:
| **Warrior** | (10/10) Designed to tank with Protection spec |
| **Paladin** | (9/10) Designed to tank with Protection spec |
| **Druid** | (8/10) Designed to tank with Feral Combat spec |
| **Shaman** | (5/10) Not designed to tank, but can tank to some degree, with Enhancement spec |

[Ask me another question]

4. The user clicks [Ask me another question].

1. In the "Question" section, the app asks the player:

"How do you feel about healing?"

[ ] I definitely want the ability to heal.
[ ] I don't care either way.
[ ] I definitely do not want to heal.

2. The player answers: I definitely want the ability to heal.

3. In the "Result" section, the app displays the following classes:

Answer:
| "I definitely want the ability to heal." |

Classes:
| **Priest** | (10/10) Designed to heal with Holy or Discipline spec |
| **Paladin** | (10/10) Designed to heal with Holy spec, exceptional single-target healing |
| **Shaman** | (9/10) Designed to heal with Restoration spec |
| **Druid** | (9/10) Designed to heal with Restoration spec |

In the "best matches so far" section, the app displays:

Answers:
| "I definitely want the ability to tank." | [Change] |
| "I definitely want the ability to heal." | [Change] |

Classes:
| 9/10 | **Paladin** | (9/10) Designed to tank with Protection spec <br>
                       (10/10) Designed to heal with Holy spec, exceptional single-target healing |
| 8/10 | **Druid**   | (8/10) Designed to tank with Feral Combat spec
                       (9/10) Designed to heal with Restoration spec |
| 5/10 | **Shaman**  | (5/10) Not designed to tank, but can tank to some degree, with Enhancement spec
                       (9/10) Designed to heal with Restoration spec |
| 0/10 | **Priest** |  (0/10) Can not tank!
                       (10/10) Designed to heal with Holy or Discipline spec |
