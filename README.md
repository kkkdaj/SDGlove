# SDGlove(Static and Dynamic hand gesture dataset with soft sensor-embedded Glove)
This dataset consists of **time-series sensor data** collected while performing hand gestures wearing a **soft sensor-embedded glove**. It includes both **static and dynamic gestures**, collected from **30 subjects** to provide richer soft-sensor-based hand-gesture data.

## File Structure
```
SDGlove/
├── SDGlove.zip                                # Full dataset — 13,421 gesture records 
│   └── s#/                                   
│       └── {Gesture_num}-{Iteration_num}.csv
├── visualization.py
├── Participant_info.md                        # Participant details
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
1. **Data format**: CSV
2. **Total number of data**: 13,421 gestures
3. **Length per iteration**: approximately 5 seconds
4. **Column description**
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
1. **Number of [Participants](./Participant_info.md)**: 30
2. **Number of gesture classes**: 12
    - **Static gesture**(S1~S7)
    - **Dynamic gesture**(D1~D5)
    <img width="800" height="240" alt="static_gesture" src="https://github.com/user-attachments/assets/4b40910c-f3b5-4f3e-9019-f3ba45c30d59" />
    <img width="800" height="295" alt="dynamic_gesture" src="https://github.com/user-attachments/assets/125bd14a-ecb1-4d82-90fb-91c636d79516" />
3. **Data collection device**: Mollison Hand (Feel the Same Inc., Korea, soft sensor-embedded glove)
    <img width="500" height="308" alt="mollisen_hand" src="https://github.com/user-attachments/assets/e70e9e7d-ac70-46ad-939b-11a251db5a64" />
    - Sensor configuration: Soft sensors at each finger joint (measuring resistance values based on the degree of flexion at MCP and PIP)
    - Sampling rate: Collected every 15ms


5. **Collection procedure**
    - Glove worn on the Participant's dominant hand
    - Each gesture performed 40 times in random order.
    - Gesture performance duration: 5 seconds
    - Rest time between gestures: 3 seconds
 
6. **Basic preprocessing** (for incorrectly performed gestures)
    - If a gesture from a different class was performed → relabeled to the corresponding class
    - If a completely incorrect gesture was performed → removed


## usage

- (시각화 예시 코드 제공 시) 코드 사용 방법 및 시각화 결과 예시 등

---

## citation(Bibtex)
- If you want to cite our Datasets, you can use our paper:
```
our bibtex
```

## publications using this dataset

| Paper title | Journal/Conference | Year |
|-----|------|-----|

## license
This project is licensed under the MIT License - see the [LICENSE](./LICENSE) file for details.

## remark
