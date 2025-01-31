## ✍️ Formula to Latex
<br>

## Overview
이미지 형태로 된 수식을 OCR 모델을 통해 Latex 형식으로 자동 변환하는 도구

<img src="https://github.com/SeoYeonnLee/Formula-To-Latex/assets/105186555/5f1bfb20-ce2a-4359-97bc-117113b6539a.png" width="600" height="200"/>

<br>
<br>

## Key Features
### 1. WebUI-based Formula Conversion
- PDF 드래그 앤 드롭으로 논문 로드
- 마우스 드래그로 수식 영역 선택
- 실시간 Latex 코드 변환 및 복사 가능

### 2. Automatic Paper Formula Conversion
- YOLO v8을 통한 자동 수식 감지
- 감지된 모든 수식의 일괄 변환
- CSV 형태로 결과 저장
  
<br>

## Model Used
1. [Pix2tex - LatexOCR](https://github.com/lukas-blecher/LaTeX-OCR)
   : 이미지 형태의 수식을 Latex 코드로 변환하는 OCR 모델

2. [YOLO v8](https://github.com/HumanSignal/labelImg)
   : 논문 내의 수식 영역을 자동으로 감지하는 object detection 모델

<br>

## Usage
### Install
```
pip install -r requirements.txt
```

### WebUI Execution
```
python Formula_WebUI.py
```

### Automatic CSV Conversion Execution
1. <a href="https://drive.google.com/file/d/1tCwXJIUm3YN_GQMrcpkWb7w-mw3s7aq5/view?usp=sharing">best.pt 다운로드</a>
2. 필요한 폴더 생성
   ```
   mkdir formula_image output_image pdf_image
   ```
3. 실행
   ```
   python Formula_csv.py --pfp "path/to/paper.pdf"
   ```


## Guide
### WebUI Instructions
1. WebUI 실행 후 흰색 영역에 PDF 드래그
2. 원하는 수식 영역을 마우스로 드래그하여 선택
3. 2-3초 대기 후 하단에 변환된 Latex 코드 확인
4. 'Copy Text' 버튼으로 코드 복사

### CSV Conversion Guide
1. 명령어 실행 후 자동 변환 대기
2. 변환 완료 시 output.csv 파일 확인
3. CSV 파일에서 필요한 Latex 코드 복사하여 사용

<br>

## Structure
```
├── Formula_WebUI.py     # WebUI 구현
├── Formula_csv.py       # CSV 변환 구현
├── doc/                 # 문서 및 이미지
├── formula_image/       # 추출된 수식 이미지
├── output_image/        # 결과 이미지
└── pdf_image/          # 변환된 PDF 이미지
```

<br>

## WebUI Inference
![play](https://github.com/X-AI-eXtension-Artificial-Intelligence/4th-ADV-SESSION/assets/97331900/a5b42e61-616e-4c29-81ce-01db58071d38)
