# SentinelFlow

**SentinelFlow** is an explainable machine-learning project for network intrusion detection.

The project explores how machine-learning models can identify potentially malicious network activity from network-flow data and how those predictions can be presented in a way that is understandable to a security analyst.

SentinelFlow is being developed as a cybersecurity + AI portfolio project, with a focus on combining machine learning, explainability, software engineering, and security-oriented evaluation.

> **Project status:** Work in progress.

---

## Overview

Traditional network intrusion detection systems monitor network activity for signs of malicious behaviour.

SentinelFlow focuses on one part of that problem: using machine learning to classify already-extracted network-flow records.

A network flow is a summary of communication between systems. Instead of analysing the actual contents of network packets, the model works with features describing the behaviour of the communication, such as:

- protocol
- connection duration
- packet counts
- transferred bytes
- traffic rates
- connection state
- timing information
- other flow-level statistics

The main goal is to build a model that can answer:

> **Does this network flow look benign or malicious?**

For suspicious flows, SentinelFlow will also explore predicting the most likely attack family and explaining which features contributed most strongly to the model's decision.

---

## Project Pipeline

The intended workflow is:

```text
Network-flow data
        ↓
Data validation and preprocessing
        ↓
Machine-learning model
        ↓
Benign / Malicious prediction
        ↓
Attack-family prediction
        ↓
SHAP explanation
        ↓
Analyst-style dashboard
