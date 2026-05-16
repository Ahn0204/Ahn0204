# 안녕하세요. 백엔드 개발자 안성진입니다.

사용자가 실제로 사용하는 서비스를 직접 구현하고,  
문제가 발생했을 때 원인을 분석하며 개선하는 과정에 흥미를 느끼는 백엔드 개발자입니다.

Spring Boot 기반 웹 서비스를 개발하며  
회원 인증 / 권한 처리, DB 설계, 실시간 기능(WebSocket), API 설계 등을 경험했습니다.

단순 기능 구현에 그치지 않고  
"왜 이런 구조로 설계했는가",  
"운영 중 어떤 문제가 발생할 수 있는가"를 함께 고민하며 개발하려고 노력하고 있습니다.

현재는 실시간 웨이팅 & 예약 시스템을 개발하며  
Spring Security 기반 권한 처리와 실시간 데이터 흐름 구조를 학습하고 있습니다.

---

# 🛠 Tech Stack

## Backend
![Java](https://img.shields.io/badge/Java-000000?style=for-the-badge&logo=openjdk)
![Spring Boot](https://img.shields.io/badge/SpringBoot-6DB33F?style=for-the-badge&logo=springboot&logoColor=white)
![Spring Security](https://img.shields.io/badge/SpringSecurity-6DB33F?style=for-the-badge&logo=springsecurity&logoColor=white)
![JPA](https://img.shields.io/badge/JPA-59666C?style=for-the-badge)
![MyBatis](https://img.shields.io/badge/MyBatis-000000?style=for-the-badge)

## Database
![MariaDB](https://img.shields.io/badge/MariaDB-003545?style=for-the-badge&logo=mariadb)
![Oracle](https://img.shields.io/badge/Oracle-F80000?style=for-the-badge&logo=oracle&logoColor=white)

## Frontend
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![jQuery](https://img.shields.io/badge/jQuery-0769AD?style=for-the-badge&logo=jquery&logoColor=white)
![Thymeleaf](https://img.shields.io/badge/Thymeleaf-005F0F?style=for-the-badge&logo=thymeleaf&logoColor=white)

## Infra & Tools
![AWS](https://img.shields.io/badge/AWS_EC2-FF9900?style=for-the-badge&logo=amazonec2&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)

---

# 📌 Main Projects

## 🥖 모두의빵
### 실시간 주문 및 배달 상태 관리 웹 서비스

> 사용자 / 점주 / 배달기사 역할을 기반으로  
> 주문과 배송 상태를 실시간으로 관리할 수 있는 서비스입니다.

### ✔ 담당 기능
- Spring Security 기반 권한 처리
- 주문 / 배송 상태 흐름 관리
- 마이페이지 기능 구현
- 실시간 주문 상태 처리
- DB 연관관계 및 상태 구조 설계

### ✔ Trouble Shooting
- 연관 데이터 조회 과정에서 발생한 N+1 문제 분석 및 Fetch Join 적용
- 주문 데이터 삭제 과정에서 참조 무결성 문제 발생 → 구조 개선 및 soft delete 적용

### ✔ Tech
`Spring Boot` `Spring Security` `JPA` `Oracle` `WebSocket`

---

## ⏳ Waiting System
### 실시간 웨이팅 & 예약 관리 웹 서비스

> 매장의 대기 현황과 예약 정보를  
> 실시간으로 확인하고 관리할 수 있는 웹 서비스입니다.

### ✔ 주요 기능
- 실시간 웨이팅 등록
- 대기 순번 관리
- 매장 혼잡도 조회
- 예약 기능
- ROLE 기반 권한 처리

### ✔ 고민한 부분
- 동일 사용자의 중복 웨이팅 방지
- 실시간 데이터 동기화 구조
- 상태값 기반 웨이팅 흐름 설계
- 사용자 / 점주 권한 분리 처리

### ✔ Tech
`Spring Boot` `Spring Security` `JPA` `MariaDB` `WebSocket`

---

## 📰 뉴스 기사 웹 서비스
### 카테고리 기반 뉴스 및 댓글 서비스

### ✔ 주요 기능
- 뉴스 카테고리 분류
- 기사 상세 조회
- 댓글 기능 구현
- 기자 마이페이지 구현

### ✔ 경험한 부분
- 댓글 CRUD 및 비동기 처리
- 화면 구성과 API 연동
- 사용자 흐름 기반 페이지 구성

### ✔ Tech
`Spring Boot` `JPA` `Oracle`

---

# 🔥 Problem Solving

## 1. Spring Security CSRF 403 문제 해결

AJAX POST 요청 과정에서  
403 Forbidden 오류가 반복적으로 발생했습니다.

문제를 분석하며 Spring Security의 CSRF 동작 방식을 이해했고,  
meta 태그 기반 토큰 전달 및 AJAX Header 설정을 통해 문제를 해결했습니다.

이를 통해 단순 기능 구현이 아니라  
보안 설정과 요청 흐름까지 함께 고려하는 경험을 할 수 있었습니다.

---

## 2. JPA 연관관계 조회 성능 개선

주문 목록 조회 과정에서  
연관 엔티티가 반복 조회되며 성능 저하 문제가 발생했습니다.

초기에는 단순 쿼리 문제라고 생각했지만,  
실제로는 JPA 지연 로딩 구조로 인해 N+1 문제가 발생하고 있었습니다.

Fetch Join을 적용하여 불필요한 쿼리 발생을 줄였고,  
조회 구조를 개선하며 성능 문제를 해결했습니다.

---

# 📚 Currently Learning

- Spring Security 인증 / 인가 구조
- WebSocket 기반 실시간 처리
- JPA 성능 최적화
- 서비스 구조 설계
- 유지보수를 고려한 백엔드 설계

---

# 📫 Contact

- GitHub : https://github.com/Ahn0204
- Email : ahn02041@gmail.com
