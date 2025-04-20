MEETING SUMMARY
Abstractive Summarization Model
• Group Number: 48
• Group Members:
– Shivam Kumar
– Pranta Pratim Roy
– Sugata Dolai
1 Overview
The MEETING SUMMARY model is a fine-tuned version of Facebook’s BART-large-xsum, specifically designed for abstractive summarization of meeting transcripts and conversational texts.
2 Model Specifications
• Base Model: facebook/bart-large-xsum
• Type: Transformer-based Abstractive Summarization
• Language: English
• Fine-tuned datasets:
– AMI Meeting Corpus
– SAMSum Conversation Dataset
– DIALOGSUM Dataset
– XSum Dataset
3 Usage Instructions
3.1 Installation
pip install transformers torch
3.2 Example Python Code
from transformers import pipeline
summarizer = pipeline("summarization", model="knkarthick/MEETING_SUMMARY")
input_text = """
John: We need to discuss the quarterly results.
Anna: Sure, the sales have increased by 10%, thanks to the new campaign.
John: Excellent, but we still need to address the rising production costs.
"""
summary_output = summarizer(input_text, max_length=100, min_length=25, do_sample=False)
print(summary_output[0][’summary_text’])
1
4 Repository Files
• pytorch model.bin: PyTorch-compatible weights
• tf model.h5: TensorFlow-compatible weights
• model.safetensors: Safe tensor format model weights
• Tokenizer files:
– tokenizer config.json
– tokenizer.json
– vocab.json
– merges.txt
– special tokens map.json
• config.json: Model configuration file
• README.md: Documentation and usage details
5 Evaluation and Performance
Evaluated on the SAMSum conversational summarization dataset, this model delivers strong performance
in generating accurate and concise summaries suitable for meetings and conversational texts.
6 Licensing
The project is released under the Apache-2.0 License.
See: Apache 2.0 License
7 Acknowledgements
We acknowledge and thank the creators of:
• Facebook BART-large-xsum
• AMI Meeting Corpus
• SAMSum Dataset
• DIALOGSUM Dataset
• XSum Dataset
8 Contributions
Contributions and suggestions are warmly welcomed. Feel free to open issues or pull requests.
9 Contact Information
• Model Author: Shivam Kumar, Pranta Pratim Roy, Sougata Dolai
• Hugging Face Page: MEETING SUMMARY
Group Information:
2
