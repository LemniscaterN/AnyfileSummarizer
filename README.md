# What's AnyFileSummarizer ?

This is a file summarization application with local LLM using [Ollama](https://ollama.com/).  
Note that the default is to use Llama 3.1, which **will result in a 4.7 GB download for Setup**.

# How to use

## Ollama setup
### macOS

`````````
brew install ollama
ollama pull llama3.1
`````````

### Linux

`````````
curl -fsSL https://ollama.com/install.sh | sh
ollama pull llama3.1
`````````

## Common Setup

```
git clone https://github.com/LemniscaterN/AnyfileSummarizer.git
cd AnyfileSummarizer

python -m venv venv
source venv/bin/activate
pip3 install -r requirements.txt

echo -e "\nafsum() {`pwd`/venv/bin/python `pwd`/main.py \"\$@\"; }" >> ~/.zshrc
source ~/.zshrc
```

## Samples
### Summarize PDF
```
afsum -pdf ./hoge/huge.pdf
```

### Summarize word
```
afsum -doc ./hoge/huge.doc
```

### Summarize pptx
```
afsum -ptx ./hoge/huge.ptx
```