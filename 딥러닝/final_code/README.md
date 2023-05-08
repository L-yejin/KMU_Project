최종 제출 code 입니다

### 폴더와 파일 설명
- [기본]폴더는 별도로 학습시키지 않은 model
- [최종training]폴더는 약 1만3천장을 10epoch으로 학습시킨 모델
- [3epoch]폴더는 약 2만5천장으로 했을 때 epoch을 3으로 학습
-해당 폴더들은 [폴더]최종코드→[폴더]yejin_ChromaGAN→[폴더]models안에 압축을 풀어서 실행시켜야 함

---

#### 데이터
[폴더]최종코드→[폴더]DATASET에 데이터 일부만 저장해놓았습니다.
[폴더]최종코드 속 1.DATASET정제.ipynb는 데이터셋 resize와 흑백변환, train,test 분리하는 내용이 들어있습니다.
[폴더]최종코드→[폴더]DATASET→[폴더]음식원본 속에 color이미지와 gray이미지 일부만 넣어뒀습니다.

---

#### ChromaGAN 실행
[폴더]최종코드 속 2.ChromaGAN.ipynb에는 Git clone해오기와 version맞추는 내용이 있고, main.py --mode 1을 실행시키면 training할 수 있고, main.py –mode 2는 학습된 내용으로 출력만 하고 싶을 때 실행시키면 결과물이 출력됩니다.
실행 전 [폴더]최종코드→[폴더]yejin_ChromaGAN→[폴더]configs 속 config.py의 경로를 수정한 뒤 사용해야합니다.

---

[폴더]최종코드→[폴더]yejin_ChromaGAN→[폴더]models 속의 colorization.pt, discriminator.pt는 기존 학습이 안된 것이고,
colorization_3.pt, discriminator_3.pt는 train data를 약 2만5천장으로 했을 때 epoch을 3으로하고 실행했을 때입니다.
colorization_final10.pt, discriminator_final10.pt는 train data를 약 1만3천장을 10epoch으로 학습했을 때 저장된 값입니다.

---

[폴더]최종코드→[폴더]yejin_ChromaGAN→[폴더]Output_final→[폴더]final_origin은 기존 모델을 돌렸을 때 나온 test데이터를 colorization한 결과입니다.
[폴더]최종코드→[폴더]yejin_ChromaGAN→[폴더]Output_final→[폴더]test_origin은 finetuning된 모델을 돌렸을 때 나온 test데이터를 colorization한 결과입니다.

---

#### 일부 저장된 Loss
[폴더]최종코드→[폴더]yejin_ChromaGAN→[폴더]models 속의 Loss_D.pkl과 Loss_G.pkl은 train시킬 때, loss저장하는 코드 추가적으로 넣어서 1epoch만 실행했을 때 나온 loss를 저장한 것입니다.
[폴더]최종코드 속 3.Loss시각화.ipynb는 위의 pkl을 열어서 시각화한 내용입니다.

---

#### 평가지표
[폴더]최종코드→[폴더]yejin_ChromaGAN→[폴더]Output_final→[폴더]원본,생성이미지_매칭시키기에서 원본이미지와 생성된 이미지를 위아래로 붙인 이미지가 생성되고, 평가지표를 실행 시켜야되는데 나온 결과와 원본 이미지간의 매칭이 불가해서 실행하지 못했습니다.
[폴더]최종코드 속 4.평가지표.ipynb는 평가지표 코드를 실행하고, 결과를 출력할 수 있는 내용입니다.
사용 시, [폴더]metrics_package 속의 main.py의 경로를 수정해야합니다.

---

#### DeOldify
DeOldify는 기존 train된 모델을 사용해서 결과 몇 가지 출력한 사진들을 
[폴더]DeOldify_rusult_image 속에 저장해놓았습니다.

InstColorization_training.ipynb는 DeOldify를 실행 시도한 코드입니다.

