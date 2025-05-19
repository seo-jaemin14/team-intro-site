# 🧩 팀 소개 웹사이트 제작 활동지

> 본 활동은 HTML/CSS와 GitHub 협업을 실제로 체험하며 배우는 실습입니다. 
> 여러분은 팀의 일원으로서 자기소개 페이지를 만들고, `index.html`과 공통 `header`를 함께 수정하게 됩니다.

---

## ✅ 목표

- HTML 문서 구조와 상대경로 이해
- 공통 컴포넌트(header/nav)의 구조화와 반복 사용 실습
- GitHub 협업 브랜치 전략과 충돌 해결 경험

---

## 📁 프로젝트 구조 설명

```plaintext
team-intro-site/
├── index.html               → 팀원 리스트가 있는 메인 페이지
├── members/
│   └── sample.html          → 자기소개 샘플 페이지
├── css/
│   └── style.css            → 공통 스타일 파일
├── README.md
└── ACTIVITY.md              → 현재 보고 있는 활동지
```



# Git Branch란?

## 1. 브랜치는 "작업 공간 복사본"

- **브랜치(branch)**는 '원본 코드'를 복사해서 내 마음대로 실험해볼 수 있는 **작업 공간**.
- 원본(주요 코드, 보통 `main` 브랜치)은 그대로 두고, 각자 브랜치에서 내 작업을 진행.

## 2. 왜 브랜치를 쓸까?

- 여러 명이 동시에 같은 파일을 고치면, 서로의 작업이 뒤섞여 **문제가 생길 수 있음**.
- **브랜치**를 쓰면, 각자 자기만의 복사본에서 작업하다가, **완성된 것만 합칠 수 있음**.

------

## 🏃‍♂️ 실습 예시로 이해하기

## 1. 브랜치 만들기

```bash
git checkout -b feature/이름
```

- 예를 들어, '지우'가 자기소개 페이지를 만들고 싶으면:
  - `feature/jiwoo`라는 이름의 브랜치를 만듭니다.
  - 이제 이 브랜치에서 마음껏 파일을 만들고 수정해도, 다른 사람 작업에는 영향이 없음

## 2. 내 브랜치에서 작업하기

- `members/jiwoo.html` 파일을 만들고,
- `index.html`에 내 이름을 추가하고,
- 저장(`git add .`, `git commit -m "메시지"`)

## 3. 작업이 끝나면, 브랜치를 합친다!

- **Pull Request**를 만들어서, 내 브랜치의 작업을 `main`(원본) 브랜치에 합치도록 요청.
- 이때, **여러 사람이 같은 부분을 수정했다면 '충돌(conflict)'**이 날 수 있음!
- 충돌이 나면, 둘 다의 내용을 잘 합쳐서 정리해주면 됨.

------

## 📦 브랜치의 장점 한눈에 보기

| 브랜치 없이                             | 브랜치 사용                        |
| --------------------------------------- | ---------------------------------- |
| 모두가 같은 파일을 직접 수정, 충돌 많음 | 각자 자기 공간에서 작업, 충돌 적음 |
| 실수하면 원본에 바로 영향               | 실수해도 내 브랜치에서만 영향      |
| 협업이 어렵고 복잡                      | 협업이 쉽고, 나중에 합치기 편함    |

------

## 🎈 한 줄 요약

> **브랜치**는 "내가 실험하고 작업할 수 있는 복사본"
> → 작업이 끝나면 원본(main)에 '합치기(Pull Request)'로 협업!



# 활동

## 🧭 1단계: 저장소 클론 및 브랜치 생성

## 1. 팀장 역할

- 팀장은 GitHub에서 프로젝트 저장소를 **fork**(포크)하여 자신의 계정에 복제본을 만듭니다.
- 팀장은 저장소의 **Settings > Collaborators** 메뉴에서 팀원들의 GitHub 아이디를 입력해 **collaborator(협업자)**로 초대합니다.
- 팀원들은 초대 메일을 수락하면 저장소에 대한 push, pull 권한을 갖게 됩니다.

## 2. 팀원 역할

