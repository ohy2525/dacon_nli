# dacon_nli
데이콘 한국어 문장 관계 분류 경진대회

## data
├ Index : train data index

├ Premise : 실제 Text

├ Hypothesis : 가설 Text

└ Label : 참(Entailment) 또는 거짓(Contradiction) 또는 중립(Neutral)



*Premise와 Hypothesis의 관계를 추론

- 추가 데이터
KLUE Official Dev Data  (https://klue-benchmark.com/tasks/68/data/download)

## Model
 Klue/roberta - large
 - Pretrained RoBERTa Model on Korean Language. See Github and Paper for more details.
 (https://huggingface.co/klue/roberta-large)
 - optimizer : Adamp
 - 
## Train
모델 1 : Klue/roberta - large ( epoch 10 )
모델 2 : Klue/roberta - large ( epoch 10 중 가장 높은 valid accuracy 모델을 저장)
모델 3 : Klue/roberta - large ( epoch 20 )
모델 4 : Klue/roberta - large ( epoch 20,  5번째 fold 제외 )

제출 : 모델의 결과의 최빈값 사용

## result
- 최종 8위
![image](https://user-images.githubusercontent.com/81752763/172536100-c366bd57-4a3f-4b32-bcdf-2f146447c7f2.png)
