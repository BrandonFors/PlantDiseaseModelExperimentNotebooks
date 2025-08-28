# PlantDiseaseModelExperimentNotebooks
A repo containing the notebooks I used to conduct experiments with different pretrained torchvision models on a plant disease dataset

Summary:
  I conducted experiments using the pretrained effnetv2-s, mobilenetv3-s, resnet18, and vitb16 models from the torchvision library. I took the PlantVillage dataset and made a train and test split. This was uploaded to hugging face datasets. I then aquired the models from torchvision.models, initialized them with the pretrained weights, and modified each of the classification heads according to the dataset. A dataset was prepared for use with each model utilizing the provided torchvision transforms that go with each respective model. I then conducted training experiments on each model using a custom training loop with mixed precision. Each of these models' state dict was uploaded to hugging face. I then evaluated each of the models on size, accuracy, f1_score, and speed. Overall, the trained effnetv2-s turned out to be the best candidate because of its superior f1_score (probably because of a larger input image size). I then made the model compatible with hugging face by creating custom hugging face config and model classes by subclassing the transformers PreTrainedConfig and PreTrainedModel. 

Link final model hugging face repo:
https://huggingface.co/BrandonFors/effnetv2_s_plant_disease

Link to hugging face space:
https://huggingface.co/spaces/BrandonFors/PlantDiseaseDetection

Link to dataset used:
https://huggingface.co/datasets/BrandonFors/Plant-Diseases-PlantVillage-Dataset

