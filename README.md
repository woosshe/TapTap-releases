# TapTap — 배포

만화책·웹툰·PDF·EPUB·TXT를 읽는 멀티플랫폼 뷰어 **TapTap**의 배포용 저장소입니다.
React Native + TypeScript로 한 벌을 쓰고, 플랫폼마다 다른 것만 확장자로 나눕니다.

A multi-platform reader for comics, webtoons, PDF, EPUB and plain text.

> **[받기 — 최신 릴리스](https://github.com/woosshe/TapTap-releases/releases/latest)**
> · [Download the latest release](https://github.com/woosshe/TapTap-releases/releases/latest)

| | |
|---|---|
| 지원 예정 | Android · iOS/iPadOS · Windows · macOS |
| 지금 동작하는 것 | **Android.** 나머지 셋은 코드는 있으나 아직 한 번도 빌드된 적이 없습니다 |
| 읽는 형식 | `cbz`·`zip` · 이미지 폴더 · `pdf` · `epub` · `txt` (`cbr`은 아직입니다) |
| 개발 순서 | Android → iOS → Windows → macOS |

이 앱은 **PC에서 USB로 복사해 넣은 파일을 읽는 것**을 주 사용 방식으로 설계했습니다.
그래서 저장 경로는 탐색기·Finder·MTP로 접근할 수 있는 위치여야 합니다.

### 설치 / Install

APK를 받아서 설치해 주세요. **「출처를 알 수 없는 앱」 설치를 허용**해야 하고,
처음 실행하면 **서재 폴더를 한 번 골라 주세요** — 그 안의 책을 읽습니다.

Download the APK and install it. You'll need to allow installing from unknown sources,
and pick a library folder once on first launch.

---

## 변경 내역

### 0.1.0 — 2026-08-22

**첫 배포입니다.** 안드로이드만 있습니다. 프로토타입이지만 읽는 데 필요한 것은 다 들어 있습니다.

**읽는 것** — CBZ·ZIP · 이미지 폴더 · PDF · EPUB · TXT

**페이지 모드(만화)**
- 한 장 / 두 장 보기, 우철·좌철. 화면을 세로로 들면 언제나 한 장입니다
- 더블탭·핀치 확대. **확대하면 그 자리를 원본에서 다시 잘라** 선명하게 그립니다
- 끝에서 한 번 더 밀면 이전·다음 권으로 넘어갑니다. 늘어나는 모션이 「여기가 끝」을 알립니다
- 자동 이미지 보정(자동 레벨) — 뿌연 스캔을 펴 줍니다

**스크롤 모드(웹툰)**
- 화면을 누르고 있으면 자동으로 굴러갑니다 (속도 7단계)
- 폭 조절 (화면의 30~100%)
- 화면에 안 들어가는 아주 긴 장도 잘라서 그립니다

**글(TXT·EPUB)**
- 브라우저의 조판으로 쪽을 나눕니다 — 글자 크기를 바꾸면 즉시 다시 흐릅니다
- 글꼴 네 가지 내장(네오둥근모Pro·나눔고딕·나눔명조·리디바탕), 배경 여섯 가지
- 글자 크기·줄 간격·글꼴·배경·여백을 **읽으면서** 바꿉니다 (쪽 넘김 모션은 옵션 화면에 있습니다)
- EPUB의 삽화와 전면 그림(표지)을 그립니다

**온라인** — Google Drive · SFTP · SMB 2/3 · FTP/FTPS. 폴더째 걸어 두는 받기 대기열이 있습니다

**서재** — 책갈피(읽던 자리·진도), 즐겨찾기, 완독한 책 감추기, 표지 썸네일

**그 밖** — 한국어/영어, 뷰어 밝기(앱 전용·시스템 공유), 화면 회전 고정, 마지막 화면에서 시작

**알려진 것**
- 빠르게 휙 넘기면 손을 떼는 순간 한 번 멈칫합니다
- 글 책은 15만 자마다 구간이 나뉘는데, 그 경계에서 넘김이 한 박자 쉽니다
- 안드로이드 7.0(API 24) 이상이 필요합니다

---

## Changelog

### 0.1.0 — 2026-08-22

**First release.** Android only. It's a prototype, but everything needed for reading is there.

**Formats** — CBZ/ZIP, image folders, PDF, EPUB, TXT

**Page mode (comics)**
- One-page or two-page spread, right-to-left or left-to-right. Always one page in portrait
- Double-tap and pinch to zoom. **Zooming re-crops that area from the original** for a sharp view
- Push past the last page to move between volumes; a rubber-band stretch says "this is the end"
- Automatic image correction (auto levels) for washed-out scans

**Scroll mode (webtoons)**
- Press and hold to auto-scroll (7 speeds)
- Width adjustment (30–100% of the screen)
- Very tall images are sliced so they actually render

**Text (TXT / EPUB)**
- Pagination by the browser's own layout engine — change the font size and it reflows instantly
- Four bundled fonts, six background themes
- Font size, line height, typeface, theme and margins are adjusted **while reading**
  (the page-turn motion lives in Settings)
- EPUB illustrations and full-page images (covers) are rendered

**Online** — Google Drive, SFTP, SMB 2/3, FTP/FTPS, with a download queue you can point at whole folders

**Library** — bookmarks (last position and progress), favorites, hiding finished books, cover thumbnails

**Also** — Korean/English, viewer brightness (app-only or shared with the system), rotation lock,
resume on the last screen

**Known issues**
- A brief hitch on release when you flick a page quickly
- Text books are split into 150,000-character sections; page turns pause at those boundaries
- Requires Android 7.0 (API 24) or newer

---

## 라이선스 / License

개인 프로젝트입니다. 지금은 사이드로딩으로만 배포합니다.

A personal project, distributed by sideloading for now.
