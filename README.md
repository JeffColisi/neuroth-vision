
# NeuroTH-Vision
(Automated recognition and quantification of TH⁺ dopaminergic neurons in immunohistochemistry (IHC) images using computer vision.)

Pipeline de **Visão Computacional em C++** para reconhecimento e quantificação automatizados de **neurônios dopaminérgicos TH⁺** em imagens de **imunohistoquímica (IHC)**, usando **OpenCV**.

> Projeto desenvolvido no contexto da disciplina de **Visão Computacional (CEFET-MG)**, com foco em uma pipeline clara, modular e reprodutível para análise histológica.

---

## 1. Objetivo

O **NeuroTH-Vision** busca fornecer um pipeline de visão computacional que permita:

- Carregar e organizar imagens IHC com marcação TH⁺;
- Pré-processar as imagens (conversão de cor, normalização, redução de ruído);
- Segmentar regiões candidatas a neurônios TH⁺ via **visão computacional clássica**  
  (limiarização, morfologia, componentes conectados etc.);
- Quantificar neurônios (contagem, densidades, estatísticas básicas);
- Visualizar resultados com *overlays* para inspeção visual.

O projeto é pensado para ser:

1. Didático (para uso em disciplina de Visão Computacional);  
2. Suficientemente organizado para servir como base de pesquisa/portfólio.

---

## 2. Tecnologias

- **Linguagem:** C++17  
- **Biblioteca principal:** [OpenCV](https://opencv.org/) (visão computacional)  
- **Build system:** CMake (>= 3.10)

Opcionalmente, podem ser adicionados posteriormente:

- Ferramentas de *logging*;
- Módulos de *deep learning* (por exemplo, integração com modelos treinados externamente).

---

## 3. Estrutura do Projeto

```text
neuroth-vision/
├── CMakeLists.txt
├── README.md
├── LICENSE
├── .gitignore
├── data/
│   ├── raw/        # imagens IHC originais
│   └── processed/  # imagens pré-processadas / máscaras intermediárias
├── docs/
│   └── figures/    # figuras para relatório/apresentação
├── include/
│   └── neuroth_vision/
│       ├── io.hpp
│       ├── preprocessing.hpp
│       ├── segmentation.hpp
│       ├── quantification.hpp
│       └── visualization.hpp
└── src/
    ├── main.cpp
    ├── io.cpp
    ├── preprocessing.cpp
    ├── segmentation.cpp
    ├── quantification.cpp
    └── visualization.cpp

