<div align="center">

<!-- 움직이는 배경 패턴 -->
<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=12&height=100&section=header&animation=fadeIn" width="100%"/>

<br/>

<!-- 애니메이션 텍스트 -->
<a href="https://git.io/typing-svg">
  <img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&pause=1000&color=6C63FF&center=true&vCenter=true&width=435&lines=Full+Stack+Developer;Payment+System+Expert;Cloud+Engineering" alt="Typing SVG" />
</a>

<br/>
<br/>

<!-- 소개 문구 -->
<table>
  <tr>
    <td>
      <img src="https://media.giphy.com/media/M9gbBd9nbDrOTu1Mqx/giphy.gif" width="100"/>
    </td>
    <td>
      <p align="left">
        <strong>숲을 보는 개발자</strong><br/>
        백엔드, 클라우드, 네트워크, 프론트엔드에 이르기까지<br/>
        소프트웨어 생명주기 전체를 아우르는 경험으로<br/>
        넓은 시각으로 아키텍처를 고민하고,<br/>
        비즈니스 요구 사항에 맞추어 빠르게 방향을 제시합니다.
      </p>
    </td>
  </tr>
</table>

<br/>

<!-- 소셜 링크 with hover 효과 -->

[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:kfromh0136@gmail.com)
[![Blog](https://img.shields.io/badge/Blog-FF5722?style=for-the-badge&logo=blogger&logoColor=white)](https://jimoou.github.io/)

</div>

<br/>

<!-- 스킬 섹션 with 3D 효과 -->
<h2 align="center">
  <img src="https://media2.giphy.com/media/QssGEmpkyEOhBCb7e1/giphy.gif?cid=ecf05e47a0n3gi1bfqntqmob8g9aid1oyj2wr3ds3mg700bl&rid=giphy.gif" width="24px">
  Tech Stack
</h2>

<div align="center">

<!-- 회전하는 스킬 카드 -->
<table>
  <tr>
    <td align="center" width="120">
      <img src="https://techstack-generator.vercel.app/java-icon.svg" width="65" height="65" />
      <br><strong>Backend</strong>
    </td>
    <td align="center" width="120">
      <img src="https://techstack-generator.vercel.app/react-icon.svg" width="65" height="65" />
      <br><strong>Frontend</strong>
    </td>
  </tr>
</table>

<!-- 스킬 배지 with 애니메이션 -->
<p>
  <img src="https://img.shields.io/badge/Spring_Boot-6DB33F?style=for-the-badge&logo=spring-boot&logoColor=white" />
  <img src="https://img.shields.io/badge/Spring_Cloud-6DB33F?style=for-the-badge&logo=spring&logoColor=white" />
  <img src="https://img.shields.io/badge/Spring_Batch-6DB33F?style=for-the-badge&logo=spring&logoColor=white" />
  <img src="https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white" />
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" />
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white" />
  <img src="https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white" />
</p>

</div>

<br/>

<!-- 경력 및 프로젝트 섹션 -->
<h2 align="center">
  💼 Work Experience & Projects
</h2>

<div align="left">

### 💳 주식회사 한국결제데이터

**풀스택 개발자** | _2025.02 - Present_

<details>
<summary><b>매입 배치 아키텍처 개선</b> - 장애 격리 (기여도 100%)</summary>

- **기간**: 2025.12 - 2026.01
- **기술**: Java, MyBatis Batch, EventBus
- **문제 상황**:
  - For문 내 단건 실패 시 전체 배치가 무한 실패하는 구조
  - 2초 Interval Daemon 구조로 처리 지연 시 주기 불규칙
  - 에러 알람 부재로 장애 인지까지 시간 지연
- **해결 과정**:
  - Fail-Fast 검증 패턴으로 For문 진입 전 조기 실패 감지
  - 에러 격리 테이블과 재시도 상한(3회)으로 장애 전파 차단
  - MyBatis BATCH 모드로 대량 INSERT 성능 최적화
  - FDS를 EventBus 기반 비동기로 분리, 트랜잭션 경계 축소
- **성과**: 단건 오류가 전체에 영향 없는 구조로 개선, 장애 복구 시간 대폭 단축
- **관련글**: [크리스마스에 터진 매입 장애, 아키텍처로 해결하다](https://jimoou.github.io/backend/2025/12/29/post57.html)

</details>

<details>
<summary><b>가맹점 인증/인가 시스템 마이그레이션</b> - Spring Security 4.2.5 도입 (기여도 100%)</summary>

- **기간**: 2025.12
- **기술**: Spring Security, Session
- **문제 상황**:
  - SessionInterceptor 단일 의존, 세션 관리 DB 테이블 부재
  - 클라이언트 주도 세션 타임아웃 처리로 보안 취약
  - URL 직접 입력(Forced Browsing) 및 파라미터 변조 차단 불가
- **해결 과정**:
  - Spring Security Filter Chain 기반 인증/인가 체계로 전환
  - 커스텀 SessionFilter로 Referer 검증, Forced Browsing 차단
  - UserDetails 상속으로 레거시 JSP 세션 객체 호환 유지
  - 파일 다운로드 경로 노출 방지 (임시 토큰 방식 전환)
- **성과**: Forced Browsing/파라미터 변조 차단, 표준 인증 체계 구축, 보안취약점 점검 기준 통과
- **관련글**: [레거시 인증/인가 시스템 Spring Security 4.2.5로 마이그레이션 하기](https://jimoou.github.io/backend/2025/12/15/post49.html) | [Spring redirect와 리버스 프록시의 함정](https://jimoou.github.io/backend/2025/12/17/post51.html)

</details>

<details>
<summary><b>대용량 데이터 조회 성능 최적화</b> - N+1 쿼리 문제 해결 (기여도 100%)</summary>

- **기간**: 2025.09 - 2025.10
- **기술**: MariaDB, SQL, INDEX
- **문제 상황**:
  - 매입내역 조회 시 4만건 로딩에 30초 소요 (VIEW 남용, N+1 문제)
  - 승인내역 조회 시 4만건 로딩에 43초 소요 (JOIN 키 인덱스 부재)
- **해결 과정**:
  - VIEW 해체 후 직접 쿼리로 변경, N+1 문제를 JOIN으로 해결
  - 조인 키 컬럼에 인덱스 추가
- **성과**:
  - 매입내역 조회 30초 → 2초 (93% 단축)
  - 승인내역 조회 43초 → 4초 (91% 단축)
- **관련글**: [SQL 쿼리 튜닝으로 실적 쌓자](https://jimoou.github.io/database/2025/12/18/post53.html)

</details>

<details>
<summary><b>실시간 정산/지급대행 Batch 재설계</b> (기여도 100%)</summary>

- **기간**: 2025.08
- **기술**: Java, Thread, Daemon, MariaDB
- **문제 상황**:
  - 실시간 정산/가맹점 지급대행 Batch 모듈이 분리되어 각각 10초와 5분으로 동작
  - 분리된 동작으로 인해 가맹점 계정 계좌에 존재하는 잔액 차이로 간헐적 이체 실패 및 민원 발생
- **해결 과정**:
  - 분리된 모듈 통합작업 실행
  - Thread, Daemon으로 순차적 실행 보장
  - 레거시 시스템에서 개별 Connection을 사용한 배치작업을 통해 트랜잭션 개별 관리
- **성과**: 실시간정산/지급대행 사용시 5분 정산(실제 10~13분 뒤 지급)을 5분 정산(실제 5분 뒤 지급)으로 단축, 가맹점 민원 감소
- **관련글**: [금융 결제 시스템에서 TimeoutException 완전 정복하기](https://jimoou.github.io/backend/2025/07/29/post35.html)

</details>

<details>
<summary><b>지급대행 개발</b> (기여도 33%)</summary>

- **기간**: 2025.06 - 2025.08
- **기술**: Java, Spring MVC, 금융 VAN API
- 금융 VAN을 통한 지급대행 API 연동 개발 및 Batch 모듈 개발

</details>

<details>
<summary><b>레거시 DAO의 트랜잭션 문제 해결</b> (기여도 100%)</summary>

- **기간**: 2025.06
- **기술**: Java, Spring Transaction Manager, JdbcTemplate, ThreadLocal, HikariCP
- **문제 상황**:
  - 지급대행 서비스 신규 개발시 입출금 내역과 잔액 업데이트 시 트랜잭션 미보장으로 금액 불일치 위험
  - 디컴파일된 레거시 DAO 라이브러리가 Auto Commit 모드로 작동하여 부분 실패 시 롤백 불가능
  - 레거시 DAO의 Statement 사용 및 문자열 결합 방식의 보안 취약점 확인
- **해결 과정**:
  - 디컴파일을 통한 레거시 라이브러리 동작 원리 분석
  - 리플렉션으로 레거시 HikariDataSource 획득, 이중 커넥션 풀 방지
  - JdbcTemplate + TransactionTemplate 기반 Wrapper 클래스 설계
  - NamedParameterJdbcTemplate으로 파라미터 바인딩 방식 전환
- **성과**: 신규 DAO로 교체를 통해 금융 거래 원자성 확보 및 SQL Injection 취약점 제거
- **관련글**: [레거시 DAO의 트랜잭션 문제, JdbcTemplate Wrapper로 해결하기](https://jimoou.github.io/backend/2025/12/19/post54.html)

</details>

<details>
<summary><b>차액정산 시스템 현대화</b> - Spring Batch 기반 재설계 (기여도 100%)</summary>

- **기간**: 2025.05
- **기술**: Spring Batch, Quartz, Java, MySQL
- **문제 상황**:
  - R-JAVA/쉘스크립트/크론탭으로 운영되던 레거시 시스템의 불안정성
  - PG사별 상이한 가이드라인으로 인한 코드 중복 및 개별 결과 테이블 관리
  - 신규 PG사 추가 시 차액정산 과정 전체 코드 재작성 필요로 테스트 포함 3주의 개발 기간 소요
- **해결 과정**:
  - Spring Batch 기반 모듈형 아키텍처로 전면 재설계
  - 데이터 세팅, 파일 생성, 업로드, 주기적 결과 수신, 데이터 업데이트를 독립적인 Task로 분리
  - PG사별 인터페이스 추상화로 PG사 추가 시 기존 Task 수정 없이 구현체만 추가하는 구조 확립
  - PG사별 결과 테이블을 통합 테이블로 일원화
- **성과**: PG사 추가 소요 시간 3주 → 1일 (95% 단축, 테스트 기간 제외), 아웃소싱 비용 절감
- **관련글**: [Spring Batch ExecutionContext 저장 오류 해결기](https://jimoou.github.io/java/2025/06/30/post34.html) | [배치 작업의 불편한 진실](https://jimoou.github.io/java/2025/08/06/post37.html)

</details>

<details>
<summary><b>정산대사 API 개발</b> (기여도 100%)</summary>

- **기간**: 2025.05
- **기술**: Java, Spring MVC, REST API
- 단독 정산대사 API 기능 개발 및 가이드 작성, 배포, 문의 응대

</details>

---

### 💰 워너페이먼츠(주)

**풀스택 개발자** | _2024.04 - 2025.02_

<details>
<summary><b>정산 시스템 재구축</b> - PHP에서 Spring Boot로 마이그레이션</summary>

- **기간**: 2024.04 - 2024.10
- **기술**: Spring Boot, JSP, jQuery, MySQL, AWS

</details>

---

### 🎥 제노소프트(주)

**네트워크/시스템 엔지니어** | _2023.11 - 2024.01_

- 고객사 기술 지원 및 네트워크 환경 구축
- VPN, 방화벽 설정 등 네트워크 보안 구현
- Windows 및 Linux 기반 시스템 유지보수

</div>

<br/>

<!-- 개인 프로젝트 섹션 -->
<h2 align="center">
  📚 Personal Projects
</h2>

<div align="left">

### ArteModerni

**MSA 미술품 경매거래 플랫폼** | _2023.08 - 2023.09_

- **기술 스택**: Spring Boot, Spring Cloud, Kafka, AWS, Firebase
- **주요 기능**:
  - Microservices Architecture 설계 및 구현
  - Kafka를 활용한 이벤트 기반 통신
  - 실시간 경매 시스템 구현
- **링크**: [GitHub](https://github.com/wooriFisa-Final-Project-F4) | [YouTube](https://youtu.be/q5TcMswiwkA?si=Q6hmtbj7NC_NVrJN)

</div>

<br/>

<!-- 교육 섹션 -->
<h2 align="center">
  🎓 Education & Certification
</h2>

<div align="left">

### 📚 Boot Camp

- **TOSS Learner's High 2기** (2025.12.16 ~ 2026.01.16)

- **WOORI FIS ACADEMY 1기 Cloud Engineering** (2023.04 - 2023.09)
  - 핀테크 IT 인재 양성 교육 과정
  - 우리 FIS 현직자 강의를 통한 금융 도메인 기술 이해
- **UDEMY X STARTERS 3기 Backend** (2022.11 - 2023.03)
  - 클라우드 기반 백엔드 개발자 양성 교육
  - 실무자와의 면접 및 코딩테스트 경험

### 🏆 Certification

- **리눅스 마스터 2급** (2023.06.30)

### 🤝 Mentoring

- **SIAT Mate 온라인 튜터** (2023.11 - 2023.12)
  - SK C&C X 행복한 학교재단
  - IT 진로 희망 청년장애인 대학생 Java 멘토링

</div>

<br/>

<!-- 방문자 수 카운터 -->
<div align="center">
  
![](https://komarev.com/ghpvc/?username=Jimoou&color=blueviolet)

</div>

<div align="center">
  <i>항상 새로운 기술을 배우고 성장하는 개발자가 되겠습니다.</i>
</div>

<!-- 움직이는 푸터 -->
<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=12&height=100&section=footer&animation=fadeIn" width="100%"/>
