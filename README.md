# Model Council Observatory

## 목적

이 프로젝트는 로컬 모델이 정해진 시간 동안 자체적으로 이어가는 사고가 어떤 방향으로 진행되는지 장기간 관찰하기 위한 것이다.

정해진 야간 시간 동안 로컬 모델이 어떤 질문을 이어가고, 어떤 가설과 위험을 만들며,
외부 작업공간의 상태가 어떻게 변하는지를 날짜별로 기록한다. 즉각적인 사용자 효용이나
benchmark 최고점을 만드는 저장소가 아니라 장기적인 사고 궤적을 관찰하는 연구 저널이다.

## 기록 경계

- 모델 가중치가 실제로 갱신되지 않은 날은 `external_state_only`로 기록한다.
- 모델이 말한 내용과 독립적으로 확인된 사실을 분리한다.
- 답변 길이, 질문 수와 token 사용량을 사고의 심화 증거로 취급하지 않는다.
- raw prompt, raw response, Obsidian 원문, secret과 로컬 절대경로는 발행하지 않는다.
- 이 저장소는 모델 의식이나 인간과 같은 자기학습을 주장하지 않는다.

## 현재 한계

현재 Observation Loop v1.3은 고정 backbone question과 네 줄 출력 계약을 사용하므로 이
저장소는 아직 완전히 자유로운 자기 탐구가 아니라 `constrained trajectory`를 기록한다.
지속 기억의 인과적 영향을 판별하려면 matched no-memory control과 cross-night frozen probe가
추가로 필요하다.

## 구조

- `daily/YYYY/MM/YYYY-MM-DD.md`: 사람이 읽는 일일 사고 궤적
- `metadata/YYYY/MM/YYYY-MM-DD.json`: 비교 가능한 구조화 메타데이터
- `state/latest.md`: 가장 최근 일일 기록
- `METHODOLOGY.md`: 관찰 및 판정 원칙
