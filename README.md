# Lodestone Genesis Archive  
**Prototype Edge-Based AI Training Framework**  
*Status: Archived – Superseded by Praetor SC Initiative*
---

## Overview

**Lodestone** was an experimental training framework developed by [Praetor Defense](https://praetordefense.us) to explore sovereign, adaptive AI model training on edge hardware.

This archive contains Lodestone versions **v0.2 through v0.5**, each representing key milestones toward training large language models on limited compute platforms such as Jetson AGX Xavier.

> ⚠️ Lodestone is no longer under active development.  
> It has been officially **archived** following the launch of the **Synthetic Cognition (SC)** initiative.

---

## Included Versions

- `Lodestone v0.2` – Initial runtime scaffolding and tokenizer testing.
- `Lodestone v0.3` – First integration of live loss visualization.
- `Lodestone v0.4` – STRATINET v0.1 introduced for signal-aware memory.
- `Lodestone v0.5` – Stable prototype capable of training 1.1B models with dynamic memory adaptation.

---

## Installation & Usage (v0.5 Only)

### Setup

```bash
# Navigate to v0.5
cd "Lodestone v0.5"

# Create virtual environment
python3 -m venv lodestone-venv
source lodestone-venv/bin/activate

# Manually install dependencies
pip install torch transformers matplotlib
```

*(You may add other libraries used in `main.py` depending on your configuration.)*

### Launch Training

```bash
python3 main.py
```

---

## Changing the Model

In `main.py`, locate the model loading lines:

```python
tokenizer = AutoTokenizer.from_pretrained('tiiuae/falcon-3b-instruct')
model = AutoModelForCausalLM.from_pretrained('tiiuae/falcon-3b-instruct')
```

To change the model, replace `'tiiuae/falcon-3b-instruct'` with any compatible HuggingFace CausalLM model (e.g., `'mistralai/Mistral-7B-Instruct-v0.1'`).

---

## Development Timeline

See `LodestoneDevTimeline.odt` for a full breakdown of version progression and feature milestones.

---

## Image Reference

`Figure_1.png` contains a visualization from STRATINET’s signal tracking in Lodestone v0.5.

---

## License
 
See `LICENSE.txt` and `NOTICE.txt` for details.

---

## Legacy Note

Lodestone represents the foundational research that led to the launch of the **Synthetic Cognition (SC)** initiative — Praetor Defense’s next-generation platform for non-biological cognition.

This repository is archived for historical and technical reference.
```
