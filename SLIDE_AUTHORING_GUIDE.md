# Slide Authoring Guide

이 폴더의 HTML 자료는 발표 청중을 위한 슬라이드다. CLI 실행 계획, 내부 작업 추적, task id, staging asset 관리 절차를 정리하는 문서가 아니다.

## 작성 원칙

- 청중이 이해해야 하는 배경, 핵심 결과, 해석, 의사결정 포인트만 포함한다.
- 코드 구조, CLI 명령어, task id, dry-run, cleanup, staging prefix 같은 내부 실행 정보는 제외한다.
- “무엇을 했다”보다 “무엇을 알 수 있는가”를 중심으로 쓴다.
- 통계 결과는 표본 수, RMSE, Bias, r 등 해석에 필요한 지표와 함께 직관적으로 보여준다.
- raw-valid와 raw-gap처럼 해석이 달라지는 subset은 분리해서 제시한다.
- 주장은 과도하게 단정하지 않고, “현재 결과에서는”, “주요 원인 후보”, “검토 필요”처럼 증거 수준에 맞춰 표현한다.
- 불필요한 영문 용어는 피하고, 필요한 경우 처음 등장할 때 짧게 설명한다.
- “이다/입니다”식 문장보다 짧은 명사형 또는 간결한 서술형을 우선한다.

## 포함할 내용

- 연구 질문과 현재 목표
- 사용한 원자료와 기준 기간
- 주요 전처리 방법의 의미
- 핵심 통계 결과와 해석
- 남은 불확실성과 원인 후보
- 산출 기간과 소요 시간 추정
- 다음 판단에 필요한 검증 항목

## 제외할 내용

- CLI 명령어 목록
- 로컬 파일 수정 내역
- GEE task id
- staging/production asset prefix 세부값
- cleanup 실행 절차
- 코드 함수명 중심 설명
- 작업자용 체크리스트

## 표현 예시

권장:

```text
raw MODIS 관측이 있는 픽셀에서는 저자 산출물과 거의 일치.
오차는 gap-filled LST 영역에 집중.
2021-2024 전지구 확장에는 약 4-8주 필요.
```

비권장:

```text
CLI로 export task를 실행했고 staging prefix에 저장.
cleanup dry-run 후 execute 예정.
다음 단계는 predictor stack export.
```
