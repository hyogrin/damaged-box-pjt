# Amazon Bedrock Titan Image Generator 모델을 활용한 데이터셋 생성으로 Amazon Rekognition / Amazon Lookout for Vision 으로 도메인에 특화된 객체 찾기

---



## Detect domain-specific objects with Amazon Rekognition custom labeling using Titan Image Generator on Amazon Bedrock

 
#### PROBLEM STATEMENT
특정 도메인에 특화된 객체를 찾거나 라벨링하여 단순 반복적인 업무를 자동화하는 AI/ML 유스케이스는 산업 전반에서 다양한 사례를 보고되고 있습니다. 하지만 실제 특정 업무 도메인을 담당하고 있는 조직에서 객체 인식용 딥러닝 모델을 학습하려면 많은 노력과 리소스, 전문인력이 필요하며 초기 데이터셋 확보가 어려운 경우가 많습니다. 
Amazon의 완전관리형 이미지/비디오 검색 및 분석 서비스인 Amazon Rekognition의 경우, 데이터 과학자와 같은 전문 인력은 필요 없을 정도로 쉽게 딥러닝 모델을 학습, 배포할 수 있는 서비스를 제공하고 있지만, 커스텀 라벨링을 통한 비즈니스에 고유한 객체를 추론하는 서비스를 개발하기 위한 학습/테스트용 데이터셋을 충분하게 확보하는 것은 서비스 개발팀에 또다른 어려움이 되는 경우가 많습니다. 

 
#### HOW ARE YOU SOLVING THE PROBLEM STATEMENT?
Amazon Bedrock에 pre-built된 Titan Image Generator 모델을 활용하면 학습과 테스트 시 필요하지만 확보가 어려운 이미지 데이터를 손쉽게 생성하고, 생성된 이미지를 Amazon Rekignition의 자동 라벨링 기능을 활용하여 쉽고, 빠르게 특정 도메인에 특화된 이미지추론 모델을 학습/서비스 할 수 있습니다. 

1. Amazon Bedrock
 - Generate a damaged / normal carbon boxes
 - Upload generated images to S3 bucket
2. Amazon Rekognition
 - Create Amazon Rekognition Custom Labels Projects
 - Register Training Dataset
 - Allow Amazon Rekognition to access the S3 bucket
 - Train and start the model
 - Inference an image by created model
 
#### BENEFIT
Data Scientist가 없는 서비스 개발팀에서도 쉽고 빠르게 생성형 AI기술을 활용하여 정확도 높고, 특정 도메인에 특화된 객체인식 서비스를 개발할 수 있습니다.  (Amazon Rekognition, Amazon Lookout for vision 학습 시 모두 활용 가능) 

 
#### DATASETS
모든 데이터셋은 Bedrock의 Titan Image Generator 모델을 활용해 생성한 이미지를 활용합니다. 

 
#### AWS SERVICES
Amazon Bedrock, Titan Image Generator Model(v1), S3, Amazon SageMaker, Amazon Rekognition
 
