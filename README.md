<div align="center">

# 여형구 · AI / ML Engineer

**AI Engineer · Computer Vision · MLOps · LLM / RAG · VLM**

*모델보다 데이터를 먼저 보고, 반복되는 일은 도구로 바꿉니다.*

![Data-Centric CV](https://img.shields.io/badge/Data--Centric%20CV-059669?style=flat-square&logoColor=white)
![MLOps](https://img.shields.io/badge/MLOps-7C3AED?style=flat-square&logoColor=white)
![LLM · RAG · Agent](https://img.shields.io/badge/LLM%20%C2%B7%20RAG%20%C2%B7%20Agent-2563EB?style=flat-square&logoColor=white)

</div>

<br>

## 👋 소개

스타트업에서 2년 3개월간, 항공 수하물 X-ray 보안검색 도메인에서 데이터 파이프라인부터 모델 학습, LLM 서비스까지 AI 개발의 전 과정을 직접 맡아왔습니다. 모델 성능이 막히면 원인을 데이터에서 찾아 오토라벨링·검수·클러스터링 도구를 직접 만들어 라벨을 정제했고, 반복되는 작업은 AI 코딩 도구를 활용해 빠르게 자동화했습니다. 이렇게 만든 모델은 **실제 장비에 탑재되어 현장에서 운용 중**입니다.

Computer Vision을 코어로 LLM·RAG·Agent와 백엔드·MLOps까지 폭넓게 다루며, 모델 개발에 그치지 않고 테스트·CI·평가·로깅 등 **운영을 전제로** 시스템을 0부터 직접 설계·구축하는 데 강점이 있습니다.

<br>

## 📌 Featured Projects

### [xray-agent-platform](https://github.com/wahoman/xray-agent-platform)

RAG 문서 질의응답 + X-ray 이미지 판독을 **하나의 Agent가 상황에 맞게 골라 쓰는** FastAPI 백엔드

- **LangGraph 라우팅** — `route → rag / chat / vision → generate` + LLM 실패 시 폴백
- **멀티모달 VLM** — vision 경로에서 **VLM(gpt-4o)로 이미지를 직접 판독** (탐지 텍스트만 넘기지 않음)
- **2-Stage 검색** — Qdrant 벡터 + PostgreSQL 키워드를 **RRF 융합** 후 LLM reranker로 재정렬
- 장비 매뉴얼 기반 **hit@k 평가셋 50케이스** · async · 에러 표준화(request-id) · pytest · CI · Docker Compose
- **Kubernetes(Helm) 배포** — Compose 스택을 Helm 차트로 전환 · initContainer 기동 순서 · 헬스체크 기반 자가복구 (minikube 검증)

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

### [Lora — X-ray 위협물 이미지 생성](https://github.com/wahoman/Lora)

부족한 X-ray 위협물 클래스 데이터를 **Stable Diffusion LoRA 파인튜닝**으로 생성해 보강

- **SD 1.5 + LoRA (kohya_ss)** — 소량 데이터로 직접 파인튜닝해 X-ray 가위 이미지 생성
- **데이터 중심 실험** — 30장 vs 150장 학습 비교로 데이터 양이 생성 품질에 미치는 영향 검증
- 물리 기반 합성(TIP)과 함께, 데이터 부족을 **생성 모델로도 보강**

### [My_Travel](https://github.com/wahoman/My_Travel) · [Live ↗](https://my-travel-tau-five.vercel.app)

SVG 지도에서 고르면 읍/면/동까지 뽑아주는 **여행지 랜덤 룰렛** (배포·운영 중)

- 프론트(React)·백엔드·배포까지 혼자 **end-to-end**로 구현 · 콜드스타트 이슈에 정적 + Vercel 전환
- 전국 **247개 시/군/구 → 읍/면/동** 데이터 직접 구축 · OpenAI 코스 생성 · 카카오맵·카카오톡 공유 · SEO

<br>

## ⚡ Highlights

- **라벨 정제로 성능 개선** — 임베딩 클러스터링 + 자체 검수 도구로 50만 장 라벨 정제, 모델 변경 없이 **mAP 0.50 → 0.86**
- **비용 절감** — few-shot 오토라벨링으로 10만 장을 직접 처리, **외주 환산 약 3,000만 원 절감**
- **GPU 가속** — TIP 합성 100만 장 컬러매핑을 NumPy → CuPy(GPU)+병렬로 **약 2주 → 반나절**
- **실험 자동화** — 매 실험 수 시간의 수동 작업 → 통합 런처 + MLflow로 **클릭 한 번**
- **데이터 운영** — 100GB 학습 데이터를 버전별 SQLite DB로 **1GB 이하 보관**, 반복 업무를 **40여 개 도구**로 자동화
- **생성 데이터 증강** — 부족한 위협물 클래스를 **Stable Diffusion LoRA 파인튜닝**으로 생성해 보강 (물리 합성 + 생성 모델 이중 접근)

<br>

## 🛠 Tech Stack

- **CV / ML** — `Python` `PyTorch` `YOLO11 / seg` `DINOv2` `UMAP` `HDBSCAN` `OpenCV` `CuPy(CUDA)` `NumPy` `Pandas` `Stable Diffusion` `LoRA(kohya_ss)` `imgaug`
- **LLM / Agent** — `LangGraph` `VLM(gpt-4o)` `Qdrant` `RRF Hybrid` `LLM Reranker` `OpenAI API`
- **Backend / MLOps** — `FastAPI` `PostgreSQL` `SQLite` `Docker(Compose)` `Kubernetes(Helm)` `GitHub Actions CI` `MLflow` `ONNX/TensorRT` `Gradio` `PyQt`
- **Web** — `React` `Vercel` `외부 API 연동(OpenAI·TourAPI·KakaoMap)`
- **AI 코딩 도구** — `Claude` `Cursor` `GPT` `Gemini`
