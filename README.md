# k8s-rca-llm

Fine-tune an LLM to do Kubernetes/cloud incident triage:
- Evidence (events/logs/audit) → structured RCA output (root cause, confidence, evidence refs)
- Optional: safe next kubectl checks
- Optional: manifest linting + patch suggestions

This repo contains scripts and notebooks to explore public K8s datasets, build “incident episodes” (JSONL), and run QLoRA/SFT training using the Hugging Face ecosystem (TRL/Transformers). The training loop uses TRL’s SFTTrainer-style supervised fine-tuning. 
