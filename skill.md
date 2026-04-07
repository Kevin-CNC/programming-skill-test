---
name: full-stack-coding
description: Use this skill for any software engineering task — writing, fixing,
  refactoring, reviewing, or explaining code across the full stack. Trigger for
  frontend, backend, database, DevOps, algorithm, testing, Git, or clean code
  questions. Also use when the user mentions architecture, API design, CI/CD,
  containerization, or SOLID principles — even if they don't frame it as a
  "coding" request.
---

## Overview
Use this skill when the user asks for help with any software engineering task — writing, reviewing, debugging, or explaining code across the full stack. This covers frontend, backend, databases, DevOps, algorithms, and engineering best practices.

---

## Trigger Conditions
Activate this skill when the user:
- Asks to write, fix, refactor, or explain code in any language
- Requests help with architecture, system design, or API design
- Asks about algorithms, data structures, or Big O complexity
- Needs guidance on testing, CI/CD, containerization, or cloud deployment
- Asks about Git workflows, code reviews, or clean code principles

---

## Execution Instructions

### Step 1 — Identify the Task Layer
Determine which part of the stack the request targets:

| Layer | Covers |
|---|---|
| **Frontend** | HTML, CSS, JavaScript/TypeScript, React, Vue |
| **Backend** | Node.js, Python, Go, REST APIs, Auth |
| **Database** | SQL (PostgreSQL/MySQL) or NoSQL (MongoDB/Redis) |
| **DevOps** | Docker, CI/CD, cloud hosting, monitoring |
| **Algorithms** | Sorting, searching, graph traversal, Big O |
| **Best Practices** | SOLID, Git, testing, clean code |

### Step 2 — Apply the Relevant Knowledge

#### Data Types & Structures
- Primitives: Strings, Integers, Booleans, Floats, Null/Undefined
- Arrays, Objects/Dictionaries, Sets, Stacks (LIFO), Queues (FIFO)

#### Control Flow
- Conditionals: `if / else if / else / switch`
- Loops: `for / while / do-while`
- Recursion: always define a base case to prevent stack overflow

#### Algorithms & Complexity
- `O(1)` Constant · `O(log n)` Binary Search · `O(n)` Linear · `O(n²)` Nested loops
- Sorting: QuickSort, MergeSort, BubbleSort
- Searching: Linear vs Binary Search
- Graph traversal: BFS (queue-based) and DFS (stack/recursive)

#### Frontend
- HTML5 semantic tags: `<article>`, `<nav>`, `<section>`
- CSS3: Flexbox, Grid, responsive media queries
- JavaScript ES6+: arrow functions, destructuring, template literals

#### Backend
- RESTful APIs: `GET / POST / PUT / DELETE`
- Auth: JWT and OAuth2
- Runtimes: Node.js, Python (Django/Flask), Go

#### Databases
- **SQL:** ACID compliance, JOINs (Inner/Left/Right), normalization
- **NoSQL:** document storage, key-value pairs, horizontal scaling

#### SOLID Principles
- **S** — Single Responsibility: one reason to change per class
- **O** — Open/Closed: open for extension, closed for modification
- **L** — Liskov Substitution: subtypes must be substitutable for base types
- **I** — Interface Segregation: no unused method dependencies
- **D** — Dependency Inversion: depend on abstractions, not concretions

#### Git Workflow
```bash
git checkout -b feature-name   # create branch
git add .                      # stage changes
git commit -m "Clear message"  # commit
git rebase main                # rebase before merging
```

#### Testing Strategy
| Type | Tool Examples | Purpose |
|---|---|---|
| Unit | Jest, PyTest | Test individual functions |
| Integration | Supertest, Pytest | Test module interactions |
| E2E | Cypress, Selenium | Simulate user behavior |
| TDD | Any | Write tests before code |

#### DevOps
- CI/CD: GitHub Actions, Jenkins
- Containers: Docker (Images, Containers, Dockerfiles)
- Cloud: AWS (EC2, S3, Lambda), Azure, GCP
- Monitoring: Sentry, LogRocket

### Step 3 — Format the Response

- **Code:** always wrap in fenced blocks with the correct language tag
- **Explanations:** lead with what the code does, then how
- **Debugging:** state the root cause first, then the fix
- **Architecture advice:** use a short prose explanation followed by a diagram or pseudocode if helpful
- **Keep it concise** — avoid restating the question or padding with disclaimers

---

## Reusable Code Patterns

### JavaScript — Async Fetch
```javascript
async function fetchData(url) {
  try {
    const response = await fetch(url);
    if (!response.ok) throw new Error('Network error');
    return await response.json();
  } catch (error) {
    console.error('Fetch failed:', error);
  }
}
```

### Python — List Comprehension
```python
# Squares of even numbers only
squares = [x**2 for x in numbers if x % 2 == 0]
```

### SQL — JOIN with Filter
```sql
SELECT users.name, orders.amount
FROM users
JOIN orders ON users.id = orders.user_id
WHERE orders.status = 'completed';
```

---

## Output Quality Checklist
Before responding, verify:
- [ ] Code is syntactically correct and runnable
- [ ] Variable names are descriptive, not single letters (unless conventional)
- [ ] Edge cases are handled (empty input, null values, errors)
- [ ] The solution matches the complexity requirements (don't over-engineer)
- [ ] Any security implications are flagged (e.g., SQL injection, exposed secrets)

---

## Key Reminders
- Coding mastery is about **logic**, not memorising syntax
- Prefer **readable** code over clever code
- Always consider **technical debt** — easy now can mean costly later
- Recommend tests whenever writing non-trivial logic
- Flag when a task would benefit from a different approach than requested
