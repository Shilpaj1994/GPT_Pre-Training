# Pre-Training

This section focuses on Embeddings and Pre-training.

![LLM Training Steps](./assets/LLMfromScratch2.png)

In this project, a GPT (decoder-only) model is trained on Shakespeare data. The model architecture follows the original GPT design with multi-head self-attention and feed-forward layers. Key specifications include:

- 8 transformer layers
- 8 attention heads 
- 384 embedding dimensions
- 512 context window size
- ~50k vocabulary size

The model is trained using cross-entropy loss and AdamW optimizer with weight decay. Training is done on Shakespeare's works to learn the language patterns and writing style. The trained model can generate Shakespeare-style text given a prompt.



### Project Structure

```
.
├── assets              # Images for README
├── nano_gpt_model.pt   # Trained model
├── S12Trained.ipynb    # Notebook for training
├── input.txt           # Shakespeare data
├── README.md           # This file
└── requirements.txt    # Dependencies
```

### Install Dependencies

```
pip install -r requirements.txt
```

### Run the Notebook

```
jupyter notebook S12Trained.ipynb
```

### Training Logs

Training logs for few steps are shown below:

```bash
GPU Memory: 0.68GB / 1.77GB
step 10,000 | loss: 0.5863 | lr: 6.00e-05 | dt: 684.74ms | tok/sec: 5981.86 | norm: 3.94
    
GPU Memory: 0.68GB / 1.77GB
step 10,100 | loss: 0.5372 | lr: 6.00e-05 | dt: 687.72ms | tok/sec: 5955.88 | norm: 3.74
    
GPU Memory: 0.67GB / 1.77GB
step 10,200 | loss: 0.6054 | lr: 6.00e-05 | dt: 685.72ms | tok/sec: 5973.31 | norm: 5.71
    
GPU Memory: 0.68GB / 1.77GB
step 10,300 | loss: 0.5850 | lr: 6.00e-05 | dt: 686.01ms | tok/sec: 5970.77 | norm: 4.36
    
GPU Memory: 0.68GB / 1.77GB
step 10,400 | loss: 0.3319 | lr: 6.00e-05 | dt: 684.77ms | tok/sec: 5981.53 | norm: 4.68
    
GPU Memory: 0.68GB / 1.77GB
step 10,500 | loss: 0.4140 | lr: 6.00e-05 | dt: 684.41ms | tok/sec: 5984.70 | norm: 3.21
    
GPU Memory: 0.68GB / 1.77GB
step 10,600 | loss: 0.4008 | lr: 6.00e-05 | dt: 683.34ms | tok/sec: 5994.10 | norm: 3.58
    
GPU Memory: 0.68GB / 1.77GB
step 10,700 | loss: 0.3951 | lr: 6.00e-05 | dt: 685.49ms | tok/sec: 5975.26 | norm: 3.81
    
GPU Memory: 0.68GB / 1.77GB
step 10,800 | loss: 0.3022 | lr: 6.00e-05 | dt: 687.40ms | tok/sec: 5958.64 | norm: 3.06
    
GPU Memory: 0.68GB / 1.77GB
step 10,900 | loss: 0.4287 | lr: 6.00e-05 | dt: 686.75ms | tok/sec: 5964.31 | norm: 3.60
    
GPU Memory: 0.68GB / 1.77GB
step 11,000 | loss: 0.2447 | lr: 6.00e-05 | dt: 687.35ms | tok/sec: 5959.12 | norm: 3.35
    
GPU Memory: 0.68GB / 1.77GB
step 11,100 | loss: 0.2773 | lr: 6.00e-05 | dt: 688.83ms | tok/sec: 5946.35 | norm: 2.71
    
GPU Memory: 0.67GB / 1.77GB
step 11,200 | loss: 0.2839 | lr: 6.00e-05 | dt: 687.56ms | tok/sec: 5957.31 | norm: 3.90
    
GPU Memory: 0.68GB / 1.77GB
step 11,300 | loss: 0.3481 | lr: 6.00e-05 | dt: 684.68ms | tok/sec: 5982.32 | norm: 3.68
    
GPU Memory: 0.78GB / 1.77GB
step 11,400 | loss: 0.1913 | lr: 6.00e-05 | dt: 685.73ms | tok/sec: 5973.18 | norm: 2.93
    
GPU Memory: 0.68GB / 1.77GB
step 11,500 | loss: 0.2605 | lr: 6.00e-05 | dt: 685.74ms | tok/sec: 5973.11 | norm: 2.96
    
GPU Memory: 0.68GB / 1.77GB
step 11,600 | loss: 0.2029 | lr: 6.00e-05 | dt: 689.04ms | tok/sec: 5944.49 | norm: 2.84
    

Reached target loss! Final loss: 0.0889 at step 11,663
Model saved to gpt_model.pt
```

### Model Output

```bash
Once upon a time to not;
More slaughter'd, sweet Rivers, I receive my children, and title with pardon hither
That one stuff'd with a conquest; and teeth, of my? Why, in life thee,
Which now not joy of foe, thought o'n slaughter bed,
And, is mine own soul me, not so heavy in every day:
The tyrant from one curst my death lies;
For the ground is nothing henceforth fell executioner come
```

### Try it out

App Link
