# AI-Powered Personalized Learning Pathways in Online Education

> A research-backed intelligent tutoring system that generates dynamic, personalized learning paths using RAG, NLP, and LLMs.

---

## 📄 Research Paper

**Title:** AI-Powered Personalized Learning Pathways in Online Education  
**Institution:** JSS Academy of Technical Education, Noida, India  
**Department:** Computer Science and Engineering  
**Authors:** Mrs. Rachna Jain · Deepanshi Jain · Anmol Gupta · Arpan Jaiswal  

---

## 🧠 Overview

Traditional one-size-fits-all education fails to address the diverse learning needs of students. This project proposes an **AI-Powered Learning Path Generator** that dynamically builds personalized, goal-driven learning roadmaps by combining:

- **Retrieval-Augmented Generation (RAG)** — for accurate, context-aware content retrieval
- **Large Language Models (LLMs)** — for natural language understanding and path generation
- **Natural Language Processing (NLP)** — for learner profiling, intent detection, and content analysis
- **AI Mentor Chatbot** — for real-time feedback, motivation, and adaptive interaction

The system accepts voice, text, and image inputs, processes them through a pipeline, and outputs a tailored learning path aligned with the learner's goals and skill gaps.

---

## 🏗️ System Architecture

```
User Input (Text / Voice / Image)
        │
        ▼
  NLP Preprocessing
  (ASR → Tokenization → NER → Lemmatization)
        │
        ▼
  Vector Database (Semantic Embeddings)
        │
        ▼
  RAG Framework ──────────────► Knowledge Base
        │
        ▼
  LLM (Fine-tuned on learner queries)
        │
   ┌────┴────────────────┐
   ▼                     ▼
Learning Path         AI Mentor
Generator             Chatbot
   │                     │
   └────────┬────────────┘
            ▼
   Integrated Learning Platform
   (Progress Tracker + Feedback Loop)
```

---

## ⚙️ Core Components

### 1. Data Pipeline
- Sources: Kaggle datasets, online learning platforms, institutional records, learner resumes
- Preprocessing: Normalization, tokenization, stop-word removal, NER, lemmatization
- Split: **70% training / 20% validation / 10% testing**
- Embeddings: High-dimensional vector space via semantic encoders / OpenAI embeddings

### 2. RAG + Vector Database
- Retrieves semantically relevant content from the vector store before generating responses
- Unlike standalone LLMs, RAG **acts** rather than just reacts — generating specific, grounded pathways
- Minimizes hallucination through live retrieval from up-to-date knowledge bases

### 3. Personalized Path Generation (LLM)
- Fine-tuned on contextual datasets: learner queries, topic explanations, feedback interactions
- Generates goal-driven roadmaps aligned to individual skill gaps and learning pace
- Dynamically updates paths as the learner progresses

### 4. AI Mentor Chatbot
- Powered by the same LLM + RAG stack
- Provides: concept explanations, real-time Q&A, motivational prompts, adaptive feedback
- Continuously updates the learner's vector profile based on interaction history

### 5. Progress Tracker
- Monitors: quiz scores, session length, engagement frequency
- Visualizes learning milestones, skill gaps, and progress predictions
- Feeds data back into the learner profile for continuous path refinement

---

## 📊 Evaluation Metrics

| Metric | Formula | What It Measures |
|--------|---------|-----------------|
| **Performance Uplift Ratio (PUR)** | `(PostTest − PreTest) × 100 / PreTest` | Learning improvement after system interaction |
| **Semantic Retrieval Precision (SRP)** | `Relevant Recommendations / Total Recommendations` | RAG retrieval accuracy and hallucination reduction |
| **Active Engagement Rate (AER)** | `Active Learning Time / Total Session Time` | Depth of learner interaction per session |

---

## 📈 Results

The proposed model was benchmarked against prior works including Yang et al. (2025), Naseer et al. (2024), and Ming Yang et al. (2023) across five performance dimensions:

