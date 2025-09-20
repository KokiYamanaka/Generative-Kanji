# Key Links

- [Hugging Face](https://huggingface.co/kokiy365/Generative-Kanji) : Includes checkpoints, updated weights  
- [Quickview on dataset](original/target_dataset/kanji-even.csv)


# Key Directories 
Where to find what
```
Project/
├── Logs/
│ └── logs4/text2image-fine-tune # sample generated in training, loss curve, SNR plot
│
├── original/
│ ├── subset/ # JIS 208 level 2 Kanji
│ └── target_dataset/ # 1600 samples used to train the model
│
└── script/
├── train.ipynb # fine-tune interface
└── train_text_to_image_lora.py # fine-tune actual script
```

## Training Configuration 

| **Component**                  | **Diffusion-Kanji**                              |
| ------------------------------ | ------------------------------------------------ |
| **Source**                     | KANJIDIC2                                        |
| **Filtering Criteria**         | JIS X 208, selectively choose 16 different radicals |
| **Train/Inference Image Size** | 128×128                                          |
| **Captioning Style**           | Multi English phrase or Single                   |
| **Single/Multi Definitions**   | Single, Multi                                    |
| **Number of Samples**          | 1600                                             |
| **Base Model**                 | **Stable Diffusion v1-4**                        |
| **LoRA Rank**                  | 64                                               |
| **Alpha**                      | 4                                                |
| **Batch Size**                 | 1                                                |
| **Learning Rate**              | 1.00E-04                                         |
| **Learning Scheduler**         | cosine                                           |
| **Epochs**                     | 50                                               |

