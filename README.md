# Helpful Dev Feeds

주관적으로 도움이 됐던 피드들 모음

## 새 글 발행

### 1. 파일 생성

`src/data/blog/` 디렉토리에 마크다운 파일을 생성합니다.

파일명 규칙: `YYYY-MM.md` (예: `2025-01.md`)

### 2. Frontmatter 작성

파일 상단에 아래 형식의 frontmatter를 작성합니다.

```yaml
---
title: "주간 피드 2025-01"
description: "2025/01/06 ~ 2025/01/11 주간 피드 정리"
pubDatetime: 2025-01-11T00:00:00Z
tags: ["weekly", "2025", "개발", "에세이"]
---
```

| 필드 | 필수 | 설명 |
|------|------|------|
| `title` | O | 글 제목 |
| `description` | O | 글 설명 (목록에 표시) |
| `pubDatetime` | O | 발행일 (`YYYY-MM-DDT00:00:00Z` 형식) |
| `tags` | - | 태그 배열 (기본값: `["others"]`) |
| `author` | - | 작성자 (기본값: 사이트 설정의 author) |
| `featured` | - | 홈 상단 Featured 섹션에 노출 (`true`/`false`) |
| `draft` | - | `true`로 설정하면 비공개 |
| `ogImage` | - | OG 이미지 URL 또는 로컬 이미지 경로 |

### 3. 본문 작성

Frontmatter 아래에 마크다운으로 본문을 작성합니다.

```markdown
---
title: "주간 피드 2025-01"
description: "2025/01/06 ~ 2025/01/11 주간 피드 정리"
pubDatetime: 2025-01-11T00:00:00Z
tags: ["weekly", "2025", "개발"]
---

> 인용문이나 한줄 소감

## 카테고리

- [글 제목](https://example.com) (2025/01/10)
    - 글에 대한 소감이나 요약
```

### 4. 로컬 확인

```bash
npm run dev
```

`http://localhost:4321/helpful-feeds/` 에서 새 글이 정상적으로 표시되는지 확인합니다.

### 5. 배포

`main` 브랜치에 push하면 GitHub Actions를 통해 자동 배포됩니다.

## Development

```bash
npm install
npm run dev
```

```bash
npm run build
npm run preview
```
