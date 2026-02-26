# Bias Evaluation of Domain-Specific BERT Models

This repo contains the code and results for evaluating whether domain-specific pretraining (biomedical, financial, legal) amplifies or attenuates (gender) biases, compared to general-purpose BERT. Three complementary benchmarks are used: 

- **StereoSet** (StereoSetBiasEvaluation.ipynb) — measures LMS (language modelling ability), SS (stereotype preference), and ICAT (combined fairness score) across gender, profession, race, and religion bias types using 2,106 intrasentence examples.

- **CrowS-Pairs** (CrowSPairsBiasEvaluation.ipynb) — measures stereotype preference rate using pseudo-log-likelihood on 1,508 sentence pairs across 9 bias categories including gender, race, religion, nationality, and disability. 
  
- **C-WEAT** (C_WEAT_BiasEvaluation.ipynb) — measures gender bias in contextualised embeddings via Cohen's d effect size. Tests whether each model associates man vs woman more strongly with high-status vs supportive roles, using 28 domain-specific sentence templates per domain.

Models evaluated and their HuggingFace names: 
- **BERT-base-uncased** (bert-base-uncased)  
- **BioBERT** (dmis-lab/biobert-base-cased-v1.2)  
- **FinBERT** (ProsusAI/finbert)  
- **LegalBERT** (nlpaueb/legal-bert-base-uncased)  
