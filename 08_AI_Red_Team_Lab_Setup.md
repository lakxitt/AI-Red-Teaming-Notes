# 🛠️ AI Red Team Lab Setup (Kali Linux)

A complete step-by-step guide to set up an **AI Red Teaming Lab** on **Kali Linux**. This environment includes LLM frameworks, adversarial ML tools, prompt testing tools, vector databases, Docker, Ollama, and development utilities.

---

# 📋 Prerequisites

- Kali Linux (Latest Version)
- Internet Connection
- At least **16 GB RAM** (Recommended)
- 100+ GB Free Storage (Recommended)
- NVIDIA GPU (Optional, but recommended for local LLMs)

---

# Step 0 — Update Kali Linux

Update all installed packages.

```bash
sudo apt update && sudo apt full-upgrade -y
```

Install essential utilities.

```bash
sudo apt install -y git curl wget unzip build-essential software-properties-common
```

Verify Git installation.

```bash
git --version
```

Expected Output

```text
git version 2.x.x
```

---

# Step 1 — Install Miniconda

Download Miniconda.

```bash
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
```

Make the installer executable.

```bash
chmod +x Miniconda3-latest-Linux-x86_64.sh
```

Run the installer.

```bash
./Miniconda3-latest-Linux-x86_64.sh
```

### During Installation

- Type:

```text
yes
```

- Accept the default installation location.

- When prompted:

```text
Do you wish to initialize Miniconda?
```

Type:

```text
yes
```

Close the terminal and open it again.

Verify the installation.

```bash
conda --version
```

Expected Output

```text
conda 24.x.x
```

---

# Step 2 — Create a Python Environment

Create a dedicated Conda environment.

```bash
conda create -n ai-redteam python=3.11 -y
```

Activate it.

```bash
conda activate ai-redteam
```

Verify Python.

```bash
python --version
```

Expected Output

```text
Python 3.11.x
```

---

# Step 3 — Upgrade pip

Upgrade the Python package manager.

```bash
pip install --upgrade pip
```

Verify the version.

```bash
pip --version
```

---

# Step 4 — Install AI Libraries

## Install PyTorch

```bash
pip install torch torchvision torchaudio
```

## Install Hugging Face Transformers

```bash
pip install transformers datasets
```

## Install Machine Learning Packages

```bash
pip install scikit-learn pandas numpy matplotlib
```

## Install API Libraries

```bash
pip install openai anthropic python-dotenv requests
```

Verify all installations.

```bash
python -c "import torch, transformers, openai; print('Everything OK')"
```

Expected Output

```text
Everything OK
```

---

# Step 5 — Install Garak

Install Garak.

```bash
pip install garak
```

Verify.

```bash
python -m garak --version
```

---

# Step 6 — Install Microsoft PyRIT

Install PyRIT.

```bash
pip install pyrit
```

Verify.

```bash
python -c "import pyrit; print('PyRIT Installed')"
```

Expected Output

```text
PyRIT Installed
```

---

# Step 7 — Install IBM ART

Install the Adversarial Robustness Toolbox.

```bash
pip install adversarial-robustness-toolbox
```

Verify.

```bash
python -c "from art.attacks.evasion import FastGradientMethod; print('ART OK')"
```

Expected Output

```text
ART OK
```

---

# Step 8 — Install Node.js

Install Node.js and npm.

```bash
sudo apt install -y nodejs npm
```

Verify the installation.

```bash
node -v
npm -v
```

If the Node.js version is below **18**, install the latest LTS release.

```bash
curl -fsSL https://deb.nodesource.com/setup_22.x | sudo -E bash -
sudo apt install -y nodejs
```

Verify again.

```bash
node -v
```

---

# Step 9 — Install Promptfoo

Install Promptfoo globally.

```bash
sudo npm install -g promptfoo
```

Verify.

```bash
promptfoo --version
```

---

# Step 10 — Install Ollama

Install Ollama.

```bash
curl -fsSL https://ollama.com/install.sh | sh
```

Enable and start the service.

```bash
sudo systemctl enable ollama
sudo systemctl start ollama
```

Verify the service.

```bash
systemctl status ollama
```

---

# Step 11 — Download Llama 3.2

Download the model.

```bash
ollama pull llama3.2
```

List installed models.

```bash
ollama list
```

Expected Output

```text
llama3.2
```

Run the model.

```bash
ollama run llama3.2
```

Test it.

```text
Hello
```

Exit.

```text
/bye
```

---

# Step 12 — Install Docker

Install Docker and Docker Compose.

```bash
sudo apt install -y docker.io docker-compose
```

