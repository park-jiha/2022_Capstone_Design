# 2022_Capstone_Design

## Code Update
- Face Pose(with Retina Face) 2021.10.04 ver.
- 2022.1.25 ver. : 좌, 우, 정면, 위, 아래, 왼쪽 위, 왼쪽 아래, 오른쪽 위, 오른쪽 아래 범위 지정, angle 값 검토
- 2022.3.16 ver. : 좌, 우 방면 5분할(세분화), 카메라와 객체 사이 거리 기준 160cm / retinaface 이외의 detection 모델 검토(mediapipe) -> 어두운 환경에서 인식률 저하 문제 

## 목적
- 사용자의 얼굴을 웹캠을 이용해 실시간으로 입력받음
- Roll, Pitch, Yaw를 이용한 3D 방향값 도출
- 사용할 환경에 가장 적합한 최적의 모델을 찾는 과정
- Use for Metaverse - 시선 처리

## Models

### 2. WHENet(https://github.com/Ascend-Research/HeadPoseEstimation-WHENet)
- RGB 이미지에서 오일러 각(Roll, Pitch, Yaw) 값을 계산
- YOLO_v3 를 이용한 Face Detection
- Problem : Version 문제(Tensorflow-gpu)

<img src="https://user-images.githubusercontent.com/62232217/148342110-e2c43c5e-8cb7-4244-b8ca-b97141dce0df.gif"  width="400" height="300"/>
