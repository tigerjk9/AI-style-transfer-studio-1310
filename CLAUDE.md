# CLAUDE.md — AI 그림체 변환 (Style Transfer Studio)

## 한 줄 정의
사진 한 장 → 6가지 그림체(지브리·짱구·마블·디즈니·레트로·웹툰)로 캐릭터 변신.

## 라이브 / 저장소
- 🌐 https://ai-style-transfer-1310-studio.vercel.app/
- 🐙 https://github.com/tigerjk9/AI-style-transfer-studio-1310

## 기술 스택
- 단일 `index.html` (Vanilla JS)
- Tailwind CSS CDN + Pretendard + JSZip 3.10.1
- Gemini 2.5 Flash Image (`gemini-2.5-flash-image`, BYOK)

## 핵심 데이터
- `PHOTO_STYLES[]` 6개: `{name, prompt}` (각 스타일별 정밀 영문 프롬프트)
- 모든 프롬프트에 13:10 인쇄용 출력 강제 + 얼굴 정체성 보존

## 핵심 결정
- 다중 스타일 동시 선택 가능 (BYOK 비용 사용자 부담)
- 스타일별 1~3장 슬라이더로 조절 (총 최대 18장)
- 13:10 인쇄용 카드 + 개별/ZIP 다운로드

## 변경 핵심 이력
- 2026-04-19: Gemini 모델명 GA 전환 (`-preview` 제거) + Vercel 호스팅으로 전환 (Netlify 종료)

## 부스 등록
🍌 나노 바나나 시리즈 1번 카드 (`nanoBananaApps[0]` in 부스 index.html)
