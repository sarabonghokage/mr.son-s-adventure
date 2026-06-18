# 손우주의 대모험

브라우저에서 바로 실행되는 정적 HTML/JS 게임 모음입니다. 빌드 과정 없이 배포할 수 있습니다.

## 포함된 게임

| 페이지 | 설명 |
|--------|------|
| [index.html](index.html) | 메인 메뉴 · 스테이지 모드 |
| [survive.html](survive.html) | 생존 (맵 프로토타입) |
| [lacero.html](lacero.html) | lácĕro 카드 PvE |
| [aigo.html](aigo.html) | 아이고 대모험 플랫포머 |

## 로컬 실행

웹 서버 없이도 `index.html`을 브라우저에서 열면 대부분 동작합니다.  
파일 프로토콜 제한을 피하려면 간단한 서버를 쓰는 것을 권장합니다.

```bash
# Python
python -m http.server 8080

# Node (npx)
npx serve .
```

이후 `http://localhost:8080` 접속.

## GitHub Pages 배포

1. GitHub에 저장소를 만들고 이 폴더를 푸시합니다.

```bash
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/<사용자>/<저장소>.git
git push -u origin main
```

2. 저장소 **Settings → Pages**에서  
   **Build and deployment → Source**를 **GitHub Actions**로 선택합니다.

3. `main` 브랜치에 푸시하면 `.github/workflows/pages.yml`이 자동으로 배포합니다.

4. 몇 분 후 `https://<사용자>.github.io/<저장소>/` 에서 접속할 수 있습니다.

## Netlify / Vercel (대안)

빌드 명령 없이 **루트 디렉터리**를 그대로 배포하면 됩니다.

| 항목 | 값 |
|------|-----|
| Build command | *(비움)* |
| Publish directory | `.` (루트) |

## 구조

```
index.html          메인 진입점
survive.html        생존 모드
lacero.html         카드 PvE
aigo.html           플랫포머
css/                스타일
js/                 게임 로직
```
