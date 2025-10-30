My complete chat with the LLM (Chat GPT) is available on this link, one can use this for evaluation
https://chatgpt.com/share/6903ee93-6e34-8002-910d-c30640b56b28

📘 NLP Preprocessing & Coreference Resolution Pipeline

This repository contains a Jupyter Notebook that demonstrates a complete text-processing pipeline using SpaCy, Coreferee, and custom regex-based preprocessing. The workflow includes:

Text cleaning & normalization

Tokenization & POS tagging

Dependency parsing

Coreference resolution

Speaker & dialogue detection

Dependency tree visualization

Consolidated preprocessing pipeline

📂 Dataset

This notebook uses sample text embedded directly in the code — there is no external dataset required.

Example text used inside the notebook:

"Alice went to the park. She saw Bob there. They talked for hours…"

Feel free to modify the text variable to input your own dataset or connect it to a text corpus.

🛠️ Setup & Installation
✅ Requirements

Ensure you have Python 3.10 and install the dependencies:

pip install spacy==3.3.3 coreferee==1.3.0 jupyter
pip install huggingface_hub==0.20.3
# 1. Install AllenNLP and AllenNLP models
pip install allennlp==2.10.1
pip install allennlp-models==2.10.1

# 2. Install spaCy language models
pip install en-core-web-lg==3.3.0
pip install en-core-web-sm==3.3.0

# If you haven't installed spaCy itself
pip install spacy==3.3.0

# 3. Install Hugging Face Hub
pip install huggingface-hub==0.20.3

# 4. Install NetworkX
pip install networkx==3.4.2


Note: The notebook currently uses the Transformer-based English model (en_core_web_lg).
If you prefer a smaller model, switch to en_core_web_sm, but coreference resolution requires the transformer model.

🚀 How to Run
jupyter notebook


Open notebook.ipynb and run the cells in order.

📊 Output & Results

The notebook displays:

✅ Cleaned text output
✅ POS tags & dependency parse
✅ Coreference resolution chains
✅ Speaker / dialogue detection results
✅ Dependency tree visualization

Example Output Snippet
-- POS & Dependency Parsing --
Token: Alice | POS: PROPN | Dependency: nsubj
Token: went | POS: VERB | Dependency: ROOT
...


Coreference example:

Coreference groups:
[ "Alice", "She" ]
[ "Alice and Bob", "They" ]

🧠 Project Purpose

This notebook serves as a learning/demo tool to show how to:

Preprocess and clean raw text for NLP

Perform linguistic annotation

Resolve coreference

Extract speaker references

Build reusable NLP functions

It can be extended for:

Chatbot preprocessing

Narrative analysis

Dialogue extraction in scripts/novels

Topic or entity-based text mining

📎 Notes

Coreferee supports English only at the moment.

Dependency visualization may not render in some notebook environments (e.g., some cloud notebook services).
Run locally for best results.

📄 License

MIT License — feel free to use and modify.