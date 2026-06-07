# 안녕하세요, 여형구입니다 👋

**Computer Vision을 코어로, 필요한 시스템을 0부터 만드는 AI / ML 엔지니어입니다.**

X-ray 보안검색 도메인의 스타트업에서 유일한 AI 개발자로 일하며,
데이터 파이프라인 → 모델 학습 → 서비스 백엔드까지 전 과정을 직접 설계하고 구축해 왔습니다.

> "막히면 데이터부터 의심한다" — 모델이 아니라 라벨을 고쳐 성능을 끌어올린 경험(mAP 0.50 → 0.86)이 저를 가장 잘 설명합니다.

<br>

## 🔭 대표 프로젝트

| 프로젝트 | 소개 | 키워드 |
|---|---|---|
| **[xray-agent-platform](https://github.com/wahoman/xray-agent-platform)** | 문서 질의응답(RAG)과 X-ray 이미지 탐지를 하나의 Agent가 상황에 맞게 골라 쓰는 FastAPI 백엔드. hybrid 검색(RRF)+LLM reranker 2단계, hit@k 평가 하니스, mock↔openai provider로 키 없이 CI/데모 | `LangGraph` `Qdrant` `PostgreSQL` `RRF` `reranker` `Docker` |
| **[ml-experiment-launcher](https://github.com/wahoman/ml-experiment-launcher)** | 데이터셋 빌드 → 학습 → 검증 → 테스트셋 평가를 한 화면으로 묶은 YOLO 실험 런처. 학습은 subprocess로 격리(UI가 죽어도 학습 유지), MLflow로 실험 기록·비교·재현 | `Gradio` `subprocess` `MLflow` `Ultralytics` |

<br>

## 🛠 Tech Stack

**CV / ML** &nbsp;—&nbsp; Python · PyTorch · YOLO11 · DINOv2 · OpenCV · CuPy · UMAP · HDBSCAN

**LLM / RAG** &nbsp;—&nbsp; LangGraph · Qdrant · 임베딩 · hybrid 검색(RRF) · reranker

**Backend / MLOps** &nbsp;—&nbsp; FastAPI · PostgreSQL · Docker · GitHub Actions · MLflow · Gradio · PyQt

<br>

## 💡 일하는 방식

- **막히면 데이터부터 의심합니다.** 모델이 객체를 놓칠 때 아키텍처를 키우는 대신 라벨을 들여다봤고, 임베딩 클러스터링(DINOv2+HDBSCAN)과 자체 검수 도구로 라벨을 정제해 모델 변경 없이 성능을 올렸습니다.
- **반복은 시스템으로 바꿉니다.** 매 실험 몇 시간씩 걸리던 수동 작업을 통합 런처와 MLflow로 묶어 클릭 한 번으로 줄였습니다.
- **숫자는 정직하게 다룹니다.** 검색 품질은 hit@k로 직접 측정하고, 데이터셋이 작아 생기는 한계는 한계라고 말합니다.

<br>

## 📫 Contact

**hgy8401@naver.com**
