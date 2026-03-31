# clarify 설계 근거 (Design Rationale)

## 목적

기존 3개 스킬(think-clear, product-think, spec-clear)을 학술 근거 기반으로 통합·개선한 단일 스킬.

**핵심 문제:** 모호한 상태의 사용자가 AI의 도움을 받아 (1) 명료화하고 (2) 검증하고 (3) 실행 가능한 스펙으로 만드는 과정이 끊김 없이 이어져야 한다.

---

## 학술 근거 매핑 (8개 도메인)

### 1. FBI 행동변화 계단 모델 (BCSM)

**원전:** FBI Crisis Negotiation Unit, 1990년대 개발
**핵심:** Active Listening → Empathy → Rapport → Influence → Behavioral Change (순서 필수)

**적용:**
- Phase 0의 반영(mirror) 필수화: 기존 스킬은 바로 분석/선택지로 진입했으나, BCSM에 따르면 라포 없이는 영향(전제도전 등)이 작동하지 않음
- 전제도전을 반영 2회 + 요약 1회 후로 배치: 기존 product-think는 Q3에서 바로 전제도전했으나, 이는 BCSM 순서를 위반

**근거:** "ALS(Active Listening Skills) allowed negotiators to better understand the emotion driving dangerous behavior" — FBI LEA, 2024

**v2 추가 — Chris Voss 전술적 공감:**
- 잠정적 프레이밍("~인 것 같네요") 사용 시 편도체 활성이 감소하고 이성적 처리가 활성화됨 (신경과학 근거)
- 단정적 진술("당신은 ~입니다") 대비 저항이 현저히 줄어듦
- Phase 0 반영에 잠정적 프레이밍을 필수 형식으로 추가

### 2. 동기면담 (MI) — Miller & Rollnick

**원전:** Miller & Rollnick, Motivational Interviewing, 3rd ed. (2012)
**핵심:** OARS (Open questions, Affirmations, Reflections, Summaries) + 교정반사(Righting Reflex) 억제

**적용:**
- 교정반사 억제: AI의 가장 큰 위험은 사용자가 모호할 때 바로 구조/해결책을 제시하는 것. MI에서 이를 "righting reflex"라 부르며, 역효과를 낳음
- **v2 추가 — 정량적 근거:** MI 메타분석에서 치료자의 MI 일치 행동과 내담자 변화 대화 간 상관 r=.55 (p<.001) (PMC5958907). 200+ RCT에서 MI 효과 입증, 75% 연구에서 임상적 유의미 효과 (Rubak & Sandbaek, 2005)
- 반영(Reflection)을 명시적 기법으로: 기존 스킬에는 "사용자 말 반영" 규칙이 없었음
- "안 하기"의 정당화: MI는 "변화하지 않을 권리"를 존중. clarify에서 "안 하기도 좋은 결정"으로 명시

### 3. PEACE 면담 모델 (UK Police)

**원전:** UK Home Office + 심리학자 협업, 1992년 도입
**핵심:** Planning → Engage → Account/Clarify → Closure → Evaluate. 모래시계 질문법 (열린→닫힌→열린)

**적용:**
- 모래시계 질문법 도입: 기존 3개 스킬 모두 "선택지 우선"으로 닫힌 질문에 편향. PEACE에 따르면 초반 열린 질문이 더 풍부한 정보를 추출함
- Phase 1 첫 턴: 선택지 없는 열린 질문 → 이후 선택지로 수렴 → 마무리에 다시 열린 질문

**근거:** "PEACE uses an 'hourglass' style of questioning. First open questions, then targeted, then open again, to increase reliability and accuracy." — UK Police Training

### 4. 자연주의 의사결정 (NDM) — Gary Klein

**원전:** Klein, Sources of Power (1999). RPD 모델 + Data/Frame Theory (Klein, Moon, Hoffman, 2006, IEEE Intelligent Systems).
**핵심:** 전문가는 패턴매칭 + 멘탈 시뮬레이션으로 모호함 해소. 최적화보다 만족화(satisficing).

**적용:**
- 멘탈 시뮬레이션 질문: "이 접근법을 채택했을 때 3개월 후를 그려보세요" — 사용자에게 story building을 유도
- 만족화 원칙: 6/10이면 충분. 기존 spec-clear에 있던 원칙을 NDM으로 학술적 정당화
- "안 하기"도 전문가적 판단: Klein의 연구에서 전문가는 "하지 않는 선택"을 적극적으로 함
- **v2 추가 — 패턴 프로브 (Data/Frame Theory):** "이 상황이 뭘 떠올리게 하나요?" → 사용자의 암묵적 프레임(mental model)을 명시화 → "그때와 지금의 차이점은?" → 프레임 스트레스 테스트. Klein의 Sensemaking 연구: 모호함은 데이터와 프레임의 불일치에서 발생하며, 전문가는 Reframing(프레임 교체)으로 해소한다.

**근거:**
- "RPD focuses on satisficing" — Klein (1993)
- 소방관 연구: 134개 의사결정 중 117개(87%)에서 옵션 비교 대신 RPD 사용 — Klein, Calderwood, Clinton-Cirocco (1986-1989)
- "Experts and novices use the same reasoning processes, but experts have a richer repertoire of frames" — Klein (2006)

### 5. 인지면담 (CI) — Fisher & Geiselman

**원전:** Fisher & Geiselman (1992). Enhanced Cognitive Interview.
**핵심:** 맥락 복원(Mental Reinstatement) + 시점 전환 + 자유 회상

