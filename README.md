# electra-ka

## Introduction

**electra-ka** is an open-source model for the Georgian language. 

The model is available on [huggingface hub](https://huggingface.co/jnz/electra-ka)

The model is trained on 33GB of Georgian text collected from 4854621 pages in the commoncrawl archive.

The [fine-tuned model](https://huggingface.co/jnz/electra-ka-discrediting) is also available on the hub.

```python
from transformers import ElectraTokenizerFast
model = ElectraForSequenceClassification.from_pretrained("jnz/electra-ka-discrediting")
tokenizer = ElectraTokenizerFast.from_pretrained("jnz/electra-ka")

inputs = tokenizer("your text goes here...", return_tensors="pt")
predictions = model(**inputs)
```

Under the hood, the electra model uses the same architecture as BERT, but to avoid misuse can only serve as a discriminator, which makes it much harder to use for text generation.

BERT architecture language model for Georgian language.

To read more about electra please refer to the paper [ELECTRA: Pre-training Text Encoders as Discriminators Rather Than Generators](https://openreview.net/pdf?id=r1xMH1BtvB).

In case of any questions/comments please feel free to reach out at djanezashvili[at]gmail.com



