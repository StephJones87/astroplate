---
title: "Getting Started on Your First Coding/Data Project"
meta_title: "Kickstart Your First Data Project with Confidence"
description: "A beginner-friendly guide to taking your first steps in real-world coding and data projects."
date: 2024-05-03T00:00:00Z
image: "/images/data-projects-shoes.png"
categories: ["Data Projects"]
author: "Steph"
tags: ["data", "python", "portfolio", "beginner"]
draft: false
---

So you've been dabbling in coding and you're ready to make it feel a bit more *real*—like you're actually building something. But how do you take that leap from tutorials to your first proper project?

## Shift Your Mindset: It's Not Just About Showing Off

People often say, “Build a portfolio of projects to show employers!” And that’s valid advice. But if you're a perfectionist like me, aiming to impress others can sometimes make you freeze up. You end up with 12 half-finished projects and a creeping sense of inadequacy.

So here’s my take: don't build a portfolio for others—build one for yourself.

Let your projects document your learning. Let them remind you, *“I can do this.”*

## What Even *Is* a Data Project?

That depends on your interests, but a simple data project usually has four main steps:

### 1. Find Some Data

Good news: data is **everywhere**.

- Try the [Office for National Statistics](https://www.ons.gov.uk/) for well-structured public data.
- Or, if you’re feeling more adventurous, [Kaggle](https://www.kaggle.com/) is an incredible resource for quirky, fun, and beginner-friendly datasets. For example, [this collection of fun datasets](https://www.kaggle.com/code/rtatman/fun-beginner-friendly-datasets) includes everything from avocado prices to shoe reviews. I found one on women's shoes—so let's use that.

Once you've downloaded your CSV, **open it in Excel**. Yep, Excel. It’s a fast way to take a first look:

- What columns are there?
- How many rows?
- Is the dataset *long* (many rows) or *wide* (many columns)?
- Does anything look messy?

This visual check only takes 30 seconds and helps you start forming questions about the data.

### 2. Load It Into Python

Now let’s get it into your code environment. I recommend using [Google Colab](https://colab.research.google.com/) for this—it’s fast, free, and doesn't require setup.

```python
import pandas as pd
data = pd.read_csv('data_womens_shoes.csv') # needs to match your filename
data.shape  # shows number of rows and columns
data.columns  # lists column names
data.head()  # shows the first 5 rows
data.info()  # info on data types and missing values
data.describe()  # summary stats for numeric columns 
```

Questions to ask:

- Are there missing values?
- Which columns look useful?
- What story might this data tell?

This exploration phase is **crucial**. It’s where ideas for analysis or visuals often emerge.

### 4. Do Something With It

Now you decide where your project goes:

- **Want to analyse trends?** Try grouping by product type or price range and calculating averages.
- **Want to visualise it?** Use `matplotlib` or `seaborn` to create bar charts, scatter plots, or histograms.
- **Want to practice data cleaning?** Try handling missing values, renaming columns, or filtering rows.

Here's a simple visualisation example:

```python
import seaborn as sns
import matplotlib.pyplot as plt

sns.histplot(data['prices.amountMax'], bins=20)
plt.title('Distribution of Max Shoe Prices')
plt.xlabel('Price')
plt.ylabel('Count')
plt.show()
```

And if you're feeling brave, you can **save your cleaned or summarised dataset** with:

```python
data.to_csv('cleaned_shoes_data.csv', index=False)
```

Exporting it can be a nice final step—especially if you want to revisit it later or include it in a portfolio.

## Final Thoughts

The first project isn’t about perfection. It’s about momentum.

Let yourself play. Let the questions guide you. Your only goal? **Finish something**—even something small.

Then celebrate it. You’ve taken a real step from "learning to code" to "being a coder."

---

👟 *P.S. If you did end up exploring that shoe dataset, I’d love to hear what you discovered. Tag me or share it with a friend—let’s keep building.* 💙
