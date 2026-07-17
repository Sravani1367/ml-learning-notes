# Machine Learning Notes — Part 2 🤖

---

## 3. AI vs ML vs Deep Learning

**Definition:**
Artificial Intelligence (AI) is the broad field of building machines that can perform tasks requiring human-like intelligence. Machine Learning (ML) is a subset of AI in which machines learn patterns from data. Deep Learning (DL) is a subset of ML that uses multi-layered neural networks to learn complex patterns.

They're **nested inside each other**, like Russian dolls:
```
AI  >  ML  >  Deep Learning
```

![AI vs ML vs Deep Learning](images/ai-vs-ml-vs-dl.svg)

**Beautiful example to remember it:**
- **AI** = A robot that can navigate your house (broad goal: act intelligently)
- **ML** = That robot learns the layout of your house by bumping into furniture a few times and remembering (learns from experience/data)
- **Deep Learning** = The robot uses a neural network with many layers to recognize *your face* vs a stranger's, from raw camera pixels alone (complex pattern recognition via layered "neurons")

**Key takeaway:**
- All Deep Learning is ML, all ML is AI — but **not all AI is ML** (e.g., a chess engine using hardcoded rules is AI but not ML)
- **Not all ML is Deep Learning** (e.g., a spam filter using simple statistics is ML but not DL)

---

## 4. Types of Machine Learning

**Definition:**
Machine Learning is broadly classified into three types based on how the model learns from data: Supervised Learning, Unsupervised Learning, and Reinforcement Learning.

### Supervised Learning
The model is trained on **labeled data** — meaning every input comes with the correct answer attached. The model learns by comparing its guess to the actual answer and correcting itself.

Think of it like studying with an answer key. You solve a question, check the answer key, see where you went wrong, adjust — repeat a thousand times until you're good at it.

**Examples:**
- Predicting house prices (input: size, location → output: price — you already know past sale prices)
- Spam detection (input: email → output: spam/not spam — trained on emails already labeled by humans)
- Predicting whether a student passes or fails based on study hours

### Unsupervised Learning
The model is given **unlabeled data** — no answer key at all. It has to find hidden patterns or groupings on its own.

Think of it like being dropped into a room full of strangers with no name tags, and you naturally start grouping people by who's dressed similarly, who's talking to whom, etc. — nobody told you the categories, you found them yourself.

**Examples:**
- Customer segmentation (grouping shoppers by buying behavior, with no predefined categories)
- Grouping news articles by topic without being told the topics beforehand
- Anomaly detection (spotting a weird transaction pattern without being told what "weird" means beforehand)

---

## 5. Learning Patterns: Instance-Based vs Model-Based

Beyond *what kind* of data a model learns from, there's also *how* it stores and uses what it learned — this splits into two techniques.

### Instance-Based Learning
The system **memorizes the training examples** and, when given something new, compares it directly to those stored examples to make a decision. No general "rule" is built — it just checks "what does this new thing look most similar to?"

Think of it like a kid who hasn't learned math formulas but has memorized every homework problem and its answer — when a new problem looks similar to one they've seen, they just copy the closest match.

**Example:** K-Nearest Neighbors (KNN) — to classify a new fruit as apple or orange, it looks at the *closest* fruits in its memory and goes with the majority.

### Model-Based Learning
The system uses the training data to **build a general model/formula** that captures the underlying pattern — then throws away the raw data and uses that formula to make predictions on new inputs.

Think of it like a kid who studies enough problems to actually *derive the formula* (like distance = speed × time), and now can solve brand new problems without needing to remember every example ever seen.

**Example:** Linear Regression — it learns a formula like `price = 3×size + 50000` from the data, and uses that formula directly for any new house size, even one it's never seen.

---
