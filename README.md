<div align="center">

# 김민준 | Backend Developer

### AI, data, and performance flows connected through Spring backend systems

Java/Spring Boot 기반으로 API 계약, 비동기 처리, 데이터 흐름, 성능 검증까지 연결하는 백엔드 개발자입니다.

철도 신호장치 SIL4 인증 프로젝트에서 익힌 검증 습관을 바탕으로, 서비스 코드에서도 실패 가능성·운영 흐름·근거 있는 개선을 먼저 봅니다.

[![Email](https://img.shields.io/badge/Email-alswns5620%40naver.com-03C75A?style=flat-square&logo=naver&logoColor=white)](mailto:alswns5620@naver.com)
[![Portfolio](https://img.shields.io/badge/Portfolio-minjoon.me-2563EB?style=flat-square&logo=googlechrome&logoColor=white)](https://minjoon.me)
[![GitHub](https://img.shields.io/badge/GitHub-UncleSamsun-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/UncleSamsun)

</div>

---

## Positioning

> AI 기능, 데이터 파이프라인, 추천/검색/성능 병목을 백엔드 계약과 운영 흐름으로 연결하는 개발자.

- Spring Boot 백엔드에서 인증, API 계약, DB, Redis, 외부 스토리지, 테스트를 한 흐름으로 설계합니다.
- Python AI worker, GCS Signed URL, Redis Streams/SSE처럼 런타임이 다른 구성요소의 경계를 명확히 나눕니다.
- "개선했다"보다 `k6`, `JMeter`, `EXPLAIN ANALYZE`, 테스트 결과처럼 다시 확인 가능한 근거를 남깁니다.
- AI 도구를 단순 코드 생성이 아니라 기획, 설계 검토, 품질 기준, 문서화 워크플로에 통합해 사용합니다.

## Tech Stack

| Area | Stack |
|---|---|
| Backend | `Java 17/25`, `Spring Boot 3/4`, `Spring Security`, `Spring Batch`, `WebSocket/STOMP` |
| Data | `PostgreSQL`, `pgvector`, `MySQL`, `MyBatis`, `JPA`, `Querydsl`, `Elasticsearch` |
| Async / Infra | `Redis Streams`, `Redis Pub/Sub`, `SSE`, `Docker`, `GCS Signed URL`, `AWS S3` |
| AI / Data Pipeline | `Python`, `FastAPI`, `MediaPipe Pose`, `OpenCV`, `KR-SBERT`, `TF-IDF`, `Selenium` |
| Test / Observability | `JUnit 5`, `Mockito`, `Testcontainers`, `pytest`, `k6`, `JMeter`, `Prometheus`, `Grafana`, `Swagger` |

## Featured Projects

### [Hola Climbing](https://minjoon.me/projects/hola-climbing/) | AI Climbing SNS

2인 팀 프로젝트. 백엔드와 AI 파이프라인을 전담했습니다.

클라이밍 영상을 업로드하면 AI가 동작 기술과 dynamic/static 성향을 분석하고, SNS 피드·암장·기록·월간 리포트로 연결하는 서비스입니다.

- `GCS v4 Signed URL`로 대용량 영상 업로드를 WAS에서 분리
- `Redis Streams + Pub/Sub + SSE`로 AI 분석 요청, 진행률, callback 저장 흐름 분리
- `PostgreSQL + pgvector` 기반 추천 피드와 `Redis snapshot cursor` 적용
- 로컬 성능 검증 기준 추천 피드 HTTP p95 `251.233ms -> 122.642ms`, cursor aggregate p95 `9.794ms`
- Tech: `Java 25`, `Spring Boot 4`, `MyBatis`, `PostgreSQL`, `pgvector`, `Redis`, `GCS`, `Python`, `FastAPI`, `MediaPipe`

[Live Service](https://hola-climb.app) · [Portfolio Detail](https://minjoon.me/projects/hola-climbing/)

### [카페감수광](https://minjoon.me/projects/cafe-gamsugwang/) | Data Recommendation Pipeline

제주 카페 리뷰와 위치 데이터를 수집·정제해 취향 기반 추천으로 연결한 프로젝트입니다.

데이터 수집, 전처리, 키워드 정제, 추천 API 흐름을 담당했습니다.

- Kakao Map API 응답 제한 대응: 200m 격자 + GeoJSON 육지 필터링으로 검색 좌표 `47,190개` 생성
- 카페 `3,950개`, 리뷰 `22,144개` 수집
- 리뷰 원천 키워드 `80,601개 -> 30,336개`로 정제
- `FastAPI` 데이터 처리 서버와 `Spring Boot` 서비스 서버 분리
- Tech: `Spring Boot`, `FastAPI`, `Redis`, `Elasticsearch`, `Selenium`, `KR-SBERT`, `TF-IDF`

[Backend](https://github.com/UncleSamsun/cafe-gamsugwang-be) · [Crawler](https://github.com/UncleSamsun/cafe-gamsugwang-crawling) · [Embedding](https://github.com/UncleSamsun/cafe-gamsugwang-embedding)

### [The Last Supper](https://minjoon.me/projects/the-last-supper/) | Waiting & Reservation

식당 예약과 현장 웨이팅을 함께 관리하는 서비스입니다.

웨이팅 파트와 JMeter 부하 검증을 중심으로 Redis 기반 동시성 제어와 운영 지표를 다뤘습니다.

- 500명/1초 웨이팅 등록 spike를 JMeter로 재현
- `Redis atomic + queue + async` 처리로 max response `233ms -> 7ms`
- Redis 적용 후 시나리오별 평균 응답 시간 `40.9%~47.8%` 감소
- `Spring Batch`로 운영 종료 후 웨이팅 이력 처리 흐름 분리
- Tech: `Spring Boot`, `JPA`, `Redis`, `MySQL`, `Spring Batch`, `JMeter`, `Prometheus`, `Grafana`

[Backend](https://github.com/UncleSamsun/The-Last-Supper) · [Frontend](https://github.com/UncleSamsun/The-Last-Supper-Front)

## More Work

| Project | Focus | Link |
|---|---|---|
| ReadAndShare | 이메일 인증, BCrypt, 사용자 검색/탈퇴, member 도메인 테스트 보강 | [GitHub](https://github.com/UncleSamsun/read-and-share) |
| JsonStore | 고객/관리자 JWT 경계, Redis cart, FCM 알림, 주문·재고 테스트 | [Backend](https://github.com/UncleSamsun/json-store-be) / [Frontend](https://github.com/UncleSamsun/json-store-fe) |
| DevKnowledge | Obsidian vault, Graphify, global AI rules, project watcher 기반 AI memory system | Private |

## Background

- SSAFY Java Web Track, 자율 프로젝트 Hola Climbing 발표 완료 후 개인 고도화 중
- Kakao x goorm 구름톤 딥다이브 백엔드 과정 수료
- 철도 신호장치 개발 경력: SIL4 인증 문서, VectorCAST/Code Inspector 기반 테스트, HW 연동 검증
- 사내 공모전: Xamarin 기반 창고 자재관리 앱 단독 개발, 현장 실사용 경험

## GitHub Stats

<div align="center">

![GitHub Stats](https://github-readme-stats-sigma-five.vercel.app/api?username=UncleSamsun&show_icons=true&theme=tokyonight)

[![Solved.ac Profile](http://mazassumnida.wtf/api/v2/generate_badge?boj=minjoun5620)](https://solved.ac/minjoun5620/)

![Profile Views](https://komarev.com/ghpvc/?username=UncleSamsun&label=Profile+Views&color=blueviolet&style=flat-square)

</div>
