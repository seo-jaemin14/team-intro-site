# 팀 자기소개 프로젝트

이 레포지토리는 프론트엔드 수업의 GitHub 협업 실습을 위한 저장소입니다.

## 📋 실습 가이드

1. 이 저장소를 클론합니다.
2. 브랜치를 생성합니다.

```bash
git checkout -b feature/이름
```
3. members/이름.html 파일을 만듭니다.
4. index.html에 본인의 링크를 추가합니다.
5. 커밋 후 푸시하고 PR을 생성합니다.

## 🧱 파일 구조 예시
```
index.html                # 전체 팀원 목록
members/
  └── 이름.html           # 각자의 소개 페이지
css/
  └── style.css           # 공통 스타일 시트
```

## 📦 배포
GitHub Pages를 통해 배포할 수 있습니다.

Settings → Pages → main 브랜치 선택 후 저장

---

## 📝 팀원이 작업할 예시

### 새로운 팀원이 할 일

1. `feature/홍길동` 브랜치 생성
2. `members/hong.html` 파일 추가
3. `index.html`에 다음 라인 추가:

```html
<li><a href="./members/hong.html">홍길동의 자기소개</a></li>
```