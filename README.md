<div align="center">

# 김민준 | Backend Developer

<a href="mailto:alswns5620@naver.com"><img src="https://img.shields.io/badge/Email-alswns5620%40naver.com-03C75A?style=for-the-badge&logo=naver&logoColor=white" alt="Email" /></a>
<a href="https://minjoon.me"><img src="https://img.shields.io/badge/Portfolio-minjoon.me-2563EB?style=for-the-badge&logo=googlechrome&logoColor=white" alt="Portfolio" /></a>
<a href="https://github.com/UncleSamsun"><img src="https://img.shields.io/badge/GitHub-UncleSamsun-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub" /></a>

<br />
<br />

<a href="https://git.io/typing-svg">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&duration=2600&pause=900&color=2563EB&center=true&vCenter=true&width=760&lines=Backend+Developer;AI+%C2%B7+Data+%C2%B7+Performance+Flows;Spring+Backend+%2B+Async+Pipelines" alt="Typing SVG" />
</a>

<p>
  AI 기능, 데이터 파이프라인, 추천/검색/성능 병목을<br />
  <strong>백엔드 계약과 운영 흐름으로 연결하는 개발자</strong>
</p>

</div>

---

## Focus

| I care about | How it shows up |
|---|---|
| AI pipeline as a service contract | Spring callback/SSE, Python worker, GCS upload, Redis Streams |
| Data flow quality | 수집, 정제, 저장 구조, 검색/추천 입력 데이터 검증 |
| Performance evidence | k6, JMeter, EXPLAIN ANALYZE, p95, 재측정 가능한 결과 |
| Reliable delivery | 테스트, 문서화, 에러/응답 표준화, 운영 경계 분리 |

## Tech Stack

### Core Backend

<p align="center">
  <a href="https://skillicons.dev">
    <img src="https://skillicons.dev/icons?i=java,spring,hibernate,maven,gradle&theme=light" alt="Core backend stack" />
  </a>
</p>

### Data, Cache, Search

<p align="center">
  <a href="https://skillicons.dev">
    <img src="https://skillicons.dev/icons?i=postgres,mysql,redis,elasticsearch&theme=light" alt="Data stack" />
  </a>
</p>

### AI, Infra, Tooling

<p align="center">
  <a href="https://skillicons.dev">
    <img src="https://skillicons.dev/icons?i=python,fastapi,opencv,docker,aws,gcp,githubactions,linux&theme=light&perline=8" alt="AI and infra stack" />
  </a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/MyBatis-SQL%20control-334155?style=flat-square" alt="MyBatis" />
  <img src="https://img.shields.io/badge/pgvector-vector%20search-4169E1?style=flat-square" alt="pgvector" />
  <img src="https://img.shields.io/badge/Redis%20Streams-async%20jobs-DC382D?style=flat-square&logo=redis&logoColor=white" alt="Redis Streams" />
  <img src="https://img.shields.io/badge/SSE-progress%20stream-2563EB?style=flat-square" alt="SSE" />
  <img src="https://img.shields.io/badge/GCS-Signed%20URL-4285F4?style=flat-square&logo=googlecloud&logoColor=white" alt="GCS Signed URL" />
  <img src="https://img.shields.io/badge/Testcontainers-integration%20test-2496ED?style=flat-square&logo=docker&logoColor=white" alt="Testcontainers" />
  <img src="https://img.shields.io/badge/k6-load%20test-7D64FF?style=flat-square&logo=k6&logoColor=white" alt="k6" />
  <img src="https://img.shields.io/badge/JMeter-performance-D22128?style=flat-square&logo=apache&logoColor=white" alt="JMeter" />
</p>

## Project Proof

