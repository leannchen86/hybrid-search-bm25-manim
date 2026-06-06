# Vector Search Is Not Enough - Manim Explainer

Manim animation source code for the video [Why vector search is not enough and we need BM25](https://youtu.be/3FbJOKhLv9M).

This repo explains why dense-vector retrieval is powerful but incomplete. It uses short visual scenes to compare sparse lexical matching, dense semantic similarity, term-frequency scoring, document-length normalization, and BM25-style weighting.

## What This Teaches

- The difference between sparse vectors and dense embedding vectors.
- Why semantic similarity can miss exact, rare, or time-sensitive terms.
- How term frequency, inverse document frequency, and document length affect lexical retrieval.
- Why hybrid retrieval often works better than pure vector search for real RAG systems.

## Repo Map

- `sparse_vs_dense_vector.py` - side-by-side sparse and dense vector explanation.
- `word2embedding.py`, `king_vector.py`, `capital_city_txt.py` - embedding intuition scenes.
- `tokenizing.py`, `tf_scores.py`, `tf_doc_length.py`, `bm25_idf.py` - lexical retrieval and BM25 concepts.
- `time_related_terms.py` - examples where exact or contextual terms matter.
- `semantic_posit_numbers.py`, `straight_number_line.py` - geometry and similarity intuition.

## Running A Scene

Install Manim in a Python environment:

```bash
python -m venv .venv
source .venv/bin/activate
pip install manim
```

Render a preview scene:

```bash
manim -pql sparse_vs_dense_vector.py VectorComparison
```

Render the BM25 IDF scene:

```bash
manim -pql bm25_idf.py BM25IDFVisualization
```

Use `-pqh` instead of `-pql` for a higher-quality render.

## Why This Exists

RAG tutorials often jump straight to embeddings. This explainer slows down the retrieval problem and shows why lexical signals still matter, especially when developer systems need precision, recency, rare terms, or query-specific constraints.
