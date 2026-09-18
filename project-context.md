# KOR-0050 marketing site context

## Scope

- This repository is the independent public marketing and study site for released app `KOR-0050` only.
- App source is read-only: `/Users/youngjunma/Documents/various test prep apps project/services/kor/00/kor-0050`.
- Android package and iOS bundle identifier: `app.mcyj.examprep.kor0050`.
- Production target: `https://mcyj.github.io/construction-safety-engineer-korea-exam-prep-web/`.

## Verified store state — 2026-09-19

- Google Play detail page resolves publicly for `app.mcyj.examprep.kor0050`.
- Apple Search API returned no matching public app in KR, US, or GB storefronts.
- Therefore Google Play is the only active Store link. App Store is a localized, disabled “Coming Soon” control with no `apps.apple.com` URL.
- Both marketplace controls use the same 194 × 75 px outer frame; official badge artwork keeps its native aspect ratio.

## Content and official facts

- Korean and English routes are published, with 10 substantive study guides per locale.
- Current official qualification name: 건설안전기사 / Engineer Construction Safety (`jmCd=1440`).
- Written exam: five subjects, 20 multiple-choice questions per subject, 30 minutes per subject (100 questions / 150 minutes total).
- Practical exam: combined written response (90 minutes, 60 points) and task analysis (about 50 minutes, 40 points).
- Passing rules: at least 40 points in every written subject and a 60-point written average; at least 60 points in the practical exam.
- Current official specification period: 2026-01-01 through 2030-12-31.
- Canonical sources:
  - `https://www.q-net.or.kr/crf005.do?id=crf00503&jmCd=1440`
  - `https://www.q-net.or.kr/crf005.do?id=crf00503s02&jmCd=1440&jmInfoDivCcd=B0`
  - `https://www.q-net.or.kr/rcv013.do?gId=&gSite=Q&id=rcv01306s02&jmCd=1440`

## Design and implementation

- Visual thesis: mint app imagery inside a cream construction-blueprint field, with dark green ink and a yellow/green hazard stripe.
- Global Korean-safe wrapping uses `word-break: keep-all` with `overflow-wrap: break-word`.
- The site is a dependency-free static generator. `npm run build` writes `dist/`; `npm run check` validates routes, metadata, links, app identity, marketplace state, badge sizing, and wrapping rules.
- GitHub Actions builds, checks, and deploys the `dist/` artifact to GitHub Pages.

## Verification log

- 2026-09-19: local build generated 34 indexable routes and 36 HTML files total.
- 2026-09-19: local checker passed metadata, links, page count, `keep-all`, Google Play identity, disabled App Store state, and equal badge frames.
