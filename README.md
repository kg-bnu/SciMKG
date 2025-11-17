
<img width="1024" height="1024" alt="Gemini_Generated_Image_1p5o1e1p5o1e1p5o" src="https://github.com/user-attachments/assets/6fb13ed9-28da-4456-9b73-02fe25ea50f6" />
<h1 align="center">SciMKG: A Multimodal Knowledge Graph for Science Education with Text, Image, Video and Audio </h1>
<p align="center">
  <!-- <!-- Stars / Forks -->
  <a href="https://github.com/kg-bnu/SciMKG">
    <img src="https://img.shields.io/github/stars/kg-bnu/SciMKG?style=flat-square&logo=github&label=Stars" />
  </a>
  <a href="https://github.com/kg-bnu/SciMKG/fork">
    <img src="https://img.shields.io/github/forks/kg-bnu/SciMKG?style=flat-square&logo=github&label=Forks" />
  </a> 

  <!-- PyPI -->
   <a href="https://test.pypi.org/project/scimkg/">
	<img src="https://img.shields.io/badge/dynamic/json?url=https://test.pypi.org/pypi/scimkg/json&label=TestPyPI&query=%24.info.version&color=blue" />
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

<table>
  <tr>
    <th align="center">Discipline</th>
    <th align="center">Knowledge Points</th>
    <th align="center">Concepts</th>
    <th align="center">Exercises</th>
    <th align="center">Triples</th>
  </tr>
  <tr>
    <td align="center">Biology</td>
    <td align="center">526</td>
    <td align="center">16,839</td>
    <td align="center">255</td>
    <td align="center">191,928</td>
  </tr>
  <tr>
    <td align="center">Physics</td>
    <td align="center">521</td>
    <td align="center">11,015</td>
    <td align="center">288</td>
    <td align="center">145,666</td>
  </tr>
  <tr>
    <td align="center">Chemistry</td>
    <td align="center">309</td>
    <td align="center">6,776</td>
    <td align="center">220</td>
    <td align="center">65,806</td>
  </tr>
</table>


<table>
  <tr>
    <th align="center">Modality</th>
    <th align="center">Items</th>
    <th align="center">Concept Coverage</th>
  </tr>
  <tr>
    <td align="center">Image</td>
    <td align="center">10,527</td>
    <td align="center">39%</td>
  </tr>
  <tr>
    <td align="center">Video</td>
    <td align="center">10,425</td>
    <td align="center">80%</td>
  </tr>
  <tr>
    <td align="center">Audio</td>
    <td align="center">34,630</td>
    <td align="center">100%</td>
  </tr>
</table>



## 🧠 Applications
SciMKG enables:
* Multimodal educational question answering
* Multimodal question generation
* Cross-modal knowledge retrieval
* Intelligent tutoring systems
* Science education agents
* Curriculum-level analytics



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





