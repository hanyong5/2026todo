# CLAUDE.md

## 폴더 구조

```
.
├── api/    # 백엔드 (Node.js, Express/Nest)
├── web/    # 프론트엔드 (React/Next.js)
└── docs/   # 문서
```

## 실행 명령어

```bash
# api
cd api && npm install
cd api && npm run dev

# web
cd web && npm install
cd web && npm run dev
```

## 테스트 명령어

```bash
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
