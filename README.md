# CodeGen
 Language models are increasingly used beyond natural language to understand and  synthesize programming languages. This has multiple very important applications, including  automating code generation and documentation, understanding and transforming large legacy  codebases, making data querying and visualization interactive, etc.



Objective: Language models are increasingly used beyond natural language to understand and 
synthesize programming languages. This has multiple very important applications, including 
automating code generation and documentation, understanding and transforming large legacy 
codebases, making data querying and visualization interactive, etc. The goal is to apply existing 
models to solve various software-related tasks and further fine-tune an existing model to expand 
it to a new language that is not already supported by the model.

Tasks


1. Evaluate the program synthesis and documentation quality of a given small code LM.
◦ Generate a program for a given problem description.
◦ Generate documentation for a given program.
◦ Generate commit messages from file diffs.
2. Evaluate interactive querying of databases using small code LM.
◦ Generate the SQL query from text and evaluate it.
3. Compare the performance of small code LM against that of an LLM.
◦ Measure improvements from using a RAG-based system.
◦ Index some programs of the same language and use it for RAG to evaluate gains 
from it. Use embeddings from a small code LM for semantic search. Also consider 
indexing abstract syntax trees and using it for retrieval.
◦ Draw the top-K (test with various K) similar docs from the index for each test query to 
pass to LLM and evaluate gains from this approach.
Resources
1. Model candidates: Start with the codegen-350M-multi or similar for a small code LM. 
Use embeddings from the same small code LM for indexing and querying. Use any 
LLMs for subsequent RAG.
2. Use the Spider or BirdBench dataset for SQL and use the CoDocBench dataset.
3. When evaluating natural language text, use the BLEU or BERT score for similarity. 
Similarly, when comparing synthesized programs against ground-truth, evaluate them 
using metrics like CodeBLEU or CodeBERTScore, but also execution accuracy of the 
generated program, where feasible.
References
1. codegen-350M-multi: https://huggingface.co/Salesforce/codegen-350M-multi
2. CoDocBench: https://github.com/kunpai/codocbench
3. Spider: https://spider2-sql.github.io/
4. BirdBench: https://bird-bench.github.io/
5. CodeParrot: https://huggingface.co/datasets/codeparrot/github-code
6. CodeBLEU: https://arxiv.org/abs/2009.10297
7. CodeBERTScore: https://arxiv.org/abs/2302.05527
8. Datasets: https://github.com/codefuse-ai/Awesome-Code-LLM#8-datasets
Check Points for the Project
• Check Point-1: Documentation Generation + Training on Subset for a new language (2 
weeks)
• Check Point-2: SQL generation + training on complete data on new language (5 weeks)
• Check Point-3: RAG System + Trained Model Evaluation (8 weeks)
• Check Point-4: Final Deployment and overall system evaluation (Put their model into the 
RAG system and evaluate) (11 weeks
