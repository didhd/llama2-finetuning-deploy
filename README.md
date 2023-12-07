# LLama2 LLM Fine-tuning on Amazon SageMaker

이 프로젝트는 Amazon SageMaker에서 LLama2 Large Language Model (LLM)을 미세 조정하는 방법을 보여줍니다. Hugging Face의 PEFT (Parameter Efficient Fine-tuning) 기법과 QLoRA (Quantized Low-Rank Adapters)를 사용하여, 대규모 언어 모델을 더 효율적으로 미세 조정할 수 있습니다.

## 주요 기능

- **허깅페이스 인증**: Hugging Face 계정을 사용하여 모델과 데이터셋에 접근합니다.
- **PEFT 및 QLoRA**: 대규모 언어 모델을 더 효율적으로 미세 조정할 수 있는 최신 기술을 사용합니다.
- **SageMaker 통합**: Amazon SageMaker를 활용하여 쉽고 빠르게 미세 조정을 진행합니다.

## 시작하기

1. **허깅페이스 계정 설정**: 먼저 [허깅페이스 가입](https://huggingface.co/join) 후 [토큰 설정](https://huggingface.co/settings/tokens)을 완료해야 합니다.

2. **SageMaker 환경 설정**: SageMaker Studio 또는 SageMaker 노트북 인스턴스에서 PyTorch 기반 커널을 사용합니다.

3. **인스턴스 선택**: 훈련 작업에는 최소 `ml.g5.2xlarge` 인스턴스를 사용하며, 분산 훈련에는 `ml.g5.12xlarge`를 권장합니다.

4. **데이터셋 준비**: `kyujinpy/KOR-OpenOrca-Platypus` 데이터셋을 사용하여, 구조화된 예시들을 처리합니다.

5. **훈련 실행**: 훈련 스크립트와 Hugging Face Estimator를 사용하여 SageMaker에서 훈련 작업을 시작합니다.

## 중요 사항

- **QLoRA**: 4비트로 양자화된 모델과 저차원 어댑터를 사용하여, 대규모 모델의 메모리 사용량을 줄이면서 성능을 유지합니다.
- **하드웨어 요구 사항**: 다양한 모델 크기에 적합한 인스턴스 유형과 설정에 주의하십시오.

## 노트북

자세한 내용은 
* [fine-tune-llama-2-13b-on-amazon-sagemaker.ipynb](https://github.com/didhd/llama2-finetuning-deploy/blob/main/fine-tune-llama-2-13b-on-amazon-sagemaker.ipynb)

  
노트북을 참고하십시오.

---

