# Legal Intelligence Agentic System

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://python.org)
[![Gradio](https://img.shields.io/badge/Gradio-UI-orange.svg)](https://gradio.app)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

An AI-powered legal intelligence system that combines Retrieval-Augmented Generation (RAG), Large Language Models (LLMs), and agentic workflows to assist in legal case analysis and precedent-based reasoning.

## 🎯 Project Overview

This system was developed as part of the Hannoworks Internship Assignment, demonstrating the implementation of a sophisticated legal intelligence platform capable of:

- **Precedent-Based Analysis**: Retrieving and analyzing relevant legal precedents
- **Multi-Perspective Arguments**: Generating comprehensive arguments for both petitioner and respondent
- **Constitutional Law Focus**: Specializing in Indian constitutional law and privacy rights
- **Agentic Reasoning**: Multi-step legal reasoning with evidence integration

## 🏗️ System Architecture

```
User Input → Legal Agent → Document Processor → Vector Store → Legal Reasoner → Output
     ↑                                                                              ↓
Gradio UI ←←←←←←←←←←←←←←←←←←←←←←←←←←←←←←←←←←←←←←←←←←←←←←←←←←←←←←←←←←←←←←←←←← Results
```

### Core Components

1. **DocumentProcessor**: Handles legal document preprocessing and intelligent chunking
2. **VectorStore**: Manages embeddings and similarity search using FAISS
3. **LegalReasoner**: Provides AI-powered legal analysis using Groq LLM
4. **LegalAgent**: Orchestrates the complete agentic workflow

## 🚀 Features

- **🔍 Intelligent Precedent Retrieval**: Vector-based similarity search for relevant case law
- **⚖️ Comprehensive Legal Analysis**: Multi-faceted case analysis with structured reasoning
- **👥 Multi-Perspective Arguments**: Generate arguments for both sides of legal disputes
- **🎯 Constitutional Law Expertise**: Specialized in Indian constitutional law and privacy rights
- **📊 Interactive UI**: User-friendly Gradio interface for easy interaction
- **🔧 Modular Architecture**: Easily extensible and maintainable design

## 📋 Requirements

```
python>=3.8
gradio>=4.0.0
sentence-transformers>=2.2.0
faiss-cpu>=1.7.4
groq>=0.4.0
numpy>=1.21.0
pandas>=1.3.0
```

## 🛠️ Installation

1. **Clone the repository**:
```bash
git clone https://github.com/yourusername/legal-intelligence-system.git
cd legal-intelligence-system
```

2. **Install dependencies**:
```bash
pip install -r requirements.txt
```

3. **Get Groq API Key**:
   - Sign up at [Groq Console](https://console.groq.com/)
   - Generate your API key
   - Keep it handy for system setup

## 🎮 Usage

### Running on Kaggle (Recommended)

1. **Upload the notebook** to Kaggle
2. **Enable internet access** in notebook settings
3. **Run all cells** to start the system
4. **Access the Gradio interface** through the provided public link

### Local Deployment

1. **Run the main script**:
```bash
python legal_intelligence_system.py
```

2. **Open your browser** to `http://localhost:7860`
3. **Follow the setup instructions** in the interface

### System Setup

1. **Enter your Groq API Key** in the Setup tab
2. **Optionally add legal documents** or use default privacy law precedents
3. **Click "Build Knowledge Base"** to initialize the system
4. **Wait for confirmation** that the knowledge base is ready

### Analyzing Legal Cases

1. **Navigate to Case Analysis tab**
2. **Enter your case description** (a sample is provided)
3. **Adjust the number of precedents** to retrieve (3-10)
4. **Click "Analyze Case"** and wait for results
5. **Review the comprehensive analysis** including:
   - Relevant precedents with similarity scores
   - Detailed legal analysis
   - Petitioner arguments
   - Government/Respondent arguments

## 📖 Example Usage

### Sample Case Analysis

**Input**: 
"In 2025, a new case challenges a government policy that mandates all citizens to submit biometric data for accessing public services. A petitioner argues that the policy violates their privacy rights, citing the 2017 Supreme Court judgment."

**Output**:
- **Precedents**: K.S. Puttaswamy v. Union of India (2017) and related privacy cases
- **Analysis**: Comprehensive legal analysis applying the three-fold test
- **Arguments**: Detailed arguments for both petitioner and government

### Precedent Search

**Query**: "right to privacy Article 21 biometric data"
**Results**: Ranked legal precedents with similarity scores and relevant excerpts

## 🔧 Configuration

### Key Configuration Parameters

```python
GROQ_API_KEY = "your_api_key_here"      # Your Groq API key
EMBEDDING_MODEL = "all-MiniLM-L6-v2"     # Sentence transformer model
LLM_MODEL = "llama3-8b-8192"             # Groq LLM model
VECTOR_DIM = 384                         # Embedding dimensions
CHUNK_SIZE = 1000                        # Document chunk size
CHUNK_OVERLAP = 200                      # Chunk overlap for context
```

### Customization Options

- **Legal Document Corpus**: Add your own legal documents to the knowledge base
- **Precedent Count**: Adjust the number of precedents retrieved (3-10)
- **Analysis Depth**: Modify prompt templates for different analysis styles
- **UI Themes**: Customize the Gradio interface appearance

## 🏛️ Legal Domain Focus

The system is specifically designed for:

- **Indian Constitutional Law**: Article 21, fundamental rights, privacy law
- **Privacy Rights Cases**: Puttaswamy judgment and related precedents
- **Government Policy Challenges**: Biometric data, surveillance, digital governance
- **Multi-stakeholder Analysis**: Petitioner vs. Government perspectives

## 🔍 Technical Details

### RAG Pipeline
- **Document Processing**: Text cleaning, chunking with overlap
- **Vector Embeddings**: Sentence-BERT with 384-dimensional vectors
- **Similarity Search**: FAISS L2 distance with normalized embeddings
- **Context Integration**: Precedent integration with legal reasoning

### Agentic Workflow
1. **Query Processing**: Understanding legal case descriptions
2. **Precedent Retrieval**: Vector similarity search for relevant cases
3. **Context Preparation**: Formatting precedents for LLM consumption
4. **Legal Analysis**: Multi-step reasoning with constitutional law focus
5. **Argument Generation**: Perspective-specific argument development

### LLM Integration
- **Model**: Groq's Llama3-8B-8192 for fast inference
- **Prompting**: Specialized legal prompts with constitutional law context
- **Temperature Control**: 0.3 for analysis, 0.4 for argument generation
- **Token Management**: Optimized token usage for comprehensive responses

## 📊 Performance Metrics

- **Precedent Retrieval**: Sub-second similarity search across document corpus
- **Analysis Generation**: 10-30 seconds for comprehensive legal analysis
- **Argument Quality**: Structured, legally sound arguments with precedent citation
- **UI Responsiveness**: Real-time feedback and status updates

## 🚦 Limitations and Future Work

### Current Limitations
- **Language**: English language legal documents only
- **Jurisdiction**: Focused on Indian constitutional law
- **Document Size**: Memory constraints for very large legal corpora
- **Real-time Updates**: No automatic legal database updates

### Future Enhancements
- **Multi-language Support**: Support for regional Indian languages
- **Broader Jurisdiction**: Extension to other legal domains
- **Fine-tuning**: Custom legal language model training
- **Feedback Loop**: User rating system for continuous improvement
- **Cloud Deployment**: Scalable production deployment
- **API Integration**: REST API for external system integration

## 🤝 Contributing

We welcome contributions! Please see our [Contributing Guidelines](CONTRIBUTING.md) for details.

### Development Setup

1. Fork the repository
2. Create a feature branch: `git checkout -b feature-name`
3. Make your changes and add tests
4. Submit a pull request with detailed description

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- **Hannoworks** for providing the internship assignment opportunity
- **Groq** for providing fast LLM inference capabilities
- **Sentence Transformers** for high-quality embeddings
- **FAISS** for efficient vector similarity search
- **Gradio** for the intuitive user interface framework

## 🎓 Educational Use

This project serves as an educational example of:
- Retrieval-Augmented Generation (RAG) implementation
- Agentic AI system design
- Legal domain AI applications
- Modern NLP pipeline architecture
- Production-ready AI system development

---
