## Companion repository for:

*Bernard et al., (2026). Using GPT to measure business complexity, The Accounting Review.*

Paper links: [SSRN](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=4480309) - [The Accounting Review](https://publications.aaahq.org/accounting-review/article-abstract/101/3/67/14397/Using-GPT-to-Measure-Business-Complexity)

## Table of contents

- **1. Appendix**
    - [SSRN](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=4480309)
- **2. Models**
    - Available on [Hugging Face](https://huggingface.co/Ties/gpt-business-complexity)
    - See the `models` folder for more details and setup instructions. 
- **3. Paper datasets**
    - Available in the `datasets` folder, each are briefly described below.

## Dataset descriptions

**Notes**
- See the paper and its appendix for full details on dataset construction and variable definitions.

### Dataset 1: `Paper` 

The original paper dataset, covers up to May 2024. It includes CIK and `gvkey` and is scoped to observations with coverage in the various WRDS datasets that underly the analyses in the paper.  

**Complexity at the filing level**

Provided at `datasets/paper/complexity_filing.dta`

![Dataset_1](screenshots/complexity_filing.png)

**Complexity at the filing+category level**

Provided at `datasets/paper/complexity_filing_category.dta`

![Dataset_2](screenshots/complexity_filing_category.png)

### Dataset 2: `update_202609`

An incremental update to cover May 2024 to August 2026. This update covers the entire CIK universe in Edgar without matching it to WRDS. It does not include `gvkey` and it includes CIKs regardless of whether they have data in the WRDS datasets used in the original analyses. As a result, this incremental dataset covers more companies than the original `paper` dataset (which is pre-filtered on WRDS coverage).

See: `datasets/update_202609/`