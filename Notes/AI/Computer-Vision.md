## 👁️ Computer Vision (CV)

Computer Vision allows AI to "see" and interpret the physical world. In 2025, CV has shifted from simple pattern matching to **Spatial Understanding** and **Vision-Language Models (VLMs)**.

---

### 1. Key Computer Vision Tasks

* **Image Classification:** Identifying what is in an image (e.g., "This is a car").
* **Object Detection:** Identifying *what* and *where* (e.g., drawing bounding boxes around multiple pedestrians).
* **Image Segmentation:** Defining the exact pixel-level boundary of objects.
    * *Semantic Segmentation:* Labels every pixel (e.g., all "tree" pixels are green).
    * *Instance Segmentation:* Distinguishes between different objects of the same type (e.g., Tree #1 vs. Tree #2).
* **Pose Estimation:** Tracking human joints and movement for sports or security.

---

### 2. Modern CV Trends (2025)

* **Task-Agnostic Architectures:** Instead of separate models for detection and segmentation, 2025 models use a single "backbone" to do everything.
* **Edge-Optimized Vision:** Running real-time vision on drones and cameras without cloud dependency.

---

## How AI Thinks & Creates (IR to GenAI)

This module breaks down the bridge between raw data and the final AI output, covering the mechanics of Information Retrieval (IR) and the math behind image/video generation.

---

### 1. Information Retrieval (IR) & Vector Search

- When you ask an AI a question, it doesn't just "remember"—it often searches. This is called **RAG (Retrieval-Augmented Generation)**.

#### ** The Tokenization & Vectorization Phase**

1.  **Tokenization:** The AI breaks your input text into "tokens" (chunks of characters).
2.  **Vectorization:** Each token (and the whole query) is converted into a **Vector Embedding**—a long list of numbers representing the "meaning" of the text in high-dimensional space.
3.  **The Search:** The AI takes your query vector and looks into a **Vector Database** (like Pinecone or Milvus). It doesn't look for exact words; it looks for the **nearest neighbors** (vectors mathematically close to yours) using **Cosine Similarity**.

---

### 2. The Answer Generation Process

- Once the relevant facts are retrieved, the LLM starts the **Autoregressive Generation** process.

* **Context Injection:** The retrieved facts are pasted into the "hidden" part of your prompt.
* **Next-Word Prediction:** The AI doesn't write a whole paragraph at once. It calculates the **probability** of the next single token.
    * *Example:* For "The sky is...", the AI calculates: **Blue (92%)**, **Cloudy (5%)**, **Green (0.1%)**.
* **Sampling:** It picks the most likely token (or uses "Temperature" to add variety) and then feeds that word back into the input to predict the *next* one. This loops until the answer is complete.

---

### 3. Creating Pixels: The Diffusion Process

- Image and video generation don't "copy-paste" pieces of art. They use a physics-inspired process called **Diffusion**.

#### **Step 1: Forward Diffusion (The Training)**

- AI is trained by taking a clear image and slowly adding **Gaussian Noise** (random pixels) until it looks like "TV Static." The AI learns exactly how much noise was added at each step.

#### **Step 2: Reverse Diffusion (The Generation)**

1.  **Initial State:** The AI starts with a canvas of **100% Random Pixels** (pure noise).
2.  **Guided Denoising:** Guided by your text prompt, a neural network (usually a **U-Net**) "guesses" which pixels are noise and removes them.
3.  **Iterative Refinement:** This happens 20–50 times. With each step, the "static" begins to take the shape of the objects you described until a high-definition image emerges.

---

### 4. Video Generation: Adding the Time Dimension

Video generation (like Sora or Kling) is essentially **3D Diffusion**.

* **Spatio-Temporal Patches:** Instead of just 2D pixels, the AI generates "cubes" of data that include height, width, and **time**.
* **Temporal Consistency:** To prevent "flickering," the AI uses **Temporal Transformers**. These ensure that a pixel representing a "cat's ear" in Frame 1 stays a "cat's ear" in Frame 2, 3, and 4.
* **The Random Start:** Just like images, videos start as a **3D block of random noise** and are "denoised" into a coherent moving sequence.

---
