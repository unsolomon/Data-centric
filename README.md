# 🧱 Data-Centric NLP 전체 요약

> **NAVER Boostcamp AI Tech – Data-Centric NLP 강의 정리**  
> 강의자: 박찬준 (Upstage AI)

---

## 🧩 Recap (요약 개념 정리)

- **AI System = Code + Data (Model / Algorithm)**  
  → 모델링보다 **데이터 품질 향상**에 초점  
- **Data Flywheel & DMOps**:  
  데이터 수집 → 모델 학습 → 서비스 개선 → 데이터 재수집의 순환 구조  
- **학계 vs 산업의 간극**:  
  학계는 제한된 데이터와 평가 중심, 산업은 실제 데이터 품질 개선 중심  

---

## 🪜 강의별 핵심 요약

### 1️⃣ Data-Centric AI란 무엇인가
- 모델보다 데이터 중심의 접근
- AI 성능 향상의 80%는 **데이터 품질 확보**에서 결정됨

### 2️⃣ Data-Centric AI in the Wild
- 실제 산업 적용 사례: Data Flywheel / DMOps
- 좋은 데이터 파이프라인 설계가 핵심

### 3️⃣ Data Management (DMOps)
- 데이터 라벨링, 버전 관리, 평가까지 포함한 **데이터 운영 체계**
- Crowd Sourcing + 자동화 Tool → 효율적 데이터 품질 확보

### 4️⃣ 국내외 NLP 데이터
- 세종계획 → 모두의 말뭉치 → HyperCLOVA까지 발전
- Multilingual, Low-resource 언어 확장 트렌드

### 5️⃣ 특이한 NLP Task
- Hate Speech, Fake News, Dialogue 등 **실세계 중심 NLP**
- 한국어 특화 데이터셋과 응용 증가

### 6️⃣ NLP History (Data-Centric 시각)
- 규칙 기반 → 통계 기반 → 딥러닝 → LLM  
- 데이터 품질과 양의 진화  
- Human Feedback 기반 학습의 부상

### 7️⃣ Data-Centric NLP 응용
- 모델 수정 없이 성능 향상  
  → Tokenization, Augmentation, Filtering  
- Inter-Annotator Agreement로 품질 측정  
- Data Lifecycle (Motivation → Maintenance)

### 8️⃣ Recent Work
- ChatGPT 기반 증강(ChatAug), Back-Translation  
- 병렬 데이터 필터링, 합성 데이터  
- IAA 개선 및 주석자 예측 연구  
- Label error, imbalance, privacy 등 Data-centric 과제

### 9️⃣ Future of Data-Centric NLP
- Multi-Modal AI (텍스트+이미지)
- Neuro-Symbolic AI (지식+추론)
- RLHF (Human Feedback)
- GPT-4 & LLM 시대 도래

### 🔟 총정리 및 미래 방향성
- Scaling Law: 모델 크기보다 데이터 구성 중요
- Multilingual / Multimodal / Domain-Specific AI
- Prompt Engineering과 Holistic Evaluation
- 데이터 품질 = AI 경쟁력

---

## 🌍 미래의 Data-Centric AI 방향성 (Recap 요약 추가)

| 키워드 | 설명 |
|--------|------|
| **Scaling Law** | "크게, 더 크게" — 데이터와 모델 균형의 핵심 |
| **Foundation Models** | PaLM, LLaMA, GPT-4 등 범용 모델 |
| **Multimodal AI** | 텍스트+이미지+로봇 센서 통합 (예: PaLM-E, Kosmos-1) |
| **Multilingual AI** | No Language Left Behind (Meta), BLOOM |
| **External Knowledge** | 위키데이터·지식그래프 결합 |
| **Synthetic Data** | 생성형 AI 기반 데이터 확장 |
| **Domain Specialized** | 산업별 특화 LLM (의료, 법률 등) |
| **Prompt Engineering** | Chain-of-Thought, Template, Manager |
| **Data = Prompt = Money** | 데이터 자체가 자산이 되는 시대 |

---

## 🎯 복습 및 프로젝트 가이드

- 각 강의 md 파일별 핵심 요약 연결  
- Readme 내 링크를 통해 학습 흐름 유지  
- 개인 프로젝트 시 `Data-centric improvement` 포인트 참고  
  - Augmentation / Filtering / Annotation 개선 중심  

---

## 📚 Reference
- Naver Connect Foundation (NAVER Boostcamp AI Tech)
- Upstage AI – 박찬준 강의자료
- Bommasani et al., 2023, *On the Opportunities and Risks of Foundation Models*
- Liu et al., 2023, *Pre-train, Prompt, and Predict*
