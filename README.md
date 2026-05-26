# WBS

간트 차트 기반의 프로젝트 일정 관리 도구. 다수 참여 프로젝트에서 업무를 Level 1~4로 분해하고
RFP 번호·담당자·산출물·상태·일정을 한 화면에서 관리합니다.

브라우저에서 단독 실행되는 정적 SPA — 별도 백엔드/설치 없이 `index.html`을 열거나 정적 서버로
호스팅하면 됩니다. 데이터는 `localStorage`에 저장되고 JSON/Excel로 import·export 가능합니다.

## 1차 기능

- **Level 1~4 계층 업무 분해** — 행마다 레벨 뱃지, 인덴트, 펼치기/접기.
- **컬럼**: 업무명 · RFP No. · 담당자 · 산출물 · 상태 · 시작일 · 완료일.
- **상태**: 대기 · 진행중 · 완료 · 차단 · 보류 (5종).
- **간트 차트**: 시작일·완료일 기준 막대, 상태별 색상, 오늘 라인, 주말 음영.
- **부모 자동 집계**: 일정 없는 상위 업무는 자손 일정의 min/max로 자동 산정.
- **Import / Export**: JSON (전체 복원) · Excel (xlsx, 한 화면 데이터).
- **무빌드**: 단일 HTML, vanilla JS, fc-ui Glass 테마 사용.

## 추후 계획 (collaboration)

- 실시간 동시 편집·코멘트
- 의존성(predecessor) 표시
- 마일스톤·진행률 입력
- 멤버 권한 관리

## 실행

```bash
# 가장 간단:
open index.html
# 정적 서버:
python3 -m http.server 8000
```

## 라이선스

[LICENSE](./LICENSE)
