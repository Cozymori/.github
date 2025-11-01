# RepublicOfGamja 프로젝트 기여 가이드

RepublicOfGamja에 기여하는 것에 관심을 가져주셔서 감사합니다! 우리는 모든 사람의 기여를 환영합니다. 프로젝트에 참여함으로써 [행동 강령](../../CODE_OF_CONDUCT.md)을 준수하는 것에 동의하게 됩니다.

## 시작하기

### 사전 준비사항

기여하기 전에 다음 사항들을 확인해주세요:
- GitHub 계정
- 로컬 머신에 Git 설치
- Git 및 GitHub 워크플로우에 대한 기본 이해
- 프로젝트 기술 스택에 대한 익숙함

### 개발 환경 설정

1. 저장소를 GitHub 계정으로 포크하세요
2. 포크한 저장소를 로컬에 클론하세요:
```bash
   git clone https://github.com/YOUR-USERNAME/REPOSITORY-NAME.git
   cd REPOSITORY-NAME
```
3. 원본 저장소를 upstream 원격으로 추가하세요:
```bash
   git remote add upstream https://github.com/RepublicOfGamja/REPOSITORY-NAME.git
```
4. 작업을 위한 새 브랜치를 생성하세요:
```bash
   git checkout -b feature/your-feature-name
```

## 기여 방법

### 이슈 보고

이슈를 생성하기 전에:
- 중복을 피하기 위해 기존 이슈를 검색하세요
- 가능한 경우 이슈 템플릿을 사용하세요
- 명확하고 자세한 정보를 제공하세요

버그를 보고할 때 포함할 사항:
- 버그 설명
- 재현 단계
- 예상 동작
- 실제 동작
- 스크린샷 (해당하는 경우)
- 환경 세부정보 (OS, 브라우저, 버전 등)

기능 요청의 경우 설명할 사항:
- 해결하려는 문제
- 제안하는 해결책
- 고려한 대안

### 코드 기여

#### 코드 스타일

- 프로젝트의 기존 코드 스타일을 따르세요
- 의미 있는 변수 및 함수 이름 사용
- 가능한 경우 자체 문서화 코드 작성
- 복잡한 로직에 대한 주석 추가
- 함수를 작고 집중적으로 유지
- 언어별 규칙 준수

#### 테스트

- 새 기능에 대한 테스트 작성
- 모든 기존 테스트가 통과하는지 확인
- 기존 기능을 수정할 때 테스트 업데이트
- 좋은 테스트 커버리지 목표

## Git 커밋 메시지 가이드

### 커밋 메시지 형식
```
<type>(<scope>): <subject>
```
- **type**: 커밋 타입 (필수)
- **scope**: 변경 범위 (선택)
- **subject**: 간단한 설명 (필수)

### 커밋 타입

#### feat: 새로운 기능
```bash
feat: Add new feature
feat(auth): Add user signup API endpoint
```

#### fix: 버그 수정
```bash
fix: Fix bug
fix(parser): Fix null pointer exception
```

#### docs: 문서 수정
```bash
docs: Update documentation
docs(readme): Update installation guidelines
```

#### style: 코드 스타일 변경 (기능 변경 없음)
```bash
style: Change code formatting
style(api): Apply Prettier formatting
```

#### refactor: 코드 리팩토링 (기능 변경 없음)
```bash
refactor: Improve code structure
refactor(user): Simplify UserService logic
```

#### test: 테스트 코드 추가/수정
```bash
test: Add or modify tests
test(auth): Add test cases for login failures
```

#### chore: 빌드, 설정 등 기타 작업
```bash
chore: Update build configuration
chore: Add *.log to .gitignore
```

#### perf: 성능 개선
```bash
perf: Improve performance
perf(api): Optimize database query
```

#### ci: CI/CD 설정 변경
```bash
ci: Update CI pipeline
ci: Add GitHub Actions workflow
```

#### build: 빌드 시스템 변경
```bash
build: Update dependencies
build: Update webpack configuration
```

#### revert: 이전 커밋 되돌리기
```bash
revert: Revert "feat: Add new feature"
```

### 작성 규칙

#### 1. 명령형 현재형 사용

✅ 좋은 예:
```bash
feat(auth): Add user login functionality
fix(api): Resolve CORS issue
docs: Update API documentation
```

❌ 나쁜 예:
```bash
feat(auth): Added user login functionality
fix(api): Resolved CORS issue
docs: Updated API documentation
```

#### 2. 제목은 50자 이내로 작성
```bash
✅ feat(auth): Add OAuth2 authentication
❌ feat(auth): Add OAuth2 authentication with Google, Facebook, and Twitter providers
```

#### 3. 제목 첫 글자는 대문자로
```bash
✅ feat: Add new feature
❌ feat: add new feature
```

#### 4. 제목 끝에 마침표 사용 금지
```bash
✅ feat: Add user authentication
❌ feat: Add user authentication.
```

#### 5. scope를 사용하여 변경 범위 명시
```bash
feat(auth): Add login endpoint
feat(user): Add profile page
feat(api): Add rate limiting
fix(database): Fix connection pool leak
```

### 고급 사용법

