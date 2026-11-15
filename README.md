
# 👋 안녕하세요, 손예빈입니다!

Java와 Spring Boot를 중심으로 백엔드 개발을 공부하고 있습니다.

사람과 시스템, 둘 다 고민하는 개발자가 되고 싶습니다.

특히 **동시성 제어, 데이터 정합성, 실패 상황을 고려한 설계와 검증**에 관심을 두고 있습니다.

## 🛠 Tech Stack

### Backend
`Java` `Spring Boot` `Spring Data JPA` `Spring Security` `JWT`

### Database
`MySQL` `MariaDB` `Flyway`

### Testing & Tools
`JUnit` `Vitest` `Playwright` `Git` `GitHub Actions`

### Frontend
`JavaScript` `React` `HTML` `CSS`

### Previous Project Experience
`PHP` `Apache` `jQuery` `Android (Java/XML)`

---

## 🚀 Featured Project

### 🎨 DailyAtelier — 미술품 경매·거래 웹 서비스

**개인 프로젝트 | 2026.03 ~ 현재**

`Java 17` `Spring Boot` `JPA` `MySQL` `Flyway` `React`

**동시 입찰과 경매 마감의 경합, 포인트 거래의 정합성, 외부 리소스 처리 실패를 고려해 설계한 웹 서비스입니다.**

2023년 팀 졸업작품을 Spring Boot와 React 기반으로 재설계·재구현했습니다.

신진·개인 작가의 작품 등록부터 구매자의 입찰, 낙찰, 주문, 내부 포인트 결제, 배송, 환불까지 이어지는 거래 흐름을 구현했습니다.

**주요 기술 경험**

- **동시성 제어** — 동일 작품의 입찰과 자동 마감이 충돌할 때 현재가·예치금·낙찰 결과의 불일치를 방지하도록 비관적 락과 트랜잭션 적용
- **거래 정합성** — 포인트 변경 근거를 추적하고 중복 반영을 방지하기 위해 불변 원장, 예치 관리 및 멱등성 키 설계
- **외부 리소스 관리** — DB 트랜잭션으로 외부 이미지 삭제까지 보장할 수 없는 문제를 Cleanup Outbox와 재시도 Worker로 처리
- **인증·인가** — JWT `authVersion` 및 현재 DB 권한 재검증으로 비밀번호·권한 변경 전 토큰 무효화

**테스트 및 검증**

- **동시 입찰 테스트** — 16개 계정·4개 작품에 동시 요청을 발생시켜 입찰 결과와 계정별 잔액·예치금 및 원장 합계의 일치 여부 검증
- **MySQL 검증** — 실제 MySQL 환경에서 락·제약 조건을 별도로 검증하고, 빈 DB에 Flyway V1~V11 적용 및 스키마 검증
- **자동화** — JUnit, Vitest, GitHub Actions, Playwright를 활용한 백엔드·프론트엔드·UI 테스트 구성
- **부하 관찰** — k6로 입찰 경합을 재현하고 커넥션 풀 크기 10·20·30을 비교. 처리량과 상위 백분위 응답 시간의 일관된 개선이 없어 기본값 10 유지

**현재 개선 작업**

- **진행 중** — 서비스 전반의 UI/UX 개선 및 반응형 화면 정비
- **후속 검토** — MySQL 입찰 조회 인덱스 및 배포 환경의 동시성·락 타임아웃 검증

**Links**

[💻 Source Code (dev)](https://github.com/handbinu/dailyatelier/tree/dev) · [🌐 Live Demo](https://dailyatelier-frontend.canflerang.workers.dev/) · [📖 Technical Documentation](https://github.com/handbinu/dailyatelier/blob/dev/docs/TECHNICAL.md)

> 내부 데모 포인트 기반 서비스로, 실제 외부 PG 결제는 연동하지 않았습니다.

---

## 📁 Previous Projects

### 🎨 DailyAtelier (2023) — 미술품 경매 웹 서비스

**5인 팀 졸업작품 | 팀장/PM · 프론트엔드·백엔드 개발 참여**

`PHP` `Apache` `MySQL/MariaDB` `HTML` `CSS` `JavaScript` `jQuery`

신인·개인 작가의 미술품 경매 접근성을 높이기 위해 개발한 웹 서비스입니다.

- **Backend** — PHP 기반 회원·입찰 기능 구현, 세션 관리 및 작품 등록·이미지 업로드 기능 개발 참여
- **Database** — ERD 설계 및 데이터베이스 관계 수정 참여
- **Frontend** — 일부 화면의 HTML/CSS 구현 및 디자인 참여
- **PM** — 개발 일정·역할 조율, 주간 회의 및 Trello 기반 이슈 관리

졸업작품 전시회에서 서비스를 시연하고 사용자 피드백을 수집했습니다.

[📂 GitHub Repository](https://github.com/5HapZizol/daliy-Atelier)

### 📱 PASTIME (HOBBING) — 취미 공유 익명 SNS

**대학 동아리 6인 팀 프로젝트 | 기획 · 디자인 · Android 개발 참여**

`Java 8` `Android SDK` `XML` `Git/GitHub`

사용자가 관심 분야의 게시물을 탐색하고 취미 활동을 공유할 수 있도록 기획한 Android SNS 앱입니다.

- **Android UI** — 로그인·회원가입 화면의 XML 레이아웃과 이미지 리소스 구현·수정
- **UI 구현** — 공지사항·이용약관·버전 정보·문의 화면 레이아웃 및 Java `Spinner` 기반 문의 유형 선택 UI
- **기획·디자인** — 화면 흐름도, 목업, 스토리보드 제작 참여
- **협업** — Trello·Google Sheets·Git 기반 일정 관리 및 팀 협업

[📑 Project Presentation](https://docs.google.com/presentation/d/1pTmV3WmSf7BhavLK7TAbHFKkmju1B5c1xP_imB63quA/edit)

---

## 🧩 Algorithm & Problem Solving

Java를 중심으로 자료구조와 알고리즘 문제를 풀이하고 있습니다.

| 플랫폼 | 풀이 범위 | 바로가기 |
| --- | --- | --- |
| Programmers | Lv.0 ~ Lv.3 | [프로그래머스 풀이](https://github.com/handbinu/algorithms/tree/main/프로그래머스) |
| Baekjoon | Bronze ~ Gold | [백준 풀이](https://github.com/handbinu/algorithms/tree/main/백준) |
| SWEA | D2 ~ D3 | [SWEA 풀이](https://github.com/handbinu/algorithms/tree/main/SWEA) |

정렬, 해시, 스택/큐, 완전탐색, DFS·백트래킹 등을 학습하고 있습니다.

[📂 알고리즘 풀이 저장소](https://github.com/handbinu/algorithms)

### 📊 Baekjoon / Solved.ac

[![Solved.ac Profile](https://mazassumnida.wtf/api/generate_badge?boj=canflerang)](https://solved.ac/canflerang)

[🔗 Solved.ac 프로필](https://solved.ac/canflerang)

---

## 📫 Contact

**Email:** [canflerang@naver.com](mailto:canflerang@naver.com)
