# Fine-tuning-DeepSeek
Fine tuning DeepSeek-R1-Distill-Qwen-1.5B large language model using PEFT and LoRA. No resources needed (no GPU, no memory, no ollama) works fully on kaggle.In this approach, the original pretrained model weights are frozen, and instead of updating the full model, lightweight LoRA adapters are injected into specific layers. ideal for customizing large models using limited resources. 
#Training Setup
  •	Batch size = 1 (to fit a single GPU)
  •	Epochs = 3
  •	Learning rate = 1e-5
  •	No intermediate checkpoint saving
  •	FP16 training enabled
#Observed training behavior
  •	Initial loss: ~3.46
  •	Final loss after 6000 steps: ~0.10
  •	Loss consistently declined with each 100-step interval.
  •	Indicates successful convergence with no signs of overfitting
