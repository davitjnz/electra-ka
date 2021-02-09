# electra-ka

## Introduction

**electra-ka** is a is the first public Georgian language model. 

The model is available on [huggingface hub](https://huggingface.co/jnz/electra-ka) and it is public for everyone.

I hope this model will make the life of thous Data Scientists working with the Georgian language much easier. 

The model is trained on 33GB of Georgian text collected from 4854621 pages in the commoncrawl archive.

For sequence classification tasks on ideological propaganda on social media, it has achieved 91.3% accuracy.

The [fine-tuned model](https://huggingface.co/jnz/electra-ka-fake-news-tagging) is also available on the hub. You can start using it with simple few lines of code:

```python
from transformers import ElectraTokenizerFast
model = ElectraForSequenceClassification.from_pretrained("./electra-ka-fake-news-tagging")
tokenizer = ElectraTokenizerFast.from_pretrained("./electra-ka-fake-news-tagging/")

inputs = tokenizer("your text goes here...", return_tensors="pt")
predictions = model(**inputs)
```

Under the hood, the electra model uses the same architecture as BERT, but to avoid misuse can only serve as a discriminator, which makes it much harder to use for text generation.

To read more about electra please refer to the paper [ELECTRA: Pre-training Text Encoders as Discriminators Rather Than Generators](https://openreview.net/pdf?id=r1xMH1BtvB).

In case of any questions/comments please feel free to reach out at djanezashvili[at]gmail.com

Have a great coding!



