# Llama 기반으로 AWS 에서 RAG 구축하기

## 개요
Amazon Bedrock과 SageMaker를 사용하여 생성형 AI 모델을 배포하고 활용하는 방법을 소개합니다. 주요 내용으로는 Bedrock을 통한 임베딩 및 텍스트 생성, SageMaker를 이용한 Llama 모델 배포, OpenSearch를 활용한 지식 베이스 구축, 그리고 RAG(Retrieval-Augmented Generation) 시스템 구현 등이 포함됩니다. 이를 통해 실제 비즈니스 문제를 해결하는 데 도움이 되는 AI 솔루션을 만들어볼 수 있습니다.

## 파일별 설명

### 0. foundation model - bedrock.ipynb
이 노트북에서는 Amazon Bedrock의 기본 기능을 소개합니다. Titan 임베딩 모델을 사용하여 텍스트 임베딩을 생성하고 유사도를 계산하는 방법, Claude 3 Haiku 모델을 이용한 텍스트 생성 및 이미지 분석 방법, 그리고 스트리밍 방식의 텍스트 생성 구현 방법을 배우게 됩니다. 이를 통해 Bedrock의 다양한 기능을 실습해볼 수 있습니다.

### 1. foundation model - deploy_llama-3.2-1b-instruct.ipynb
이 노트북에서는 SageMaker JumpStart를 사용하여 Llama 3.2 1B Instruct 모델을 배포하는 방법을 배웁니다. 모델 엔드포인트를 생성하고 호출하는 방법을 상세히 설명하고 있어, 실제 서비스에 모델을 적용하는 방법을 이해할 수 있습니다.

### 2. foundation model - inference_llama-3.2-1b-instruct.ipynb
이 노트북에서는 SageMaker 엔드포인트에 배포된 Llama 3.2 1B Instruct을 boto3를 사용하여 호출하는 방법을 소개합니다. 모델 추론 예시와 응답 처리 방법을 자세히 설명하고 있어, 실제 애플리케이션에서 모델을 활용하는 방법을 배울 수 있습니다.

### 3. (Option) foundation model - inference_llama-3.2-1b-instruct-huggingface.ipynb
이 노트북은 HuggingFace 에서 Llama 3.2 1B Instruct 모델을 SageMaker 엔드포인트로 배포하는 방법을 소개합니다. 배포된 모델을 사용한 추론 예시도 제공하여, HuggingFace 모델을 AWS 환경에서 활용하는 방법을 배울 수 있습니다.

### 4. (Option) foundation model - inference_llama-3.1-8b-vllm.ipynb
이 노트북에서는 vLLM을 사용하여 Llama 3.1 8B 모델을 SageMaker에 배포하는 방법을 설명합니다. 스트리밍 방식의 텍스트 생성 구현과 채팅 템플릿 사용 예시를 제공하여, 대규모 언어 모델을 효율적으로 활용하는 방법을 배울 수 있습니다.

### 5. knowledge base - setup_opensearch.ipynb
이 노트북에서는 OpenSearch 도메인을 생성하고 설정하는 방법을 소개합니다. 도메인 생성 완료 대기 및 엔드포인트 확인 과정을 상세히 설명하여, 지식 베이스 구축을 위한 기초를 마련할 수 있습니다.

### 6. knowledge base - store_document_to_opensearch.ipynb
이 노트북에서는 PDF 문서를 읽고 청크 단위로 분할하는 방법을 설명합니다. 분할된 문서를 OpenSearch에 벡터로 변환하여 저장하는 과정을 소개하여, 실제 문서를 지식 베이스화하는 방법을 배울 수 있습니다.

### rag.ipynb
이 노트북에서는 RAG(Retrieval-Augmented Generation) 시스템을 구현하는 방법을 배웁니다. OpenSearch에 저장된 문서를 검색하고, 이를 기반으로 생성형 AI 모델을 사용하여 질문에 답변하는 과정을 상세히 설명합니다. 이를 통해 실제 비즈니스 문제를 해결하는 AI 솔루션을 만드는 방법을 배울 수 있습니다.