| Metric | Reviewed Models | Proposed Model |
|--------|----------------|----------------|
| Path Accuracy | Moderate | Significantly Higher |
| Engagement | Limited real-time adaptation | Continuous, adaptive |
| Skill Improvement | 10–20% gains | **25–35% improvement** |
| RAG Accuracy | No live retrieval | Vector DB live retrieval |
| User Satisfaction | Static feedback | Real-time, personalized |

> The proposed model achieved an **average improvement of 25–35%** across all metrics compared to existing approaches.

---

## 🔬 Tech Stack

| Layer | Technology |
|-------|-----------|
| Language Understanding | NLP, Named Entity Recognition (NER) |
| Path Generation | LLM (fine-tuned), Transformer-based models |
| Knowledge Retrieval | RAG, Vector Database, Semantic Encoders |
| Voice Input | Automatic Speech Recognition (ASR) |
| Multimodal Input | Text, Voice, Image |
| Deployment | Cloud-based, modular architecture |

---

## 🆚 Proposed vs. Reviewed Models

| Parameter | Reviewed Models | Proposed Model |
|-----------|----------------|----------------|
| Adaptability | Static / semi-adaptive | Fully adaptive, real-time |
| Technology Stack | ML, CNN, or Transformers used separately | LLM + NLP + RAG integrated |
| Personalization | Pre-trained on limited profiles | Dynamic profiling + continuous feedback |
| Data Retrieval | Static / predefined datasets | RAG-based live retrieval from vector DB |
| User Interaction | No direct interaction | Multimodal AI Mentor Chatbot |
| Feedback | Limited, static | Real-time, integrated into learning path |
| Scalability | Dataset/infrastructure-constrained | Cloud-based, modular, scalable |

---

## 🔭 Future Scope

- Expand support for **multiple languages** and global educational repositories
- Integrate with **diverse learning platforms** for a more universal experience
- Strengthen **data privacy**, bias mitigation, and model transparency mechanisms
- Investigate long-term effectiveness across **larger, diverse learner populations**
- Scale into a fully functional **Intelligent Tutoring System (ITS)**

---

## 📚 Key References

1. Subramanian et al. — *AI-Powered Learning Pathways: Personalized Learning and Dynamic Assessments*, IJACSA, 2025
2. Yang & Liang — *Personalized Learning Path Recommendation System Based on LLM*, Applied Sciences, 2023
3. Naseer et al. — *Integrating deep learning techniques for personalized learning pathways*, Heliyon, 2024
4. Rodrigues et al. — *AI-Driven Intelligent Tutoring Systems in Engineering Education*, IEEE Access, 2024
5. Yang & Wen — *AI-Powered Personalized Learning Journeys*, Journal of Information Systems Engineering, 2023

---

## 📁 Project Structure

```
├── backend/               # Flask backend and API routes
├── frontend/              # React frontend (Vite + Tailwind)
├── src/
│   ├── agents/            # Base, research, and teaching agents
│   ├── data/              # Vector store, BM25 retriever, document store
│   ├── ml/                # Embeddings, reranker, query rewriter, model orchestrator
│   ├── services/          # Chatbot, conversation manager, progress tracker
│   └── utils/             # Cache, config, semantic cache, observability
├── web_app/               # Main Flask web application
│   ├── templates/         # HTML templates
│   ├── static/            # CSS and JS assets
│   └── learning_paths/    # Pre-generated learning path JSONs
├── migrations/            # Database migration scripts
├── worker/                # Celery async worker
├── requirements.txt       # Python dependencies
├── Dockerfile             # Container configuration
└── README.md
```

---

## 🚀 Getting Started

```bash
# Clone the repository
git clone https://github.com/deepanshi-jain/intelligent-tutor.git
cd intelligent-tutor

# Set up virtual environment
python -m venv .venv
.venv\Scripts\Activate.ps1   # Windows
# or
source .venv/bin/activate     # Linux/Mac

# Install dependencies
pip install -r requirements.txt

# Configure environment variables
cp .env.example .env
# Edit .env with your API keys

# Initialize the database
python init_db.py

# Run the application
python run.py
```

---

## 📜 License

This project is licensed under the terms specified in the [LICENSE](LICENSE) file.

---

*Research conducted at JSS Academy of Technical Education, Noida, India · Department of Computer Science and Engineering*
