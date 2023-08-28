# factual.semantics

A DIY example #healthcare #chatbot builder, demonstrating in a #Jupyter notebook how to generate an indexable Focused Language Model (FLM) from #pubmed content and the #UMLS.   

Make your own chatGPT for healthcare! This example generates a language model and knowledge graph of "mindfulness" articles and concepts.   

Conforms to the emerging standards for AI in healthcare.

health data modeling   
novel, focused language modeling   

![weird](/weird.svg)

Documents to get

"What defines mindfulness-based programs? The warp and the weft"
https://pubmed.ncbi.nlm.nih.gov/28031068/?format=pubmed
https://pubmed.ncbi.nlm.nih.gov/28031068/

"Meditators' Non-academic Definition of Mindfulness"
https://pubmed.ncbi.nlm.nih.gov/35634214/?format=pubmed
https://pubmed.ncbi.nlm.nih.gov/35634214/
https://www.ncbi.nlm.nih.gov/pmc/articles/PMC9127491/

UMLS to get

https://www.nlm.nih.gov/research/umls/META3_current_semantic_types.html
https://www.nlm.nih.gov/research/umls/new_users/online_learning/UMLST_001.html

python mmlrestclient.py https://ii-public2vm.nlm.nih.gov/metamaplite/rest/annotate mmlinput.txt --output mmloutput.txt

python mmlrestclient.py https://ii.nlm.nih.gov/metamaplite/rest/annotate mmlinput.txt --output mmloutput.txt --docformat sldiwi --resultformat mmi

