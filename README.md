# SDGlove

## Overview
- Data name: SDGlove(Static and Dynamic hand gesture dataset with soft sensor embedded Glove)
- This dataset consists of time-series sensor data collected while performing hand gestures wearing a soft sensor embedded glove. It includes both static and dynamic gestures, collected from a large number of subjects to provide richer soft sensor-based hand gesture data.

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
Research using hand gesture recognition based on this dataset can be applied in environments such as:
- Virtual safety training and robot teleoperation in hazardous industrial processes (manufacturing, construction, etc.)
- Supporting post-surgical patients in accurately and independently performing repeated hand rehabilitation exercises
- Sign language education
- Assistive communication devices that convert hand gestures into text/speech for the hearing impaired
- Sports motion analysis and coaching
- VR/AR-based home training, healthcare, gaming, etc. 

## Data description
- Data format: csv
    - {sbject number}/{gesture number}-{iteration number}.csv
- Total number of data: 13,453 gesture
- Length per iteration: approximately 5 seconds
- Column description
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
