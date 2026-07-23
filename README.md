# SDGlove

## Overview
- Data name: SDGlove(Static and Dynamic hand gesture dataset with soft sensor embedded Glove)
- 이 데이터는 soft sensor embedded glove을 착용한 상태로 hand gesture를 수행하며 수집된 시계열 센서 데이터입니다.
- 정적 동작과 동적 동작을 모두 포함하며, 다수의 피험자를 대상으로 실험을 진행하여 보다 풍성한 soft sensor 기반 hand gesture 데이터를 제공합니다.

## File Structure
```
SDGlove/
├── SDGlove.zip                                # Full dataset — 13,453 gesture records 
│   └── s#/                                    # subject number
│       └── {Gesture_num}-{Iteration_num}.csv
├── visualization.py
├── Participant_info.md                                # Participant details
├── README.md                
└── NOTICE.md
```

## Tasks
이 데이터를 통한 hand gesture recognition 연구는 아래와 같은 환경에서 활용될 수 있습니다.
- 위험한 공정(제조, 건설 등) 환경에서의 가상 안전 교육
- 수술 후 환자들이 여러 손 동작을 수행하며 스스로 재활 치료를 수행할 수 있도록 지원
- 수화 교육
- VR/AR 활용 홈트레이닝, 헬스케어, 게임 등

## Data description
- 데이터 형식: csv
    - {sbject number}/{gesture number}-{iteration number}.csv
- 총 데이터 개수: 13,453 gesture
- 한 iteration 당 길이: 약 5초
- 데이터 column 소개
    - timestamp
    - sensor_1~snesor_10: 엄지mcp, 엄지pip, 검지mcp, 검지pip, 중지mcp, 중지pip, 약지mcp, 약지pip, 소지mcp, 소지pip, 


## Experimental setup
- number of subject: 30
- number of gesture class: 12
  - Static gesture(S1~S7)
    <img width="800" height="240" alt="static_gesture" src="https://github.com/user-attachments/assets/4b40910c-f3b5-4f3e-9019-f3ba45c30d59" />
  - Dynamic gesture(D1~D5)
    <img width="800" height="295" alt="dynamic_gesture" src="https://github.com/user-attachments/assets/125bd14a-ecb1-4d82-90fb-91c636d79516" />
- 수집 장비: Mollison Hand(soft sensor embedded glove)
    - 센서 구성: 손가락 관절별 소프트 센서(MCP, PIP의 굽힘 정도에 따른 저항값 측정)
    - 측정 단위:
    - 측정 속도: 15ms마다 수집

- 수집 방법
    - 피험자의 주 사용 손에 장갑 착용
    - 각 제스처를 40회씩 랜덤한 순서로 수행
    - 제스처 수행 시간: 5초
    - 제스처 간 쉬는 시간: 3초
 
- 기본 전처리(잘못 수행된 제스처에 대해)
  1) 다른 class의 동작 수행한 경우 → 해당 동작으로 재라벨링
  2) 완전히 틀린 동작을 수행한 경우 → 삭제


## usage

- (시각화 예시 코드 제공 시) 코드 사용 방법 및 시각화 결과 예시 등

---

## citation
- 다정 논문 게재 후 작성

## publications using this dataset

- 추후 우리 데이터 사용한 논문이 생기면 지속적으로 추가?

## license

- mit할건지 or 다른거 할건지 결정 후 작성
- 우선 mit

## remark

- 기타 안내 사항
