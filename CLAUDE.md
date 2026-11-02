# CLAUDE.md

## 폴더 구조

```
.
├── api/                    # 백엔드 (Express + better-sqlite3)
│   └── src/
│       ├── app.js          # Express 앱 (라우트 정의, GET /api/health 등)
│       ├── index.js        # 서버 실행 (listen)
│       └── *.test.js       # Vitest + Supertest 테스트
├── web/                    # 프론트엔드 (React + TypeScript + Vite)
│   └── src/
│       ├── App.tsx
│       ├── main.tsx
│       └── *.test.tsx      # Vitest + React Testing Library 테스트
├── docs/                   # 요구사항(requirements.md)·API 스펙(api-spec.md) 문서
├── reports/test/           # test-writer 스킬이 남기는 테스트 실행 보고서
├── .claude/
│   ├── agents/             # planner, builder, tester, reviewer
│   └── skills/             # requirements-writer, api-spec-writer, test-writer, code-review
└── .github/
    ├── workflows/          # CI (test.yml)
    └── ISSUE_TEMPLATE/     # 이슈 양식
```

api(package.json)와 web(package.json)은 루트의 npm workspaces로 묶여 있다.

## 설치 명령어

```bash
# 루트에서 한 번만 (api + web 모두 설치)
npm install
```

## 실행 명령어

```bash
# 루트에서 API(3001) + 웹(5173) 동시 실행, 웹의 /api 요청은 3001로 프록시
npm run dev

# 개별 실행
cd api && npm run dev    # API만 (http://localhost:3001)
cd web && npm run dev    # 웹만 (http://localhost:5173)
```

## 테스트 명령어

```bash
# 루트에서 api + web 테스트 모두 실행
npm test

# 개별 실행
cd api && npm test
cd web && npm test
```

## 커밋 규칙

[Conventional Commits](https://www.conventionalcommits.org/) 형식을 따른다.

```
<type>: <description>

[optional body]
```

- `feat`: 새 기능 추가
- `fix`: 버그 수정
- `docs`: 문서 변경
- `refactor`: 동작 변화 없는 코드 구조 변경
- `test`: 테스트 추가/수정
- `chore`: 빌드, 설정 등 기타 변경

예시: `feat: 할일 완료 토글 API 추가`
