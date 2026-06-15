# Federal AI Governance RAG Assistant

A retrieval-augmented assistant that answers questions about U.S. federal AI governance using only a curated corpus of NIST frameworks, technical reports, executive orders, and draft legislation -- with mandatory source citation, contextual-grounding and denied-topic guardrails, and a full per-query audit log. The project was built to test not just whether a "governed AI" system can be configured with the right controls, but whether those controls behave consistently once built. Systematic evaluation found that grounding and refusal behavior, while functioning as configured, are sensitive to query phrasing and retrieval breadth -- the same underlying content can be answered or refused depending on how a question is asked, a finding with direct implications for how governance claims about RAG systems should be evaluated (see the portfolio page below for the full evaluation).

## Portfolio Page

The [portfolio page](https://kchoover14.github.io/governed-ai-rag-bedrock) includes a full project narrative, key findings, and figures.

## Tools & Technologies

**Languages:** Python

**Tools:** AWS Bedrock | Amazon Bedrock Knowledge Bases | Amazon S3 | Amazon S3 Vectors | Amazon Bedrock Guardrails | Jupyter

**Packages:** boto3

## Environment

- `requirements.txt` -- install with `pip install -r requirements.txt`
- Requires an AWS account with access to Amazon Bedrock (an inference profile for Claude Haiku 4.5 or equivalent), an existing Bedrock Knowledge Base over the corpus, and a configured Bedrock Guardrail. Before running, update the placeholders in `notebooks/governed_rag.ipynb`: AWS profile name, region, account ID (in `HAIKU_ARN`), `KB_ID`, and `GUARDRAIL_ID`.

## Expertise

**Domain Expertise:** AI governance | federal AI policy frameworks (NIST AI RMF) | RAG architecture | responsible AI evaluation | AWS Bedrock

**Transferable Expertise:** Demonstrates the ability to translate a federal AI governance framework into a working technical control set, then critically evaluate whether those controls hold up under systematic testing -- the same judgment required to assess vendor and program claims about "governed AI" in a federal AI oversight role.

## License

- Code and scripts © Kara C. Hoover, licensed under the [MIT License](LICENSE).
- Data, figures, and written content © Kara C. Hoover, licensed under [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/).
