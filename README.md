# 🌿 Vi-TCM Topology Explorer

**A Clinical Decision Support System utilizing Natural Language Processing (NLP) and Topological Data Analysis (TDA) to decode the synergistic networks of 714 herbs within the Vietnamese Pharmacopoeia (DoTatLoi-714 Benchmark).**

## 📖 Project Overview

This repository hosts the frontend source code for the **Vi-TCM Topology Explorer**, an interactive web application developed as the practical implementation of our Q1 academic journal submission: _"Knowledge-Driven Topological Data Analysis in Traditional Medicine: Semantic Mapper and Cross-Lingual Bipartite Networks Reveal Phylogenetic Signals"_.

Unlike standard linear reduction algorithms (e.g., PCA, t-SNE) which fragment complex multi-target herbal data into isolated bins, this project utilizes **TDA Mapper** and **Persistent Homology** on native-language semantic embeddings (TF-IDF). This approach mathematically proves that ancient traditional medical classifications inherently mirror modern evolutionary biology (phylogenetic signals).

## ✨ Key Features

- **🌐 Bilingual Interface (EN/VI):** Seamlessly switch between English and Vietnamese without reloading the page, preserving indigenous ontological semantics.
- **🧬 Interactive D3.js Topology:** Explore the mathematical "shape" of traditional clinical syndromes with full zoom, pan, and hover capabilities.
- **🧠 AI-Driven Clinical Analysis:** Input patient symptoms natively in Vietnamese. The system communicates via REST API with a Hugging Face backend to extract clinical semantics.
- **💡 Decision Support System:** Automatically recommends evolutionary "Hot Nodes" (e.g., _Asteraceae_, _Zingiberaceae_) to optimize synergistic multi-herb formulations.

## 🏗️ System Architecture

This project strictly separates computation from visualization using a modern dual-environment deployment:

- **Frontend (This Repository):** Hosted on **GitHub Pages**. Utilizes HTML5, Tailwind CSS, and D3.js to deliver a high-speed, interactive topological network visualization.
- **Backend / Inference API:** Hosted on **Hugging Face Spaces**. Processes raw textual symptoms using our trained NLP vectorizer (tfidf_vectorizer.pkl) and serves predictions via FastAPI/Gradio REST endpoints.

## 📂 Repository Structure

├── index.html # Main Web Application (UI & D3.js logic)  
├── topology_data.json # Pre-computed topological graph coordinates & labels exported from Colab  
├── semantic_tda_pipeline.py # The core Python notebook/script used to train the model and extract topologies  
└── README.md # Project documentation

## 🚀 How to Run Locally

Since this is a lightweight static frontend, running it locally is incredibly simple:

- **Clone the repository:**  
   git clone \[<https://github.com/vothikimanh1007/Vi-TCM-Explorer.git\>](<https://github.com/vothikimanh1007/Vi-TCM-Explorer.git>)  
   cd Vi-TCM-Explorer

- **Launch a local server:**  
   (Due to CORS policies when fetching local JSON files, you must run it via a local web server, not just by double-clicking the HTML file).  
   python -m http.server 8000

- **View the App:** Open your browser and navigate to <http://localhost:8000>.

## 🔗 Live Demo

- **Interactive Web App:** [Vi-TCM Topology Explorer (GitHub Pages)](#4mzd2o4d2wjs) _(Insert your GH pages link here)_
- **NLP Backend API:** [TradMed-NLP-Backend (Hugging Face)](#4mzd2o4d2wjs) _(Insert your HF Space link here)_

## 🎓 Author & Citation

**Vo Thi Kim Anh** - _Faculty of Information Technology, Ton Duc Thang University, Ho Chi Minh City, Vietnam_

- _Faculty of Electrical Engineering and Computer Science, VSB - Technical University of Ostrava, Czech Republic_

If you use this code, the DoTatLoi-714 dataset, or the topological methodology in your research, please consider citing our paper (Citation details pending publication).

_Developed with ❤️ for the advancement of computational ethnopharmacology._
