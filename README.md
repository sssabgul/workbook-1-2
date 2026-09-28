# 공통수학2 전자칠판 워크북

문제 276개와 해설, 기하 보조 그림을 수업 중 표시하는 정적 웹앱입니다.

## 파일 구성

- `public/index.html`: 웹앱 전체. 문제·해설 이미지, CSS, JavaScript가 포함되어 있습니다.
- `netlify.toml`: Netlify 게시 폴더와 HTTP 헤더 설정.
- `.gitignore`: 로컬 원본 산출물, 임시 파일, 인증 정보 제외.

별도 패키지 설치, 빌드 명령, 서버, 환경 변수는 필요하지 않습니다.

## Netlify에서 GitHub 연동 배포

1. Netlify에 로그인하고 새 프로젝트를 Git 저장소에서 가져옵니다.
2. GitHub를 선택하고 `sssabgul/workbook-1-2` 저장소 접근을 허용합니다.
3. 배포 브랜치를 `main`으로 선택합니다.
4. Base directory와 Build command는 비워 두고 Publish directory를 `public`으로 설정합니다. 게시 폴더는 `netlify.toml`에도 지정되어 있습니다.
5. 배포를 실행하고 발급된 사이트 주소에서 워크북을 엽니다.

이후 `main`에 변경 사항을 푸시하면 연결된 Netlify 프로젝트가 자동으로 다시 배포합니다.

공식 설정 안내: https://docs.netlify.com/build/configure-builds/overview/

## 사용 및 수정

- `public/index.html`을 Chrome 또는 Edge로 열면 오프라인에서도 사용할 수 있습니다.
- 문제 목록이나 번호 입력으로 이동하고, 방향키로 이전·다음 문제를 표시합니다.
- 해설 보기 또는 Space 키로 해설을 열고 닫습니다.
- 기하 보조 그림이 있는 문제는 해당 버튼으로 그림을 표시합니다.
- 전체 화면 버튼이나 F11을 사용하고, 판서는 전자칠판 자체 도구를 사용합니다.
- 마지막 문제 번호는 각 브라우저의 로컬 저장소에 보관됩니다. 로컬 파일과 배포 사이트 사이에는 공유되지 않습니다.
- 웹앱을 수정할 때는 `public/index.html`을 변경하고 커밋·푸시합니다.

이미지가 포함되어 HTML 크기는 약 38 MB입니다. 첫 접속 시 전체 파일을 다운로드합니다.
로컬 `output/`의 원본 HTML과 PDF, `tmp/`의 변환 도구는 배포 대상과 Git 추적 대상에서 제외합니다.