#### Breaking Changes (주요 변경사항)
```bash
feat(api)!: Change authentication method to OAuth2

BREAKING CHANGE: JWT authentication is replaced with OAuth2.
Users need to update their authentication flow.
```

#### 여러 단락 사용
```bash
feat(auth): Add two-factor authentication

Implement TOTP-based 2FA using Google Authenticator.
Users can enable 2FA in their account settings.

Closes #123
```

#### 이슈 연결
```bash
fix(parser): Fix null pointer exception

Fixes #456
Closes #789
Related to #234
```

#### 커밋 되돌리기
```bash
revert: Revert "feat(auth): Add OAuth2 support"

This reverts commit a1b2c3d4e5f6.
Reason: OAuth2 implementation caused performance issues.
```

### 전체 예시

**예시 1: 새로운 기능**
```bash
feat(auth): Add user signup API endpoint
```

**예시 2: 버그 수정**
```bash
fix(parser): Fix null pointer exception in data parsing
```

**예시 3: 문서 수정**
```bash
docs(readme): Update installation guidelines
```

**예시 4: 스타일 변경**
```bash
style(api): Apply Prettier formatting
```

**예시 5: 리팩토링**
```bash
refactor(user): Simplify UserService logic
```

**예시 6: 테스트**
```bash
test(auth): Add test cases for login failures
```

**예시 7: 기타 작업**
```bash
chore: Add *.log to .gitignore
```

**예시 8: 성능 개선**
```bash
perf(database): Add index to user_id column
```

**예시 9: CI/CD**
```bash
ci: Add automated testing workflow
```

**예시 10: Breaking Change**
```bash
feat(api)!: Change response format to REST standard

BREAKING CHANGE: API responses now follow REST conventions.
Update client code to handle new response structure.
```

### 빠른 참조

| 타입     | 목적           | 예시                       |
|----------|----------------|----------------------------|
| feat     | 새로운 기능    | feat(auth): Add login      |
| fix      | 버그 수정      | fix(api): Fix CORS         |
| docs     | 문서           | docs: Update README        |
| style    | 포맷팅         | style: Apply linter        |
| refactor | 리팩토링       | refactor: Clean up code    |
| test     | 테스트         | test: Add unit tests       |
| chore    | 유지보수       | chore: Update deps         |
| perf     | 성능           | perf: Optimize query       |
| ci       | CI/CD          | ci: Add workflow           |
| build    | 빌드 시스템    | build: Update config       |
| revert   | 되돌리기       | revert: Revert commit      |

### 팁

- **구체적으로 작성**: 가능하면 scope 포함
- **간결하게 작성**: 제목은 짧고 명확하게
- **일관성 유지**: 팀 컨벤션 따르기
- **설명적으로 작성**: 무엇을 왜 했는지 설명 (어떻게가 아님)
- **본문 활용**: 복잡한 변경사항은 본문에 상세히 작성

### 자주 사용하는 Scope

- **auth**: 인증/인가
- **api**: API 엔드포인트
- **ui**: 사용자 인터페이스
- **database**: 데이터베이스 변경
- **config**: 설정
- **deps**: 의존성
- **security**: 보안 관련
- **i18n**: 국제화
- **a11y**: 접근성
- **seo**: SEO 관련

## Pull Request 프로세스

### PR 제출 전

1. 프로젝트 스타일 가이드라인을 따르는지 확인
2. 기능 변경 시 문서 업데이트
3. 필요한 경우 테스트 추가 또는 업데이트
4. 로컬에서 테스트 스위트 실행
5. 최신 upstream main/master에 브랜치 리베이스
6. 깔끔한 히스토리 유지를 위해 필요시 커밋 스쿼시

### PR 제출

1. 포크한 저장소에 변경사항 푸시
2. upstream 저장소로 Pull Request 생성
3. PR 템플릿 완전히 작성
4. 관련 이슈 연결
5. 필요시 메인테이너에게 리뷰 요청

### 리뷰 중

- 피드백에 신속히 응답
- 요청된 변경사항을 새 커밋으로 작성
- 같은 브랜치에 변경사항 푸시
- 피드백 해결 후 리뷰 재요청
- 리뷰 프로세스 동안 인내심과 존중 유지

### 머지 후

- 로컬 브랜치 삭제
- upstream에서 최신 변경사항 가져오기
- 포크 동기화 유지

## 커뮤니티

### 도움 받기

- 먼저 문서 확인
- 기존 이슈 및 토론 검색
- 토론이나 적절한 채널에서 질문
- 도움 요청 시 명확한 컨텍스트 제공

### 인정

우리는 다음을 포함한 모든 기여를 소중히 여깁니다:
- 코드 기여
- 문서 개선
- 버그 보고
- 기능 제안
- 커뮤니티에서 다른 사람 돕기
- 프로젝트 홍보

기여자들은 프로젝트 README 파일과 릴리스 노트에서 인정받게 됩니다.

## 라이선스

RepublicOfGamja 프로젝트에 기여함으로써, 귀하의 기여가 프로젝트와 동일한 라이선스 하에 라이선스됨에 동의합니다.

RepublicOfGamja에 기여해주셔서 감사합니다! 🎉