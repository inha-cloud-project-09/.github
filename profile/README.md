# AI 감정 분석 기반 일기 회고 및 커뮤니티 플랫폼

> **INHA CloudComputing Project 09**  
> 인하대학교 클라우드 컴퓨팅 9팀 프로젝트입니다.  
> AWS 기반 인프라와 AI를 활용한 감정 분석 일기 서비스를 개발합니다.

---

## 📌 프로젝트 개요

- ✨ **AI 기반 감정 분석 및 유사 회고 자동 추천**  
  사용자의 텍스트·이미지 데이터를 분석해 감정 벡터를 추출하고,  
  유사한 감정을 겪었던 과거 상황을 AI가 요약하여 회고 형태로 제공합니다.

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

- 🔔 실시간 시스템 모니터링
Slack 채널과 연동하여 **일기 작성, 감정 분석, 클러스터링** 등 이벤트를 실시간으로 모니터링할 수 있습니다.
<img width="854" alt="스크린샷 2025-06-10 12 00 14" src="https://github.com/user-attachments/assets/6a9a4dd5-90e5-4666-bd99-be3f5f1aedd0" />


## 🛠️ 주요 기술 스택

| 분류       | 기술 스택                                                                 |
|------------|--------------------------------------------------------------------------|
| **Cloud**  | AWS (EC2, Lambda, RDS, S3, API Gateway, Bedrock, Comprehend, SNS, SQS)   |
| **Backend**| Python, Spring Boot, MySQL                                              |
| **Frontend**| React                                                                   |
| **DevOps** | GitHub, AWS IAM, CloudWatch, Slack                                             |
| **AI**     | Claude 3.5 Sonnet, AWS Comprehend, 자체 제작 음성분석 모델           |

---

## 🧩 아키텍처 개요

<img width="1080" alt="스크린샷 2025-06-06 17 08 23" src="https://github.com/user-attachments/assets/89ffb691-f86a-4908-b6ba-25dff06859f9" />




---

