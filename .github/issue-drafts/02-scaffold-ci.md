## 목표

팀원 누구나 clone 후 바로 실행·테스트할 수 있는 환경을 만든다.

## 할 일

- [ ] npm workspaces로 api/(Express+SQLite), web/(React+TS+Vite) 뼈대
- [ ] `npm run dev`로 API와 화면 동시 실행, /api 프록시
- [ ] CLAUDE.md에 구조·명령어·GitHub 규칙 작성
- [ ] .claude/skills, .claude/agents 추가
- [ ] .github/workflows/test.yml (PR마다 npm test)
- [ ] .github/ISSUE_TEMPLATE/feature.md

## 완료 조건

- clone → npm install → npm run dev가 동작함
- 첫 PR에서 Actions test가 통과함
- main 브랜치 보호 규칙 설정됨

## 선행 이슈

- #1
