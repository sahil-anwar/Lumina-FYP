✨ Lumina
Deep Search Across All Extensions
An offline, privacy-first, multimodal semantic search system for local files.

Final Year Project · BS Computer Science · FAST–NUCES, Peshawar · 2025–2026



[!IMPORTANT]
🔒 Source Code Is Private
Lumina's complete application source code is kept in a separate, PRIVATE GitHub repository and is not publicly accessible. Access is restricted to authorized collaborators.

This public repository contains academic documentation only: the final thesis, project poster, proposal, and system diagrams. No application source code is published here.

📖 Overview
Lumina — Deep Search Across All Extensions is a local-first desktop search assistant built to help users retrieve meaningful information from collections of documents, images, recordings, and other supported files.

Unlike traditional file search, which often relies on filenames or exact keyword matches, Lumina processes file content, converts it into searchable representations, and retrieves contextually relevant results from natural-language queries. The project emphasizes offline operation, privacy, and a unified search experience across different media types.
💡 Why Lumina?
Challenge	Lumina's approach
Information is scattered across PDFs, documents, images, and recordings	Unified ingestion and search workflow
Exact keyword matching can miss relevant passages	Semantic embeddings and similarity search
Scanned images and speech aren't directly searchable	OCR and offline speech transcription
Private files should remain on the user's device	Local-first processing and storage
Large file collections are difficult to navigate	Ranked results with snippets, timestamps, and file paths


🚀 Main Capabilities
- Multimodal file indexing: Processes text/documents, images, and audio; the thesis also discusses video-oriented processing, with support depending on the available extractor.
- Semantic retrieval: Uses natural-language query embeddings and FAISS to identify relevant content.
- Optical Character Recognition (OCR): Extracts text from images with EasyOCR.
- Offline speech transcription: Uses Whisper to make spoken content searchable.
- Context-preserving chunking: Organizes extracted content into overlapping passages for retrieval.
- Custom re-ranking: Reorders candidate results using semantic similarity and additional ranking signals.
- Folder indexing and tracking: Supports adding local folders and monitoring indexing progress.
- Search and analytics interface: Displays result snippets, source locations, and indexing statistics.
- Optional AI features: The thesis describes local summarization with Ollama, smart collections, and keyword heatmaps.
🧠 How Lumina Works

High-level workflow:
1. Ingest: Select local folders and files for indexing.
2. Extract: Route supported file types to document extraction, OCR, or speech transcription.
3. Process: Split extracted content into chunks and associate it with source metadata.
4. Embed and index: Generate semantic vectors and store them in a FAISS index.
5. Search: Embed a natural-language query and retrieve relevant candidates.
6. Rank and present: Display ranked results with contextual snippets and links to original files.
The illustration and workflow summarize the thesis's architecture; individual file formats can follow different extraction paths.
Additional System Diagrams
Diagram	View
Activity diagram	[Open](diagrams/activity_lumina.png)
Flowchart	[Open](diagrams/flowchart_lumina.png)
Sequence diagram	[Open](diagrams/sequence_diagram.png)
Use-case diagram	[Open](diagrams/use_case.png)


🛠️ Technology Stack
The thesis's later implementation chapters describe the following technologies:
Component	Technology
Core language	Python 3.10+
Dependency management	Poetry
Backend / local API	FastAPI
Desktop interface	PyWebView
Frontend	HTML5, CSS3, Vanilla JavaScript
Semantic embeddings	SentenceTransformers (all-MiniLM-L6-v2)
Vector search	FAISS
Image text extraction	EasyOCR
Speech transcription	OpenAI Whisper
Additional vision model noted in the thesis	CLIP (ViT-B/32)
Optional local summaries	Ollama with qwen2.5:0.5b
Persistence	Local vector index and metadata storage


The implementation chapter documents the API at 127.0.0.1:8000, app storage under ~/.lumina, and an optional local LLM service at http://localhost:11434. Earlier project plans reference Electron; the stack above follows the later implementation description.
📚 Project Documents
Document	Description
📘 [Final Thesis](docs/Lumina-Thesis.pdf)	Project motivation, design, architecture, implementation, testing, and conclusions
🖼️ [Project Poster — PDF](docs/Lumina-Poster.pdf)	Academic poster
🖼️ [Project Poster — PNG](docs/Lumina-Poster.png)	Poster image for convenient viewing
📄 [Project Proposal](docs/Lumina-Proposal.pdf)	Initial project proposal and scope


Project Poster

🧪 Evaluation and Testing
According to the final thesis, the project reports:
- Approximately 260 automated unit and integration tests.
- A 95% test pass rate.
- Sub-100 ms FAISS vector lookup and metadata binding under the reported test conditions.
- Testing of multimodal indexing, chunk overlap, search re-ranking, index persistence, malformed-file handling, and search latency.
These are results reported in the academic thesis, not independently reproduced or verified by this documentation-only repository.
⚠️ Limitations and Future Work
The thesis notes hardware-dependent performance, incomplete support for some file formats, and the lack of personalized ranking.

Potential future improvements include encrypted multi-device synchronization, intelligent file organization, voice controls, and a plugin ecosystem.
🔒 Source Code Availability
PRIVATE — NOT OPEN SOURCE

The full Lumina implementation—including its backend, frontend, AI integration, configuration, and development assets—is private and is not distributed publicly through this repository. Its GitHub publication is intended for a separate private repository.
- Public Lumina-FYP repository: Thesis, proposal, poster, and architecture diagrams.
- Private source repository (separate): Intended for application code and implementation assets, with access restricted to authorized collaborators.
The installation commands described in the thesis are intended for users who have separately been granted access to the implementation. This repository does not provide a downloadable or runnable application.
🎓 Academic Credits
Project Team (as listed on the thesis cover):
- Sahil Anwar
- Shayan Rasool
- Azeem Ahmad
Supervisor: Dr. Ali Sayyed
Department: Computer Science
Institution: National University of Computer and Emerging Sciences (FAST–NUCES), Peshawar, Pakistan
Academic Session: 2022–2026
📝 Citation
For academic references, cite the thesis:
Anwar, S., Rasool, S., and Ahmad, A. Lumina: Deep Search Across All Extensions. Final Year Project thesis, Department of Computer Science, FAST–NUCES, Peshawar, 2025–2026.

Note: The thesis cover and declaration/approval pages show different surnames for one team member. Verify the official spelling before using the citation formally.
📜 Licensing and Use
This repository is shared for academic documentation and reference. No software license is granted for the private Lumina application source code. Please obtain permission from the relevant authors or institution before reproducing or redistributing the thesis, poster, or proposal.
Lumina — Deep Search Across All Extensions
Search locally. Find meaning. Protect privacy.
