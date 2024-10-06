# RAG-Qdrant-pipeline 

## Overview

A powerful implementation of a Retrieval-Augmented Generation (RAG) model leveraging Qdrant as a vector store and Google Gemini for generative AI. This project enables intelligent document retrieval and response generation based on the context extracted from various PDF documents. 📄

**Architecture:**
![Architecture](https://drive.google.com/uc?export=download&id=1v3ddsQzANWDlaxKOMzahgpC_g3Emn3zd)

## Table of Contents

- [Features](#features)
- [Technologies Used](#technologies-used)
- [Installation](#installation)
- [Usage](#usage)
- [Example](#example)
- [Hybrid Search](#hybrid-search)
- [Contributing](#contributing)
- [License](#license)

## Features

- 📥 Load and process PDF documents from a specified directory.
- ✂️ Split documents into manageable chunks for efficient processing.
- 🔍 Use SentenceTransformers for generating embeddings.
- 💾 Store embeddings in Qdrant for fast retrieval.
- 🤖 Leverage Google Gemini for advanced question answering.
- 🔗 Hybrid search implementation combining vector similarity and keyword matching.
- 📝 Detailed context-aware responses based on user queries.

## Technologies Used

- **Langchain**: Framework for working with LLMs and document loaders.
- **Qdrant**: Vector database for efficient storage and retrieval of embeddings.
- **Google Gemini**: Generative AI model for producing intelligent responses.
- **Sentence Transformers**: Used for creating document embeddings.
- **PyMuPDF**: For loading and processing PDF files.

## Installation

To set up the project locally, follow these steps:

1. Clone the repository:

   ```bash
   git clone https://github.com/AtharvaKulkarniIT/rag-qdrant-pipeline.git
   cd rag-qdrant-pipeline-main
   ```

2. Install the required packages:

   ```bash
   pip install langchain PyMuPDF
   pip install langchain_google_genai
   pip install sentence-transformers
   ```

3. Set up your API keys:

   Make sure to add your Qdrant and Gemini API keys to the environment variables or replace them in the code directly.

## Usage

1. **Load Documents**: Ensure your PDF documents are in the specified data folder.
2. **Run the Script**: Execute the notebook to start the RAG processing.

## Example

To get a response about the rivers in Maharashtra, you can use the following input:

```python
input_text = "Describe the rivers in Maharashtra"
response = get_gemini_response(input_text)
print(response)
```

## Hybrid Search

The hybrid search combines results from both Qdrant's vector similarity search and keyword searches on the original documents. The results are ranked using Reciprocal Rank Fusion (RRF). 🔄

## Contributing

🤝 Contributions are welcome! If you have suggestions for improvements or want to add new features, feel free to create an issue or submit a pull request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details. 
