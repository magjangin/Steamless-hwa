# Steamless-hwa

Steamless는 atom0s가 개발한 SteamStub DRM 언팩 도구입니다. 이 저장소(`Steamless-hwa`)는 **화영왕 (Hwa-young-wang)**이 유지 관리하는 포크 버전입니다.

Steamless는 컴파일된 실행 파일(PE32/PE64)에서 SteamStub DRM을 언팩하여 역공학(Reverse Engineering) 및 모딩을 원활하게 진행할 수 있도록 돕습니다.

---

## 🚀 주요 기능

- **SteamStub DRM 제거**: SteamStub 1.x, 2.x, 3.x 버전을 지원하며 x86 및 x64 아키텍처 모두를 타겟으로 합니다.
- **GUI 및 CLI 모두 지원**:
  - 사용자 친화적인 WPF 기반의 그래픽 인터페이스(`Steamless`)
  - 자동화 스크립트에 최적화된 명령줄 인터페이스(`Steamless.CLI`)
- **확장 가능한 플러그인 아키텍처**: Steamless API를 활용하여 커스텀 언팩 모듈 및 새로운 언팩 배리언트를 쉽게 추가할 수 있습니다.

---

## 🛠️ 프로젝트 구조

- **Steamless**: WPF 기반의 메인 데스크톱 프로그램입니다.
- **Steamless.CLI**: CLI 명령줄 기반 언팩 도구입니다.
- **Steamless.API**: 커스텀 플러그인 개발을 위한 코어 API 라이브러리입니다.
- **Steamless.Unpacker.Variant***: 기본으로 탑재된 SteamStub 언팩 알고리즘 구현체들입니다.
- **ExamplePlugin**: Steamless API를 활용한 플러그인 예제 프로젝트입니다.

---

## 💻 요구 사항

- **.NET Framework 4.8** 이상
- Windows OS (GUI 실행용)

---

## ⚙️ 빌드 방법

1. **Visual Studio 2022** 이상 버전으로 `Steamless.sln` 솔루션 파일을 엽니다.
2. 빌드 구성을 `Release`로 설정하고 대상 플랫폼을 `Any CPU`, `x86`, 또는 `x64`로 지정합니다.
3. NuGet 패키지 복원이 자동으로 진행되지 않을 경우 수동으로 복원합니다.
4. 솔루션을 빌드합니다.

---

## 📜 사용법

### GUI (Steamless)
1. `Steamless.exe`를 실행합니다.
2. SteamStub DRM이 적용된 대상 실행 파일을 찾아 열거나 드래그 앤 드롭합니다.
3. 언팩 옵션(섹션 헤더 유지, 임포트 바인딩 등)을 구성합니다.
4. **Unpack File** 버튼을 클릭합니다. 언팩된 실행 파일은 원본 파일과 동일한 경로에 `.unpacked`가 붙어 저장됩니다.

### CLI (Steamless.CLI)
명령 프롬프트(CMD) 또는 터미널에서 실행합니다:
```cmd
Steamless.CLI.exe --file <실행파일_경로> [옵션]
```

---

## 🤝 크레딧 및 감사의 말

- **atom0s**: Steamless의 최초 개발자입니다.
- SteamStub DRM 배리언트를 분석하고 우회법을 정립한 모든 역공학 연구원 및 기여자분들께 감사드립니다.
