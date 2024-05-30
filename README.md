# **ChatBot**

A Vietnamese chatbot 


# **Contents**
- [Overview](#overview)
- [Installation](#installation)
- [Settings](#settings)
- [Dataset](#dataset)
- [Training](#training)
- [Evaluate](#evaluate)

# **Overview**
A chatbot use LLM to genarate answer for Vietnamese question. The concept of question is GHTK' policy, system, payment method 

# **Installation**

## *Create environment*

1. Install miniconda or anaconda.
2. Create conda environment

    ```bash
    conda create -n CB python=3.9.5
    conda activate CB
    ```


## *Install dependencies*

1. Important Dependencies
    ```bash
    pip install -r requirements.txt
    ```

# **Settings**
1. Install unslot
    pip install "unsloth[cu118] @ git+https://github.com/unslothai/unsloth.git"
2. Setup Cohere
    Visit link : https://dashboard.cohere.com 
    Copy Api key to use cohere rerank
3. Arguments Training
    output_dir="<base_dir_location>",
    save_strategy="epoch",
    evaluation_strategy="steps",
    logging_steps=50,
    eval_steps=50,
    num_train_epochs = 3.0,
    per_device_train_batch_size=4,
    gradient_accumulation_steps=1,
    optim='adamw_hf',
    learning_rate=1e-5,
<!-- #     fp16=True, -->
    warmup_ratio=0.1,
    group_by_length=True,
    lr_scheduler_type='linear',

# **Dataset**
    Dataset of 1100+ question, answer and 36 provisions of the provisions of GHTK
## *Create training & testing dataset*
    run file unslot.ipynb

# **Training**
    run file unslot.ipynb

# **Evaluate**
    *Metric BLEU score 