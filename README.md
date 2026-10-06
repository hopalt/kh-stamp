# 국가유산 방문 도우미 홈페이지

https://khstamp.hopalt.com/ — 앱 소개(`index.html`)와 개인정보처리방침(`privacy/index.html`).
앱 설정의 개인정보처리방침 링크(`privacyPolicyUrl`)가 `/privacy/` 를 가리키니 주소를 바꾸지 않는다.

원본은 앱 저장소(gitlab `hopalt/kh-stamp`)의 `homepage/` 폴더다. GitHub `hopalt/kh-stamp` 는 이 폴더만 올린 배포용 저장소라 거기서 직접 고치지 않는다.

## 배포

앱 저장소 루트에서:

```
git subtree push --prefix homepage github main
```

(`github` 원격: `git remote add github https://github.com/hopalt/kh-stamp.git`)

- GitHub Pages: Settings > Pages > Deploy from a branch, `main` / `(root)`, Custom domain `khstamp.hopalt.com`(`CNAME` 파일), Enforce HTTPS
- DNS: `khstamp.hopalt.com` CNAME → `hopalt.github.io`

## 고칠 때

- 색은 앱의 `PaperColors`(`lib/core/theme/app_theme.dart`)와 맞춘다 (`style.css`)
- 스크린샷은 `docs/design/after/` 에서 줄여 `img/` 에 둔다. 실제 가족 이름·공식 사진이 보이는 화면은 쓰지 않는다
- 개인정보처리방침 내용이 바뀌면 시행일을 고치고 `docs/store/listing.md` 의 데이터 보안 답과 맞는지 본다
