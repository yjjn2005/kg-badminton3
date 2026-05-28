# KG 배드민턴 PRO v3 · 스마트 매칭 시스템 (통합판)

[v1](https://yjjn2005.github.io/kg-badminton-app/)과 [v2](https://yjjn2005.github.io/kg-badminton2/) 두 앱의 강점을 통합한 KG클럽 운영용 스마트 매칭 웹앱.

라이브: <https://yjjn2005.github.io/kg-badminton3/>

## 통합한 강점

| 영역 | v1에서 | v2에서 |
|------|-------|-------|
| 매칭 | 100점 종합 점수(급수·성비·연령·게임수·대기) | 4가지 모드 토글(공정/혼복/선착순 + 스마트) |
| 코트 | 6코트(4일반 + 1난타 + 1레슨), 톱니로 타입 전환 | 가동률·진행 표시 |
| 대기 | 드래그앤드롭 Override (체크박스 4명 → 강제배정) | 분단위 추적, 10분↑ 빨강 |
| 도착 | QR 도착인증(KG3:번호), 수동 검색 입장 | — |
| 게스트 | 일일 5인 자동 차단 | — |
| 통계 | — | 가동률·TOP5·최근 100게임 로그 |
| 알림 | — | 1분전 880Hz, 종료 660Hz 비프 |
| 운용 | 회원/총무/FAQ 18스텝 가이드 | — |
| 디자인 | — | 네이비+골드 럭셔리, Pretendard, 글래스몰피즘 |

## 기술 스택

- React 18 UMD + Babel Standalone (브라우저 JSX 변환)
- Tailwind Play CDN
- QRCode.js + Html5Qrcode (QR 발급/스캔)
- localStorage 단독 동작 (키 프리픽스 `kgp3_`)
- 단일 파일 `index.html` · 빌드 없음

## 로컬 실행

```powershell
python -m http.server 8775 --directory C:/Users/user2/kg_badminton3_app
```

http://localhost:8775 접속.

## 배포

- GitHub repo: `yjjn2005/kg-badminton3`
- GitHub Actions가 `main` 푸시 시 자동 배포 (`.github/workflows/pages.yml`)

## 데이터

- KG클럽 2025-12-12 기준 119명 (남 74 · 여 45)
- 자정 지나면 대기열/코트/기록 자동 리셋 (회원 명단은 유지)
- localStorage 외 데이터 전송 없음

## 라이선스

내부 운영용. © 2026 KG 배드민턴 클럽.
