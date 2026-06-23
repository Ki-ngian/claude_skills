# search-pubmed

Search biomedical literature on PubMed via NCBI E-Utilities.

## Dependencies

```bash
pip install biopython
```

## Usage

```bash
# Keyword search
python scripts/search_pubmed.py "Sinorhizobium AND biofilm" --max 10

# PMID lookup with abstract
python scripts/search_pubmed.py --pmid 41185614 --full

# Field-qualified search
python scripts/search_pubmed.py "hopanoid[Title/Abstract]"

# Other NCBI databases
python scripts/search_pubmed.py "TP53" --db nucleotide
```

## Parameters

| Parameter | Description | Default |
|-----------|-------------|---------|
| `query` | Search keywords (Entrez syntax) | Required |
| `--max N` | Max results | `10` |
| `--db NAME` | NCBI database | `pubmed` |
| `--pmid ID` | Lookup by PMID | — |
| `--full` | Include abstract (with `--pmid`) | off |
| `--email ADDR` | NCBI contact email | — |
| `--api-key KEY` | NCBI API Key (higher rate) | — |

## Rate limits

| Condition | Limit |
|-----------|-------|
| No API key | 3 req/s |
| With API key | 10 req/s |
