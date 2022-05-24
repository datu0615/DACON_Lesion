# DACON_Lesion
![20220524_123055](https://user-images.githubusercontent.com/84311270/169943253-af277b35-191f-4ca4-80a4-27b66e7b600c.png)
캡술 내시경 학습용 이미지 데이터셋을 활용한 캡슐 내시경 병변 검출 AI 개발.

## Dataset
1. train - 학습용 json 파일 62622개  
	├ train_100000.json  
	│	├ file_name : 파일 이름  
	│	├ shape : 객체별 label 및 객체 위치 정보  
	│	│	├ label : 객체 이름  
	│	│	├ points : 객체의 4개 꼭지점(x, y) 좌표 정보  
	│	│	├ label : 객체 이름  
	│	│	├ points : 객체의 4개 꼭지점(x, y) 좌표 정보  
	│	│	├ ...  
	│	├ imageData : base64형식 이미지 데이터  
	│	├ imageHeight : 이미지 세로 길이  
	│	└ imageWidth : 이미지 가로 길이  
	├ train_100001.json  
	├ train_100002.json  
	├ ...

2. test - 평가용 json 파일 20874개  
	├ test_200000.json  
	│	├ file_name : 파일 이름  
	│	├ imageData : base64형식 이미지 데이터  
	│	├ imageHeight : 이미지 세로 길이  
	│	└ imageWidth : 이미지 가로 길이  
	├ test_200001.json  
	├ test_200002.json  
	├ ...  

3. class_id.csv - 객체별 제출 id정보  
class : 객체이름  
class_id : 객체 id  

4. sample_submission.csv - 제출 양식  
file_name : test 파일 이름  
class_id : 검출한 객체 id  
confidence : 검출한 객체의 정확도(0~1)  
point1_x : 검출한 객체 좌상단 x좌표  
point1_y : 검출한 객체 좌상단 y좌표  
point2_x : 검출한 객체 우상단 x좌표  
point2_y : 검출한 객체 우상단 y좌표  
point3_x : 검출한 객체 우하단 x좌표  
point3_y : 검출한 객체 우하단 y좌표  
point4_x : 검출한 객체 좌하단 x좌표  
point4_y : 검출한 객체 좌하단 y좌표  

## Model
Yolov5 모델을 사용하여 진행.
