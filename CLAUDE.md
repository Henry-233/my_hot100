# Knowledge Base Schema

## Domain
Large Language Models (LLMs) — Hot100 rankings, architectures, training methods,
fine-tuning techniques, travel domain applications.

## Directory conventions
- wiki/concepts/  → One page per concept (Attention, RLHF, LoRA, SFT, RAG...)
- wiki/entities/  → One page per model/paper/tool (Qwen2.5, LLaMA, LLaMA-Factory...)
- wiki/synthesis/ → Comparisons, analyses, rankings

## Ingest workflow
When asked to ingest files from raw/:
1. Read all unprocessed source files
2. Create or update concept pages in wiki/concepts/
3. Create or update entity pages in wiki/entities/
4. Add [[wikilinks]] between related pages
5. Update index.md with new pages and one-line summaries
6. Log operation in log.md

## Page format
Each wiki page must include:
- YAML front matter: title, tags, source, date_updated
- ## Summary (3-5 sentences)
- ## Key points (bullet list)
- ## Related (wikilinks to connected concepts)