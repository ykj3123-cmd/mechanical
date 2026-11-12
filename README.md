# 열역학 표 계산기 Android App

사용자가 제공한 열역학 테이블을 기반으로 만든 오프라인 계산기 v4를
Android WebView 앱으로 패키징한 프로젝트입니다.

## 앱 기능
- Water / R134a 상태 자동 계산
- 선형보간 및 상태판정
- 기본 Rankine
- Reheat Rankine
- Regenerative Rankine
- R134a 이상 증기압축 냉동사이클
- 자가검산

앱은 `app/src/main/assets/index.html`을 로컬에서 읽기 때문에
계산 시 인터넷 연결이 필요하지 않습니다.

## Android Studio에서 APK 만들기
1. Android Studio에서 이 폴더를 Open 합니다.
2. Gradle Sync가 끝날 때까지 기다립니다.
3. Build > Build App Bundle(s) / APK(s) > Build APK(s)를 선택합니다.
4. 생성 APK:
   `app/build/outputs/apk/debug/app-debug.apk`

## GitHub Actions로 APK 만들기
프로젝트 전체를 GitHub 저장소의 main 브랜치에 올리면
`.github/workflows/build-apk.yml`이 자동으로 APK를 빌드합니다.
Actions 실행 결과의 `thermo-table-solver-apk` artifact에서 APK를 받을 수 있습니다.

## 요구사항
- Android 7.0(API 24) 이상
- compileSdk/targetSdk 35
- Java 17
