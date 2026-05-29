## LLM boilerplates in Renku
Welcome to your starter kit for working with Large Language Models (LLMs) inside Renku. This project provides two clean, lightweight Jupyter Notebooks designed to demonstrate both cloud-hosted API prompting and local open-weights model inference.

This project is based on the boilerplate provided in https://github.com/bethcg/llm-boilerplates/tree/main, gently created by Elisabet Capon (@bethcg)

### 📁 Project structure & notebooks
- `llm-boilerplates/notebooks/01_api_prompting.ipynb`: demonstrates how to connect to cloud-hosted LLM endpoints using the standard OpenAI Python SDK. It includes ready-to-use configurations for the Swiss Apertus infrastructure.
- `llm-boilerplates/notebooks/02_local_inference.ipynb`: demonstrates how to programmatically download an open-weights model from Hugging Face and run text generation locally inside your container. It utilizes a highly efficient model (SmolLM2) to ensure smooth execution on standard hardware allocations. To avoid re-downloading gigabytes of data every time your session restarts or resumes, we recommend downloading and storing your model weights in a data connector with write access.

### 🔑 Key setup step: API credentials
Before you can run the API-based notebook, your environment needs access to your credentials.

⚠️ Important: When launching your interactive Renku session, you will be prompted to enter your API credentials for Apertus.

- If you skip this step, the environment will not be able to locate your keys, and `01_api_prompting.ipynb` will throw an authorization error and fail to execute.
- Your keys are securely mounted at the system root path (`/secrets/APERTUS_API_KEY.txt`) and are automatically read into the notebook code without exposing your raw tokens in the code history.

### 🚀 Quick start
Start your Renku session and provide your API keys when prompted.
Open 01_api_prompting.ipynb to test your connection to the hosted endpoints.
Open 02_local_inference.ipynb to experiment with running lightweight models directly on your allocated compute resources.