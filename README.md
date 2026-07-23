# SDGlove(Static and Dynamic hand gesture dataset with soft sensor embedded Glove)
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
    | Column | Description |
    |-----|------|
    |sensor_1|Thumb MCP|
    |sensor_2|Thumb PIP|
    |sensor_3|Index MCP|
    |sensor_4|Index PIP|
    |sensor_5|Middle MCP|
    |sensor_6|Middle PIP|
    |sensor_7|Ring MCP|
    |sensor_8|Ring PIP|
    |sensor_9|Little MCP|
    |sensor_10|Little PIP|



## Experimental setup
- number of subject: 30
- number of gesture class: 12
  - Static gesture(S1~S7)
    <img width="800" height="240" alt="static_gesture" src="https://github.com/user-attachments/assets/4b40910c-f3b5-4f3e-9019-f3ba45c30d59" />
  - Dynamic gesture(D1~D5)
    <img width="800" height="295" alt="dynamic_gesture" src="https://github.com/user-attachments/assets/125bd14a-ecb1-4d82-90fb-91c636d79516" />
- Data collection device: Mollison Hand(soft sensor embedded glove)
    - Sensor configuration: Soft sensors at each finger joint (measuring resistance values based on the degree of flexion at MCP and PIP)
    - Sampling rate: Collected every 15ms

- Collection procedure
    - Glove worn on the subject's dominant han
    - Each gesture performed 40 times in random order
    - Gesture performance duration: 5 seconds
    - Rest time between gestures: 3 seconds
 
- Basic preprocessing (for incorrectly performed gestures)
  1. If a gesture from a different class was performed → relabeled to the corresponding class
  2. If a completely incorrect gesture was performed → removed


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
