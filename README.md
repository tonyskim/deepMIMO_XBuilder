# deepMIMO_XBuilder: Executers &amp; Builders of deepMIMO framwork
### A set of jupyter notebook scripts for executing pretrained prediction models or building user own prediction models.

본 저장소에서 제공하는 파이썬 언어 기반 주피터 노트북 스크립트는 유방암의 3D 진단영상 데이터 및 다중오믹스 데이터를 분석하여 OncotypeDX 위험지수, 예후 또는 면역형을 예측하는 모델 구동 파이썬 스크립트 코드를 제공합니다.

## 저장소의 파일 구성
* <b>UC_001.unimodal_MRI_OncoDX_predictor.ipynb</b>: 유방암의 MRI 영상데이터에서 OncotypeDX 스코어를 예측하는 모델 구동 스크립트
* <b>UC_002.multimodal_MRI_OncoDX_predictor.ipynb</b>: 유방암의 MRI 영상데이터 및 ER, PR, HER2 단백마커 데이터로부터 OncotypeDX 스코어를 예측하는 모델 구동 스크립트
* <b>UC_003-1.unimodal_MRI_TNBC_prognosis_predictor.ipynb</b>: 삼중음성유방암의 MRI 영상데이터에서 환자의 예후를 예측하는 모델 구동 스크립트
* <b>UC_003-2.unimodal_MRI_TNBC_imtype_predictor.ipynb</b>: 삼중음성유방암의 MRI 영상데이터에서 환자의 면역형을 예측하는 모델 구동 스크립트
* <b>UC_004-1.multimodal_MRI_TNBC_prognosis_predictor.ipynb</b>: 삼중음성유방암의 MRI 영상데이터 및 다중오믹스 데이터로부터 환자의 예후를 예측하는 모델 구동 스크립트
* <b>UC_004-2.multimodal_MRI_TNBC_imtype_predictor.ipynb</b>: 삼중음성유방암의 MRI 영상데이터 및 다중오믹스 데이터로부터 환자의 면역형을 예측하는 모델 구동 스크립트
* <b>UC_005.unimodal_prognosis_builder.ipynb</b>: 일반암의 3차원 영상데이터에서 환자의 예후 예측모델을 구축하는 예측모델 구축 스크립트
* <b>UC_006.multimodal_prognosis.builder.ipynb</b>: 일반암의 3차원 영상데이터와 다중오믹스 또는 임상데이터에서 환자의 예후 예측모델을 구축하는 예측모델 구축 스크립트
* <b>UC_00*.***.txt</b>: 각 스크립트를 구동할 수 있는 예제데이터의 메타정보

## 사용방법
(1) 본 저장소의 코드를 사용하려면 콘다 (Conda) 기반 가상환경을 생성해야 합니다.
<pre><code>$> conda create -n [your_vitural_envriment_name]
$> conda activate [your_vitural_envriment_name]
</code></pre>

(2) 사용자의 콘다 환경을 활성화(activation)한 후, 사용자는 다음과 같은 필수 패키지를 conda 또는 pip 명령을 이용하여 설치해야 합니다:

<pre><code>#넘파이, 판다스, 맷플롯립 설치
$> conda install numpy pandas matplotlib

#주피터 노트북 설치
$> conda install jupyter notebook

#OpenCV 설치
$> conda install –c conda-forge opencv

#케라스 설치
$> pip install keras

#텐서플로 설치
$> pip install tensorflow

#기타 패키지 설치
$> pip install scikit-learn lifelines pydot np_utils
$> conda install pymysql
$> conda install nibabel graphviz tabulate

#패키지 목록 최종 확인
$> conda list

#본 저장소가 제공하는 'environment.yml'에 노트북 스크립트를 구동에 필요한 패키지 정보가 기술되어 있습니다.
</code></pre>

(3) 본 저장소에서 제공하는 ipynb 노트북 스크립트 및 예제 환자 메타정보데이터 (*.txt) 파일을 임포트 합니다.

(4) deepMIMO 웹사이트 (http://deepMIMO.appex.kr) 에서 제공하는 사전구축 예측모델 (*.hdf5) 및 nifti 형식의 예제 MRI 데이터를 다운로드 받아, ipynb 노트북 스크립트가 위치한 동일 폴더에 위치 시킵니다.

(5) 마지막으로, 다음 명령어로 주피터 노트북 프로그램을 실행하십시오. 제공된 노트북 스크립트를 구동할 수 있습니다.
<pre><code>$> jupyter notebook</code></pre>
