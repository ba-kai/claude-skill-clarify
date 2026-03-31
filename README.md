# claude-skill-clarify

모호한 생각을 실행 가능한 스펙으로 바꿔주는 Claude Code 스킬입니다.

FBI 행동변화 계단 모델(BCSM), 동기부여 면담(MI), 자연주의적 의사결정(NDM), 인지면담, PEACE 모델 등 근거 기반 질문 기법을 통합했습니다.

## 작동 방식

4단계 적응형 질문 프로토콜:

| Phase | 이름 | 목적 |
|-------|------|------|
| 0 | LISTEN | 반영 + 감정 라벨링, 상태 감지 |
| 1 | EXPLORE | 모호한 생각에서 방향 찾기 |
| 2 | CHALLENGE | 아이디어 검증, 더 나은 프레이밍 |
| 3 | SPECIFY | 구현 가능한 스펙 생성 |

## 산출물

- **PM 시나리오**: 사용자 시나리오, 예외 상황, 안 하는 것
- **구현 스펙**: Goal, Acceptance Criteria (WHEN/THEN), Constraints, Open Questions

## 설치

### 방법 1: 파일 복사 (가장 간단)

```bash
# 프로젝트별 설치
mkdir -p .claude/commands
curl -o .claude/commands/clarify.md \
  https://raw.githubusercontent.com/ba-kai/claude-skill-clarify/main/.claude/commands/clarify.md
```

```bash
# 글로벌 설치 (모든 프로젝트에서 사용)
mkdir -p ~/.claude/commands
curl -o ~/.claude/commands/clarify.md \
  https://raw.githubusercontent.com/ba-kai/claude-skill-clarify/main/.claude/commands/clarify.md
```

### 방법 2: Git clone

```bash
git clone https://github.com/ba-kai/claude-skill-clarify.git
cp claude-skill-clarify/.claude/commands/clarify.md ~/.claude/commands/
```

## 사용법

Claude Code에서 다음 중 하나로 실행:

```
/clarify
```

또는 자연어 트리거:

- "생각 정리"
- "스펙 만들자"
- "아이디어 검증"
- "뭘 해야 할지"
- "이거 해볼까"
- "기능 정리"
- "명확하게 해줘"

## 5원칙

1. **먼저 듣고, 나중에 물어라** — 반영 없이 질문하지 않는다
2. **질문은 상황에 맞춰** — 모호도에 따라 열린/닫힌 질문 적응
3. **모르는 건 모른다고** — 추측으로 채우지 않는다
4. **시나리오로 생각하라** — "유저가 X하면 Y가 보인다" 형태
5. **충분하면 멈춰라** — 6/10이면 실행한다

## 요구사항

- [Claude Code](https://docs.anthropic.com/en/docs/claude-code) CLI

## 라이선스

MIT
