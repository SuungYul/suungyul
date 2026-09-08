<h1 align="center">안녕하세요, 박성열입니다.</h1>

<p align="center"><b>Backend × Data, end to end.</b></p>

<p align="center">
제약·헬스케어 <b>B2B 제품 2개</b>의 DB·API·데이터 파이프라인·인프라를 설계하고 운영하는 백엔드·데이터 엔지니어입니다.<br/>
문제를 정의하고 대안을 비교한 뒤, 데이터가 들어오는 지점부터 제품에 전달되는 화면까지 책임지며 결과와 트레이드오프를 운영 데이터로 검증합니다.
</p>

<p align="center">
  <a href="https://suungyul.github.io/suungyul/"><img src="https://img.shields.io/badge/Portfolio-0FA968?style=for-the-badge&logo=googlechrome&logoColor=white" alt="Portfolio"/></a>
  <a href="mailto:pmtf00@gmail.com"><img src="https://img.shields.io/badge/Gmail-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"/></a>
</p>

---

### About Me

- GC(녹십자홀딩스) 재직 1년 5개월(2025.04~2026.09). 모바일 앱 개발로 합류해 정규직 전환 후 백엔드·데이터·인프라를 전담합니다.
- 개발 1명(본인)·PM 1명·디자인 1명으로 병원 약 8만 곳·진단검사 1,310만 행을 다루는 제품을 운영합니다.
- 구조가 없던 FastAPI 서버와 불안정한 데이터 배치를 레이어드 아키텍처와 Airflow 기반으로 재구축했습니다.
- 아키텍처와 우선순위는 직접 판단하고, Claude·Codex는 구현과 검증을 가속하는 도구로 활용합니다.
- 연락: **pmtf00@gmail.com**

### What I've Built

- **백엔드 성능 엔지니어링** — 약 8만 병원의 데이터를 제공하는 CRM에서 인수한 레거시 API 최대 6분 → 개선 후 0.2초, 병원 상세 조회 92초 → 0.3초
- **병원 고객군·추가 제안 목록** — 운영 사용자 26명이 사용하는 서비스에서 거래의 최근성·빈도·금액으로 병원 고객군을 나누고, 함께 팔리는 제품을 캠페인 조건으로 연결
- **진단검사 사업부 확장** — 매출 데이터가 없는 사업부에 검사 건수 기준을 적용하고 1,310만 행의 월별 증분 적재 구성
- **병원 업로드 매칭** — 병원 마스터 8만 건·62행 업로드 기준 150초 → 7초, NDJSON 스트리밍 진행률, PII 스캔·차단 적용
- **병원 CRM 데이터 정합성 개선** — 행정구역 개편에 따른 코드 연결 단절을 보정해 누락 병원 약 1,900건 복구
- **개원예정 탐지 파이프라인** — 채용 플랫폼 6곳 수집·OCR·LLM 판정. 86분 → 13분, 외주비 연 1,200만 원 대체. 2025.09 이후 개원분 커버리지 71.3%, 평균 64일 선탐지
- **인프라 현대화** — 사내 최초 GitLab CI/CD 도입, AWS EC2 ARM·RDS Blue/Green 무중단 이관

### Representative Decision

- **문제 정의** — 병원 마스터 8만 건과 62행 업로드를 비교하는 데 150초가 걸려 60초 게이트웨이 제한을 넘었고, 사용자는 정상 처리 중인 작업도 실패로 인식했습니다.
- **의사결정** — 타임아웃만 늘리지 않고 ID 인덱스·지역 선분할로 매칭 비용을 먼저 줄인 뒤, NDJSON 스트리밍으로 실제 진행률을 전달했습니다.
- **결과** — 자동매핑을 150초 → 7초(62행 기준)로 단축하고, 더 긴 작업도 진행 상태를 확인하며 완료할 수 있게 했습니다.
- **트레이드오프** — 프론트 스트림 파싱과 미들웨어 처리가 복잡해지는 대신, 스트리밍 응답에만 압축을 우회하고 기존 동기 API를 fallback으로 유지해 변경 범위를 제한했습니다.

### Tech Stack

**Data Engineering**

![Airflow](https://img.shields.io/badge/Airflow-017CEE?style=flat-square&logo=apacheairflow&logoColor=white)
![Snowflake](https://img.shields.io/badge/Snowflake-29B5E8?style=flat-square&logo=snowflake&logoColor=white)
![MariaDB](https://img.shields.io/badge/MariaDB-003545?style=flat-square&logo=mariadb&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white)

**Backend**

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)

**Data Analysis**

![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat-square&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat-square&logo=numpy&logoColor=white)

**Infra / DevOps**

![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazonwebservices&logoColor=white)
![GitLab CI](https://img.shields.io/badge/GitLab%20CI-FC6D26?style=flat-square&logo=gitlab&logoColor=white)
![Nginx](https://img.shields.io/badge/Nginx-009639?style=flat-square&logo=nginx&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)

**Product Clients**

![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Flutter](https://img.shields.io/badge/Flutter-02569B?style=flat-square&logo=flutter&logoColor=white)
![Dart](https://img.shields.io/badge/Dart-0175C2?style=flat-square&logo=dart&logoColor=white)

### Certifications & Awards

- 정보처리기사 · SQLD (2024)
- 캡스톤디자인 경진대회 금상 (2024) · 육군 참모총장 표창 (사이버, 2021)

### GitHub Stats

<p align="center">
  <img height="165" src="https://github-readme-stats.vercel.app/api?username=SuungYul&show_icons=true&hide_border=true&theme=vue" alt="stats"/>
  <img height="165" src="https://github-readme-stats.vercel.app/api/top-langs/?username=SuungYul&layout=compact&hide_border=true&theme=vue" alt="top languages"/>
</p>
