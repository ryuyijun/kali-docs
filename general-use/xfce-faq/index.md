---
title: 칼리 리눅스 Xfce FAQ
description:
icon:
weight: 10
author: ["re4son",]
번역: ["xenix4845"]
---

새로운 칼리 리눅스 데스크톱은 믿을 수 없을 정도로 빠르고 매우 아름다워요. 빠르게 익숙해질 수 있도록 몇 가지 팁과 요령을 소개해요.

#### 주제

- [데스크톱 환경 전환하기](#switch-desktop-environments)
- [HiDPI](#hidpi)
- [테마](#theme)
- [터미널이 표시되지 않을 때](#no-terminal-showing-up)
- [언어 설정](#language-settings)
- [피드백](#feedback)

&nbsp;
&nbsp;
&nbsp;

#### 데스크톱 환경 전환하기

**Q:** 새로운 테마가 너무 마음에 들어서 꼭 갖고 싶은데, 시스템을 재설치하지 않고 가능할까요? 기존 칼리 리눅스 설치본을 어떻게 마이그레이션할 수 있을까요?

**A:** 터미널 세션에서 `sudo apt update && sudo apt install -y kali-desktop-xfce`를 실행하여 새로운 칼리 리눅스 Xfce 환경을 설치하세요. "*기본 디스플레이 관리자*"를 선택하라는 메시지가 표시되면 `lightdm`을 선택하세요.

다음으로, `update-alternatives --config x-session-manager`를 실행하고 Xfce 옵션을 선택하세요. Gnome 윈도우 매니저도 제거하고 싶다면(준비가 되었다고 확신하기 전까지는 권장하지 않음), `apt purge --autoremove kali-desktop-gnome`을 실행하세요. 이 작업은 Xfce 설정 *이후에* 실행해야 해요.

재부팅 후 다음 로그인 시 Xfce 테마가 적용될 거예요. `update-alternatives` 명령을 실행하지 않았다면, 로그인 화면의 오른쪽 상단 모서리에 있는 세션 선택기에서 "Xfce"를 선택할 수 있어요.

&nbsp;
&nbsp;

**Q:** Xfce를 설치했는데 미리보기처럼 보이지 않아요. 동일하게 만들려면 어떻게 해야 하나요?

**A:** 문제가 있는 경우, 구성 파일이 제대로 설정되지 않았을 수 있어요. 먼저 .cache, .config, .local을 백업하세요. 그다음, `rm -r .cache .config .local`을 실행한 후 재부팅하면 이러한 문제가 해결될 가능성이 높아요.

&nbsp;
&nbsp;

**Q:** Xfce 대신 GNOME이 있는 칼리 리눅스 이미지를 어떻게 얻을 수 있나요?

**A:** [kali.org/downloads/](/get-kali/)에서 Kali GNOME 이미지를 다운로드하면 돼요.

&nbsp;
&nbsp;

**Q:** Xfce를 사용해 봤는데 정말 좋지만, GNOME으로 다시 전환하고 싶어요. 어떻게 할 수 있나요?

**A:** 터미널 세션에서 `sudo apt update && sudo apt install -y kali-desktop-gnome`을 실행할 수 있어요.
다음 로그인 시 로그인 화면의 오른쪽 상단 모서리에 있는 세션 선택기에서 "GNOME"을 선택할 수 있어요.

&nbsp;
&nbsp;

#### HiDPI

**Q:** HiDPI 화면을 사용하고 있는데 모든 것이 너무 작게 보여요. 개선할 방법이 있나요?

**A:** [HiDPI 페이지](/docs/general-use/hidpi/)를 참조하세요.

&nbsp;
&nbsp;

#### 화면 캡처

**Q:** 스크린샷을 어떻게 찍을 수 있나요?

**A:** 키보드의 `Print Screen` 키를 누르면 스크린슈터가 실행돼요. Enter를 누르면 스크린샷이 찍혀요. 또는 빠른 실행 패널(애플리케이션 메뉴 옆 패널의 맨 오른쪽 아이콘)에서 "*스크린 레코더*" 아이콘을 클릭하고 "스크린샷"을 선택할 수 있어요.

&nbsp;
&nbsp;

**Q:** 화면 활동을 비디오로 어떻게 녹화할 수 있나요?

**A:** 키보드에서 `Ctrl` & `Print Screen`을 누르면 스크린 레코더가 실행돼요. `Enter`를 누르면 녹화가 시작돼요. 또는 빠른 실행 패널(애플리케이션 메뉴 옆 패널의 맨 오른쪽 아이콘)에서 "*스크린 레코더*" 아이콘을 클릭할 수도 있어요.

&nbsp;
&nbsp;

#### 테마

**Q:** 더 밝은 테마로 어떻게 전환할 수 있나요?

**A:** 칼리 리눅스는 두 가지 기본 테마를 제공해요: 다크와 라이트.
라이트 테마로 전환하려면,
"*설정 -> 모양새*"로 이동하여:

&nbsp;&nbsp;&nbsp;&nbsp;\- "*스타일*" 탭에서 "*Kali-Light*" 선택
&nbsp;&nbsp;&nbsp;&nbsp;\- "아이콘" 탭에서 "Flat-Remix-Blue-Light" 선택

"*설정 -> 윈도우 관리자*"로 이동하여:

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;\- "*스타일*" 탭에서 "*Kali-Light*" 선택

"*라이트*"에서 "*다크*"로 전환하려면, 이 설정에서 다크 테마를 선택하면 돼요.

&nbsp;
&nbsp;

**Q:** 오른쪽에 있는 버튼들이 마음에 들지만, 왼쪽에 있으면 더 좋겠어요. 어떻게 전환할 수 있나요?

**A:** "*설정 -> 윈도우 관리자 -> 스타일 -> 버튼 레이아웃*"에서 버튼을 한쪽에서 다른 쪽으로 이동할 수 있어요. "Title" 단어의 다른 쪽으로 끌어다 놓기만 하면 돼요.

&nbsp;
&nbsp;

#### 터미널이 표시되지 않을 때

**Q:** 터미널을 실행하려고 할 때 창은 나타나지만 내용이 비어 있어요, 왜 그런가요?

**A:** 그래픽과 사용 중인 xfwm4 컴포지터에 문제가 있을 수 있어요.
컴포지터를 비활성화하려면,
데스크톱의 메인 메뉴에서 "*설정 -> 윈도우 관리자 트윅*"으로 이동하여:

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;\- "*컴포지터*" 탭에서, 디스플레이 컴포지팅 활성화 체크 해제

여전히 컴포지터를 원하지만 xfwm4 컴포지터가 작동하지 않는다면, "*compton*"과 같은 대안을 사용할 수 있어요.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;\- `sudo apt install -y compton`

그런 다음 로그인 시 자동 실행되도록 하려면,
"*설정 -> 세션 및 시작*"으로 이동하여:

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;\- "*애플리케이션 자동 시작*" 탭에서, "*추가*"를 클릭하고 이름에 "*Compton*", 명령에 "*compton*"을 입력한 다음 "*확인*"을 클릭하고, 로그아웃했다가 다시 로그인하세요.

또는 VM에서 이 문제가 발생하는 경우 VM 설정에서 3D 가속을 비활성화하세요.

&nbsp;

#### 언어 설정

**Q:** GUI 언어를 어떻게 변경할 수 있나요?

**A:** LightDM 로그인 화면에서 상단 패널의 오른쪽에 있는 언어 선택기를 사용하여 원하는 언어를 선택하세요.

&nbsp;&nbsp;&nbsp;

**Q:** 키보드 레이아웃을 어떻게 변경할 수 있나요?

**A:** 키보드 레이아웃은 "*설정 -> 키보드 -> 레이아웃*"에서 변경할 수 있어요.

&nbsp;

**Q:** "*설정 -> 키보드 -> 레이아웃*"을 통해 사용할 수 없는 다른 입력 방법(예: 일본어(Anthy))을 어떻게 설정할 수 있나요?

**A:** 다양한 입력 방법을 구성하기 위해 ibus를 설치할 수 있어요. Anthy의 경우 ibus-anthy도 설치해야 해요:

`sudo apt install -y ibus ibus-anthy`

이제 "*설정 -> iBus 환경설정*"을 통해 다양한 입력 방법을 추가하고 구성할 수 있어요.
구성이 완료되면, 패널 오른쪽에 새로 추가된 "iBus" 아이콘을 사용하여 선호하는 입력 방법을 선택할 수 있어요.
사용 가능한 입력 방법 엔진 목록은 다음을 참조하세요:

https://en.wikipedia.org/w/index.php?title=Intelligent_Input_Bus#Available_input_method_plugins_and_engines

&nbsp;

#### 피드백

**Q:** 질문이 있는데 어떻게 연락할 수 있나요?

**A:** [Kali 포럼](https://forums.kali.org/)에 가입하세요. 활발한 커뮤니티의 본거지이며 칼리 리눅스에 관한 모든 것을 논의하기 위한 최적의 장소예요.

&nbsp;
&nbsp;

**Q:** 버그를 발견했어요. 누구에게 말해야 하나요?

**A:** 멋져요. 버그가 있다는 사실이 아니라 당신이 그것을 발견했다는 것이요. [칼리 리눅스 버그 트래커](https://bugs.kali.org/)에 버그 리포트를 열어주세요. 칼리 리눅스를 개선하는 데 도움을 주셔서 정말 감사해요.