- 각 팀원은 팀장이 초대한 저장소의 주소를 복사하여, 본인 컴퓨터에 **clone**(복제)합니다[6](https://autumnly1007.tistory.com/247).

  ```bash
  git clone [저장소 주소]
  cd [저장소 폴더명]
  ```

- 자신의 작업을 독립적으로 진행하기 위해, 본인 이름을 딴 브랜치를 생성하고 이동합니다.

  ```bash
  git checkout -b feature/본인_이름
  ```

  예시:

  ```bash
  git checkout -b feature/jiwoo
  ```

## 3. 요약 흐름

1. 팀장이 저장소를 fork하고 collaborator로 팀원 초대
2. 팀원들은 초대 수락 후, 저장소를 clone
3. 각자 `feature/본인_이름` 브랜치 생성 후 작업 시작

이 과정을 통해 모든 팀원이 원본(main) 코드에 직접 영향을 주지 않고, 각자 독립적으로 개발을 진행할 수 있습니다

# 활동

## 🧑‍💻 2단계: 자기소개 페이지 만들기

- `members/이름.html` 파일을 만듭니다.
- `members/sample.html`의 구조를 복사해서 넣습니다.
- 자신을 소개하는 내용을 자유롭게 작성합니다.

```html
<!DOCTYPE html>
<html lang="ko">

<head>
    <meta charset="UTF-8">
    <!-- 본인 이름 작성 -->
    <title>홍길동의 자기소개</title>
    <link rel="stylesheet" href="../css/style.css" />
</head>

<body>
    <header>
        <!-- 팀 이름 작성 -->
        <h1>ㅇㅇㅇ 소개</h1>
        <nav>
            <ul>
                <li><a href="../index.html">홈</a></li>
                <li><a href="./sample.html">샘플</a></li>
                <!-- 팀원별 자기소개 링크가 여기에 추가될 예정 -->
            </ul>
        </nav>
    </header>
    <main>
        <h2>이름: 홍길동</h2>
        <section>
            <h3>기본 정보</h3>
            <ul>
                <li><strong>학과:</strong> </li>
                <li><strong>학번:</strong> </li>
                <li><strong>연락처(이메일):</strong> </li>
            </ul>
        </section>

        <section>
            <h3>나에 대해</h3>
            <ul>
                <li><strong>취미:</strong> </li>
                <li><strong>관심사/좋아하는 것:</strong> </li>
                <li><strong>특기:</strong> </li>
            </ul>
        </section>

        <section>
            <h3>팀에서 내 역할</h3>
            <ul>
                <li>웹 개발, 디자인, 그리고 새로운 기술을 배우는 것 외에 맡은 역할을 자유롭게 작성하세요.</li>
            </ul>
        </section>
        <section>
            <h3>자유롭게 하고 싶은 말</h3>
            <p>자유롭게 자기소개를 마무리하는 글을 작성하세요.</p>
        </section>

        <p><a href="../index.html" class="back-btn">← 돌아가기</a></p>
    </main>
</body>

</html>
```

------

## 🧩 3단계: 메인 페이지(index.html)에 본인 링크 추가

`index.html`의 nav와 main `<ul>` 안에 다음 줄을 추가합니다:

```html
<li><a href="./members/이름.html">[본인 이름]의 소개</a></li>
```

> 모든 사람이 이 위치를 수정하므로, 이후 병합 시 충돌이 날 수 있습니다.

# 활동

## 💥 4단계: GitHub에 푸시 & Pull Request 생성

```bash
git add .
git commit -m "Add 자기소개 페이지: 이름"
git push origin feature/이름
```

- GitHub 웹사이트에서 Pull Request를 생성하세요.
- 팀원들과 충돌을 해결하거나 리뷰하면서 병합을 진행합니다.

------

## ⚔️ 5단계: 충돌(conflict) 발생 시 해결하기

> 대부분의 충돌은 `index.html`이나 `header`의 `<ul>` 항목 수정에서 발생합니다.

```html
<<<<<<< HEAD
<li><a href="./members/sample.html">길동</a></li>
=======
<li><a href="./members/jiwoo.html">지우</a></li>
>>>>>>> feature/jiwoo
```

- `<li>` 항목을 병합하여 두 사람의 링크가 모두 보이도록 정리합니다.
- 충돌 해결 후 `git add .` → `git commit` → `git push`로 해결 완료

------

## 🎯 확장 미션 (선택 과제)

- Git Pages를 활용해 완성한 웹사이트를 배포해보세요.
- `style.css`에 팀 고유 색상/폰트/버튼 스타일을 정의해보세요.
- 모든 페이지에 동일한 `nav`가 반복되는 것이 불편한가요?
  - 그렇다면 왜 불편한지, 어떻게 해결할 수 있을지 토의해보세요.

------

## 📝 제출 체크리스트

-  자기소개 HTML 파일 생성 완료
-  `index.html`에 본인 링크 추가
-  Pull Request 생성 및 병합 완료
-  Git 충돌 발생 시 해결 경험 완료 (선택적)
-  활동 후 소감 작성 (optional)

------

### 💡 힌트: 상대경로 이해하기

- `./` : 현재 폴더
- `../` : 한 단계 상위 폴더

| 현재 위치            | 링크 대상            | href 경로              |
| -------------------- | -------------------- | ---------------------- |
| `index.html`         | `members/jiwoo.html` | `./members/jiwoo.html` |
| `members/jiwoo.html` | `index.html`         | `../index.html`        |

------

### 🚀 활동 마무리 후 생각해 볼 질문들

- 공통 컴포넌트를 페이지마다 복사해 사용하는 것의 문제점은?
- 상대경로를 실수했을 때 나타나는 대표적인 현상은?
- 충돌을 방지하기 위한 브랜치 작성/병합 전략은?
- 실제 웹 개발에서 이런 문제들을 어떻게 해결할까?

------

> 협업은 단순히 코드를 나누는 것이 아니라 **함께 정리하고 구조를 이해하는 과정**입니다.
>  고생 많았어요! 🌱