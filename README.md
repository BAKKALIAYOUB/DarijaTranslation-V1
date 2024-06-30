# Model Card for DarijaTranslation-V1

This model translates text from English to Darija (Moroccan Arabic). <br>
HuggingFace :  https://huggingface.co/BAKKALIAYOUB/DarijaTranslation-V1


### Model Description

This model, designed for translating text from English to Darija (Moroccan Arabic), excels in handling general, everyday language such as greetings ("hi, how are you?"). It accurately translates common phrases and sentences typically encountered in informal communication. Additionally, the model has the capability to conjugate verbs correctly in the context of the translation.
- **Developed by:** BAKKALI AYOUB
- **Model type:** Translation
- **Language(s) (NLP):** English to Darija (Moroccan Dialect)
- **Finetuned from model :** marefa-nlp/marefa-mt-en-ar

## How to Get Started with the Model

Use the code below to get started with the model:

```python
from transformers import pipeline

# Initialize the translation pipeline
pipe = pipeline("translation", model="BAKKALIAYOUB/DarijaTranslation-V1")

# Translate text
translated_text = pipe("putin is the president of russia")
print(translated_text)
```

# Training  Details
## Training Data
The training data are from multiple source : `atlasia/darija-translation`, `BounharAbdelaziz/English-to-Moroccan-Darija`, and other csv file that contain adverbs, adjectives, preposition and nouns translation from english to darija.

#### Training Hyperparameters

- **Training regime**: fp16 mixed precision
- **Epochs** : 6
- **Learning rate** : 2e-5
- **Batch size** : 32
  
#### Speeds, Sizes, Times


- **Hardware** : GPU P100 ith 16 GB memory
- **Training**:
  
| Epoch   | Training Loss | Validation Loss |
|---------|---------------|-----------------|
| 1       | 0.398500      | 0.356238        |
| 2       | 0.330500      | 0.307416        |
| 3       | 0.297300      | 0.282857        |
| 4       | 0.276900      | 0.269981        |
| 5       | 0.263200      | 0.262747        |
| 6       | 0.256800      | 0.260168        |