<table>
  <tr>
    <td width="50%" valign="top">
      <h3><a href="https://minjoon.me/projects/hola-climbing/">Hola Climbing</a></h3>
      <p><strong>AI Climbing SNS</strong></p>
      <p>2인 팀. Spring Boot 백엔드와 Python AI worker pipeline 전담.</p>
      <ul>
        <li>GCS Signed URL로 대용량 영상 업로드 분리</li>
        <li>Redis Streams + Pub/Sub + SSE로 AI 분석 흐름 분리</li>
        <li>PostgreSQL + pgvector 추천 피드, Redis snapshot cursor 적용</li>
        <li>추천 피드 HTTP p95 <code>251.233ms -> 122.642ms</code></li>
        <li>cursor aggregate p95 <code>9.794ms</code></li>
      </ul>
      <p>
        <a href="https://hola-climb.app"><img src="https://img.shields.io/badge/Live-Service-16A34A?style=flat-square" alt="Live Service" /></a>
        <a href="https://github.com/UncleSamsun/hola-climbing-server"><img src="https://img.shields.io/badge/Backend-GitHub-181717?style=flat-square&logo=github" alt="Backend GitHub" /></a>
        <a href="https://github.com/UncleSamsun/hola-climbing-ai"><img src="https://img.shields.io/badge/AI-GitHub-181717?style=flat-square&logo=github" alt="AI GitHub" /></a>
      </p>
    </td>
    <td width="50%" valign="top">
      <h3><a href="https://minjoon.me/projects/cafe-gamsugwang/">카페감수광</a></h3>
      <p><strong>Data Recommendation Pipeline</strong></p>
      <p>제주 카페 리뷰와 위치 데이터를 추천 가능한 형태로 수집·정제.</p>
      <ul>
        <li>Kakao Map 제한 대응: 200m grid + GeoJSON 육지 필터</li>
        <li>검색 좌표 <code>47,190개</code>, 카페 <code>3,950개</code></li>
        <li>리뷰 <code>22,144개</code> 기반 키워드 추출</li>
        <li>원천 키워드 <code>80,601개 -> 30,336개</code> 정제</li>
        <li>FastAPI 데이터 처리 서버와 Spring Boot 서비스 서버 분리</li>
      </ul>
      <p>
        <a href="https://github.com/UncleSamsun/cafe-gamsugwang-be"><img src="https://img.shields.io/badge/Backend-GitHub-181717?style=flat-square&logo=github" alt="Backend GitHub" /></a>
        <a href="https://github.com/UncleSamsun/cafe-gamsugwang-crawling"><img src="https://img.shields.io/badge/Crawler-GitHub-181717?style=flat-square&logo=github" alt="Crawler GitHub" /></a>
      </p>
    </td>
  </tr>
  <tr>
    <td width="50%" valign="top">
      <h3><a href="https://minjoon.me/projects/the-last-supper/">The Last Supper</a></h3>
      <p><strong>Waiting & Reservation</strong></p>
      <p>현장 웨이팅 부하를 재현하고 Redis 기반 동시성 제어로 개선.</p>
      <ul>
        <li>500명/1초 웨이팅 등록 spike를 JMeter로 재현</li>
        <li>Redis atomic + queue + async 처리 적용</li>
        <li>max response <code>233ms -> 7ms</code></li>
        <li>시나리오별 평균 응답 시간 <code>40.9%~47.8%</code> 감소</li>
        <li>Spring Batch로 운영 종료 후 웨이팅 이력 처리 분리</li>
      </ul>
      <p>
        <a href="https://github.com/UncleSamsun/The-Last-Supper"><img src="https://img.shields.io/badge/Backend-GitHub-181717?style=flat-square&logo=github" alt="Backend GitHub" /></a>
        <a href="https://github.com/UncleSamsun/The-Last-Supper-Front"><img src="https://img.shields.io/badge/Frontend-GitHub-181717?style=flat-square&logo=github" alt="Frontend GitHub" /></a>
      </p>
    </td>
    <td width="50%" valign="top">
      <h3>More Work</h3>
      <p><strong>ReadAndShare</strong></p>
      <ul>
        <li>이메일 인증, BCrypt, 사용자 검색/탈퇴</li>
        <li>member 도메인 중심 테스트 보강</li>
      </ul>
      <p><strong>JsonStore</strong></p>
      <ul>
        <li>고객/관리자 JWT 경계, Redis cart, FCM 알림</li>
        <li>주문·재고 테스트와 권한 흐름 분석</li>
      </ul>
      <p><strong>DevKnowledge</strong></p>
      <ul>
        <li>Obsidian vault, Graphify, global AI rules, project watcher</li>
      </ul>
      <p>
        <a href="https://github.com/UncleSamsun/read-and-share"><img src="https://img.shields.io/badge/ReadAndShare-GitHub-181717?style=flat-square&logo=github" alt="ReadAndShare GitHub" /></a>
        <a href="https://github.com/UncleSamsun/json-store-be"><img src="https://img.shields.io/badge/JsonStore-GitHub-181717?style=flat-square&logo=github" alt="JsonStore GitHub" /></a>
      </p>
    </td>
  </tr>
</table>

## Background

| Experience | Notes |
|---|---|
| SSAFY Java Web Track | Hola Climbing 발표 완료 후 개인 고도화 중 |
| Kakao x goorm Deep Dive | Java/Spring Boot 백엔드 과정 |
| Railway signal system | SIL4 인증 문서, VectorCAST/Code Inspector, HW 연동 검증 |
| Internal product app | Xamarin 창고 자재관리 앱 단독 개발, 현장 실사용 경험 |

## GitHub Stats

<div align="center">

<img height="165" src="https://github-readme-stats-sigma-five.vercel.app/api?username=UncleSamsun&show_icons=true&theme=tokyonight&hide_border=true" alt="GitHub Stats" />
<img height="165" src="https://github-readme-stats-sigma-five.vercel.app/api/top-langs/?username=UncleSamsun&layout=compact&theme=tokyonight&hide_border=true" alt="Top Languages" />

<br />
<br />

[![Solved.ac Profile](http://mazassumnida.wtf/api/v2/generate_badge?boj=minjoun5620)](https://solved.ac/minjoun5620/)

<br />
<br />

![Profile Views](https://komarev.com/ghpvc/?username=UncleSamsun&label=Profile+Views&color=2563EB&style=flat-square)

</div>
