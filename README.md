<div align="center">

# 여형구 · AI / ML Engineer

**모델보다 데이터를 먼저 보고, 반복되는 일은 도구로 바꿉니다.**

X-ray 보안검색 스타트업에서 AI 개발을 혼자 맡아 —
데이터 파이프라인 · 모델 학습 · LLM 서비스까지 필요한 시스템을 0부터 설계하고 운영합니다.

![Data-Centric CV](https://img.shields.io/badge/Data--Centric%20CV-059669?style=flat-square&logoColor=white)
![MLOps](https://img.shields.io/badge/MLOps-7C3AED?style=flat-square&logoColor=white)
![LLM · RAG · Agent](https://img.shields.io/badge/LLM%20%C2%B7%20RAG%20%C2%B7%20Agent-2563EB?style=flat-square&logoColor=white)

</div>

<br>

## 🧭 How I Work

- **데이터를 먼저 봅니다** — 성능이 막히면 모델보다 라벨 품질을 의심합니다. 실제 성과(mAP 0.50 → 0.86)도 데이터에서 나왔습니다.
- **도구를 만듭니다** — 반복 업무는 Gradio·PyQt로 도구화해 누적 **40여 개**. 검수 뷰어·실험 런처·인덱싱까지 직접 만들어 팀의 시간·비용을 줄였습니다.
- **AI 도구를 손발처럼 씁니다** — Claude·Cursor·GPT 등 AI 코딩 도구로 빠르게 만들되, 만든 코드는 직접 검증·리팩토링·테스트해 운영 품질까지 완성합니다.
- **빨리 배우고 바로 적용합니다** — CV로 시작해 임베딩 클러스터링, RAG·Agent, VLM까지 필요할 때 익혀 동작하는 서비스로 만들었습니다.

<br>

## 📌 Featured Projects

### [xray-agent-platform](https://github.com/wahoman/xray-agent-platform)

RAG 문서 질의응답 + X-ray 이미지 판독을 **하나의 Agent가 상황에 맞게 골라 쓰는** FastAPI 백엔드

- **LangGraph 라우팅** — `route → rag / chat / vision → generate` + LLM 실패 시 폴백
- **멀티모달 VLM** — vision 경로에서 **VLM(gpt-4o)로 이미지를 직접 판독** (탐지 텍스트만 넘기지 않음)
- **2-Stage 검색** — Qdrant 벡터 + PostgreSQL 키워드를 **RRF 융합** 후 LLM reranker로 재정렬
- 장비 매뉴얼 기반 **hit@k 평가셋 50케이스** · async · 에러 표준화(request-id) · pytest · CI · Docker Compose

### [ml-experiment-launcher](https://github.com/wahoman/ml-experiment-launcher)

데이터셋 빌드 → 학습 → 검증 → 평가를 한 화면으로 묶은 **YOLO 통합 실험 런처**

- **subprocess 학습 격리** — UI가 죽어도 학습은 계속, SIGTERM 안전 중단
- **symlink 가상 데이터셋** — 실험마다 데이터 복제 없이 구성
- **MLflow 실험 추적** — params·metrics 자동 기록 + 과거 실험 소급 등록(backfill)
- **ONNX · TorchScript · TensorRT Export** — 장비 탑재 배포 흐름까지 연결 · 탭별 모듈 구조 · CI

### [object-cluster-refine](https://github.com/wahoman/object-cluster-refine)

YOLO 라벨 정제를 위한 **비지도 pseudo-class 발견** 파이프라인

- **DINOv2(768D) + X-ray 색(75D) + 크기** 특징 융합 → UMAP → HDBSCAN
- 실무에서 **mAP 0.50 → 0.86**을 만든 기법을 범용 패키지로 공개
- lazy import 설계 — torch 없이도 CLI·테스트 동작 · pytest · CI

### [Auto-Labeling](https://github.com/wahoman/Auto-Labeling)

X-ray 데이터셋을 혼자 대규모로 구축·정제한 **오토라벨링 · 검수 파이프라인**

- **Few-shot 오토라벨링** — 소량 수동 라벨로 YOLO11-seg 학습 → 그 모델로 대량 오토라벨링 → 검수·재학습 반복
- **PyQt 로컬 검수 뷰어** — 키보드 한 손 조작, 삭제 되돌리기 (웹 업로드 없이 보안·속도 확보)
- 10만 장 규모를 혼자 처리해 **외주 환산 약 3,000만 원 절감** · 클래스 세분화로 성능 개선·오탐 감소

### [My_Travel](https://github.com/wahoman/My_Travel) · [Live ↗](https://my-travel-tau-five.vercel.app)

SVG 지도에서 고르면 읍/면/동까지 뽑아주는 **여행지 랜덤 룰렛** (배포·운영 중)

- 프론트(React)·백엔드·배포까지 혼자 **end-to-end**로 구현 · 콜드스타트 이슈에 정적 + Vercel 전환
- 전국 **247개 시/군/구 → 읍/면/동** 데이터 직접 구축 · OpenAI 코스 생성 · 카카오맵·카카오톡 공유 · SEO

<br>

## ⚡ Highlights

- **라벨 정제로 성능 개선** — 임베딩 클러스터링 + 자체 검수 도구로 50만 장 라벨 정제, 모델 변경 없이 **mAP 0.50 → 0.86**
- **비용 절감** — few-shot 오토라벨링으로 10만 장을 직접 처리, **외주 환산 약 3,000만 원 절감**
- **GPU 가속** — TIP 합성 100만 장 컬러매핑을 NumPy → Cu