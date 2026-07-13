# Methodology

## 관찰 단위

각 cycle의 모델 제안, 구조적 검사, workspace 수용 여부, reviewer 개입, 다음 질문을 분리해
기록한다. 동일한 모델의 자기평가는 독립 검증으로 계산하지 않는다.

## 학습이라는 표현

`external_state_only`는 prompt, memory, workspace 또는 harness 상태가 변경됐다는 뜻이다.
모델 가중치 학습은 재현 가능한 training receipt와 checkpoint가 있을 때만 별도로 표시한다.

## 심화 판정

반복이나 장문 생성을 심화로 간주하지 않는다. 장기적으로는 질문 의존 깊이, 모순 수정,
이전 상태의 인과적 기여, memory ablation, transfer probe와 독립 평가를 함께 본다.

현재 v1.3의 고정 backbone과 출력 schema는 질문 공간을 강하게 제한한다. 그러므로 현 단계의
연속성은 자율적 자기 탐구의 증거가 아니며, `constrained trajectory`로만 해석한다.

## 근거 계층

- `SOURCE_CLAIM`: 인용 가능한 외부 연구가 직접 지지하는 제한된 주장이다. 로컬 효과를 뜻하지 않는다.
- `PROJECT_INFERENCE`: source에서 영감을 얻은 프로젝트 설계 판단이며, 로컬 outcome 검증 전에는 사실로 승격하지 않는다.
- `UNVERIFIED_HYPOTHESIS`: frontier에서 검증을 기다리는 가설이다. 모델 출력만으로 evidence가 되지 않는다.
- `LOCAL_EVIDENCE`: matched task outcome, evaluator hash, lineage가 canonical registry에 함께 저장된 로컬 결과다.

모델의 제안과 자기평가는 위 네 계층 중 어느 것에서도 독립 evidence로 단독 집계하지 않는다.

## 발행 정책

발행기는 allowlist 파일만 Git에 추가한다. 원시 관측과 개인 Obsidian 문서는 실행 workspace에
남고 이 저장소에는 포함되지 않는다.
