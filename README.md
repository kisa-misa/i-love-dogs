# My awesome README.md
Всем привет! Я догадалась что это задача Question answering, для каждого example взяла \
question = "Какой фрагмент текста соответствует размеру {}?".format(example['label']) \
context = example['text'] 

За baseline я взяла код с 🤗 курса по Question answering https://huggingface.co/course/chapter7/7?fw=pt#postprocessing \
Использовала предобученную русскоязычную модель distilrubert-tiny-cased-conversational \
Свою модель сохранила в 🤗 Hub https://huggingface.co/kisa-misa/distilrubert-tiny-cased-conversational 

How to use from the 🤗/transformers library \
from transformers import AutoTokenizer, AutoModelForQuestionAnswering \
tokenizer = AutoTokenizer.from_pretrained("kisa-misa/distilrubert-tiny-cased-conversational") \
model = AutoModelForQuestionAnswering.from_pretrained("kisa-misa/distilrubert-tiny-cased-conversational") \

Тетрадку с исследованием можно найти по ссылке https://colab.research.google.com/gist/kisa-misa/7b258fce39990f4688ae9ef7a279fb3d/-question-answering-pytorch.ipynb 
