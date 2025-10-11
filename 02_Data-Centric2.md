## 🧩 핵심 정리

| 구분 | Model-Centric | Data-Centric |
|------|----------------|--------------|
| 초점 | 모델 구조 개선 | 데이터 품질 개선 |
| 목적 | 새로운 알고리즘 개발 | 깨끗하고 일관된 데이터 확보 |
| 개선 방법 | 코드/모델 수정 | 데이터 증강, 필터링, 라벨 품질 향상 |
| 주체 | 연구자 중심 | 데이터 엔지니어, 큐레이터 중심 |
| 환경 | 학계 중심 | 산업 현장 중심 |

---

## 1️⃣ Data-Centric이란?

### 🔄 AI 서비스의 MLOps 개발 사이클
AI 프로젝트는 일반적으로 다음 순서로 진행된다:  
**프로젝트 정의 → 데이터 준비 → 모델 학습 및 디버깅 → 배포 및 유지보수**

이 흐름을 **MLOps (Machine Learning Operations)** 라 부르며,  
최근에는 대규모 언어모델(LLM) 시대를 맞아 **LLMOps**로 확장되고 있다.

#### ⚙️ MLOps
- NVIDIA, Google 등의 기업에서 제시한 AI 개발 프레임워크  
- 목표: **지속적 통합(Continuous Integration)** 과 **자동화된 학습 파이프라인** 구축  
- 모델의 성능 개선보다는 **데이터 품질 관리 및 운영 자동화**가 중심

#### ⚙️ LLMOps
- 초거대 언어모델(LLM)의 **데이터 구조를 효율적으로 관리**하고  
  다양한 고객의 요구에 맞게 **튜닝 및 최적화된 인프라 환경**을 제공하는 운영 체계  
- 즉, **데이터 중심의 대규모 모델 활용 전략**

---

## 2️⃣ Data-Centric AI in Real-World (In the Wild)

### 🌀 Data-Flywheel
AI 서비스가 데이터를 생성하고, 그 데이터를 다시 개선된 서비스에 활용하는 **순환 구조**를 의미한다.

1. 고객의 사용 데이터를 수집  
2. 이를 학습 데이터로 가공  
3. 모델을 개선하여 다시 서비스에 반영  
4. 다시 새로운 데이터를 축적  

