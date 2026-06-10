<div align="center">

# 여형구 · AI / ML Engineer

**모델보다 데이터를 먼저 보고, 반복되는 일은 도구로 바꿉니다.**

X-ray 보안검색 스타트업의 유일한 AI 개발자 —
데이터 파이프라인 · 모델 학습 · 서비스 백엔드까지 필요한 시스템을 0부터 설계하고 구축합니다.

![Data-Centric CV](https://img.shields.io/badge/Data--Centric%20CV-059669?style=flat-square&logoColor=white)
![MLOps](https://img.shields.io/badge/MLOps-7C3AED?style=flat-square&logoColor=white)
![LLM · RAG · Agent](https://img.shields.io/badge/LLM%20%C2%B7%20RAG%20%C2%B7%20Agent-2563EB?style=flat-square&logoColor=white)

</div>

<br>

## 🧭 How I Work

- **데이터를 먼저 봅니다** — 성능이 막히면 모델보다 라벨 품질을 의심합니다. 실제 성과(mAP 0.50 → 0.86)도 데이터에서 나왔습니다.
- **도구를 만듭니다** — 검수 뷰어(PyQt), 실험 런처(Gradio), 클러스터링 패키지까지. 반복 작업은 시스템으로 바꿉니다.
- **빨리 배우고 바로 적용합니다** — CV로 시작해 임베딩 클러스터링, RAG · Agent, LangGraph를 필요해질 때마다 익혀 동작하는 서비스로 만들었습니다.

<br>

## 📌 Featured Projects

<table>
<tr>
<td width="50%" valign="top">

### [xray-agent-platform](https://github.com/wahoman/xray-agent-platform)

RAG 문서 질의응답 + X-ray 이미지 탐지를 **하나의 Agent가 골라 쓰는** FastAPI 백엔드

- **LangGraph** 라우팅 — `route → rag / chat / vision → generate` + 폴백
- **2-Stage 검색** — Qdrant 벡터 + PostgreSQL 키워드 **RRF 융합** → LLM reranker
- 장비 매뉴얼 기반 **hit@k 평가셋 50케이스** · pytest 32 · CI
- 에러 응답 표준화(code · request-id) · Docker Compose 전체 스택

`FastAPI` `LangGraph` `Qdrant` `PostgreSQL` `Docker`

</td>
<td width="50%" valign="top">

### [ml-experiment-launcher](https://github.com/wahoman/ml-experiment-launcher)

데이터셋 빌드 → 학습 → 검증 → 평가를 한 화면으로 묶은 **YOLO 통합 실험 런처**

- **subprocess 학습 격리** — UI가 죽어도 학습은 계속, SIGTERM 안전 중단
- **symlink 가상 데이터셋** — 실험마다 데이터 복제 없이 구성
- **MLflow 추적** — params·metrics 자동 기록 + 과거 실험 소급 등록(backfill)
- 탭별 모듈 구조 · **pytest 136** · CI

`Gradio` `Ultralytics` `MLflow` `subprocess`

</td>
</tr>
<tr>
<td width="50%" valign="top">

### [object-cluster-refine](https://github.com/wahoman/object-cluster-refine)

YOLO 라벨 정제를 위한 **비지도 pseudo-class 발견** 파이프라인

- **DINOv2(768D) + X-ray 색(75D) + 크기** 특징 융합 → UMAP → HDBSCAN
- 다중 회전 임베딩 · 2단 크기 필터 · hardlink 데이터셋 출력
- 실무에서 mAP 0.50 → 0.86을 만든 기법을 **범용 패키지로 공개**
- lazy import 설계 — torch 없이도 CLI·테스트 동작 · **pytest 75**

`DINOv2` `UMAP` `HDBSCAN` `OpenCV`

</td>
<td width="50%" valign="top">

### [My_Travel](https://github.com/wahoman/My_Travel) · [Live ↗](https://my-travel-tau-five.vercel.app)

SVG 지도에서 고르면 읍/면/동까지 뽑아주는 **여행지 랜덤 룰렛** (운영 중)

- React + FastAPI(Render)로 시작 → 콜드스타트 문제에 **백엔드 제거, 정적 + Vercel 전환**
- 전국 **247개 시/군/구 → 읍/면/동** 데이터 직접 구축 (100% 커버)
- 카카오맵 장소검색 · 카카오톡 공유(deep-link) · SEO

`React` `Kakao Maps` `Vercel`

</td>
</tr>
</table>

<br>

## ⚡ Highlights

| | |
|---|---|
| **라벨 정제로 성능 개선** | 임베딩 클러스터링 + 자체 검수 도구로 50만 장 라벨 정제 → 모델 변경 없이 **mAP 0.50 → 0.86** |
| **위기 대응** | 라벨링 외주 결렬 시 few-shot 오토라벨링 파이프라인으로 **10만 장 / 3주** 처리 |
| **물리 기반 합성** | Beer-Lambert 곱셈 합성 + CuPy(GPU) — 겹친 물체의 투과까지 정합한 X-ray 합성으로 클