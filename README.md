# What's sumpdf ?
[Ollama](https://ollama.com/)を利用したローカルLLMによるファイル要約アプリです。
デフォルトではLlama 3.1を利用するため、**Setupに4.7GBのダウンロードが発生する**ことに注意してください。


# How to use

## Setup
```
git clone [hoge]
cd pdfSummarize

brew install ollama
ollama pull llama3.1

python -m venv venv
source venv/bin/activate
pip3 install -r requirements.txt

echo -e "\nsumpdf() {`pwd`/venv/bin/python `pwd`/main.py \"\$@\"; }" >> ~/.zshrc
source ~/.zshrc
```

## Summarize PDF
```
sumpdf -pdf ./hoge/huge.pdf
```

## Summarize word
```
sumpdf - ./hoge/huge.pdf
```




# For Mac User
1. ./setup.sh

# For Linux