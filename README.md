# Homeworker - Handwriting Synthesis

![](img/banner.svg)

## Overview

Homeworker is an implementation of handwriting synthesis experiments inspired by the paper [Generating Sequences with Recurrent Neural Networks](https://arxiv.org/abs/1308.0850) by Alex Graves. The original repository has been migrated to TensorFlow v2 with improved structure. This project closely follows the paper with a few deviations, producing handwriting samples of similar quality to those presented in the research.

## Installation

```shell
git clone https://github.com/Eeman1113/Homeworker/
cd Homeworker
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```

Run the demo:

```shell
python main.py
```

## Usage

```python
from handwriting_synthesis.hand import Hand

lines = [
    "Father time, I'm running late",
    "I'm winding down, I'm growing tired",
    "Seconds drift into the night",
    "The clock just ticks till my time expires",
]
biases = [0.75 for _ in lines]
styles = [9 for _ in lines]
stroke_colors = ['red', 'green', 'black', 'blue']
stroke_widths = [1, 2, 1, 2]

hand = Hand()
hand.write(
    filename='img/usage_demo.svg',
    lines=lines,
    biases=biases,
    styles=styles,
    stroke_colors=stroke_colors,
    stroke_widths=stroke_widths
)
```

![](img/usage_demo.svg)

## Demonstrations
<img width="601" alt="Screenshot 2023-11-19 at 10 23 24 PM" src="https://github.com/Eeman1113/Homeworker/assets/54275491/8c52d696-15c7-4821-9e75-b7cbf59d14bd">

<img width="613" alt="Screenshot 2023-11-19 at 10 23 55 PM" src="https://github.com/Eeman1113/Homeworker/assets/54275491/fae820b4-94ff-4b5c-8875-cd0d850472c2">


## Training

A pretrained model is included, but instructions for training your own model can be found in [model/README.md](model/README.md).

## Contribute

Contributions, pull requests, and packaging improvements are welcome. 
If you encounter problems or have feature requests, feel free to open an issue.

---

**Note:** This project was initially designed as a reference implementation for a research paper. While the focus remains on the machine learning aspects, contributors are encouraged to enhance usability, add support for more advanced drawing features, animations, or any other improvements. The AI model powering this project is affectionately named "Homeworker."
