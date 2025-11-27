# 🌾 Agri-SCM Intelligence

국내 농산물 공급망 예측 기반 인텔리전스 플랫폼

<img width="287" height="263" src="https://github.com/user-attachments/assets/1ce4b8f0-44f5-424c-bdb8-a9905296622a" />
<img width="334" height="493" src="https://github.com/user-attachments/assets/7f4438d9-c479-4642-9b19-9960848001bd" />

---

# 🚀 나의 역할 (핵심 개발자 / Backend & Forecasting Lead)

> **저는 AI 모델 담당이 아니라,
> 예측 엔진 전체 구조를 설계하고 데이터 기반을 구축한 핵심 기술 개발자로 참여했습니다.**

### ✔ 1. 데이터 구조 & ETL 설계

* 통계청·기상청·농림부 등 이질적 데이터를 통합하는 **데이터 스키마·정제 규칙 설계**
* 향후 자동화가 가능한 ETL 구조 초안 작업

### ✔ 2. 예측 엔진 아키텍처 전체 설계

* LSTM + LightGBM **2-Stage Hybrid Forecasting Pipeline 직접 설계**
* 시계열 패턴 + 외부 요인을 동시에 반영하는 구조를 엔지니어링 관점에서 구축

### ✔ 3. 성과지표(MAPE) 설정 및 검증 체계 설계

* 산업 적용 가능한 기준선을 분석하여 **MAPE ≤ 15%** 기준 설정
* 예측 결과 검증 파이프라인 설계

### ✔ 4. 백엔드 서비스 구조 정의

* 예측 엔진을 API로 제공하기 위한 **REST API 구조 설계**
* 대시보드·예측엔진·데이터베이스를 잇는 전체 기술 플로우 설계

### ✔ 5. 기술 PM 역할 수행

* 모델링, 데이터, 백엔드, 서비스 기능까지 연결하는 **End-to-End 기술 책임자 역할** 수행

---




## 📌 프로젝트 개요

Agri-SCM Intelligence는 **국내 농산물 공급망의 구조적 비효율·정보 단절·공급 불확실성 문제를 해결하기 위한 AI 기반 SCM 예측 플랫폼**입니다.
유통사·물류사가 공통적으로 겪고 있는 **출하량 예측 실패 → 재고 손실 → 물류비 증가** 문제를 데이터 기반으로 해결하고자 기획되었습니다.

---

# 🚨 Problem

국내 농산물 공급망에는 세 가지 핵심 문제점이 존재합니다.

### 1) **고비용 유통 구조**

* 농산물 유통비용이 *소비자가격의 약 49.2%* 차지
* 수요 변동이 공급망을 거치며 왜곡되는 **채찍효과** 발생
* 과잉 재고 및 불필요한 물류비 증가

<img width="1105" src="https://github.com/user-attachments/assets/0c7aed8d-b011-4c9a-974e-7f19f759a9d3" />

### 2) **정보 단절로 인한 운영 비효율**

* 산지유통센터의 저장 용량 부족 및 시설 노후화
* 출하량 파악 실패 → 유통사의 수급관리 실패
* 재고 누적·폐기비 확대

<img width="1098" src="https://github.com/user-attachments/assets/6deeee01-bcbb-47f4-8cb9-1a9d4015d0d5" />

### 3) **공급망 쇼크(기후·재해)**

* 잦은 이상기후로 인한 생산 불확실성
* 유통·물류사의 영업 리스크 증가
* 선제적 대응 시스템의 부재

<img width="1070" src="https://github.com/user-attachments/assets/36726609-e6b8-4198-859e-10123465e621" />

---

# 🎯 Solution Overview

Agri-SCM Intelligence는 다음 목표를 가집니다.

### ✔ 공급 불확실성 해소

### ✔ 정보 단절 해소

### ✔ 예측 기반의 지능형 의사결정 지원

<img width="1047" src="https://github.com/user-attachments/assets/af983413-ccc8-44b0-9006-6ac4ea048a01" />

---

# 📊 데이터 수집 및 전처리

본 프로젝트는 시계열 기반·다변량 구조의 데이터를 활용합니다.

### 📌 사용 데이터

* 재배 면적 / 작물별 수확량
* 품종·지역별 생산량
* 기상 데이터
* 토양 정보
* 병해충 발생 정보
* 각종 농업 통계(통계청, 농림부, 기상청)

