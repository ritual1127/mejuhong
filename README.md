# 몽글 파일함 🌷

GitHub Pages에 올려 사용할 수 있는 간단한 파일 공유 페이지입니다.

## 1. 파일 추가하기
1. `files` 폴더에 공유할 PDF 또는 MP4 동영상을 넣습니다.
2. `index.html`을 메모장 또는 VS Code로 엽니다.
3. `const ACCESS_PASSWORD = "1234";`에서 비밀번호를 바꿉니다.
4. `const FILES = [ ... ];` 부분에 파일 정보를 추가합니다.

예시:
```js
const FILES = [
  {
    name: "프로젝트 안내문.pdf",
    path: "files/project-guide.pdf",
    type: "pdf",
    size: "1.2 MB",
    description: "프로젝트 안내 자료"
  },
  {
    name: "소개 영상.mp4",
    path: "files/intro.mp4",
    type: "video",
    size: "18 MB",
    description: "프로젝트 소개 영상"
  }
];
```

파일 이름과 `path`의 파일명이 정확히 일치해야 합니다. `type`은 PDF일 때 `pdf`, 동영상일 때 `video`입니다.

## 2. GitHub Pages 배포
1. GitHub에서 새 저장소(repository)를 만듭니다.
2. `index.html`, `files` 폴더, 이 README를 저장소 최상위에 업로드합니다.
3. 저장소의 **Settings → Pages**로 이동합니다.
4. **Build and deployment → Deploy from a branch**를 선택합니다.
5. Branch는 `main`, 폴더는 `/ (root)`로 선택하고 Save를 누릅니다.
6. 잠시 기다리면 `https://사용자이름.github.io/저장소이름/` 주소로 접속할 수 있습니다.

## 3. 보안 관련 안내
이 프로젝트는 요청하신 **간단 잠금형**입니다. 비밀번호가 브라우저에 전달되는 HTML/JavaScript 안에 들어 있으므로 개발자 도구나 페이지 소스에서 확인할 수 있습니다. 또한 파일 주소를 직접 아는 사람은 로그인 화면을 거치지 않고 파일에 접근할 수 있습니다.

따라서 공개되어도 괜찮은 자료를 편하게 공유하는 용도로만 사용하세요. 개인정보, 비밀 문서, 민감한 파일을 보호하는 용도로는 사용하면 안 됩니다. 실제 접근 제어가 필요하면 서버 측 비밀번호 검증과 비공개 파일 저장소를 사용해야 합니다.
