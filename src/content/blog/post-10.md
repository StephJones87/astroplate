---
title: "CS50 Cybersecurity: Why Sites Don’t Store Your Password"
meta_title: "CS50 Cybersecurity Lecture: Password Hashing Explained"
description: "Understanding one-way hash functions and password safety from CS50’s Cybersecurity course with David Malan."
date: 2025-06-25T00:00:00Z
image: "/images/cs50-cybersecurity.jpg"
categories: ["Cybersecurity"]
author: "Steph Jones"
tags: ["cs50", "cybersecurity", "hashing", "passwords", "david malan"]
draft: false
---

Have you ever wondered how websites protect your password—even in the event of a data breach? The key lies in a clever technique: they **never store your actual password**. Instead, they store a **hash** of it, generated using a **one-way hash function**.

A one-way hash function is a special kind of algorithm that takes an input of **arbitrary length** (like your 8- or 20-character password) and produces a **fixed-length** string of characters—typically a long, random-looking sequence. Critically, it’s *one-way*: it’s easy to compute the hash from the input, but computationally infeasible to reverse the process and retrieve the original input from the hash.

When you create an account, the website runs your password through a hash function and saves only the resulting hash. Later, when you log in, your input is hashed again and compared to the stored value. If they match, you’re authenticated—without anyone ever needing to know your actual password.

With additional safeguards like *salting* (adding random data before hashing), even identical passwords will produce unique hashes, making mass password theft harder. It’s one of the most important building blocks in secure software design—and one of the reasons your data can stay safer online.
