# master-thesis

Authorship verification seeks to determine whether two texts share the same author. 
Existing approaches often perform poorly in cross-domain scenarios. 
The influential Impostor approach of Koppel and Winter (2014) introduced hard negative sampling to sharpen predictions, yet it struggles to fix confounding variables during inference. 
This thesis investigates whether LLMs can help address these limitations. 
Specifically, we employ LLM-generated paraphrases as hard negatives. 
Since these paraphrases aim to preserve the confounding variables of the original text, they mitigate domain-related biases during inference. 
Moreover, by constructing a tailored case for each input text pair, the approach eliminates out-of-distribution issues, ensuring that comparisons remain within the distribution defined by the pair itself.
We evaluate the approach in the traditional human-authored authorship verification setting and find that the LLM-based extension outperforms the original baselines. 
At the same time, our results reveal the practical and conceptual challenges of integrating LLMs into authorship verification, including issues of reliability, hallucination, and control over paraphrase quality.

![Impostor approach workflow: (1) Impostor generation, (2) creation of feature vectors using frequent 4-grams, (3) random dimensionality reduction, (4) similarity computation and selection of the most similar candidate.](images/imposter/impostor.svg)
