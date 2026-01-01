# Multi-Agent Content Generation System

## Overview
This project implements a **true message-driven multi-agent system** that automatically generates
structured, machine-readable content pages from a fixed product dataset.
It was developed for the **Kasparro – Applied AI Engineer Challenge**.

The focus of this project is **system design and agent orchestration**, not UI or domain knowledge.

---

## Problem Statement
Design and implement a modular agentic automation system that:
- Uses independent agents
- Coordinates them through an orchestrator
- Generates structured JSON content automatically

---

## System Architecture
The system is composed of autonomous agents communicating via messages:

- **ParserAgent** – Parses raw product data into an internal model
- **QuestionAgent** – Generates 15+ categorized user questions
- **ContentAgent** – Applies reusable content logic blocks
- **PageAgent** – Assembles and writes JSON output pages
- **Orchestrator** – Routes messages and coordinates execution

Agents do not directly call each other and do not share global state.

---

## Reusable Logic Blocks
- `benefits_block` – Extracts benefits
- `usage_block` – Extracts usage instructions
- `comparison_block` – Compares with a fictional product

---

## Templates
Custom templates are defined for:
- FAQ Page
- Product Description Page
- Comparison Page

---

## Generated Outputs
After execution, the following JSON files are generated:
- `faq.json`
- `product_page.json`
- `comparison_page.json`

All outputs are clean, structured, and machine-readable.

---

## How to Run
```bash
python orchestrator.py
```

Generated files will appear in the `outputs/` directory.

---

## Scope & Assumptions
- Only the provided dataset is used
- No external APIs or research
- Comparison includes a fictional product
- Focus is on agentic system design

---

## Purpose
This project demonstrates production-style agentic architecture with
clear agent boundaries, message passing, and orchestration.
