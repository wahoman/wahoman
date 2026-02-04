# 👋 2년차 AI 개발자 여형구입니다

## 🌟 Introduction

KT 에이블 스쿨과 메타버스 아카데미를 거쳐, 현재 AI & Data Engineer로 재직 중입니다.
단순한 모델링을 넘어, 데이터 생성(Synthesis)부터 **모델 구조 설계(Architecture)**, 그리고 대규모 데이터 처리 인프라(MLOps)까지 AI 개발 전 과정을 주도적으로 수행하고 있습니다.

특히 **물리학 기반의 데이터 합성**으로 데이터 부족 문제를 해결하고, **GPU 가속 및 커스텀 툴 개발**을 통해 비효율적인 워크플로우를 개선하는 데 강점이 있습니다.

### 🎓 Education
- **2023.05 ~ 2023.12**: 메타버스 아카데미 AI 과정 수료 (우수 수료생)
- **2022.07 ~ 2023.01**: KT 에이블 스쿨 AI 과정 수료

---

## 🚀 Key Competencies

### 1. Data Engineering & Curation
- **Physics-based Data Synthesis**: X-ray 물성(Log Attenuation)을 반영한 고정밀 합성 데이터 생성 알고리즘 구현
- **Unsupervised Curation**: DINOv2 임베딩과 HDBSCAN 군집화를 활용한 데이터 편향 제거 및 균형 확보
- **Data Integrity**: 대규모 데이터셋의 무결성 검증 및 자동 복구 파이프라인 구축

### 2. Advanced Modeling
- **Custom Architecture**: 소형 객체(Small Object) 탐지 성능 향상을 위한 YOLOv11 P2-P5 Neck 구조 설계
- **Analysis System**: 취약 각도 분석을 위한 9-View 동시 비교 뷰어 개발 및 오탐률 30% 개선
- **Transformer Application**: CNN의 한계를 보완하기 위한 RT-DETRv2 도입 및 최적화

### 3. MLOps & Infrastructure
- **GPU Acceleration**: `CuPy` 커널 최적화를 통한 전처리 파이프라인 속도 10배 향상
- **Custom DVC**: `SQLite` 인덱싱 기반의 1TB+ 데이터 버전 관리 및 시점 복원 시스템 구축
- **Internal Tooling**: 연구원 협업 효율화를 위한 PyQt5 기반 GUI 라벨링/검수 툴 40종 개발

---

## 🛠 Tech Stack

<div align="center">

### Languages
<img src="https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white" height="25"/>
<img src="https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black" height="25"/>
<img src="https://img.shields.io/badge/SQL-4479A1?logo=postgresql&logoColor=white" height="25"/>

### AI & ML
<img src="https://img.shields.io/badge/PyTorch-EE4C2C?logo=pytorch&logoColor=white" height="25"/>
<img src="https://img.shields.io/badge/TensorFlow-FF6F00?logo=tensorflow&logoColor=white" height="25"/>
<img src="https://img.shields.io/badge/YOLO-0078D4?logo=yolo&logoColor=white" height="25"/>
<img src="https://img.shields.io/badge/OpenCV-5C3EE8?logo=opencv&logoColor=white" height="25"/>
<img src="https://img.shields.io/badge/LangChain-000000?logo=langchain&logoColor=white" height="25"/>
<img src="https://img.shields.io/badge/CuPy-76B900?logo=nvidia&logoColor=white" height="25"/>

### Backend / Web
<img src="https://img.shields.io/badge/FastAPI-009688?logo=fastapi&logoColor=white" height="25"/>
<img src="https://img.shields.io/badge/Django-092E20?logo=django&logoColor=white" height="25"/>
<img src="https://img.shields.io/badge/React-61DAFB?logo=react&logoColor=black" height="25"/>
<img src="https://img.shields.io/badge/PyQt5-41CD52?logo=qt&logoColor=white" height="25"/>

