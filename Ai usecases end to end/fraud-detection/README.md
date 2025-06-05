# OpenShift AI Fraud Detection Masterclass

Welcome to the **OpenShift AI Fraud Detection Masterclass**! This repo is your all-in-one guide to building, training, and deploying a fraud detection system using OpenShift AI. Think of it as a treasure map to mastering AI on Kubernetes, with hands-on examples and pipelines ready to explore!

## 🌍 What’s This About?

This project walks you through detecting fraudulent transactions with a full ML pipeline. It uses OpenShift AI, Kubeflow Pipelines, Ray for distributed training, and ModelMesh for inference. Whether you're learning or showcasing skills, this repo has the tools to get you started!

## 📂 What’s Inside?

### Folders

- **data/**: Holds transaction datasets (`train.csv`, `validate.csv`) for training.
- **github/**: Git-related configs or scripts (e.g., GitHub Actions).
- **pipeline/**: Contains pipeline definitions for automated workflows.
- **ray-scripts/**: Scripts for distributed training with Ray (e.g., `train_tf_cpu.py`).
- **setup/**: Setup files or configurations for the environment.
- **utils/**: Utility scripts (e.g., S3 handling).
- **workshop/**: Workshop materials or tutorials.

### Files

- **0_sandbox.ipynb**: Playground notebook for initial experiments.
- **1_experiment_train.ipynb**: Notebook for training experiments.
- **2_save_model.ipynb**: Notebook to save the trained model.
- **3_rest_requests_multi_model.ipynb**: REST API requests for multiple models.
- **4_grpc_requests_multi_model.ipynb**: gRPC API requests for multiple models.
- **5_rest_requests_single_model.ipynb**: REST API requests for a single model.
- **6_train_save_pipeline.PIPELINE**: Pipeline file for training and saving.
- **7_get_data_train_upload**: Kubeflow pipeline YAML for data, training, and upload.
- **8_distributed_training.ipynb**: Notebook for distributed training with Ray.
- **LICENSE**: Legal info for the project.
- **README.md**: This file—your project guide!
- **_.gitignore**: Excludes files (e.g., large models) from Git.

## 🚀 How It Works

1. **Experiment**: Use `0_sandbox.ipynb` and `1_experiment_train.ipynb` to test ideas.
2. **Train & Save**: Follow `2_save_model.ipynb` and `6_train_save_pipeline.PIPELINE` to train and save models.
3. **Pipeline**: Run `7_get_data_train_upload` in OpenShift AI for automated data handling and training.
4. **Distributed Training**: Explore `8_distributed_training.ipynb` and `ray-scripts/` for scalable training.
5. **Inference**: Test with `3_rest_requests_multi_model.ipynb`, `4_grpc_requests_multi_model.ipynb`, and `5_rest_requests_single_model.ipynb` using ModelMesh.
6. **Deploy**: Use S3 (e.g., `models/fraud/1/model.onnx`) for model storage.

## 🛠️ Setup

1. **Clone the Repo**:

   ```bash
   git clone https://github.com/SyedArmghanAhmad/OpenShift-AI-Usecases.git
   cd OpenShift-AI-Usecases
   ```

2. **Install Dependencies**:

   ```bash
   pip install -r ray-scripts/requirements.txt  # If requirements.txt exists
   ```

3. **Configure Environment**:
   - Set AWS credentials for S3: `AWS_ACCESS_KEY_ID`, `AWS_SECRET_ACCESS_KEY`, etc.
   - Use OpenShift AI’s JupyterLab or a local Kubernetes setup.

4. **Run Notebooks**:
   - Open in JupyterLab (e.g., via OpenShift AI) and execute cells.
   - For pipelines, use Kubeflow Pipelines UI.

5. **Inference**:
   - REST: `http://modelmesh-serving:8008/v2/models/fraud/infer`
   - gRPC: `modelmesh-serving:8033`

## 🔑 Key Highlights

- **Hands-On**: Step-by-step notebooks for learning and experimenting.
- **Scalable**: Ray and Kubeflow handle big data and distributed tasks.
- **Real-World**: ModelMesh integration for production-ready inference.
- **Secure**: S3 storage with Kubernetes secrets support.

## 📝 Notes

- Large files like `model.onnx` are excluded (use `.gitignore`) and stored in S3.
- Adjust the 0.95 fraud threshold in inference scripts as needed.
- Monitor with Prometheus for production use.

## 🤝 Contribute

Love AI on OpenShift? Fork this repo, add your twists, and send a pull request. Let’s build something epic together!

## 🙌 Thanks

Crafted with 💪 by Syed Armghan Ahmad. Powered by OpenShift AI’s awesome ecosystem!
