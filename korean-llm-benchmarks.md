# 한국어 LLM 평가 벤치마크 (Korean LLM Evaluation Benchmarks)

## 📊 종합 평가 벤치마크 (General Evaluation Benchmarks)

### 1. 주요 리더보드 및 종합 벤치마크

#### **Open Ko-LLM Leaderboard & Ko-H5 Benchmark**
- 영어 Open LLM Leaderboard를 미러링하면서 private test set을 포함
- 데이터 유출(data leakage) 문제를 방지한 평가 프레임워크
- 한국 LLM 커뮤니티에 잘 통합된 평가 도구

#### **Open Ko-LLM Leaderboard2**
- 기존 벤치마크를 실제 능력과 더 밀접하게 연관된 과제들로 전면 교체
- 4개의 native Korean 벤치마크 신규 추가
- 한국어 고유 특성을 더 잘 반영하는 개선된 버전

#### **KMMLU (Korean Massive Multitask Language Understanding)**
- **규모**: 35,030개의 전문가급 객관식 문제
- **범위**: 인문학부터 STEM까지 45개 과목
- **특징**: 번역이 아닌 오리지널 한국 시험 문제로 구성
- **변형 버전**:
  - KMMLU-HARD: 더 도전적인 문제들로 구성
  - KMMLU-Redux: 정제되고 압축된 버전
  - KMMLU-Pro: 전문자격증 시험 기반
- **성능**: 최고 공개 모델 50.5%, GPT-4 약 60% (인간 평균 62.6%)

### 2. 문화 및 언어 특화 벤치마크

#### **CLIcK (Cultural and Linguistic Intelligence in Korean)**
- **규모**: 1,995개 샘플 데이터, 11개 카테고리
- **평가 영역**:
  - 한국 문화: 역사, 지리, 법, 정치, 사회, 전통, 경제, 대중문화
  - 한국어: 텍스트, 기능, 문법
- **형식**: 4-5지선다형 객관식

#### **HAE-RAE BENCH**
- **구성**: 4개 도메인의 6개 하위 과제
- **평가 영역**: 어휘, 역사, 일반 지식, 독해 이해력
- **최신 버전**: HAE-RAE BENCH 1.1 (4,900개 인스턴스, 13개 과제)
- **특징**: 한국 문화적 맥락과 지식 recall 능력 평가

#### **KorNAT (Korean National Alignment Test)**
- **구성**:
  - 사회적 가치관: 4,000개 객관식 문제
  - 일반 상식: 6,000개 객관식 문제
- **특징**: 6,174명의 한국인 대규모 설문조사를 통한 ground truth 확보
- **목적**: 한국 사회 가치관 및 상식과의 alignment 평가

#### **KULTURE Bench**
- **구성 데이터셋**:
  - KorID: 한국 관용구 (1,631개 인스턴스)
  - KorPD: 한국 시 이해
  - 한국 문화 뉴스
- **특징**: 한국 문화에 대한 심층적 이해도 평가

---

## 🎯 Domain Specific 벤치마크

### 의료 분야 (Medical Domain)

#### **서울대병원 Medical LLM 벤치마크**
- **학습 데이터**: 3,800만 개의 비식별화된 임상 기록
- **평가 기준**: 한국 의사면허시험
- **성능**: 86.2% 점수 달성 (인간 평균 79.7%)

#### **KorMedMCQA**
- 한국 의료 전문가 자격시험 기반 객관식 문제
- 다양한 의료 분야 포함

### 법률 분야 (Legal Domain)

#### **한국 법률 언어 이해 벤치마크**
- 한국 법률 시스템과 용어에 특화
- 실무 법률 문서 이해 능력 평가

#### **KMMLU-Pro 법률 도메인**
- 변호사 자격증 시험 문제 포함
- 실제 합격 기준 반영

### 교육 분야 (Education Domain)

#### **Korean SAT LLM Leaderboard (대학수학능력시험)**
- **기간**: 2015년 ~ 2024년 수능 문제
- **출처**: 한국교육과정평가원(KICE)
- **평가 영역**:
  - 국어 (언어 이해, 핵심 내용 이해, 논리적 추론, 비판적 사고)
  - 영어
  - 수학
  - 과학 (물리, 화학, 생물, 지구과학)
  - 사회
- **특징**: 매년 수능 당일 업데이트 예정

### 전문자격증 분야 (Professional Licenses)

#### **KMMLU-Pro**
- **규모**: 2,822개 문제
- **기반**: 한국 국가전문자격증(KNPL) 공식 시험
- **특징**:
  - 실제 자격증 합격 기준 반영
  - 매년 최신 시험 문제로 업데이트
  - 100개 자격증을 한국표준산업분류(KSIC)로 분류
- **평가 도메인**: 의료, 법률, 공학, 건축 등

### 수학 분야 (Mathematics Domain)

#### **MATH GPT 벤치마크**
- **개발**: Mathpresso & Upstage 협력
- **모델 규모**: 13억 파라미터
- **성능**: GPT-4 능가 (정확도 0.488 vs 0.425)
- **특징**: 적은 계산 자원으로 높은 성능

---

## 📈 평가 방법론

### 평가 방식
- **3-shot**: 예시 3개 제공 후 평가 (Text-Davinci-003, HyperClova LK-D2)
- **5-shot**: 예시 5개 제공 (KMMLU, KMMLU-HARD)
- **Log-likelihood**: 각 선택지의 확률 계산
- **Direct/Generative**: 직접 생성 방식 평가

### 주요 지표
- 정확도(Accuracy)
- 표준 점수(Standard Score)
- 실제 자격증 합격 여부
- Domain별 세부 성능

---

## 🔧 도구 및 리소스

### 공개 플랫폼
- Hugging Face Hub (대부분의 데이터셋)
- EleutherAI's Language Model Evaluation Harness (KMMLU 통합)
- GitHub 저장소 (각 벤치마크별 코드)

### 접근성
- 대부분 공개 데이터셋으로 제공
- 평가 코드 오픈소스
- Private test set으로 데이터 contamination 방지

---

## 📝 주요 특징 및 의의

1. **한국어 고유성**: 단순 번역이 아닌 한국 원본 콘텐츠 사용
2. **문화적 맥락**: 한국 문화, 역사, 사회적 가치관 반영
3. **실용성**: 실제 자격증, 입시 등 실무 활용 가능성 평가
4. **다양성**: 일반 지식부터 전문 분야까지 광범위한 커버리지
5. **지속적 업데이트**: 매년 최신 문제로 갱신 (일부 벤치마크)

---

## 🔗 참고 링크

- [Open Ko-LLM Leaderboard](https://huggingface.co/spaces/upstage/open-ko-llm-leaderboard)
- [KMMLU Dataset](https://huggingface.co/datasets/HAERAE-HUB/KMMLU)
- [HAE-RAE GitHub](https://github.com/HAE-RAE)
- [Korean SAT Leaderboard](https://github.com/Marker-Inc-Korea/Korean-SAT-LLM-Leaderboard)

---

*최종 업데이트: 2025년 9월*