### DevOps & Tools
<img src="https://img.shields.io/badge/Git-F05032?logo=git&logoColor=white" height="25"/>
<img src="https://img.shields.io/badge/Docker-2496ED?logo=docker&logoColor=white" height="25"/>
<img src="https://img.shields.io/badge/Linux-FCC624?logo=linux&logoColor=black" height="25"/>
<img src="https://img.shields.io/badge/VS Code-007ACC?logo=visualstudiocode&logoColor=white" height="25"/>

</div>

---

## 📂 Projects

### 📌 X-ray 위해물품 탐지 솔루션 고도화 (현업 프로젝트)
**Role:** AI & Data Engineer (기여도 100%)
- **Data Synthesis**: 단순 합성이 아닌 물리적 투과율($\mu$)을 계산하여 배경과 자연스럽게 겹치는 TIP(Threat Image Projection) 엔진 개발.
- **Model Optimization**: 극소형 객체(탄피, 칼날 등) 탐지를 위해 고해상도 특징맵을 보존하는 P2-P5 Neck 아키텍처 적용.
- **Analysis Tool**: 단일 뷰의 한계를 넘기 위해 9개 시점을 동시에 분석하고 오탐 원인을 추적하는 자체 뷰어 개발.

### 📌 대규모 데이터 처리 파이프라인 구축 (In-house)
**Role:** MLOps Engineer (기여도 100%)
- **Custom DVC**: OS 파일 시스템의 탐색 속도 한계를 극복하기 위해 SQLite 기반의 인덱싱 시스템 개발 (조회 속도 0.01초 미만).
- **High Performance**: 기존 CPU(NumPy) 기반의 전처리 로직을 GPU(CuPy) 벡터 연산으로 마이그레이션하여 속도 10배 향상.
- **Automation**: 데이터 무결성 검증, 라벨링 포맷 변환, 압축 등을 원클릭으로 수행하는 사내 GUI 툴 40여 종 배포.

<br>

### 📌 Side Projects & Studies
**"다양한 기술 스택에 대한 호기심과 실행력"**

| Project Name | Description | Tech Stack |
| :--- | :--- | :--- |
| [📚 PDF RAG 챗봇](https://github.com/wahoman/pdf_tokenize_Chatbot) | **PDF 기반 RAG 챗봇 (문서 검색형 응답 시스템)** | `LangChain`, `ChromaDB`, `LLaMA` |
| [🎯 SVG 여행지 추천](https://my-travel-5.onrender.com/) | **SVG 지도 기반 지역 선택 + 랜덤 여행지 셔플 웹앱** | `React`, `FastAPI`, `Axios` |
| [🧞 챗봇 자비스](https://github.com/wahoman/Chatbot-Jarvis) | **MySQL 기반 대화 기억형 LLM 챗봇 시스템** | `LLM`, `MySQL`, `FastAPI` |
| [🎨 AI 음악 창작](https://github.com/wahoman/singsongchanson-AI.git) | **텍스트 & 이미지 기반 음악 + 앨범 아트 생성** | `MusicGen`, `Stable Diffusion` |
| [🧪 LORA 이미지 생성](https://github.com/wahoman/Lora) | **LoRA 기반 X-ray 이미지 생성 및 데이터 보강 연구** | `LoRA`, `Stable Diffusion` |
| [📊 EPL 몸값 예측](https://github.com/wahoman/EPL) | **선수 데이터 크롤링 + 머신러닝 기반 몸값 예측** | `RandomForest`, `Pandas` |
| [🧠 맞춤형 광고](https://github.com/wahoman/CNN-based_advertising_services.git) | **실시간 얼굴 인식 → 성별/연령 기반 광고 추천** | `ResNet50`, `CNN`, `Mediapipe` |

---

<div align="center">
  <b>Contact</b><br>
  📧 hgy8401@naver.com | 📞 010-3585-8401
</div>
