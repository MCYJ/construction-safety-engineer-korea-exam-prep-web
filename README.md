# 건설안전기사 필기·실기 웹사이트

출시된 RushLabs `KOR-0050` 앱을 위한 독립 한국어·영어 홍보·학습 사이트입니다.

- Production: https://mcyj.github.io/construction-safety-engineer-korea-exam-prep-web/
- 정적 생성 결과: `dist/`
- GitHub Actions가 `main` 변경 시 GitHub Pages에 배포합니다.

```bash
npm run build
npm run check
```

학습 글은 `content/articles.mjs`, 공통 페이지 생성과 locale 문구는 `scripts/build.mjs`에서 관리합니다. 새 locale을 추가할 때는 두 파일의 콘텐츠, `lang`·`hreflang`, 정책·지원 문구와 Store 상태를 함께 현지화해야 합니다.
