# Insu Yoon

**AI Engineer · Agentic ML Workflows · Healthcare AI**

I design agent and graph-based workflows that make ML experiments reproducible, auditable,
and safe to run on clinical data. Domain: early cancer detection from SERS/Raman spectra.

[LinkedIn](https://www.linkedin.com/in/yooninsu) · [Velog](https://velog.io/@yooninsu/posts) · [X](https://x.com/yooninsu)

---

## Selected work

**Stateful experiment workflow with LangGraph**
Reviewed our experiment history and found eight recurring failure modes, including ID collisions,
missing records, cohort drift, and differences below the noise floor being reported as findings.
Encoded the workflow as a 20+ node graph, from hypothesis to plan, run, number verification,
interpretation, and commit, with human approval gates and checkpoint resume. Planning, gates, and
LLM drafting are implemented and tested; script execution nodes are the next milestone.

**Multi-agent review for experiment results**
Set up specialized agents for plan critique, executability review, and result auditing. The auditor
checks reported numbers against result files and has caught rounding errors, figures with no source
file, and results traced to a superseded duplicate run. Corrections are logged append-only.

**Experiment tracking for concurrent sessions**
Built a PostgreSQL experiment ledger with phase reservations so parallel agent sessions can't claim
the same experiment ID. It now holds 227 runs across 142 phases and 4,582 metric rows.

**LLM data boundary for clinical data**
Enforced in code, not policy, that only hypotheses, code, and aggregate metrics reach an external
LLM. Spectra and patient or sample-level records stay local, and external tracing is turned off.

**Repeatable deep learning benchmarks**
Ran 12 rounds of CNN and self-supervised benchmarks against a fixed baseline, using shared folds,
5 seeds, paired comparisons, and test samples excluded from pretraining. The setup isolated one
root cause: fine-tuning was degrading pretrained encoders.

---

## Tools

LangGraph · Claude Code · PyTorch · scikit-learn · PostgreSQL · Python · SQL · Docker
