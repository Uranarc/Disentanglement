# Disentanglement: Comparing Topic Modeling and LLMs

This repository contains the code and resources for the final degree project titled "Disentanglement", authored by Daniel Nascimento and Pedro Prata. The study explores and compares topic modeling techniques (BERTopic) against Large Language Models (Llama 3) for the task of conversation disentanglement.

## Repository Structure

- **/notebooks**: Contains the Jupyter notebooks with the experimental code.
  - `Bertopic.ipynb`: Experiments using BERTopic for topic modeling.
  - `Llama.ipynb`: Experiments using Llama 3 with prompt engineering.
- **/annotation_materials**: Includes the manual and template used for data annotation. It should be noted that the file contains a sample annotation. It should not be used for research purposes.
- **/data**: This directory is intentionally left without data files. See the Data section below.
  - **/sample_data**: Contains a small, fabricated dataset to demonstrate the code's functionality.
- `requirements.txt`: A list of all Python dependencies required to run the notebooks.
- `LICENSE`: The project is licensed under the MIT License.

## How to Run

1.  Clone this repository.
2.  Create a virtual environment and install the required packages:
    ```bash
    pip install -r requirements.txt
    ```
3.  Open the notebooks in the `/notebooks` directory using Jupyter or VS Code.

## Data

Please note that due to confidentiality agreements and to protect the privacy of the participants, the original chatroom data from the Debaqi project cannot be made public. The notebooks are structured to be adapted to other conversational datasets.

## Citation

If you use this work, please cite it as follows:

> Nascimento, D., & Prata, P. (2025). *Disentanglement*. Final Degree Project, Universidade Lusófona. [Link to your GitHub Repository]