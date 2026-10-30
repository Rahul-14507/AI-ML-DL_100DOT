# 100 Days of Tech: AI/ML and Deep Learning

A 100-day structured learning program run by our college club. It covers Python, the math behind machine learning, classical ML, deep learning, NLP and Transformers, reinforcement learning, and deployment.

The learning material for all of this is free and already online. What most people lack is a clear order to follow, someone to ask when they are stuck, and a reason to show up on day 30 when the excitement has worn off. This repository is the order. The mentors and the daily check-in are the rest.

The roadmap follows the [roadmap.sh Machine Learning roadmap](https://roadmap.sh/machine-learning). Start with [docs/00-introduction.md](docs/00-introduction.md) before Day 1.

## Contents

1. [How the program works](#how-the-program-works)
2. [Weekly rhythm](#weekly-rhythm)
3. [Rules and completion](#rules-and-completion)
4. [Repository layout](#repository-layout)
5. [The 100-day roadmap](#the-100-day-roadmap)
6. [Projects](#projects)
7. [Free resources](#free-resources)
8. [If you fall behind](#if-you-fall-behind)

## How the program works

Plan for 1 to 1.5 hours a day. Each day has one topic and one task. The loop is the same every day:

1. Read the day's entry in the roadmap below.
2. Study the topic for about 45 minutes using the resources listed for that phase.
3. Do the day's task.
4. Write 2 to 3 lines in your daily log: what you did, what confused you, what you will do tomorrow.

The task matters more than the study time. Watching a video about NumPy teaches you much less than writing ten lines of NumPy that fail and then fixing them.

A mentor task for the day is posted in the group each morning at a fixed time. Reply there when you finish. A missing reply is noticed.

## Weekly rhythm

| Day of week | What happens |
|---|---|
| Monday to Thursday | One topic per day: study for about 45 minutes, then a task of 15 to 30 minutes in Colab or locally. |
| Friday | Practice day. Problems, or a small Kaggle exercise, that combine what the week covered. |
| Saturday | Live session of 60 to 90 minutes. A mentor demonstrates the week's idea, clears doubts, and gives a short challenge. |
| Sunday | A 10-question quiz that counts toward the leaderboard, plus catch-up time for anything you missed. Sunday is also the safe day to rest. |

Buffer days are built into the roadmap (Days 25, 35, 58 and 90). They exist because exams, festivals and illness will happen. Use them to catch up rather than to get ahead.

## Rules and completion

- Fork this repository. Do all your work in your own fork.
- Keep a file called `my-progress/daily-log.md` in your fork. Use the format in [templates/daily-log.md](templates/daily-log.md).
- Share your fork link once on the registration form. Mentors check forks weekly. Nobody is publicly ranked by volume of commits.
- Copy your own code. Do not copy a solution you do not understand. A task you did badly and understood is worth more than a perfect one you pasted.

To receive the completion certificate:

- At least 70 daily log entries across the 100 days
- At least 3 of the 5 mini-projects submitted
- The capstone project submitted and presented on Day 99

Streak badges are given at Days 25, 50, 75 and 100. The weekly leaderboard rewards the Sunday quiz score and consistency.

## Repository layout

```
100-days-of-tech-aiml/
  README.md                  this file
  requirements.txt           Python packages used in the first phases
  docs/
    00-introduction.md       read this first: setup, daily workflow, expectations
  templates/
    daily-log.md             format for your daily log
    weekly-review.md         Sunday self-review
  practice/
    days-03-08-python/       exercise sheets for the Python block
    days-09-13-libraries/    exercise sheets and data for NumPy, Pandas, Matplotlib, Seaborn
```

More practice folders are added as the program reaches each phase.

## The 100-day roadmap

### Phase 1: Foundations (Days 1-25)

| Day | Topic | Task |
|---|---|---|
| 1 | Orientation and setup | Create GitHub and Kaggle accounts. Fork this repo. Run a "hello world" in Google Colab. Make your first commit. |
| 2 | Introduction: what an ML engineer does | Read about ML Engineer vs AI Engineer. Write five lines on which role interests you and why. |
| 3 | Python: syntax, variables and data types | Complete `practice/days-03-08-python/exercises.md`, Day 3 section. |
| 4 | Python: lists, tuples, sets, dictionaries | Day 4 section of the practice sheet. |
| 5 | Python: loops and conditionals | Day 5 section. |
| 6 | Python: functions and built-ins | Day 6 section. |
| 7 | Python: object-oriented programming | Day 7 section. |
| 8 | Python mini project | Build the student grade manager described in the Day 8 section. |
| 9 | NumPy | `practice/days-09-13-libraries/exercises.md`, Day 9 section. |
| 10 | Pandas I: loading, inspecting, selecting | Day 10 section, using `data/students.csv`. |
| 11 | Pandas II: missing data, groupby, merge | Day 11 section. |
| 12 | Matplotlib | Day 12 section. |
| 13 | Seaborn | Day 13 section. |
| 14 | Project 1: exploratory data analysis | Pick a dataset from Kaggle. Produce a notebook with at least 5 questions asked and answered using Pandas and plots. |
| 15 | Linear algebra I: scalars, vectors, tensors | Represent vectors and matrices in NumPy. Compute dot products by hand and in code. |
| 16 | Linear algebra II: matrix operations, determinant, inverse | Multiply, transpose and invert matrices in NumPy. Check `A @ inv(A)`. |
| 17 | Linear algebra III: eigenvalues, diagonalization, SVD | Compute eigenvectors and an SVD with NumPy. Reconstruct a small matrix from its SVD. |
| 18 | Calculus I: derivatives and partial derivatives | Differentiate five functions by hand. Verify numerically with a small finite-difference function. |
| 19 | Calculus II: gradient, Jacobian, Hessian | Write code for gradient descent on f(x, y) = x^2 + y^2. Plot the path. |
| 20 | Discrete mathematics | Work through sets, logic, combinatorics and graphs basics. Solve 10 counting problems. |
| 21 | Statistics I: basic concepts and descriptive statistics | Compute mean, median, variance and quartiles for `students.csv` by hand-written functions, then compare with Pandas. |
| 22 | Statistics II: graphs and inferential statistics | Run a hypothesis test (for example a t-test with SciPy) on two groups from a dataset. |
| 23 | Probability I: basics and Bayes' theorem | Solve 8 probability problems. Implement Bayes' rule for a medical-test example. |
| 24 | Probability II: random variables, PDFs, distributions | Sample from normal, binomial and Poisson distributions. Plot histograms against theory. |
| 25 | Checkpoint | Math quiz and revision. Update your log. Use the day to catch up. |

### Phase 2: Data and classical machine learning (Days 26-58)

| Day | Topic | Task |
|---|---|---|
| 26 | Data sources: SQL basics | Practice SELECT, WHERE, ORDER BY, GROUP BY on a sample database (SQLite). |
| 27 | SQL joins and a look at NoSQL | Write 5 join queries. Read how document stores differ from tables. |
| 28 | APIs and other data sources | Pull data from a public API with `requests` and load it into a DataFrame. |
| 29 | Data formats: CSV, Excel, JSON, Parquet | Convert one dataset between all four formats. Compare file sizes. |
| 30 | Data cleaning I: missing values and duplicates | Clean a messy dataset. Document each decision in a markdown cell. |
| 31 | Data cleaning II: outliers and preprocessing | Detect outliers with IQR and z-score. Decide whether to keep, cap or drop. |
| 32 | Feature engineering | Create 5 new features from an existing dataset. Encode categorical columns. |
| 33 | Feature scaling and normalization | Apply standard and min-max scaling. Show the effect on a KNN-style distance. |
| 34 | Feature selection and dimensionality reduction (overview) | Select features using correlation and a tree-based importance score. |
| 35 | Buffer day | Catch up. Re-run your Project 1 notebook cleanly from top to bottom. |
| 36 | What machine learning is, and its types | Write a one-page note on supervised, unsupervised, semi-supervised, self-supervised and reinforcement learning with one real example each. |
| 37 | The scikit-learn workflow | Load a dataset, split, fit, predict, score. Do it once end to end on the Iris data. |
| 38 | Train/test split, pipelines | Rebuild Day 37 using a `Pipeline`. Explain why data leakage happens. |
| 39 | Linear regression | Fit a regression on a housing dataset. Interpret the coefficients. |
| 40 | Polynomial regression | Fit degrees 1 to 10. Plot training and validation error. Identify overfitting. |
| 41 | Regularization: Lasso, Ridge, Elastic Net | Compare the three on the Day 40 data. Look at which coefficients go to zero. |
| 42 | Logistic regression | Train a classifier. Interpret probabilities and the decision threshold. |
| 43 | K-Nearest Neighbors | Train KNN for several values of k. Plot accuracy against k. |
| 44 | Support Vector Machines | Try linear and RBF kernels. Visualize a decision boundary on 2D data. |
| 45 | Decision trees | Train a tree. Plot it. Explain one prediction by following the path. |
| 46 | Random forests | Compare a single tree with a forest. Read the feature importances. |
| 47 | Gradient boosting | Train a gradient boosting model. Compare with the forest. |
| 48 | Evaluation I: accuracy, precision, recall, F1, confusion matrix | Compute each metric by hand from a confusion matrix, then with scikit-learn. |
| 49 | Evaluation II: ROC-AUC, log loss | Plot an ROC curve. Explain when accuracy misleads (imbalanced data). |
| 50 | Validation: K-fold, LOOCV, hyperparameter tuning | Use cross-validation and `GridSearchCV` on one model. |
| 51 | Project 2: end-to-end supervised ML | Pick a Kaggle tabular dataset. Clean, model, evaluate and write a README for the project. |
| 52 | Unsupervised learning I: K-means | Cluster a dataset. Pick k using the elbow method and silhouette score. |
| 53 | Unsupervised learning II: hierarchical and probabilistic clustering | Draw a dendrogram. Try a Gaussian mixture. |
| 54 | Dimensionality reduction: PCA | Reduce a dataset to 2D. Plot and interpret the explained variance. |
| 55 | Autoencoders (concept), semi- and self-supervised learning | Read and summarize the idea in your own words. Sketch the architecture. |
| 56 | Project 3 (part 1): customer segmentation | Choose a dataset. Clean and explore it. |
| 57 | Project 3 (part 2) | Cluster, interpret the groups, and write the findings. |
| 58 | Midpoint checkpoint | Review your 57 days. Update your log. Pick one earlier topic to revisit. Catch up. |

### Phase 3: Deep learning (Days 59-68)

| Day | Topic | Task |
|---|---|---|
| 59 | Neurons and the perceptron | Implement a perceptron in NumPy that learns AND and OR. |
| 60 | Forward pass and activation functions | Build a 2-layer network forward pass in NumPy. Plot ReLU, sigmoid, tanh. |
| 61 | Loss functions and backpropagation | Work through backprop for a tiny network by hand. Check the gradient numerically. |
| 62 | Optimizers | Compare SGD, momentum and Adam on a toy problem. |
| 63 | PyTorch: tensors and autograd | Repeat Day 61 using autograd. |
| 64 | The training loop | Train an MLP on MNIST in PyTorch. |
| 65 | Regularization: dropout, batch normalization, early stopping | Add each to your MNIST model. Compare validation curves. |
| 66 | Convolutional neural networks | Build a small CNN. Count its parameters. |
| 67 | CNN architectures and transfer learning | Fine-tune a pretrained model on a small image dataset. |
| 68 | Project 4: image classifier | Build and evaluate an image classifier on a dataset you choose. Write a README. |

### Phase 4: NLP, Transformers and LLMs (Days 69-76)

| Day | Topic | Task |
|---|---|---|
| 69 | Text preprocessing and embeddings | Tokenize text. Train or load word embeddings. Find nearest words. |
| 70 | RNNs and LSTMs | Train a small sequence model. Note where it struggles on long text. |
| 71 | Attention | Implement scaled dot-product attention in NumPy for a toy example. |
| 72 | The Transformer architecture | Draw the architecture from memory. Explain each block in two lines. |
| 73 | Hugging Face basics | Use `pipeline` for sentiment, summarization and translation. |
| 74 | LLMs and prompting | Compare 3 prompt styles on one task. Record where each fails. |
| 75 | Retrieval-augmented generation (RAG) | Build a small question-answering tool over a text file. |
| 76 | Project 5: text project | Build a text classifier or a RAG tool. Write a README. |

### Phase 5: Reinforcement learning (Days 77-80)

| Day | Topic | Task |
|---|---|---|
| 77 | RL basics: agent, environment, reward, MDPs | Explain the loop with a worked example on paper. |
| 78 | Q-learning | Implement tabular Q-learning on a small grid or Gymnasium environment. |
| 79 | Deep Q-Networks | Read and run a DQN example. Describe the replay buffer and target network. |
| 80 | Policy gradient and actor-critic | Summarize how they differ from value-based methods. Run one example. |

### Phase 6: Deployment and MLOps (Days 81-90)

| Day | Topic | Task |
|---|---|---|
| 81 | Saving and loading models | Save a scikit-learn and a PyTorch model. Reload and verify predictions match. |
| 82 | Serving a model with FastAPI | Wrap a model in an API with one prediction endpoint. |
| 83 | Building a demo with Streamlit | Build a simple UI for one of your models. |
| 84 | Docker basics | Containerize your FastAPI app. |
| 85 | Experiment tracking with MLflow, and Git for ML projects | Log 3 runs of a model with different parameters. |
| 86 | Deploying | Deploy a demo to Hugging Face Spaces or a free cloud tier. |
| 87 | Monitoring and data drift | Simulate drift on a dataset and observe the metric drop. |
| 88 | Ethics, bias and explainability | Check a model for group-level performance gaps. Try SHAP or permutation importance. |
| 89 | Interview preparation | Answer 20 ML interview questions out loud. Record what you could not explain. |
| 90 | Buffer day | Catch up before the capstone. |

### Phase 7: Capstone (Days 91-100)

| Day | Topic | Task |
|---|---|---|
| 91 | Team formation and proposal | Form a team of 3 to 4. Submit a one-page proposal: problem, data, approach, success measure. |
| 92 | Data collection and cleaning | Gather and clean your data. |
| 93 | Exploratory analysis | Analyze the data and write down the findings that shape modelling. |
| 94 | Baseline model | Build the simplest model that works. Record its score. |
| 95 | Improve the model | Improve on the baseline and justify each change. |
| 96 | Deploy | Make it usable by someone else, as an app or an API. |
| 97 | Documentation | Write the project README: problem, method, results, how to run. |
| 98 | Demo rehearsal | Run a 5-minute presentation twice. Cut anything that does not help. |
| 99 | Demo day | Present to the club and mentors. |
| 100 | Wrap-up | Final quiz, reflections, certificates and next steps. |

Days 59 to 90 follow the usual order for deep learning, NLP and deployment. Mentors may adjust them as the program runs. Any change is announced in the group and updated here.

## Projects

| Project | Day | Focus |
|---|---|---|
| 1 | 14 | Exploratory data analysis |
| 2 | 51 | End-to-end supervised ML |
| 3 | 56-57 | Clustering and segmentation |
| 4 | 68 | Image classification |
| 5 | 76 | Text classifier or RAG tool |
| Capstone | 91-99 | Team project, deployed and presented |

Each project goes in its own folder in your fork with a README that states the problem, the data source, what you tried, the final result, and one thing that did not work. The last item is required. It shows more about your understanding than a good score does.

## Free resources

Use these as study material for the days above. You do not need all of them.

- Python: the official Python tutorial, Kaggle Learn (Python, Pandas, Data Visualization)
- Math: 3Blue1Brown's Essence of Linear Algebra and Essence of Calculus, Khan Academy for statistics and probability, StatQuest on YouTube
- Classical ML: Kaggle Learn (Intro and Intermediate ML), the scikit-learn user guide, Andrew Ng's Machine Learning Specialization (can be audited)
- Deep learning: the official PyTorch tutorials, 3Blue1Brown's neural networks series, Andrej Karpathy's Neural Networks: Zero to Hero, fast.ai
- NLP and LLMs: the Hugging Face course
- Reinforcement learning: the Hugging Face Deep RL course, Sutton and Barto's book (free online)
- Deployment: the FastAPI, Streamlit, Docker and MLflow documentation

## If you fall behind

Almost everyone does at some point. The rule is simple: do not try to repay the missed days. Skip to the current day, spend 20 minutes skimming what you missed, and carry on. You can return to the skipped topics on a buffer day or at the weekend.

Missing 3 days in a row will get a message from a mentor. That is not a warning. It is a check on whether something is blocking you.

Questions about a task go in the group chat, not in private messages, so others can learn from the answer. Say what you tried and paste the error.
