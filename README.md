# File Structure

## .env_example

Template for storing API keys (e.g., OPENROUTER_API_KEY). Rename to .env.

## environment.yml

Conda env file with required packages (e.g., cellxgene-census, scanpy, anndata).

## cellxgene_description.ipynb

Loads CELLxGENE datasets and generates summaries using metadata.

## OpenRouter_example.ipynb

Shows how to call LLMs via OpenRouter API for prompt testing.

# Usage Instructions (on WSL Ubuntu 22.04.5 LTS)

## Install Conda (if not installed):

bash
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
bash Miniconda3-latest-Linux-x86_64.sh

## Create the environment:

bash
conda env create -f environment.yml

## Activate it:

bash
conda activate cellxgene-env

## Notes

The core script is cellxgene_description.ipynb — it fetches and summarizes dataset info using LLMs.

OpenRouter_example.ipynb explores available models via the OpenRouter API and test prompts.

## API Keys
Create a .env file in the project root:

.env
OPENROUTER_API_KEY=your_openrouter_key_here

Make sure your code loads it with:

python
from dotenv import load_dotenv
load_dotenv()
