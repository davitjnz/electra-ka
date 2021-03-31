# electra-ka 

# ელექტრა-ქა

## ლინგვისტური მოდელი ქართული ენისთვის

**electra-ka**

მოდელი: [huggingface hub](https://huggingface.co/jnz/electra-ka)

The [fine-tuned model](https://huggingface.co/jnz/electra-ka-discrediting) is also available on the hub.

```python
from transformers import ElectraTokenizerFast
model = ElectraForSequenceClassification.from_pretrained("jnz/electra-ka-discrediting")
tokenizer = ElectraTokenizerFast.from_pretrained("jnz/electra-ka")

inputs = tokenizer("your text goes here...", return_tensors="pt")
predictions = model(**inputs)
```
