# Git 계정 분리 (템플릿)

개인 이메일·계정명은 **`GIT_ACCOUNTS.local.md`** 에만 적어 두세요.  
그 파일은 Git에 올라가지 않습니다.

## 로컬 전용 파일 만들기

```powershell
copy GIT_ACCOUNTS.example.md GIT_ACCOUNTS.local.md
# GIT_ACCOUNTS.local.md 를 열어 본인 계정/이메일/경로 입력
```

## 이 레포(angel-ceo) 권장 설정

```powershell
git config --global credential.useHttpPath true

git config user.name "YOUR_GITHUB_USERNAME"
git config user.email "YOUR_USERNAME@users.noreply.github.com"
git remote set-url origin https://github.com/YOUR_GITHUB_USERNAME/angel-ceo.git
```

## GitHub에 올리면 안 되는 것

- `.env`, API 키, 토큰, SSH **개인키**
- 개인 이메일·비밀번호가 적힌 메모
- `GIT_ACCOUNTS.local.md`

## 공개 레포에 있어도 되는 것

- 사이트에 공개된 업소 연락처·텔레그램 제휴 링크
- `YOUR-ANGEL-CEO-DOMAIN` 같은 도메인 placeholder
