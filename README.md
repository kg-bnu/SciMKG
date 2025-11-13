
<img width="1024" height="1024" alt="Gemini_Generated_Image_1p5o1e1p5o1e1p5o" src="https://github.com/user-attachments/assets/6fb13ed9-28da-4456-9b73-02fe25ea50f6" />
<h1 align="center">SciMKG: AMultimodal Knowledge Graph for Science Education with Text, Image, Video and Audio </h1>
<p align="center">
  <!-- <!-- Stars / Forks -->
  <a href="https://github.com/kg-bnu/SciMKG">
    <img src="https://img.shields.io/github/stars/kg-bnu/SciMKG?style=flat-square&logo=github&label=Stars" />
  </a>
  <a href="https://github.com/kg-bnu/SciMKG/fork">
    <img src="https://img.shields.io/github/forks/kg-bnu/SciMKG?style=flat-square&logo=github&label=Forks" />
  </a> 

  <!-- PyPI -->
  <a href="https://pypi.org/project/scimkg/">
    <img src="https://img.shields.io/pypi/v/scimkg?style=flat-square&label=PyPI&logo=pypi" />
  </a>

  <!-- Dataset (Zenodo) -->
  <a href="https://zenodo.org/records/17578391">
    <img src="https://img.shields.io/badge/Dataset-Zenodo-orange?style=flat-square&logo=zenodo" />
  </a>
    <!-- Web -->
  <a href="https://scimkg.lutong.space/">
    <img src="https://img.shields.io/badge/Web-Project_Page-blue?style=flat-square&logo=googlechrome" />
  </a>
    <!-- Demo -->
  <a href="https://demo.scimkg.lutong.space/">
    <img src="https://img.shields.io/badge/Demo-Online-green?style=flat-square&logo=vercel" />
  </a>
</p>

<br>


<p align="center">
  <strong>SciMKG</strong> is a large-scale multimodal educational knowledge graph (MEKG) covering text, images, videos, and audio for K-12 science education.  
  It is automatically constructed using a novel LLM-powered pipeline for concept extraction and multimodal alignment.
</p>




## 🔥 Highlights

- **Four modalities covered**: text, image, video, audio  
- **1,356** knowledge points  
- **34,630** multimodal concepts  
- **403,400** triples  
- **10,527** images · **10,425** videos · **34,630** audios  


## 🚀 Overview

SciMKG is built using an **Extraction–Verification–Integration–Augmentation (EVIA)** pipeline:

1. **Extraction**  
   Use multiple LLMs to extract K–12 science concepts from MOOC subtitles.
2. **Verification**  
   Apply self-feedback (SELF-REFINE) to prune ambiguous or irrelevant concepts.
3. **Integration**  
   Use self-consistency voting to merge multiple LLM outputs.
4. **Augmentation**  
   Expand concepts through ConceptNet & Wikipedia; generate rewritten text and audio.
5. **Multimodal Alignment**  
   Align images, videos, and audio to concepts using multimodal LLMs (e.g., GPT-4o, Gemini).

This pipeline ensures **robustness, high precision, and semantic consistency across modalities**.


## 📦 Installation

```bash
pip install scimkg
```

```python
import  scimkg
kg = scimkg("video_path,pdf_path")
triples = kg.build("subject")
rdf = triples.rdf()
```

## 📊 Dataset Statistics

| Discipline | Knowledge Points | Concepts | Exercises | Triples |
| ---------- | ---------------- | -------- | --------- | ------- |
| Biology    | 526              | 16,839   | 255       | 191,928 |
| Physics    | 521              | 11,015   | 288       | 145,666 |
| Chemistry  | 309              | 6,776    | 220       | 65,806  |

| Modality | Items  | Concept Coverage |
| -------- | ------ | ---------------- |
| Image    | 10,527 | 39%              |
| Video    | 10,425 | 80%              |
| Audio    | 34,630 | 100%             |


## 🧠 Applications
SciMKG enables:
Multimodal educational question answering (MEQA)
Multimodal question generation
Cross-modal knowledge retrieval
Intelligent tutoring systems
Science education agents
Curriculum-level analytics



## 📬 Contact

Project Lead: ethanlu@mail.bnu.edu.cn

Dataset: https://zenodo.org/records/17578391

Demo: https://demo.scimkg.lutong.space/

Web Page: https://scimkg.lutong.space/


## 📄 Citation
If you use SciMKG or our construction framework, please cite:
```mathematica
@article{SciMKG2026,
  title={SciMKG: A Multimodal Knowledge Graph for Science Education with Text, Image, Video and Audio},
  author={Tong Lu, Zhichun Wang, Yaoyu Zhou, Yiming Guan, Zhiyong Bai, Junsheng Du},
  year={2026},
  journal={AAAI}
}
```





