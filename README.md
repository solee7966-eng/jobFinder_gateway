# Gateway Service

## 소개

본 서비스는 JobFinder 프로젝트의 API Gateway 역할을 담당합니다.
외부 요청을 각 서비스(user-service, board-service)로 라우팅하는 기능을 수행합니다.

---

## 역할

* 클라이언트 요청을 각 서비스로 전달
* 서비스 경로 기반 라우팅 처리
* Eureka를 통한 서비스 탐색

---

## 접근 경로

```text
http://jobfinder-antaehoon.kro.kr/*
```

예시:

```text
http://jobfinder-antaehoon.kro.kr/user-service/*
http://jobfinder-antaehoon.kro.kr/board-service/*
```

---

## 실행 방법

### 환경 변수 설정

```bash
EUREKA_DEFAULT_ZONE=http://localhost:8761/eureka
```

---

## 참고

* 본 서비스는 MSA 구조에서 라우팅을 담당하는 서비스입니다.
* 실제 비즈니스 로직은 각 서비스에서 처리됩니다.
