# Introduction

Read this once before Day 1. It covers what the program is, what it asks of you, and how to set up.

## What this program is

100 Days of Tech is a guided schedule. We do not produce new lectures. The material for every topic already exists online for free. We give you three things instead:

- A fixed order of topics, so you never spend a week deciding what to learn next.
- Mentors you can ask, and a daily check-in so that someone notices when you stop.
- A set of projects that end in a portfolio on your own GitHub.

The domain is AI/ML, with deep learning included. The path follows the roadmap.sh Machine Learning roadmap: Python and math first, then classical ML, then deep learning, NLP, reinforcement learning, and deployment.

## What to expect

Most people who start a challenge like this do not finish it. That is normal and not a character flaw. The usual reasons are a heavy week at college, a topic that felt too hard, and the feeling of being too far behind to catch up. The program is designed around those three things:

- Buffer days are scheduled in advance.
- The topics in the first month are the simplest, and the difficulty rises slowly.
- Falling behind has a defined recovery. See "If you fall behind" in the README.

The hardest stretch is usually Days 10 to 30. By then the novelty is gone and the math starts. Plan for that dip rather than hoping to avoid it.

You do not need prior ML knowledge. You should be comfortable using a computer and willing to read error messages.

## Time commitment

1 to 1.5 hours a day. If a day only has 30 minutes available, do the task and skip the extra study. A small task done is better than a large one planned.

## Setup

Do this on Day 1. It should take under an hour.

### 1. Accounts

- GitHub: https://github.com
- Kaggle: https://www.kaggle.com
- Google account (for Colab)

### 2. Choose where you will code

Option A, Google Colab (recommended for beginners): go to https://colab.research.google.com and sign in. Nothing to install. Notebooks save to your Google Drive.

Option B, local machine: install Python 3.10 or newer and Git. Then:

```
git clone https://github.com/<your-username>/100-days-of-tech-aiml.git
cd 100-days-of-tech-aiml
python -m venv .venv
source .venv/bin/activate        # on Windows: .venv\Scripts\activate
pip install -r requirements.txt
jupyter notebook
```

### 3. Fork this repository

1. Click Fork at the top of the repository page.
2. In your fork, create a folder called `my-progress`.
3. Inside it, create `daily-log.md` using [../templates/daily-log.md](../templates/daily-log.md).
4. Commit and push. This is your Day 1 task.

### 4. Join the group

Mentors post the daily task there every morning. Reply when you finish, even with one line.

## How to do a day

1. Open the README and find today's row.
2. Study the topic for about 45 minutes. Use the resources listed in the README. Pick one resource per topic and stay with it. Switching between five tutorials on the same topic is one of the most common ways to waste time.
3. Do the task. Type the code yourself. If you copy and run, change something afterward to make sure you understand it.
4. Write your daily log: what you did, what was unclear, what is next.
5. Reply in the group.

## How to use the practice sheets

The `practice` folder contains exercise sheets for the early Python and library days. For each exercise:

- Try it without looking anything up for 10 minutes.
- If you are stuck, look up the specific thing you need, not the whole answer.
- Save your solutions in `my-progress` in a file such as `day03.py` or a notebook such as `day09.ipynb`.
- Where the sheet shows expected output, compare yours.

## Asking for help

Ask in the group, not privately. Write the question so someone can answer it without a call:

- What you were trying to do
- What you tried
- The exact error message, copied as text
- Your code, as text rather than a photo

You will often find the answer while writing the question. That is a good outcome.

## Weekly review

Every Sunday, fill in [../templates/weekly-review.md](../templates/weekly-review.md). It takes 10 minutes. It is the cheapest way to see whether you are really learning or only keeping a streak.
