# Mistral Harmlessness Evaluator

This module is a part of the Mistral Self-Alignment project, aimed at aligning the Mistral model to be harmless and prevent dangerous and harmful responses. For more details, explore related GitHub repositories like [The Lab](https://github.com/August-murr/Lab).

## Overview

The Mistral Harmlessness Evaluator is designed to test the harmlessness of the trained Mistral 7b Peft Adapters. The evaluation is based on a one-shot prompt test available [here](https://github.com/August-murr/Lab/tree/main/Self-evaluation), resulting in an 82% agreement with labeled data.

Although the module was initially written to test Peft Adapters, a Jupyter Notebook was uploaded [here] to evaluate the base Mistral model for harmlessness.

## Usage

### Installation

Clone the repository and install the necessary dependencies:

```bash
pip install requirements.txt
```

Please note that the `requirements.txt` file was written in the context of running the module in a Kaggle notebook and may not contain all the packages necessary for a local notebook.

### Running the Script

Use the following command to run the script:

```bash
python harmlessness_self_evaluator.py \
    --model_path "path/to/mistral" \
    --peft_path "path/to/peft_adapter" \
    --num_of_eval_prompts 200
```

In the example above:
- `--model_path` should be the file path or the Hugging Face Hub's ID of Mistral 7b.
- `--peft_path` should be the file path or the Hugging Face Hub's ID of the Peft Adapter.
- `--num_of_eval_prompts` is the number of red team prompts in the train and test dataset for the model to be evaluated on. Keep in mind that the number of red team prompts is limited.

## Note

This module was initially developed for personal use. If you find it useful, feel free to clone, modify, and adapt it to your use case.
