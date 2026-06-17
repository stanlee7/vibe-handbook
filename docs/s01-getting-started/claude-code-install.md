---
sidebar_position: 1
title: Claude Code 설치하기
description: Anthropic의 공식 CLI 도구인 Claude Code를 설치하는 방법
---

# Claude Code 설치하기

## 학습 목표

- Claude Code가 무엇인지 이해한다
- macOS / Windows / Linux에 Claude Code를 설치한다
- 설치 후 정상 동작을 확인한다

---

## Claude Code란?

**Claude Code**는 Anthropic이 만든 공식 CLI(터미널) 도구로, 터미널에서 직접 Claude와 대화하며 코딩 작업을 자동화할 수 있게 해줍니다.

VS Code, JetBrains 같은 IDE 확장과도 연동되며, 파일 읽기·수정·명령 실행·git 작업까지 모두 가능합니다.

:::tip 여기서 잠깐
Claude Code는 **유료 API 키** 또는 **Claude 구독(Pro/Max)** 이 필요합니다. 설치는 무료지만, 사용 시 토큰 비용이 발생합니다.
:::

---

## 사전 준비

설치 전에 다음이 준비되어 있어야 합니다.

- ✅ **Node.js 18 이상** — `node -v` 로 확인
- ✅ **터미널 사용에 익숙할 것** — Bash, Zsh, PowerShell 무엇이든 OK
- ✅ **Anthropic 계정** — [console.anthropic.com](https://console.anthropic.com) 에서 가입

Node.js가 없다면 [nodejs.org](https://nodejs.org)에서 LTS 버전을 먼저 설치하세요.

---

## 설치 (macOS / Linux / Windows 공통)

터미널을 열고 다음 명령어 한 줄을 실행합니다.

```bash
npm install -g @anthropic-ai/claude-code
```

설치가 끝나면 어떤 폴더에서든 `claude` 명령어를 쓸 수 있습니다.

---

## 설치 확인

```bash
claude --version
```

버전 번호(예: `1.x.x`)가 출력되면 성공입니다.

---

## 첫 실행

원하는 프로젝트 폴더로 이동한 뒤 실행합니다.

```bash
cd ~/my-project
claude
```

처음 실행하면 로그인 안내가 뜹니다. 안내에 따라 브라우저로 로그인하면 끝.

---

## 자주 발생하는 문제

### `command not found: claude`
→ npm 글로벌 설치 경로가 PATH에 없는 경우입니다. 다음 명령으로 경로를 확인하세요.

```bash
npm config get prefix
```

출력된 경로의 `bin` 폴더가 `~/.zshrc` 또는 `~/.bashrc`의 `PATH`에 포함되어 있어야 합니다.

### 권한 에러 (EACCES)
→ `sudo`로 설치하지 말고, npm 글로벌 디렉토리를 사용자 폴더로 옮기는 게 안전합니다. ([공식 가이드](https://docs.npmjs.com/resolving-eacces-permissions-errors-when-installing-packages-globally))

---

## 다음 단계

설치가 끝났다면, 이제 실제로 코딩 작업을 시켜볼 차례입니다.

👉 다음 레슨: *Claude Code 첫 명령 보내기* (작성 예정)
