# YOLO

윈동

step1 . https://github.com/ultralytics/yolov5      
code download

step2 . yolov5-master디렉토리에 들어가서 
pip install -r requirements.txt

step3. 각종 모듈설치 
ex) 
conda isntall git
conda install chardet

step4. roboflow에서 이미지 다운로드 후 폴더위치 선택
      폴더위치 : yolov5-master/data에 pothole 폴더 만들고 이 위치에 설치

  
cd yolov5-mater 입력 후 해당 파이썬 디렉토리로 이동

 step5.      
 python train.py --img 416 --batch 16 --epochs 20 --data pothole/data.yaml --cfg ./models/yolov5s.yaml --weights yolov5s.pt --name pothol_yolov5s

 트레인 후 yolov5-master/runs/train에 
 name으로 설정한 폴더가 생성되고 그 안에 best.pt파일 생성 
 best.pt파일이 트레인된 파일

 step6. 
python detect.py --weight runs\train\pothol_yolov5s\weights\best.pt --source C:\Users\Kimhyuntae\Desktop\Python_study\yolov5-master\data\pothole\test\images\*jpg 


햇갈리면 그냥 절대참조로 디렉토리 불러오기 

 
