# Fast.AI LangChain Presentation

This README provides the steps necessary to run the code presented in the LangChain introduction and code walkthrough. Follow these instructions to set up your environment and execute the notebook.

### 1. Create an Account at [Pinecone](https://www.pinecone.io/)
- **Note:** You will need an account, but the usage required for this notebook is well within the free tier and won't cost you anything.
- Once your account is created, create a new project. You can name this project whatever you'd like.

### 2. Create a New Index
- Name the index `textbook-vector-store`.
  - **Note:** You can name your index differently, but ensure you update the notebook to reflect the new name.
- Set the dimensions of the index to **768**.
  - **Note:** The dimensions are based on the embedding model you use. For this demonstration, a local HuggingFace `sentence-transformers/all-mpnet-base-v2` model was used, so the dimensions are 768. If you're using OpenAI's `text-embedding-3-small` embedding model, set the index dimensions to **1536**.

### 3. Set Environment Variables
- Set the `PINECONE_API_KEY` environment variable to the API key for your project. This can be found on the middle left-hand side of the screen after you have selected your project from the list.
- Set the `OPENAI_API_KEY` environment variable to your OpenAI API key.
- *(Optional)* Set your `ANTHROPIC_API_KEY` environment variable to your AnthropIC API key. This isn't used in the actual RAG implementation but is included as an example earlier in the notebook, so it's not required.

### 4. Clone the Notebook to Your Local Machine
- Clone the repository containing the notebook to your local machine.

### 5. Create a Virtual Environment
- Run the following command to create a virtual environment:
  ```Ebash
  python -m venv venv
  ```
- Enter and activate your virtual environment:
  - On Windows:
    ```Ebash
    .\venv\Scripts\activate
    ```
  - On macOS/Linux:
    ```bash
    source venv/bin/activate
    ```

### 6. Install Required Packages
- Install the required packages using the `requirements.txt` file:
  ```bash
  pip install -r requirements.txt
  ```

### 7. Install PyTorch with CUDA
- Visit [PyTorch's official website](https://pytorch.org/get-started/locally/) and get the command for your particular setup to install PyTorch with CUDA enabled in your virtual environment.
  - **For example:** On my setup, I used:
    ```bash
    pip3 install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu118
    ```

### 8. Run the Notebook
- That's it! You can now run all the cells in the notebook and create your own notebook-based textbook RAG pipeline.

*This presentation was presented live on June 29, 2024, and the video is available on YouTube at [https://www.youtube.com/watch?v=D11C8MrFEUk](https://www.youtube.com/watch?v=D11C8MrFEUk).*