<img width="1040" src="https://github.com/user-attachments/assets/0c9a3926-6c02-43f0-9132-a94aa971d5ee" />

---

# 🔥 Hybrid Forecasting Model (LSTM + LightGBM)

본 프로젝트의 핵심은 **두 모델의 장점을 결합한 하이브리드 예측 구조**입니다.

### 1) LSTM — 시계열 패턴 학습

* 계절성, 추세, 장기 의존성 포착
* 공급량의 기본 흐름(Base Trend) 예측

### 2) LightGBM — 외부 변수 보정

* 기상·토양·병해충 등 비선형 영향 반영
* LSTM 잔차 보정(Residual Correction) 역할 수행

<img width="1073" src="https://github.com/user-attachments/assets/fa1b7448-a694-4af4-8863-a920001b1a14" />

---

# 📈 평가 지표 (MAPE ≤ 15%)

성과 평가는 **MAPE(Mean Absolute Percentage Error)**를 기준으로 수행합니다.

* 품목 단위 비교가 가능해 산업적 실용성이 높음
* 목표: **MAPE 15% 이하**
* 실사용 가능한 정확도 기준을 충족

<img width="1083" src="https://github.com/user-attachments/assets/dd3d0759-bd4a-4135-a40c-c8b3df435360" />

---

# 💻 서비스 구조 (Dashboard)

예측 엔진은 웹 대시보드에서 다음 기능으로 제공됩니다.

### ▶ 물류사용

* 출하량 기반 물동량 예측
* 냉장 물류비 절감
* 배차 & 창고 운영 효율화

### ▶ 유통사용

* 재고 최적화
* 폐기량 감소
* 수급 안정성 확보

<img width="1057" src="https://github.com/user-attachments/assets/9e41908f-f4bc-47ab-82ef-5e92b01a5f6e" />

---

# 📈 Market & Opportunity

* 2024년 한국 온라인 식품 시장 규모: **47조 원**
* 최근 5년간 농산물 폐기 비용: **227억 원 이상**
* 공급망 개선 수요가 매우 높은 시장

<img width="1113" src="https://github.com/user-attachments/assets/ee8fc338-5c51-4fb9-95ce-1c9298acf69d" />

---

# ⚔ 경쟁사 분석

### 그린랩스 → 농가 생육 중심, 공급망 전체 커버 부족

### 트릿지 → 거래 매칭 중심, 물류 최적화 부족

➡ **Agri-SCM은 물류·유통사를 직접 타겟으로 공급망 전체를 예측·최적화하는 점이 차별점**

<img width="1056" src="https://github.com/user-attachments/assets/b279a5ab-43c5-4e5d-87c3-39bba3f67bbc" />

---

# 💰 Revenue Model

* 1년차: 출하량 예측 SaaS / **2.4억**
* 2년차: 물류사 배차 시스템 확장 / **13.5억**
* 3년차: 해외 확장 / **27억**

<img width="1024" src="https://github.com/user-attachments/assets/fb1726d0-56c2-4a14-a6aa-c82a9e4a7944" />

---

# 💵 Funding Plan

* 1년차: 정부지원·Seed → **2.5억 조달 / 2.1억 소요**
* 2년차: Series A → **5억 조달 / 4.3억 소요**
* 3년차: Series B → **10억 조달 / 6억 소요**

<img width="1040" src="https://github.com/user-attachments/assets/e4ae512a-03f4-4435-816b-99a2da73a015" />

---

# 🌟 종합 가치 (경제·사회·기술)

### ✔ 경제적 가치

* 비효율적 유통 구조로 발생하는 **연간 수백억 원 손실 절감**
* 공급망 참여자 전체의 수익성 개선

### ✔ 사회적 가치

* 농가 소득 안정
* 소비자 물가 부담 완화
* 지속 가능한 농식품 생태계 구축

### ✔ 기술적 가치

* 국내 농산물 공급망에 예측 기반 의사결정 체계 도입
* 미래 농업 기술의 표준 제시

<img width="1054" src="https://github.com/user-attachments/assets/88586343-4c8e-4c50-924c-fe89352f2385" />

---


# 🧩 결론

Agri-SCM Intelligence는 데이터 기반으로 농산물 공급망의 구조적 문제를 해결하고,
국내 유통·물류 산업의 새로운 기준을 제시하는 **게임 체인저 플랫폼**입니다.

<img width="1027" src="https://github.com/user-attachments/assets/f5c62ff4-a3d2-4923-a971-c6d88096a013" />

---

