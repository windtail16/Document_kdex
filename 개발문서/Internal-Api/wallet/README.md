Multi Sig 문서
=====================

### AWS KMS

- 테스트를 위하여 [aws-cli](https://aws.amazon.com/ko/cli) 설치 필요
- [configure](https://docs.aws.amazon.com/ko_kr/cli/latest/userguide/cli-chap-getting-started.html)
- [Kms GenerateDataKey](https://docs.aws.amazon.com/cli/latest/reference/kms/generate-data-key.html)를 통해서 aes key 생성 
- Dev key는 arn:aws:kms:ap-northeast-2:498266971821:alias/Dev-DataKey
- ex) aws kms generate-data-key --key-id arn:aws:kms:ap-northeast-2:498266971821:alias/Dev-DataKey --number-of-bytes 256

### 암호화 관련
- Wallet 암호화 알고리즘은 AES-256-CBC
- iv는 Buffer.from('00000000000000000000000000000000', 'hex');
- ex) key t+bzPMpMkPdJeAdmrVEeU38qGJUIA+p6/QPq1a8yDck= 로 'test' 암호화시에 A9hNZaSGu4jBWXBBzsVFlw== 나와야 함.