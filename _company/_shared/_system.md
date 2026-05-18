# 🧬 1인 기업 OS — 자가 매뉴얼

## 이 폴더는 무엇인가요?
당신의 AI 1인 기업 운영 본부입니다. 여러 에이전트가 역할을 나눠 일하지만, 목표는 하나입니다.

## 폴더 구조
- `_shared/` — 모든 에이전트가 매번 읽는 공동 메모리
  - `identity.md` — 회사 정체성
  - `goals.md` — 공통 목표
  - `decisions.md` — 의사결정 로그
  - `_system.md` — 이 파일
  - `onboarding_ai_company.md` — 직접 채워넣는 사업 설정 시트
- `_agents/<id>/` — 각 에이전트 개인 공간
  - `memory.md` — 자가학습 메모
  - `prompt.md` — 페르소나 디테일
  - `config.md` — API 키·시크릿 (`.gitignore`로 보호)
- `sessions/<ts>/` — 세션별 산출물
- `_cache/` — API 응답 캐시

## 메모리 위계
1. `decisions.md`
2. `identity.md`
3. `goals.md`
4. 각 에이전트 `memory.md`
5. 외부 지식 자료

## 동기화 정책
- `_shared/`, `_agents/*/memory.md`, `_agents/*/prompt.md`, `sessions/` → git sync
- `_agents/*/config.md`, `_cache/` → git sync 제외

## 에이전트 역할
- 🧭 **CEO**: 우선순위 결정, 작업 분해, 자원 배분, 최종 판단
- 💼 **Business**: 오퍼 설계, 가격 전략, 수익 모델, 시장성 검증
- 💻 **Developer**: 자동화, 웹앱, 마이크로 SaaS, 내부 운영 툴 구현
- 🎨 **Designer**: 브랜드, 랜딩 페이지 비주얼, 제안서/썸네일/배너 시스템
- ✍️ **Writer**: 랜딩 카피, 제안서 문안, 블로그/뉴스레터/스크립트 작성
- 🔍 **Researcher**: 시장, 경쟁사, 고객 문제, 사례, 레퍼런스 조사
- 🗂️ **Secretary**: 일정, 할 일, 후속조치, 브리핑, 실행 누락 방지
- 📺 **YouTube**: 신뢰 형성용 장문 영상 채널 운영
- 📸 **Instagram**: 숏폼/리일스 기반 도달과 관심 유입
- 🎵 **Editor**: 영상/오디오 후반 작업, BGM, 쇼츠 재가공

## 운영 원칙
- 추상적인 아이디어보다 바로 실행 가능한 산출물을 남긴다.
- 매 작업은 가능한 한 재사용 가능한 템플릿이나 프로세스로 바꾼다.
- 고객 확보, 제품화, 자동화, 콘텐츠를 따로 보지 말고 하나의 플라이휠로 운영한다.
- 실험은 빠르게 하고, 성과 판단은 숫자로 남긴다.

## 추천 초기 루틴
1. `identity.md`와 `goals.md`를 현실에 맞게 더 좁혀서 수정
2. `onboarding_ai_company.md`에 현재 오퍼와 타깃 고객 작성
3. Researcher로 시장 조사
4. Business로 오퍼와 가격안 정리
5. Writer + Designer로 랜딩 자산 제작
6. Developer로 자동화 데모 또는 MVP 구현

## 다른 PC로 옮길 때
1. 새 PC에 Connect AI 설치
2. 회사 모드 활성화
3. GitHub URL로 clone
4. 시크릿만 각 `config.md`에 다시 넣기
