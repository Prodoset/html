# 오늘의 To-do 리스트 앱

현대적이고 아름다운 UI를 가진 React 기반 To-do 리스트 애플리케이션입니다.

## 🌟 주요 기능

- ✅ 할 일 추가/삭제
- ✅ 완료 상태 토글
- ✅ 로컬 스토리지에 데이터 저장
- ✅ 완료된 항목 일괄 삭제
- ✅ 반응형 디자인 (모바일 지원)
- ✅ 아름다운 그라데이션 UI
- ✅ 실시간 통계 표시

## 🚀 배포된 앱

**Live Demo**: [https://todo-app.onrender.com](https://todo-app.onrender.com)

## 🛠 기술 스택

- React 18
- CSS3 (그라데이션, 애니메이션)
- Lucide React (아이콘)
- LocalStorage (데이터 저장)

## 📦 설치 및 실행

### 로컬 개발

1. 의존성 설치:
```bash
npm install
```

2. 개발 서버 실행:
```bash
npm start
```

3. 브라우저에서 `http://localhost:3000` 접속

### 배포

이 앱은 Render를 통해 무료로 배포되었습니다. 배포 방법은 [DEPLOYMENT.md](./DEPLOYMENT.md)를 참조하세요.

## 📖 사용법

1. **할 일 추가**: 입력창에 할 일을 입력하고 + 버튼을 클릭하거나 Enter를 누릅니다.
2. **완료 표시**: 체크박스를 클릭하여 완료 상태를 토글합니다.
3. **삭제**: 휴지통 아이콘을 클릭하여 개별 항목을 삭제합니다.
4. **완료된 항목 일괄 삭제**: 하단의 "완료된 항목 삭제" 버튼을 클릭합니다.

## 📁 프로젝트 구조

```
src/
├── components/
│   ├── Header.js          # 앱 헤더 (제목, 날짜)
│   ├── TodoForm.js        # 할 일 입력 폼
│   ├── TodoList.js        # 할 일 목록 컨테이너
│   └── TodoItem.js        # 개별 할 일 아이템
├── App.js                 # 메인 앱 컴포넌트
├── index.js              # 앱 진입점
└── index.css             # 전역 스타일
```

## ✨ 특징

- **현대적인 UI**: 그라데이션과 블러 효과를 활용한 모던한 디자인
- **반응형**: 모바일과 데스크톱 모두에서 최적화된 경험
- **애니메이션**: 부드러운 호버 효과와 전환 애니메이션
- **데이터 지속성**: 브라우저를 닫아도 데이터가 유지됩니다
- **접근성**: 키보드 네비게이션과 스크린 리더 지원

## 🚀 배포 정보

- **호스팅**: Render (무료 플랜)
- **배포 방식**: Static Site
- **자동 배포**: GitHub main 브랜치 푸시 시 자동 배포
- **도메인**: `https://todo-app.onrender.com`

## 📝 빌드

프로덕션 빌드를 생성하려면:

```bash
npm run build
```

빌드된 파일은 `build` 폴더에 생성됩니다.

## 🤝 기여하기

1. 이 저장소를 Fork하세요
2. 새로운 기능 브랜치를 생성하세요 (`git checkout -b feature/amazing-feature`)
3. 변경사항을 커밋하세요 (`git commit -m 'Add some amazing feature'`)
4. 브랜치에 푸시하세요 (`git push origin feature/amazing-feature`)
5. Pull Request를 생성하세요

## 📄 라이선스

이 프로젝트는 MIT 라이선스 하에 배포됩니다.

## 📞 문의

프로젝트에 대한 질문이나 제안사항이 있으시면 GitHub Issues를 통해 연락해주세요. 