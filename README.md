# AI Governance Knowledge Assistant on Amazon Bedrock

A retrieval-augmented assistant that answers questions about U.S. federal AI governance using only a curated corpus of NIST frameworks, technical reports, executive orders, and draft legislation -- with mandatory source citation, contextual-grounding and denied-topic guardrails, and a full per-query audit log. The project was built to test not just whether a "governed AI" system can be configured with the right controls, but whether those controls behave consistently once built. Systematic evaluation found that grounding and refusal behavior, while functioning as configured, are sensitive to query phrasing and retrieval breadth -- the same underlying content can be answered or refused depending on how a question is asked, a finding with direct implications for how governance claims about RAG systems should be evaluated (see `eval/eval_results.md`).

## Project Resources

**Repository:** [governed-ai-rag-bedrock](https://github.com/kchoover14/governed-ai-rag-bedrock)

**Data:**

  - 16 public federal AI-governance documents: the NIST AI Risk Management Framework (AI 100-1), its Generative AI Profile (AI 600-1) and Playbook, five NIST AI technical reports, seven executive orders (Biden and Trump administrations), America's AI Action Plan, and draft federal legislation (GAAIA). All sourced from nist.gov, airc.nist.gov, and the Federal Register / govinfo.gov, and ingested into an Amazon Bedrock Knowledge Base with per-document category and status metadata (e.g., `rmf`, `report`, `policy`, `legislation`; `status: draft` / `rescinded`).

**Code:**

- `notebooks/governed_rag.ipynb` -- corpus ingestion config, guardrail setup, RAG query pipeline (`ask`), decision logging (`ask_and_log`), and the evaluation runner
- `corpus/*.metadata.json` -- per-document category/status metadata sidecars for Bedrock Knowledge Base ingestion

**Project Artifacts:**

- Decision log (`decision_log.jsonl`) -- full per-query audit trail: timestamp, query, answer, retrieved sources, guardrail action, latency
- Evaluation results (`eval/eval_results.md`)

**Environment:**

- `requirements.txt` -- install with `pip install -r requirements.txt`

**License:**

- Code and scripts © Kara C. Hoover, licensed under the [MIT License](LICENSE).
- Data, figures, and written content © Kara C. Hoover, licensed under [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/).

## Tools & Technologies

**Languages:** Python

**Tools:** AWS Bedrock | Amazon Bedrock Knowledge Bases | Amazon S3 | Amazon S3 Vectors | Amazon Bedrock Guardrails | Jupyter

**Packages:** boto3

## Expertise

**Domain Expertise:** AI governance | federal AI policy frameworks (NIST AI RMF) | RAG architecture | responsible AI evaluation | AWS Bedrock

**Transferable Expertise:** Demonstrates the ability to translate a federal AI governance framework into a working technical control set, then critically evaluate whether those controls hold up under systematic testing -- the same judgment required to assess vendor and program claims about "governed AI" in a federal AI oversight role.
