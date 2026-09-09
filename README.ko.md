# Copilot Studio 실습 가이드

[English](README.md) | [한국어](README.ko.md)

Copilot Studio 에이전트를 만들고 지식·도구를 연결한 뒤, 같은 자산으로 실제 동작을 확인하는 실습 자료입니다. 독립적으로 열 수 있는 **HTML 가이드 2종**과 **Create(생성) / Use(사용) 녹화 영상 4편**을 제공합니다.

**기본 문서 언어는 영어**이며 한국어 가이드도 함께 제공합니다. 두 언어 가이드에서 연결하는 영상은 동일합니다.

## 가이드 선택

| 가이드 | 대상과 목표 | English | 한국어 |
|---|---|---|---|
| 입문자 | 업무 담당자·처음 사용하는 제작자: 가상 HR FAQ, 근거 기반 답변, 휴가 입력 검증, 본인 Teams 사용 | [Open guide](copilot-studio-hands-on-lab.html) | [가이드 열기](copilot-studio-hands-on-lab.ko.html) |
| Azure 개발자 | 개발자: REST API, Foundry 모델, MCP, Foundry IQ 검색, 승인 워크플로의 인증·실행 계약 확인 | [Open guide](copilot-studio-lab-for-azure-devs.html) | [가이드 열기](copilot-studio-lab-for-azure-devs.ko.html) |

입문 핵심 경로는 **L01 → L02 → L03 → L09**입니다. 개발자 핵심 경로는 **L04 → L05 → L12 → L14 → L20**이며, 개발자 영상에는 **선택/Preview L08 Foundry Agent**도 포함합니다.

개발자 가이드는 입문 개념에 익숙하다고 가정하지만, 필요한 최소 에이전트 생성 절차는 자체적으로 제공합니다. 입문판 완료가 개발자판 완료를 뜻하지는 않습니다. 각 가이드 앞부분의 비교표에서 두 과정의 차이를 확인할 수 있습니다.

## 실습 녹화 영상

| 가이드 | Create · 생성 | Use · 사용 |
|---|---|---|
| 입문자 | [4분 33초](copilot-studio-hands-on-lab-create-20260909.mp4) | [3분 21초](copilot-studio-hands-on-lab-use-20260909.mp4) |
| Azure 개발자 | [10분 28초](copilot-studio-lab-for-azure-devs-create-20260909.mp4) | [9분 21초](copilot-studio-lab-for-azure-devs-use-20260909.mp4) |

영상은 **한국어 자막·실습 프롬프트·응답을 사용하는 기존 녹화본 그대로**입니다. 영문 가이드를 위해 번역·더빙하거나 영상을 교체하지 않았습니다. 실제 화면에서 대기·조작 실패 구간을 축약하고 일부 실제 프레임을 읽기 쉽게 정지한 **편집본**이며, 무편집 원테이크가 아닙니다.

HTML 가이드에는 구간별 타임스탬프가 있습니다. 영상 길이와 실제 실습 소요시간은 다르며 승인·프로비저닝·인덱싱·게시 대기 시간은 별도입니다.

## 가이드 열기

문서를 사용하기 위한 빌드나 패키지 설치는 필요하지 않습니다.

1. 저장소를 다운로드하거나 clone합니다.
2. MP4 파일을 같은 디렉터리에 둔 채 HTML 가이드를 브라우저로 엽니다.
3. **Create**부터 수행하고 생성한 자산을 보존한 뒤, 동일한 저장본으로 **Use**를 진행합니다.

로컬 파일에서 클립보드 등의 기능이 제한되면 해당 디렉터리를 로컬 서버로 제공할 수 있습니다.

```bash
python3 -m http.server 8000 --bind 127.0.0.1
```

서버 실행 후 다음 주소를 엽니다.

- 입문 한국어판: <http://127.0.0.1:8000/copilot-studio-hands-on-lab.ko.html>
- 개발자 한국어판: <http://127.0.0.1:8000/copilot-studio-lab-for-azure-devs.ko.html>

GitHub 파일 뷰어에서는 HTML 소스가 표시됩니다. 웹으로 제공하려면 GitHub Pages 등의 정적 호스팅을 설정한 뒤 각 HTML 주소로 접속합니다. 언어 전환과 영상 링크가 유지되도록 상대 파일명을 보존하세요.

## 언어와 재현성

영문판의 설명·내비게이션·표·접근성 문구는 영어로 제공합니다. 실행 계약과 기존 영상의 재현에 필요한 코드·식별자·한국어 입력 및 상태 값은 유지하며, 주변 영문 설명에서 사용 의미를 안내합니다.

각 가이드의 **English / 한국어** 링크로 같은 가이드의 언어를 전환할 수 있습니다. 진행 체크박스는 로컬 편의 기능이며 실제 클라우드 작업의 성공 증거는 아닙니다.

## 사전 준비와 안전

- 승인된 비운영 Sandbox, 제작 역할, 필요한 제품 라이선스·크레딧을 사용합니다. 로그인 성공만으로 권한이 준비된 것은 아닙니다.
- Azure 연동 실습에는 승인된 외부 자산·Connection·Microsoft Entra 인증·최소 권한 RBAC가 필요합니다. HTML을 여는 것만으로 자산이 생성되지는 않습니다.
- 가상 데이터와 승인된 본인 테스트 수신자·승인자만 사용합니다. 실제 HR 신청·지급을 수행하거나 다른 사람에게 시험 승인을 보내지 않습니다.
- 문서의 환경별 자산 이름과 ID는 녹화 환경의 예시입니다. 자신의 승인된 환경에 맞게 바꾸세요. **정리 명령은 자산을 삭제할 수 있으므로 실행 전에 범위를 확인해야 합니다.**
- API 키·토큰·자격 증명·개인정보를 커밋하지 않습니다. 실습 후 워크플로와 대기 승인을 정리하되 공유 자산을 일괄 삭제하지 않습니다.

## 주요 연동의 범위

| 영역 | 이 자료에서 다루는 경로 |
|---|---|
| Foundry Model | APIM endpoint를 경유하는 native BYOM. APIM이 managed identity로 모델 backend를 호출합니다. APIM subscription key와 Foundry API key는 다릅니다. |
| Foundry Agent | 준비된 Foundry agent와 Activity protocol을 사용하는 선택/Preview native 위임 경로입니다. |
| Foundry IQ | APIM HTTP proxy를 경유한 custom MCP 경로입니다. Native Foundry IQ의 성공이나 Consumption의 전용 MCP-server import 지원을 의미하지 않습니다. |
| 승인 워크플로 | 접수·실제 ID·입력 거부·자동 승인·본인 승인/반려를 다룹니다. 실제 출력 키·타입과 ID 해석을 문서에 명시했습니다. 자동 만료는 선택이며 검증 완료로 표시하지 않습니다. |

UI·가용 기능·라이선스·Preview 상태는 테넌트와 시점에 따라 달라질 수 있습니다. 각 가이드의 확인일·사전 조건·공식 출처·완료 기준을 사용하세요. 연결 표시나 HTTP 200만으로 종단 간 성공을 판단하지 않습니다.
