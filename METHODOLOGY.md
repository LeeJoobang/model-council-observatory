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

## 발행 정책

발행기는 allowlist 파일만 Git에 추가한다. 원시 관측과 개인 Obsidian 문서는 실행 workspace에
남고 이 저장소에는 포함되지 않는다.
