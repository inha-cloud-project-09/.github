# AI 감정 분석 기반 일기 회고 및 커뮤니티 플랫폼

> **INHA CloudComputing Project 09**  
> 인하대학교 클라우드 컴퓨팅 9팀 프로젝트입니다.  
> AWS 기반 인프라와 AI를 활용한 감정 분석 일기 서비스를 개발합니다.

---

- ✨ **AI 기반 감정 분석 및 유사 회고 자동 추천**  
  사용자의 텍스트·이미지 데이터를 분석해 감정 벡터를 추출하고,  
  유사한 감정을 겪었던 과거 상황을 AI가 요약하여 회고 형태로 제공합니다.

- 🧩 **자체 제작 AI모델 일기 데이터 기반 다양한 서비스 제공**  
  FastAPI로 배포된 자체 제작 AI 모델이 사용자의 일기와 감정 데이터를 기반으로  
  회복 루틴을 제공합니다.

- 🎙️ **음성 기반 감정 분석 및 AI 공감 대화 제공**  
  사용자의 음성을 텍스트로 변환한 뒤 감정 벡터를 분석하여,  
  AI가 위로, 격려, 공감 등 정서적 반응을 제공합니다.

- 👥 **감정 벡터 기반 유저 클러스터링 및 커뮤니티 매칭**  
  실시간 감정 벡터를 기반으로 유저들을 자동 분류하고,  
  비슷한 감정을 가진 사람들끼리 대화할 수 있는 감정 나눔방을 자동 추천합니다.

- ☁️ **AWS 기반 서버리스 인프라 구성**  
  Lambda, S3, RDS, API Gateway, SNS/SQS, CloudWatch 등  
  AWS 자원을 활용하여 유연하고 확장 가능한 MSA 아키텍처를 설계합니다.

- 🔁 **CloudWatch, SNS, SQS 기반 정기 자동화 파이프라인**  
  매일 새벽 1시, CloudWatch 스케줄러가 실행되며  
  **모든 사용자의 최신 감정 벡터를 기반으로 커뮤니티 클러스터를 재구성**합니다.  
  또한 유저가 일기를 작성하면 자동으로 SNS와 SQS를 통해 Lambda 함수들을 트리거하여  
  감정 분석 → 클러스터링까지 이어지는 전체 프로세스를 자동화합니다

- 🧩 **기능 단위 Lambda 마이크로서비스 설계**  
  감정 분석, 회고 추천, 클러스터링, 커뮤니티 기능을 각각 독립된 Lambda 함수로 분리하여  
  유지보수와 배포가 효율적인 구조를 구현합니다.

- 🌐 **RESTful API 설계**

- 🔔 Slack 채널과 연동하여 **일기 작성, 감정 분석, 클러스터링** 등 이벤트를 실시간으로 모니터링할 수 있습니다.
<img width="854" alt="스크린샷 2025-06-10 12 00 14" src="https://github.com/user-attachments/assets/6a9a4dd5-90e5-4666-bd99-be3f5f1aedd0" />
<img width="753" alt="스크린샷 2025-06-15 21 41 03" src="https://github.com/user-attachments/assets/0026a9c7-86f4-4268-b610-b37d2e69e2d5" />


## 🛠️ 주요 기술 스택

| 분류       | 기술 스택                                                                 |
|------------|--------------------------------------------------------------------------|
| **Cloud**  | AWS (EC2, Lambda, RDS, S3, API Gateway, Bedrock, Comprehend, SNS, SQS)   |
| **Backend**| Python, Spring Boot, MySQL                                              |
| **Frontend**| React, NextJS                                                                |
| **DevOps** | GitHub, AWS IAM, CloudWatch, Slack                                             |
| **AI**     | Claude 3.5 Sonnet, AWS Comprehend, 자체 제작 AI모델           |

---

## 🧩 아키텍처 개요

<img width="1007" alt="스크린샷 2025-06-15 22 51 22" src="https://github.com/user-attachments/assets/9bd7465a-eeff-43e1-9287-a61a667faf63" />





---
## 사용 예시
### AI 일기 분석 회고
<img width="762" alt="스크린샷 2025-06-15 21 39 41" src="https://github.com/user-attachments/assets/c4f32c57-3b3c-42ba-b682-87e1b0db3381" />

### 일기 데이터를 기반으로 AI와 음성 대화
<img width="839" alt="스크린샷 2025-06-15 21 39 10" src="https://github.com/user-attachments/assets/5df0b20e-8564-4c09-8112-578b7a880664" />

### 감정과 일기 데이터 기반 AI 회복 루틴 제공
<img width="760" alt="스크린샷 2025-06-15 21 52 01" src="https://github.com/user-attachments/assets/1136180a-a995-478c-aff0-615241503eb9" />
<img width="750" alt="스크린샷 2025-06-15 21 52 26" src="https://github.com/user-attachments/assets/7843b2c5-63ec-46d9-810a-7b049002fee1" />
<img width="741" alt="스크린샷 2025-06-15 21 52 46" src="https://github.com/user-attachments/assets/43e018ee-ad39-46ce-b282-5923d357f1ee" />
<img width="262" alt="스크린샷 2025-06-15 21 53 18" src="https://github.com/user-attachments/assets/1479c1dc-f5df-4ba0-9e33-e12cb39df349" />


### 날씨 데이터 기반 감정 예측
<img width="1042" alt="스크린샷 2025-06-15 21 49 28" src="https://github.com/user-attachments/assets/8a6674cd-c34e-429e-b488-403af8187144" />

