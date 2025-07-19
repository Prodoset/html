# 배포 가이드

이 가이드는 To-do 앱을 GitHub에 업로드하고 Render를 통해 무료로 배포하는 방법을 설명합니다.

## 1. GitHub에 코드 업로드

### 1.1 GitHub 저장소 생성
1. GitHub.com에 로그인
2. "New repository" 클릭
3. 저장소 이름: `todo-app` (또는 원하는 이름)
4. Public으로 설정
5. "Create repository" 클릭

### 1.2 로컬 코드를 GitHub에 푸시

```bash
# Git 초기화
git init

# 모든 파일 추가
git add .

# 첫 번째 커밋
git commit -m "Initial commit: Todo app with React"

# GitHub 원격 저장소 추가 (YOUR_USERNAME을 실제 사용자명으로 변경)
git remote add origin https://github.com/YOUR_USERNAME/todo-app.git

# 메인 브랜치로 푸시
git branch -M main
git push -u origin main
```

## 2. Render를 통한 배포

### 2.1 Render 계정 생성
1. [Render.com](https://render.com)에 접속
2. GitHub 계정으로 로그인

### 2.2 새 서비스 생성
1. Render 대시보드에서 "New +" 클릭
2. "Static Site" 선택

### 2.3 서비스 설정
- **Name**: `todo-app` (또는 원하는 이름)
- **Repository**: GitHub에서 생성한 저장소 선택
- **Branch**: `main`
- **Build Command**: `npm install && npm run build`
- **Publish Directory**: `build`

### 2.4 환경 변수 설정 (선택사항)
- **NODE_VERSION**: `18.0.0`

### 2.5 배포
1. "Create Static Site" 클릭
2. 배포가 완료될 때까지 대기 (보통 2-3분)
3. 제공된 URL로 접속하여 앱 확인

## 3. 자동 배포 설정

Render는 GitHub 저장소와 연결되어 있어서:
- `main` 브랜치에 푸시할 때마다 자동으로 재배포
- Pull Request를 생성하면 미리보기 URL 제공

## 4. 커스텀 도메인 설정 (선택사항)

1. Render 대시보드에서 서비스 선택
2. "Settings" 탭으로 이동
3. "Custom Domains" 섹션에서 도메인 추가
4. DNS 설정 업데이트

## 5. 문제 해결

### 빌드 실패 시
- `package.json`의 스크립트가 올바른지 확인
- Node.js 버전이 18 이상인지 확인
- 모든 의존성이 올바르게 설치되었는지 확인

### 404 에러 시
- `public/_redirects` 파일이 올바르게 생성되었는지 확인
- SPA 라우팅이 제대로 설정되었는지 확인

## 6. 성능 최적화

### 빌드 최적화
```bash
# 프로덕션 빌드
npm run build

# 빌드 크기 확인
npm install -g serve
serve -s build
```

### 환경 변수
- `GENERATE_SOURCEMAP=false`: 소스맵 생성 비활성화로 빌드 크기 감소

## 7. 모니터링

Render 대시보드에서:
- 배포 상태 확인
- 로그 확인
- 성능 메트릭 확인

## 8. 업데이트 배포

코드를 수정한 후:
```bash
git add .
git commit -m "Update: 새로운 기능 추가"
git push origin main
```

Render가 자동으로 새로운 배포를 시작합니다. 