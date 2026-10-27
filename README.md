# Hobby Recommendation System

A rule-based Python application that provides personalized hobby recommendations and supports wildcard querying based on user preferences. 

The system uses a knowledge base of hobbies categorized across five criteria to match users with ideal activities or allow users to search the knowledge base using custom query filters.

---

## Features

- **Personalized Recommendation System**: Answers a interactive questionnaire to find the single ideal hobby set matching all five of your criteria.
- **Flexible Hobby Querying**: Filter the hobby knowledge base using specific parameters or wildcard (`-`) filters to see all matching activities.
- **Robust Input Validation**: Handles input normalization (lowercasing and whitespace stripping) and guides users back to valid inputs upon mistake.
- **Rule-Based Knowledge Representation**: Organizes hobbies using an object-oriented `Hobby` class structure.

---

## Hobby Classification Criteria

The system categorizes hobbies using the following 5 parameters:

| Parameter | Type | Options | Description |
| :--- | :--- | :--- | :--- |
| **Location** | String | `indoor`, `outdoor` | Environment where the activity takes place. |
| **Category** | String | `active`, `calm` | Physical/energy demand level. |
| **Social Preference** | String | `alone`, `social` | Group size or solo setting. |
| **Budget** | String | `low`, `high` | Expected financial cost. |
| **Tech Preference** | Boolean | `True` (`yes`), `False` (`no`) | Whether the hobby involves technology or digital elements. |

---

## Getting Started

### Prerequisites

- Python 3.x installed on your machine. No external dependencies or libraries are required.

### Execution

1. Clone the repository:
```bash
git clone https://github.com/lujxain/hobby_recommender.git
cd hobby_recommender
```
2. Run the script:

```bash
python hobby_recommender.py
```

---

## Usage Guide

Upon running the program, you will present with a main menu:

```text
Welcome dear user. Choose one of the following: 
1. Get hobby recommendations
2. Query hobbies
3. Quit
```

### Option 1: Get Recommendations
Select `1` to answer 5 guided questions. The system evaluates your exact profile against the knowledge base and outputs matching recommendations.

**Example Input Sequence:**
- Location: `indoor`
- Category: `calm`
- Social: `alone`
- Budget: `low`
- Tech: `yes`

**Output:**
```text
The recommended hobbies for your intersets are: Sudoku - Free Coding Courses - Mobile Puzzle Games - Crossword Puzzles
```

### Option 2: Query Hobbies
Select `2` to run customizable search queries. Enter `-` for any criteria you want to leave open as a wildcard.

**Example Query Input:**
- Location: `outdoor`
- Category: `-`
- Social: `alone`
- Budget: `low`
- Tech: `-`

**Output:**
```text
The query : Hobby(hobby, outdoor, _, alone, low, _) results:
Photography - Digital drawing
Yoga - Gardening - Fishing - Landscape photography
Drone racing
Jogging - Solo cycling
```

---

## Code Architecture

- **`Hobby` Class**: Defines the data structure representing each hobby knowledge entry.
- **`hobbies` List**: The central knowledge base storing predefined `Hobby` instances.
- **`recommend_hobby()`**: Performs exact rule-matching for all 5 parameters.
- **`query_hobby()`**: Handles multi-criteria filtering with support for wildcard searching.
- **`get_valid_input()`**: Helper function for handling terminal IO and validation logic.
- **`get_input()`**: Manages the CLI navigation flow and interactive menu loops.