이 순환 고리를 강화할수록 서비스 품질이 점점 향상된다.  
➡️ 대표 사례: [Upstage AI](https://www.upstage.ai/)의 “AI Pack”

---

### ⚙️ DMOps (Data Management Operations)
“좋은 데이터를 만들기 위한 체계적인 운영 구조”  
데이터 중심 AI의 핵심은 **데이터 파이프라인의 자동화와 품질 제어**에 있다.

#### 💼 주요 직무 단계
1. **Schema Design** – 데이터 구조 및 스키마 정의  
2. **Collection** – 원천 데이터 수집  
3. **Annotation** – 데이터 라벨링 및 품질 검증  
4. **Evaluation** – 데이터 평가 및 품질 측정  
5. **Versioning** – 데이터 버전 관리

#### 🧰 Data Labeling Tool
- 데이터 작업을 위한 협업 도구 및 시각화 환경 구축
- 라벨링 툴 품질이 데이터 품질을 결정짓는 핵심 요인

---

### 💬 Real-World 사례

#### 🧩 ChatGPT
- GPT-3 성능 향상은 새로운 모델이 아닌 **데이터 품질 개선**으로부터 시작됨.  
- OpenAI는 사람의 피드백을 이용해 “좋은 응답 vs 나쁜 응답”을 학습시켜  
  **데이터 가중치(weighting)** 를 조정하는 방식으로 ChatGPT를 발전시킴.

#### 🚗 Tesla
- 모델의 예측 결과를 다시 데이터셋 개선에 활용하는 **Data Engine 구조**를 적용.  
- 실제 운전 중 발생한 예외 데이터를 수집 → 데이터셋 업데이트 → 재학습 반복.

---

### 👥 실제 데이터 팀의 역할 구조

#### 1️⃣ 데이터팀
- 서비스 기획자와 함께 **필요 데이터의 종류, 수량, 품질 기준** 논의  
- 외주 크라우드소싱 기반으로 라벨링 진행  
- 작업 가이드, 단가, 품질 검증, Q&A 대응 등을 담당  
- 완성된 데이터는 모델 개발팀에 전달

#### 2️⃣ 모델팀
- **Data Curator**, **IDE Developer**, **Model Researcher** 등으로 구성  
- 데이터를 활용해 모델 구조 설계 및 학습 수행

#### 3️⃣ 서빙팀
- **Model Engineer**, **App Developer**, **Backend Engineer** 등이 참여  
- 실시간 추론 및 배포 시스템 관리

➡️ 이 세 팀이 하나의 **“One Team”**으로 유기적으로 협력해야 Data-Centric AI가 완성된다.

---

## 3️⃣ Data-Centric AI in Academia (학계 관점)

### 🎓 연구가 어려운 이유

1. **좋은 데이터를 수집하기 어렵다.**  
   - 데이터는 여전히 “미지의 영역”이며, 확보 비용이 크다.

2. **라벨링의 기준이 불명확하다.**  
   - 같은 이미지라도 사람마다 라벨링 기준이 달라질 수 있다.  
   - ➡️ 해결책: **라벨링 가이드라인 표준화 및 일관성 확보**

3. **데이터의 질(Quality)이 양보다 중요하다.**  
   - `Small Data / Clean Labels`가 `Big Data / Noisy Labels`보다 더 나은 성능을 낼 수 있다.

4. **데이터 불균형(Data Imbalance)**  
   - 소수 클래스(rare cases)도 균형 있게 포함되어야 한다.

5. **학계는 고정된 테스트셋 내에서만 경쟁한다.**  
   - 반면, 실제 산업(In the Wild)은 서비스 요구사항에 따라 유연한 데이터셋을 설계해야 한다.

---

## 4️⃣ Academia ↔ Industry 간극을 줄이기 위한 시도

### 🧠 DataPerf
> *“Benchmarks for Data-Centric AI Development” (Mark et al., 2022)*

#### 🎯 목표
- ML 파이프라인의 **데이터 중심 단계**를 벤치마크화  
- 데이터셋의 **유지·관리·평가**를 쉽게 반복할 수 있는 구조 설계  
- 모델을 고정하고, 데이터만 개선해 성능 향상을 검증하는 새로운 벤치마크 제시

#### 📊 주요 벤치마크 유형
| 유형 | 설명 | 평가 지표 |
|------|------|-----------|
| **Training Set Creation** | 학습 데이터를 새로 구성 | 새로운 데이터로 학습한 모델의 정확도 |
| **Test Set Creation** | 새로운 테스트 데이터 추가 | 잘못된 라벨 수정 전후 정확도 |
| **Selection Algorithm** | 데이터 서브셋 선택 | 서브셋으로 학습한 모델 성능 |
| **Debugging Algorithm** | 잘못된 라벨 탐지 및 수정 | 수정 후 모델 정확도 개선 |
| **Slicing Algorithm** | 의미 기반 데이터 분할 | 그룹화된 데이터 정확도 |
| **Valuation Algorithm** | 데이터셋 기여도 추정 | 예측 정확도 개선률 |

---

## 5️⃣ Data-Centric AI 연구 및 커뮤니티

### 🌍 주요 리소스
- [NeurIPS Data-Centric AI Workshop](https://www.datacentricai.org/neurips21/)
- [DataPerf Official Website](https://www.datacentricai.org/)
- **논문:** *DataPerf: Benchmarks for Data-Centric AI Development (Mark et al., 2022)*  
- **강의:** *DMOps: Data Management Operation and Recipes (Choi & Park, 2023)*  
- **대회:** [MachineHack Data-Centric AI Competition](https://machinehack.com/tournaments/data_centric_ai_competition_2023)

---


## 📘 참고 및 출처

- NAVER Connect Foundation, *Data-Centric NLP Lecture Series*  
- Andrew Ng, *Campaign for Data-Centric AI (2021)*  
- Choi & Park, *DMOps: Data Management Operations and Recipes (2023)*  
- Mark et al., *DataPerf: Benchmarks for Data-Centric AI Development (2022)*  
- [Upstage AI Blog](https://www.upstage.ai/blog/business/data-centric-ai-modeling)  
- [NeurIPS Data-Centric AI Workshop](https://www.datacentricai.org/neurips21/)  

---