Enable and start Docker.

```bash
sudo systemctl enable docker
sudo systemctl start docker
```

Verify the installation.

```bash
docker --version
```

Run the test container.

```bash
sudo docker run hello-world
```

---

# Step 13 — Install Qdrant

Pull the Docker image.

```bash
sudo docker pull qdrant/qdrant
```

Run the container.

```bash
sudo docker run -d \
-p 6333:6333 \
--name qdrant \
qdrant/qdrant
```

Open in your browser.

```text
http://localhost:6333
```

---

# Step 14 — Clone DVLLM

Clone the repository.

```bash
git clone https://github.com/payu/DVLLM.git
```

Move into the project directory.

```bash
cd DVLLM
```

Install dependencies.

```bash
pip install -r requirements.txt
```

Run the application.

```bash
python app.py
```

Open in your browser.

```text
http://127.0.0.1:5000
```

---

# Step 15 — Install Visual Studio Code

Install VS Code.

```bash
sudo apt install code
```

If the package is unavailable, add Microsoft's repository.

```bash
wget -qO- https://packages.microsoft.com/keys/microsoft.asc | gpg --dearmor > packages.microsoft.gpg

sudo install -D -o root -g root -m 644 packages.microsoft.gpg \
/usr/share/keyrings/packages.microsoft.gpg

echo "deb [arch=amd64 signed-by=/usr/share/keyrings/packages.microsoft.gpg] https://packages.microsoft.com/repos/code stable main" \
| sudo tee /etc/apt/sources.list.d/vscode.list

sudo apt update

sudo apt install code
```

---

# Step 16 — Install VS Code Extensions

Install recommended extensions.

```bash
code --install-extension ms-python.python

code --install-extension ms-toolsai.jupyter

code --install-extension humao.rest-client

code --install-extension mikestead.dotenv

code --install-extension ms-azuretools.vscode-docker
```

---

# Step 17 — Configure Hugging Face

Install the Hugging Face Hub.

```bash
pip install huggingface_hub
```

Log in.

```bash
huggingface-cli login
```

Paste your Hugging Face access token when prompted.

---

# Step 18 — Create Environment Variables

Create a `.env` file.

```bash
nano .env
```

Example configuration.

```env
OLLAMA_BASE_URL=http://localhost:11434

HF_TOKEN=your_huggingface_token

OPENAI_API_KEY=

ANTHROPIC_API_KEY=
```

Save and exit.

```text
Ctrl + O
Enter
Ctrl + X
```

---

# Step 19 — Final Verification

Run the following commands to verify that everything is working.

```bash
python --version
```

```bash
conda activate ai-redteam
```

```bash
python -m garak --version
```

```bash
python -c "from pyrit.common import default_values; print('PyRIT OK')"
```

```bash
python -c "from art.attacks.evasion import FastGradientMethod; print('ART OK')"
```

```bash
ollama list
```

```bash
curl http://localhost:11434/api/tags
```

```bash
curl http://localhost:6333
```

```bash
promptfoo --version
```

```bash
python -c "import openai, dotenv; print('Keys OK')"
```

---

# 📦 Installed Tools

| Tool | Purpose |
|------|---------|
| 🐍 Miniconda | Python environment management |
| 🔥 PyTorch | Deep learning framework |
| 🤗 Transformers | Hugging Face LLM library |
| 📊 Scikit-learn | Machine learning toolkit |
| 🛡️ Garak | LLM vulnerability scanner |
| 🔴 Microsoft PyRIT | AI Red Teaming framework |
| 🧪 IBM ART | Adversarial ML testing |
| 📝 Promptfoo | Prompt evaluation framework |
| 🦙 Ollama | Local LLM runtime |
| 🧠 Llama 3.2 | Open-source language model |
| 🐳 Docker | Container platform |
| 📚 Qdrant | Vector database |
| 🧩 DVLLM | LLM vulnerability testing platform |
| 💻 VS Code | Code editor |
| 🤗 Hugging Face Hub | Model repository and authentication |

---

# 🎯 Next Steps

After completing this setup, your AI Red Team lab is ready for:

- Prompt Injection Testing
- Jailbreak Evaluation
- Garak Security Scans
- Microsoft PyRIT Assessments
- IBM ART Adversarial Attacks
- Promptfoo Benchmarking
- Local LLM Testing with Ollama
- RAG Security Experiments
- Vector Database Security Testing
- AI Red Teaming Research

---

⭐ If you found this guide helpful, consider starring the repository and following for more AI Security, LLM Red Teaming, RAG Security, and Adversarial Machine Learning resources.
