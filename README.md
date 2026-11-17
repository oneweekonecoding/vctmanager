# 발로란트 프로게임단 키우기 (VCT 매니저)

VCT 2026 시즌(Champions 2026 종료 기준) 실제 선수, 감독 데이터로 48개 VCT 팀 중 하나를 맡아 운영하는 웹 게임입니다.
`index.html` 한 파일로 돌아가고, 서버나 빌드 과정이 필요 없습니다.

## GitHub Pages에 올리는 방법

1. GitHub에서 새 저장소를 만듭니다. (예: `vct-manager`, Public)
2. 이 폴더의 파일을 모두 올립니다. `.github` 폴더와 `.nojekyll`도 포함해야 합니다.
   - 웹에서 올릴 때: 저장소의 **Add file > Upload files**에 폴더 안 파일을 끌어다 놓고 Commit
   - 터미널에서 올릴 때:
     ```bash
     git init
     git add .
     git commit -m "VCT 매니저 첫 배포"
     git branch -M main
     git remote add origin https://github.com/<아이디>/vct-manager.git
     git push -u origin main
     ```
3. 저장소 **Settings > Pages > Build and deployment > Source**를 **GitHub Actions**로 바꿉니다.
4. **Actions** 탭에서 "Deploy to GitHub Pages"가 끝나면 아래 주소로 접속할 수 있습니다.
   `https://<아이디>.github.io/vct-manager/`

`.github` 폴더를 올리기 어렵다면 3번에서 Source를 **Deploy from a branch**, 브랜치 `main`, 폴더 `/ (root)`로 골라도 됩니다.

## 업데이트할 때
새 `index.html`로 덮어쓰고 커밋하면 1~2분 뒤 자동으로 다시 배포됩니다.

## 참고
- 세이브는 브라우저 localStorage에 저장됩니다. 주소(도메인)가 바뀌면 이전 세이브는 따라오지 않습니다.
- 글꼴은 Google Fonts에서 불러오고, 나머지 이미지와 데이터는 모두 `index.html` 안에 들어 있습니다.
- 데이터 출처: vlr.gg, Liquipedia 검색 결과, Sheep Esports, THESPIKE, valo2asia 등. 팬 메이드 게임이며 Riot Games와 관련이 없습니다.
