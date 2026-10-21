# Editables

make editable 스튜디오의 사내 작업 도구입니다. 미디어 변환 · 이름 일괄 변경 · SVN 형상관리 · 텍스처 도구 · 3D 뷰어를 한 앱에서 다룹니다.

이 저장소에는 설치 파일과 자동 업데이트 파일만 올라갑니다. 소스 코드는 비공개입니다.

> **사내 전용 소프트웨어입니다.** make editable 구성원만 사용할 수 있으며, 외부로 재배포할 수 없습니다.

## 설치

[Releases](https://github.com/ktk-ring/editables-releases/releases/latest)에서 운영체제에 맞는 파일을 받습니다.

| 운영체제 | 파일 |
| --- | --- |
| Windows 10 · 11 (x64) | `Editables-Setup-<버전>.exe` |
| macOS 12 이상 (Apple Silicon) | `Editables_<버전>_aarch64.dmg` |

`Editables_<버전>_x64-setup.exe` · `*.app.tar.gz` · `*.sig` · `latest.json`은 자동 업데이트용 파일입니다.

### 처음 실행할 때 경고

코드 서명 인증서를 쓰지 않는 사내 배포라, 처음 한 번 운영체제 경고가 표시됩니다.

- **Windows**: "Windows의 PC 보호" 창에서 **추가 정보 → 실행**
- **macOS**: DMG에서 Editables를 **응용 프로그램** 폴더로 끌어 놓은 뒤, 앱을 **우클릭 → 열기 → 열기**
  - "손상되었기 때문에 열 수 없습니다"가 표시되면 터미널에서 다음 명령을 실행한 뒤 다시 엽니다.

    ```bash
    xattr -dr com.apple.quarantine /Applications/Editables.app
    ```

## 업데이트

앱이 시작할 때 이 저장소의 `latest.json`으로 새 버전을 확인합니다. 새 버전이 있으면 사이드바에 표시되고, **설정 → 앱 정보**에서 설치 후 다시 시작합니다. 업데이트 파일은 서명으로 검증되며, 서명이 맞지 않으면 설치되지 않습니다.

## 라이선스

- Editables 자체에는 오픈소스 라이선스를 부여하지 않습니다. 모든 권리는 make editable에 있습니다.
- 함께 배포되는 FFmpeg(GPL v3) · Apache Subversion(Apache 2.0) · 글꼴(SIL OFL 1.1) · 라이브러리의 고지는 [THIRD-PARTY-NOTICES.md](THIRD-PARTY-NOTICES.md)에 있습니다. 앱의 **설정 → 앱 정보 → 오픈소스 라이선스**에서도 볼 수 있습니다.