**적용:**
- 시점 전환 질문: "해결된 내일 아침을 상상해보세요" — think-clear에 이미 존재, clarify에 계승
- 과거 맥락 복원 추가: "이 문제가 처음 생겼을 때를 떠올려보세요" — 반복 문제에 효과적
- 자유 회상 원칙: Phase 1 첫 턴의 열린 질문이 이에 해당

### 6. ACTA (Applied Cognitive Task Analysis) — Militello & Hutton

**원전:** Militello & Hutton (1998). Ergonomics, 41(11).
**핵심:** Task Diagram → Knowledge Audit → Simulation Interview. 암묵지를 구조적으로 추출.

**적용:**
- **v2 추가 — Task Diagram을 Phase 1에 도입:** "이걸 3-5개 조각으로 나눠보면?" → "가장 판단이 어려운 부분은?" 이 2단계 질문으로 모호함이 사는 위치를 빠르게 특정. ACTA의 핵심 통찰: "전문가에게 '어떻게 하세요?'라고 물으면 피상적 답이 나온다. 3-6개로 분해시켜야 암묵지가 드러난다."
- Knowledge Audit 프로브: "이 영역에서 경험 많은 사람만 아는 것이 있다면?" — Phase 2에 적용
- 암묵지 프로브: "초보자가 이 상황에서 가장 놓치기 쉬운 것은?" — Phase 2의 개선 의지(Route D)에 적용

**근거:** "ACTA is intended to assist in identification of key cognitive elements required to perform a task proficiently." 대학원생에게 방법을 가르친 후 소방지휘관과 해군 전자전 전문가를 인터뷰시킨 결과, 전문가 전용 교육 자료 개발에 성공 — Militello & Hutton (1998)

### 7. 심리언어학 — 질문 프레이밍

**원전:** Kahneman System 1/2, Connor Desai & Reimers (2019), PEACE 질문 연구
**핵심:** 닫힌 질문 = 낮은 인지부하 but 편향 가능, 열린 질문 = 높은 인지부하 but 풍부한 정보

**적용:**
- 적응적 질문 유형: 모호도에 따라 열린/닫힌 전환
  - 모호도 8+: 열린 (탐색 필요)
  - 모호도 4-7: 선택지 (수렴 필요)
  - 모호도 1-3: 확인 (검증만)

### 8. 전문성 연구 — Ericsson

**원전:** Ericsson, Krampe & Tesch-Romer (1993). Psychological Review.
**핵심:** 전문가-초보 차이의 핵심은 메타인지 — "자기가 뭘 모르는지 아는 능력"

**적용:**
- 메타인지 체크포인트: Phase 전환 시 "명확도 몇 점?" 자기 평가
- 불확실성 영역 자각: "지금 가장 불확실한 부분이 어디라고 느끼세요?"

---

## 유사 스킬 대비 차별점

| 스킬 | 핵심 메커니즘 | clarify 차별점 |
|------|-------------|---------------|
| ouroboros | 모호성 ≤ 0.2 정량 게이트 | 4영역 대시보드 + 적응적 질문 유형 |
| Clear Thought Patterns | 16개 인지 도구 통합 | PM 맞춤 + 듀얼 문서 출력 + 파일 영속 |
| GStack office-hours | 6가지 강제 질문 + 전제도전 | 학술 근거 기반 질문 순서 + 라포 우선 |
| Brainstorm (MadAppGang) | 멀티모델 합의 점수 | 단일 모델에서 대화 품질로 승부 |
| Socratic Thinking MCP | 58개 방법론 라이브러리 | 자동 라우팅 + 최소 인지부하 |

---

## 기존 3개 스킬 → clarify 매핑

| 기존 | clarify Phase | 개선 사항 |
|------|-------------|----------|
| think-clear | Phase 0 + 1 | 잠정적 프레이밍 반영 추가 (Voss), 열린질문 시작, ACTA 분해 요청, Known/Unknown 맵 |
| product-think | Phase 2 | 라포 후 전제도전 (BCSM 순서), 패턴 프로브 (Klein Data/Frame), 암묵지 프로브 (ACTA), 멘탈 시뮬레이션 (RPD 87%) |
| spec-clear | Phase 3 | 적응적 질문 유형 (심리언어학), 자동 Phase 전환 |
| (없었음) | Phase 0 LISTEN | 신규 — FBI BCSM + Voss 전술적 공감 기반 |
| (없었음) | ACTA 분해 | 신규 — Phase 1에서 3-5개 조각 분해 후 모호함 위치 특정 |
| (없었음) | 패턴 프로브 | 신규 — Phase 2에서 암묵적 프레임 명시화 + 스트레스 테스트 |
| (없었음) | 파일 영속 | 신규 — ~/.clarify/latest.md |
| (없었음) | 메타인지 체크 | 신규 — Ericsson 전문성 연구 기반 |

---

## 참고 문헌

- Klein, G. (1999). *Sources of Power: How People Make Decisions*. MIT Press.
- Miller, W.R. & Rollnick, S. (2012). *Motivational Interviewing*, 3rd ed. Guilford Press.
- Fisher, R.P. & Geiselman, R.E. (1992). *Memory-Enhancing Techniques for Investigative Interviewing*. Charles C Thomas.
- Militello, L.G. & Hutton, R.J.B. (1998). Applied Cognitive Task Analysis. *Ergonomics*, 41(11), 1618-1641.
- Ericsson, K.A., Krampe, R.T. & Tesch-Romer, C. (1993). The Role of Deliberate Practice. *Psychological Review*, 100(3), 363-406.
- FBI Crisis Negotiation Unit. Behavioral Change Stairway Model. *FBI Law Enforcement Bulletin*, 2024.
- PEACE Interview Model. UK Home Office, 1992.
- Kahneman, D. (2011). *Thinking, Fast and Slow*. Farrar, Straus and Giroux.
