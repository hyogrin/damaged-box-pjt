# damaged-box-pjt - Amazon Bedrock Titan Image Generator 모델을 활용한 Amazon Rekognition 커스텀 라벨링으로 도메인에 특화된 객체 찾기

---

## Overview
특정 도메인에 특화된 객체를 찾거나 라벨링하여 단순 반복적인 업무를 자동화하는 AI/ML 유스케이스는 산업 전반에서 다양한 사례를 보고되고 있습니다. 하지만 실제 특정 업무 도메인을 담당하고 있는 조직에서 객체 인식용 딥러닝 모델을 학습하고 배포, 서비스를 구성하려면 많은 노력과 리소스가 필요한 것이 사실입니다. 본 기술 블로그에서는 
Amazon Bedrock, Titan Image Generator Model, Amazon Rekognition 을 활용하여 쉽고 빠르게 실환경에 적용 가능한 도메인 특화된 객체를 찾는 서비스를 구성하는 방법을 소개합니다. 


#### BLOG POST TITLE
Amazon Bedrock Titan Image Generator 모델을 활용한 Amazon Rekognition 커스텀 라벨링으로 도메인에 특화된 객체 찾기
Detect domain-specific objects with Amazon Rekognition custom labeling using Titan Image Generator on Amazon Bedrock

#### Permalink
영문 URL 로 Permalink 를 만들어 주세요. (주로 제목의 영문 번역을 사용합니다.)
예) https://aws.amazon.com/ko/blogs/tech/detect-domain-specific-objects-with-amazonrekognition-customlabeling-using-titan-image-generator-on-amazon-bedrock


#### LEARNING LEVEL
Intermediate (200)

 
#### AUTHORS
Hyo Choi/hyogrin

 
#### PROBLEM STATEMENT
Amazon Rekognition에서 커스텀 라벨링을 통한 비즈니스에 고유한 객체 및 장면을 찾는 서비스를 개발하기 위해서는 학습/검증/테스트용 데이터셋을 구하기 어려운 경우가 빈번하게 발생합니다. Amazon Bedrock에 pre-built된 Titan Image Generator 모델을 활용하면 학습과 테스트에 필요한 데이터를 손쉽게 생성할 수 있습니다. 

 
#### HOW ARE YOU SOLVING THE PROBLEM STATEMENT?
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
Data Scientist가 없는 서비스 개발팀에서도 쉽고 빠르게 생성형 AI기술을 활용하여 정확도 높고, 특정 도메인에 특화된 객체인식 서비스를 개발할 수 있습니다.  

 
#### RELATED TFC
어떤 TFC에서 검토해야 하는지 기술해 주세요.(ex. Compute/Storage/Network/DB/Analytics/AI/Container/IoT/Serverless/etc)
AI

 
#### DATASETS
모든 데이터셋은 Bedrock의 Titan Image Generator 모델을 활용해 생성한 이미지를 활용합니다. 

 
#### AWS SERVICES
Amazon Bedrock, Titan Image Generator Model(v1), S3, Amazon SageMaker, Amazon Rekognitio
 