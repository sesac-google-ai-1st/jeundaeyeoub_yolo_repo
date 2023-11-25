# jeundaeyeoub_yolo_repo
# [Highway Project Result Report by Jeun DaeYeoub]

### 1. Project 진행과정
####   (1) Data(수도권영동선 1-1) download 후 CH01 ~ CH04만 선택
####   (2) my_Highway_3 code 실행
####       * 실행과정에서 dataPath 변경, code error 발생 등을 수정중이었으나,<br>결과 제출 시한때문에 code 수정 미완성 상태로 code upload.
####   (3) 모델 학습전에 train data 중 20%를 test data로 분리
####   (4) 모델은 nano, small, medium 3가지 실행

### 2. 학습결과평가
####   (1) nano model은 epochs=75로 학습하였으나,<br>학습결과를 볼 때 epochs=100이상으로 설정하여 추가학습이 필요해 보임
####   [nano_model_result](https://github.com/sesac-google-ai-1st/jeundaeyeoub_yolo_repo/blob/main/nano_model/results.png)
####   [nano_model_mAP50 etc](https://github.com/sesac-google-ai-1st/jeundaeyeoub_yolo_repo/blob/main/nano_model/nano_model_result(epochs%3D75).jpg)

####   (2) small model은 epochs=100으로 학습하였으나, detection data가 생기지 않아,<br>mAP50 등의 결과만 확보함
####   [small_model_mAP50 etc](https://github.com/sesac-google-ai-1st/jeundaeyeoub_yolo_repo/blob/main/small_model_result(epochs%3D100).jpg)
####   (3) medium model은 epochs=200으로 학습하였으나, epochs=108에서 학습이 멈추었고,<br>그 학습모델에 별도 저장한 test images로 detection한 결과 중 4장의 example을 올렸음.<br>test images detection결과 Bus, Truck도 잘 detection함.
####   [medium_model_reult](https://github.com/sesac-google-ai-1st/jeundaeyeoub_yolo_repo/blob/main/medium_model/results.png)
####   * medium_model에서는 mAP50 등의 결과를 채집하지 못함.(workbench down)
####   [test_example_images_with_medium_model](https://github.com/sesac-google-ai-1st/jeundaeyeoub_yolo_repo/tree/main/test_example_images_medium_model)

### 3. 보완이 필요한 사항
####   (1) train data에 Bus Images가 현격히 부족하여 추가할 필요가 있음.<br>우리가 다운받았던 Bus객체추가 data에는 Images만 있고 labels data가 없어서 사용하지 못함.
####   (2) detection test를 Images data가 아닌 동영상 data로 해 볼 필요성을 느낌.
####   (3) 야간 data, 다양한 날씨상태하에서 data에 대해서는 추가 학습이<br> 필요할 것으로 생각됨.
