# Essential Tools

This repo contains easy to use functions to handle common tasks.

### Convert Folder to HuggingFace Dataset Format
```python
#==============================================
#       FOLDER TO HUGGINGFACE DATASET
#==============================================

config = folderToHFDataset(
    trainDataset='/kaggle/input/brain-tumor-mri-data/brain-tumor-mri-dataset', 
    valDataset=None, 
    testDataset=None 
    )

dataset = config.getDataset()
```

### Upload to HuggingFace Hub
```python
#================================================
#        DEPLOY DATASET TO HUGGINGFACE HUB
#================================================

from huggingface_hub import notebook_login


notebook_login()

dataset.push_to_hub("Docty/Oral-Cancer")
```
