# 🔒 정보보안 분야별 수업자료 (Level 0~10)

GitHub Pages용 정적(Static) 커리큘럼 사이트입니다. 빌드 과정 없이 HTML만으로 동작합니다.

## 🌐 보는 방법

배포 후 `https://계정명.github.io/저장소명/` 접속

## 🗂 구조

| 구분 | 내용 |
|---|---|
| `index.html` | 전체 목차 (분야 카드 + 분야×레벨→장 표) |
| `field-*.html` 7개 | 분야별 레벨 그룹 강의 목록 (예: `field-forensics.html`) |
| `web-l*.html` 등 75개 | 기술(장)별 개별 수업자료 (예: `forensics-l00-01.html`) |

- **막 = Level (난이도 0~10)**, **장 = 기술별 개별 파일**
- 예: 웹 Level 5 → `XSS` · `CSRF` · `SSRF` 3장 분리
- 네비게이션: 상단바(분야 선택) + 왼쪽 사이드바(레벨별 장 목록)

## 📚 분야별 장 수

| 분야 | 장 수 | 범위 예시 |
|---|---|---|
| 🌐 웹 | 13 | HTTP → XSS/CSRF/SSRF → SQLi → JWT → 모의해킹 프로젝트 |
| 🔍 리버싱 | 10 | 어셈블리 → 정적/동적 분석 → 패킹 → crackme |
| 💥 포너블 | 11 | 메모리 구조 → BOF → ROP → Heap → 커널 개요 |
| 🧬 포렌식 | 10 | 증거보존 → 로그/디스크/메모리 분석 → 보고서 |
| 🔐 암호학 | 11 | 고전암호 → AES/RSA → 취약점 → TLS |
| 🖥️ 시스템 | 10 | 리눅스 기초 → 권한상승 → 하드닝 → 진단 실전 |
| 🧩 Misc | 10 | CTF 입문 → 파이썬 → OSINT → Write-up |

## 🚀 GitHub Pages 배포

1. 필요한 파일만 add (`.omo/`, `.codegraph`, `_config.yml` 제외 — Pages는 `.nojekyll`로 정적 서빙)
   ```bash
   git add index.html README.md .nojekyll field-*.html web-l*.html reversing-l*.html pwnable-l*.html forensics-l*.html crypto-l*.html system-l*.html misc-l*.html
   git commit -m "ASCII 파일명으로 정규화: 한글 NFD/NFC 404 해결"
   git push
   ```
2. 저장소 **Settings → Pages → Branch: `main`, 폴더: `/ (root)`** 선택
3. `https://계정명.github.io/저장소명/` 접속

## ⚠️ 이용 주의

모든 실습은 본인 소유 VM·실습용 사이트(허가된 환경)에서만 수행하세요. 허가 없는 실제 시스템 대상 해킹 시도는 처벌 대상입니다.
