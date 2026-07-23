# 브리퐁 (Briefong)

시각장애인이 이커머스 상품 정보를 더 빠르게 탐색하도록 돕는 **데스크톱 웹 프로토타입 시연 사이트**입니다.

> 이 저장소는 실제 쿠팡 서비스나 공식 제휴 서비스가 아닌 교육·연구용 프로토타입입니다. 화면의 상품, 가격, 리뷰, URL은 시연용 가상 데이터입니다.

## 주요 시연 기능

- 기존 선형 탐색과 브리퐁 핵심정보 우선 탐색 비교
- 음성 검색 및 음성 명령 흐름 시연
- 상품 상세 페이지와 접근성 뷰 전환
- 상품명·가격·배송·리뷰·구매·상세정보 섹션 탐색
- 글자 크기 조절, 고대비 모드, 음성 읽기
- 상품 이미지 포인터 위치 기준 2.5배 확대
- API 없이 가능한 기능과 API 연결 후 가능한 AI 기능 구분

## 파일 구조

```text
.
├── index.html
├── briefong-icon.png
├── headphones-product.svg
├── site.webmanifest
├── robots.txt
├── .nojekyll
└── .github/
    └── workflows/
        └── deploy-pages.yml
```

## GitHub Pages 배포

### 1. 저장소에 파일 업로드

새 GitHub 저장소를 만든 뒤 이 폴더의 **내용 전체**를 저장소 최상위(root)에 업로드합니다. `index.html`이 하위 폴더가 아니라 저장소 첫 화면에 보여야 합니다.

### 2. Pages 설정

1. 저장소의 **Settings**로 이동
2. 왼쪽 메뉴에서 **Pages** 선택
3. **Build and deployment → Source**를 **GitHub Actions**로 선택
4. `main` 브랜치에 파일을 올리면 `Deploy Briefong to GitHub Pages` 워크플로가 실행됨
5. **Actions** 탭에서 배포 완료 여부 확인

배포 주소는 일반적으로 다음 형식입니다.

```text
https://깃허브아이디.github.io/저장소이름/
```

### Git 명령어로 업로드할 경우

```bash
git init
git branch -M main
git add .
git commit -m "Deploy Briefong prototype"
git remote add origin https://github.com/깃허브아이디/저장소이름.git
git push -u origin main
```

## 로컬 실행

`index.html`을 Chrome에서 직접 열어도 기본 기능을 확인할 수 있습니다. 웹 서버 환경과 동일하게 확인하려면 다음 명령을 실행합니다.

```bash
python -m http.server 8000
```

그다음 Chrome에서 `http://localhost:8000`에 접속합니다.

## 단축키

| 단축키 | 기능 |
|---|---|
| `Shift + Space` | 음성 검색 시연 |
| `Space` | 음성 명령 시연 |
| `Alt + Z` | 접근성 뷰 켜기/끄기 |
| `Alt + P` | 상품명 영역 이동 |
| `Alt + C` | 가격 영역 이동 |
| `Alt + B` | 구매 영역 이동 |
| `Alt + D` | 상세정보 영역 이동 |
| `Alt + R` | 마지막 음성 안내 다시 듣기 |

## 배포 전 점검 결과

- 외부 JavaScript/CSS 라이브러리 사용 없음
- API 키, 액세스 토큰, 비밀번호 없음
- 서버 또는 데이터베이스 연결 없음
- 사용자 입력 및 음성 데이터 전송 없음
- 브라우저의 Web Speech API 음성 출력 기능만 사용

## 팀

**Re:Creator:Crew**
