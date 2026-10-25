# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

Personal portfolio site for 이영근, published with GitHub Pages as a user site (`grwtergis3733-droid.github.io`). Pages serves `main` as-is, so a push to `main` is a deploy.

The whole site is one static file, `index.html`, with inline CSS and no JavaScript. There is no build step, package manager, linter or test suite.

## Running locally

Open `index.html` in a browser, or serve the folder:

```bash
python -m http.server 8000
```

## Structure and conventions

- Content and UI text are in Korean (`lang="ko"`). The page uses `word-break: keep-all` so Korean words don't break mid-word.
- Colors are CSS custom properties on `:root`, redefined under `@media (prefers-color-scheme: dark)`. Add new colors as tokens in both places rather than hard-coding them.
- Layout: a centered `.container` (max 880px) holding `header`, `section`s and `footer`. Each `section` has a small, muted, letter-spaced `h2` label (the footer's "연락처" uses the same style).
- "만든 것" (projects) is a `.cards` grid of numbered placeholder cards ("곧 채워질 예정"). Replace placeholders with real projects as they're built.
- "진행 중" shows current progress on a 20-week roadmap (`.status`). Update the week number as the roadmap advances.
- Mobile adjustments live in the single `@media (max-width: 480px)` block at the end of the stylesheet.

## Commits

Commit messages are short Korean summaries (e.g. `1주차: 포트폴리오 v0`, `연락처 이메일 추가`).

## 프로젝트 배경

- 20주 산출물 중심 학습 로드맵의 진열대 역할을 하는 포트폴리오 사이트
- 매주 만든 결과물을 "만든 것" 섹션에 카드로 추가한다
- GitHub Pages로 배포 (main 브랜치, 루트)

## 작업 규칙

- 외부 라이브러리 없이 HTML과 CSS만 사용
- 휴대폰에서도 잘 보이게 유지
- 나는 코딩 입문자라서, 명령을 실행할 때 무엇을 왜 하는지 한두 줄로 설명해줘
- 작업을 마치면 커밋하고 push할지 물어봐줘

## 진행 상황

- 1주차 완료: 포트폴리오 v0 배포
- 다음: 2주차 취득세 계산기 (별도 폴더에서 진행 예정)
