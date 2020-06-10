# Text Mining
[![Build Status](https://travis-ci.com/Allegheny-Mozilla-Fellows/textMining.svg?branch=master)](https://travis-ci.com/Allegheny-Mozilla-Fellows/textMining)
[![codecov](https://codecov.io/gh/Allegheny-Mozilla-Fellows/textMining/branch/master/graph/badge.svg)](https://codecov.io/gh/Allegheny-Mozilla-Fellows/textMining)

An automated text-mining tool written in Python to measure the technical
responsibility of students in computer science courses, being used to analyze
students' reflection documents and five questions survey based on Natural language
processing in the Department of Computer Science at Allegheny College.


## Install

This program uses [Pipenv](https://github.com/pypa/pipenv) for dependency installation.

Once you have cloned the repository:

- If needed, install and upgrade the `pipenv` with `pip`: `pip install pipenv --user`
- To install dependencies and use the program with `pipenv`: `pipenv install`:

TextMining relied on `en_core_web_sm`, a small English model trained on
written web text (blogs, news, comments), that includes vocabulary, vectors,
syntax and entities.

To install the pretrained model, you can run this following command:

```bash
pipenv run python -m spacy download en_core_web_sm
```

## Web Interface



## Command Line Interface

To learn about the command line interface of textMining, type in
  `pipenv run python textmining.py -h`

  ```bash
  $ pipenv run python textmining.py -h

  usage: textmining.py [-h] [--directory DIRECTORY] [--function FUNCTION]

  optional arguments:
    -h, --help            show this help message and exit
    --directory DIRECTORY
                          Directory with mardown documents to analyze (default: None)
    --function FUNCTION   Function to analyze (frequency/summary) (default: None)

  Sample usage: python3 textmining.py --directory /path/to/markdown_directory --function frequency
  ```



- To run streamlit, type in
  `pipenv run streamlit run streamlit_web.py`

- For a sample input diretory, use `resources/cs100f2019_lab05_reflections`

- Sample usage -> run frequency analysis:

  ```bash
  $ pipenv run python textmining.py --directory resources/cs100f2019_lab05_reflections --function frequency

  [('editing', 213), ('genome', 202), ('technology', 181), ('dna', 135), ('string', 107), ('random', 96), ('harm', 93), ('use', 89), ('code', 86), ('program', 81), ('lab', 76), ('assignment', 74), ('complete', 66), ('cause', 64), ('practice', 63), ('experience', 62), ('learn', 59), ('task', 59), ('letter', 58), ('challenge', 52), ('method', 51), ('make', 51), ('want', 50), ('value', 49), ('like', 48), ('run', 47), ('team', 47), ('character', 46), ('technical', 44), ('people', 44), ('position', 44), ('great', 43), ('change', 42), ('user', 40), ('face', 39), ('add', 38), ('replace', 38), ('think', 37), ('way', 37), ('java', 37), ('new', 37), ('class', 36), ('gene', 35), ('command', 35), ('display', 34), ('solution', 34), ('avoid', 33), ('overcome', 32), ('output', 31), ('work', 31)]

  ```

## Contribute

To install the development dependencies with `pipenv`: `pipenv install --dev --skip-lock`
