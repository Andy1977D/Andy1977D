## Profile Andy1977D

## In this profile, I showcase some ideas I developed independently from any customer project


<h1 align="center">🛒 Regalscan – Real-time Shelf-Monitoring with YOLO v8 & LangChain-RAG</h1>

<p align="center">
 Computer-Vision pipeline that detects products on retail shelves to improve the shopping experience.<br>
 <strong>Python • YOLO v8 • OpenCV • LangChain • FAISS • AI</strong>
</p>

<p align="center">
  <a href="https://github.com/andy1977d/regalscan/actions">
    <img alt="Build" src="https://github.com/andy1977d/regalscan/workflows/ci/badge.svg">
  </a>
  <a href="https://opensource.org/licenses/MIT"><img alt="MIT" src="https://img.shields.io/badge/License-MIT-green.svg"></a>
  <a href="https://github.com/andy1977d/regalscan/releases"><img alt="release" src="https://img.shields.io/github/v/release/andy1977d/regalscan"></a>
</p>

---

## ✨ Why Regalscan?

* **Lost sales** ≈ 4 % in German retail stem from empty facings / stock-outs and/or people giving up searching for their product after a couple of minutes. 
* Store audits are still **manual & costly**.  
* Existing CV solutions struggle with **lighting & occlusion** in real stores.

Regalscan shows how a **compact edge-model (YOLOv8-n)** can help finding the right product
That can improve the shopping experience and in enhance the customer binding, if provided by a supermarket
Many additional features as in-shop navigation cand be included as well.

---

## 🏗️ Architecture

```mermaid
graph LR
X[Target Objects] --> Y[Ref. Feature Extract ConvNext]
Y -->E
A[Cam/Raspi] --> C[YOLO v8 Inference]
C --> D[Feature Extract ConvNext]
D --> E[Cosine Similarity FAISS]
E --> G[Item pick]
G --> H[Visualization]

