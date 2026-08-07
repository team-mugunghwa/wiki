# wiki

## commit-message-style-guide
### Commit Message Format
```
<type>(<scope>): <subject>
<BLANK LINE>
<body>
<BLANK LINE>
<footer>
```

### Type
- **feat**: 새로운 기능 추가, 요구 사항 변경으로 인해 기존 기능 변경
- **fix**: 버그 수정
- **docs**: 문서 추가 및 수정 (주석 등)
- **style**: 코드 스타일 수정 (포매팅, 세미콜론 누락 등)
- **refactor**: 프로덕션 코드 리팩토링 (버그 수정이나 기능 추가를 제외한 코드 변경)
- **test**: 테스트 코드 추가 및 리팩토링 (기능을 구현할 때 테스트 코드를 함께 작성했다면 feat 사용)
- **chore**: 빌드, 배포 등 기타 작업들을 추가 및 수정
- **rename**: 파일명 변경
- **remove**: 파일 삭제
- **revert**: 작업 되돌리기


## Workflow

### 1. 이슈 생성
GitHub Issues에 작업 항목을 등록하고 이슈 번호를 발급받는다.

### 2. 로컬에서 develop 브랜치 최신화
```bash
git checkout develop
git pull origin develop
```

### 3. feature 브랜치 생성
```bash
git checkout -b feature/{이슈번호}-{작업명}
```
예: `feature/23-annual-leave-calendar`

### 4. 작업 진행
생성한 브랜치에서 작업하며, 커밋은 의미 단위로 나누고 Conventional Commits 규칙을 따른다.
```bash
git add .
git commit -m "feat: 휴가 신청 캘린더 UI 추가 (#23)"
```

### 5. 원격 저장소에 feature 브랜치 push
```bash
git push origin feature/{이슈번호}-{작업명}
```

### 6. PR(Pull Request) 생성 및 Merge
- `feature/{이슈번호}-{작업명}` → `develop`으로 PR 생성
- 이슈 번호 연결 (`Closes #23` 등 PR 본문에 명시 시, 머지 시 이슈 자동 종료)
- 리뷰어 지정 후 코드리뷰 진행
- 리뷰 승인 후 Merge


## Useful links

### 문서 및 일정 관리
https://www.notion.com/ko

https://trello.com/

https://www.atlassian.com/ko/software/jira

https://www.atlassian.com/ko/software/confluence

### 디자인
https://www.figma.com/ko-kr

### 다이어그램
https://www.drawio.com

https://excalidraw.com

https://mermaid.js.org

https://www.erdcloud.com

### 시스템 아키텍처
https://www.cloudcraft.co

### 일정 조율
https://lettucemeet.com
