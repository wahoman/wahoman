# 여형구 · AI / ML Engineer

Computer Vision을 코어로 — 데이터 파이프라인, 모델 학습, 서비스 백엔드까지
**필요한 시스템을 0부터 설계하고 구축합니다.**

X-ray 보안검색 도메인의 스타트업에서 유일한 AI 개발자로 일하며,
모델보다 데이터를 먼저 보고, 반복되는 일은 도구로 바꾸는 방식으로 문제를 풀어왔습니다.

`Data-Centric CV` · `MLOps` · `LLM / RAG / Agent`

<br>

## Featured Projects

### [xray-agent-platform](https://github.com/wahoman/xray-agent-platform)

문서 질의응답(RAG)과 X-ray 이미지 탐지를 **하나의 Agent가 상황에 맞게 골라 쓰는** FastAPI 백엔드

- **LangGraph StateGraph** 라우팅 — `route → rag / chat / vision → generate`, LLM 실패 시 폴백
- **2-Stage 검색** — 벡터(Qdrant) + 키워드(PostgreSQL full-text)를 RRF로 융합 후 LLM reranker로 재정렬
- **검증 가능한 품질** — hit@k 평가 하니스 · pytest + GitHub Actions CI · mock↔openai provider로 API 키 없이 데모
- Docker Compose 전체 스택 · 헬스체크 · request-id 로깅

### [ml-experiment-launcher](https://github.com/wahoman/ml-experiment-launcher)

데이터셋 빌드 → 학습 → 검증 → 평가를 한 화면으로 묶은 **YOLO 통합 실험 런처**

- **subprocess 학습 격리** — UI가 죽어도 학습은 계속, SIGTERM 안전 중단
- **symlink 가상 데이터셋** — 실험마다 데이터 복제 없이 구성
- **MLflow 실험 추적** — params·metrics 자동 기록, 도입 이전 실험까지 소급 등록(backfill)하는 스크립트 포함

<br>

## Highlights

| | |
|---|---|
| **라벨 정제로 성능 개선** | 임베딩 클러스터링(DINOv2 · UMAP · HDBSCAN)과 자체 검수 도구로 50만 장 라벨 정제 → 모델 변경 없이 **mAP 0.50 → 0.86** |
| **위기 대응** | 라벨링 외주 결렬 시 few-shot 오토라벨링 파이프라인으로 **10만 장 / 3주** 처리 |
| **물리 기반 합성** | Beer-Lambert 곱셈 합성 + CuPy(GPU) 가속 — 겹친 물체의 투과까지 정합한 X-ray 합성으로 클래스 불균형 완화 |
| **실험 자동화** | 매 실험 수 시간 걸리던 수동 작업 → 통합 런처 + MLflow로 **클릭 한 번** |

<br>

## Tech Stack

**CV / ML**

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=for-the-badge&logo=opencv&logoColor=white)
![YOLO11](https://img.shields.io/badge/YOLO11-111F68?style=for-the-badge)
![DINOv2](https://img.shields.io/badge/DINOv2-4B32C3?style=for-the-badge)
![CuPy](https://img.shields.io/badge/CuPy-76B900?style=for-the-badge)
![UMAP](https://img.shields.io/badge/UMAP-5A6B8C?style=for-the-badge)
![HDBSCAN](https://img.shields.io/badge/HDBSCAN-5A6B8C?style=for-the-badge)

**LLM / RAG**

![LangGraph](https://img.shields.io/badge/LangGraph-1C3C3C?style=for-the-badge&logo=langgraph&logoColor=white)
![Qdrant](https://img.shields.io/badge/Qdrant-DC244C?style=for-the-badge)
![RAG](https://img.shields.io/badge/RAG%20%C2%B7%20Hybrid%20Search-2563EB?style=for-the-badge)

**Backend / MLOps**

![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white)
![MLflow](https://img.shields.io/badge/MLflow-0194E2?style=for-the-badge&logo=mlflow&logoColor=white)
![Gradio](https://img.shields.io/badge/Gradio-F97316?style=for-the-badge)
![PyQt](https://img.shields.io/badge/PyQt-41CD52?style=for-the-badge&logo=qt&logoColor=white)

<br>

## Contact

**hgy8401@naver.com**
