# Claude Code Skills

A collection of reusable skills for [Claude Code](https://claude.ai/code).

## Available Skills

### [search-pubmed](search-pubmed/)

Search biomedical literature on PubMed via NCBI E-Utilities. Supports keyword search, PMID lookup, and full Entrez query syntax.

```
pip install biopython
```

| Quick example |
|---|
| `Search PubMed for Sinorhizobium fredii biofilm papers` |
| `Look up PMID 41185614 with abstract` |
| `Is there any research on hopanoids in Sinorhizobium? Check if it's a gap.` |

---

## Install

### Install a single skill

```bash
# From packaged .skill file
/install search-pubmed/search-pubmed.skill

# Or copy into skills directory manually
cp -r search-pubmed/ ~/.claude/skills/
```

### Clone the whole collection

```bash
git clone https://github.com/<user>/claude-skills.git
cd claude-skills
# Copy desired skills:
cp -r search-pubmed/ <your-project>/.claude/skills/
```

## Skill Structure

Each skill follows the standard layout:

```
skill-name/
├── SKILL.md           # Skill definition (required)
├── scripts/           # Executable code
├── references/        # Reference docs loaded on demand
└── skill-name.skill   # Packaged for /install
```

## License

MIT — see [LICENSE](LICENSE).
