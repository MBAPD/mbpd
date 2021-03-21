Bukkit API로 플러그인을 개발하기 위해서는 기반 서버 소프트웨어를 의존(Dependent)해야 개발할 수 있다. 서버 소프트웨어를 기반으로 작성하지 않으면 Bukkit API가 제공하는 기능들을 호출할 수 없을테니 말이다.

상위 문서인 **1. 기본 세팅하기**에서도 언급했지만, Bukkit API는 Bukkit -> Spigot -> Paper ... 등 여러가지 포크 버전이 있으며, 이 중 가장 다운로드 과정이 편하고 가장 대중적으로 사용되는 Paper를 사용하도록 하겠다.

# Paper 설치

[https://papermc.io/downloads](https://papermc.io/downloads) - Paper 공식 다운로드 사이트

상기된 사이트에서 아래 이미지를 따라한다.

![](https://raw.githubusercontent.com/MBAPD/mbpd/main/%E2%85%A0.%20%EB%A7%A8%20%EB%95%85%EC%97%90%20%ED%97%A4%EB%94%A9%ED%95%98%EA%B8%B0/1.%20%EA%B8%B0%EB%B3%B8%20%EC%84%B8%ED%8C%85%ED%95%98%EA%B8%B0/2%20-%20Paper%20%EC%84%A4%EC%B9%98%ED%95%98%EA%B8%B0/1.png)

작성일 기준 가장 최신 빌드의 Paper를 다운받아 주었다.

![](https://raw.githubusercontent.com/MBAPD/mbpd/main/%E2%85%A0.%20%EB%A7%A8%20%EB%95%85%EC%97%90%20%ED%97%A4%EB%94%A9%ED%95%98%EA%B8%B0/1.%20%EA%B8%B0%EB%B3%B8%20%EC%84%B8%ED%8C%85%ED%95%98%EA%B8%B0/2%20-%20Paper%20%EC%84%A4%EC%B9%98%ED%95%98%EA%B8%B0/2.png)

경로는 자신이 원하는 곳에 받아둔다. 저장할 파일 이름은 원본 그대로 사용해도 좋으나 편의상 여기서는 `paper.jar`로 임의로 변경했다.

혹시나! 싶어서 이야기하지만 만약 파일의 확장자 (`.jar`, `.txt` 등...)가 보이지 않는 경우는, 폴더 탐색기 창 상단의 **보기** 탭 > 가장 우측의 **옵션** > 상단 두번째 **보기** 탭 > 스크롤을 내려 **알려진 파일 형식의 파일 확장명 숨기기** 를 **체크 해제**한다.

![](https://raw.githubusercontent.com/MBAPD/mbpd/main/%E2%85%A0.%20%EB%A7%A8%20%EB%95%85%EC%97%90%20%ED%97%A4%EB%94%A9%ED%95%98%EA%B8%B0/1.%20%EA%B8%B0%EB%B3%B8%20%EC%84%B8%ED%8C%85%ED%95%98%EA%B8%B0/2%20-%20Paper%20%EC%84%A4%EC%B9%98%ED%95%98%EA%B8%B0/3.png)

`paper.jar`를 설치한 폴더에 새 텍스트 파일을 생성해 준다.

![](https://raw.githubusercontent.com/MBAPD/mbpd/main/%E2%85%A0.%20%EB%A7%A8%20%EB%95%85%EC%97%90%20%ED%97%A4%EB%94%A9%ED%95%98%EA%B8%B0/1.%20%EA%B8%B0%EB%B3%B8%20%EC%84%B8%ED%8C%85%ED%95%98%EA%B8%B0/2%20-%20Paper%20%EC%84%A4%EC%B9%98%ED%95%98%EA%B8%B0/4.png)

해당 텍스트 파일의 이름을 `open_server.bat` 으로 변경해준다.

![](https://raw.githubusercontent.com/MBAPD/mbpd/main/%E2%85%A0.%20%EB%A7%A8%20%EB%95%85%EC%97%90%20%ED%97%A4%EB%94%A9%ED%95%98%EA%B8%B0/1.%20%EA%B8%B0%EB%B3%B8%20%EC%84%B8%ED%8C%85%ED%95%98%EA%B8%B0/2%20-%20Paper%20%EC%84%A4%EC%B9%98%ED%95%98%EA%B8%B0/5.png)

생성한 `open_server.bat` 파일을 우클릭 > 편집(E)을 클릭하여 메모장 창을 켠다.

![](https://raw.githubusercontent.com/MBAPD/mbpd/main/%E2%85%A0.%20%EB%A7%A8%20%EB%95%85%EC%97%90%20%ED%97%A4%EB%94%A9%ED%95%98%EA%B8%B0/1.%20%EA%B8%B0%EB%B3%B8%20%EC%84%B8%ED%8C%85%ED%95%98%EA%B8%B0/2%20-%20Paper%20%EC%84%A4%EC%B9%98%ED%95%98%EA%B8%B0/6.png)

빈 메모장에 `java -jar paper.jar`를 입력한다. 만약 아까 다운로드 받은 jar 파일의 이름이 다른 경우 해당 파일의 이름으로 `paper.jar` 부분을 변경한다. 

수정 및 저장 후 메모장을 닫고, `open_server.bat`을 더블 클릭하여 배치 파일을 실행한다.

![](https://raw.githubusercontent.com/MBAPD/mbpd/main/%E2%85%A0.%20%EB%A7%A8%20%EB%95%85%EC%97%90%20%ED%97%A4%EB%94%A9%ED%95%98%EA%B8%B0/1.%20%EA%B8%B0%EB%B3%B8%20%EC%84%B8%ED%8C%85%ED%95%98%EA%B8%B0/2%20-%20Paper%20%EC%84%A4%EC%B9%98%ED%95%98%EA%B8%B0/7.png)

위와 같이 명령 프롬프트에 `Downloading vanilla jar...` 와 `Patching vanilla jar...` 이후 시스템 상의 Java 버전을 출력하고 `Loading libraries... please wait...` 메세지가 출력됐으면 이제 창을 닫아도 된다. 사실 굳이 안 닫아도 얼마 있다가 짧은 단말마 후에 지가 알아서 닫힌다.

![](https://raw.githubusercontent.com/MBAPD/mbpd/main/%E2%85%A0.%20%EB%A7%A8%20%EB%95%85%EC%97%90%20%ED%97%A4%EB%94%A9%ED%95%98%EA%B8%B0/1.%20%EA%B8%B0%EB%B3%B8%20%EC%84%B8%ED%8C%85%ED%95%98%EA%B8%B0/2%20-%20Paper%20%EC%84%A4%EC%B9%98%ED%95%98%EA%B8%B0/8.png)

명령 프롬프트 창의 짧은 단말마 이후, 같은 폴더 안에 `cache` 폴더가 생성되었을 것이다. 폴더 안을 들어가 보자.

![](https://raw.githubusercontent.com/MBAPD/mbpd/main/%E2%85%A0.%20%EB%A7%A8%20%EB%95%85%EC%97%90%20%ED%97%A4%EB%94%A9%ED%95%98%EA%B8%B0/1.%20%EA%B8%B0%EB%B3%B8%20%EC%84%B8%ED%8C%85%ED%95%98%EA%B8%B0/2%20-%20Paper%20%EC%84%A4%EC%B9%98%ED%95%98%EA%B8%B0/9.png)

안을 보면 사진처럼 `mojang`으로 시작하는 jar 파일과 `patched`로 시작하는 jar 파일이 존재할 것인데, 우리의 관심사는 바로 `patched`로 시작하는 파일이다. 사진에서는 `patched_1.16.5.jar` 파일이며, 우리는 이 파일을 프로젝트가 의존하도록 하여 개발을 시작할 것이다.

# IntelliJ 프로젝트에 Paper를 라이브러리로 등록하기

IntelliJ IDEA & JDK 설치 과정 이후 끄지 않고 계속 진행하는 중에는 상관없지만, 혹시 창을 끈 경우에는 다시 IntelliJ IDEA를 검색하여 프로그램을 실행시켜주자.

![](https://raw.githubusercontent.com/MBAPD/mbpd/main/%E2%85%A0.%20%EB%A7%A8%20%EB%95%85%EC%97%90%20%ED%97%A4%EB%94%A9%ED%95%98%EA%B8%B0/1.%20%EA%B8%B0%EB%B3%B8%20%EC%84%B8%ED%8C%85%ED%95%98%EA%B8%B0/2%20-%20Paper%20%EC%84%A4%EC%B9%98%ED%95%98%EA%B8%B0/10.png)

자동으로 어제 만들었던, 마지막으로 열었던 프로젝트를 보여줄 것이다. 사진대로 우리가 생성했던 프로젝트를 우클릭, **Open Module Settings**를 클릭해 주자.


![](https://raw.githubusercontent.com/MBAPD/mbpd/main/%E2%85%A0.%20%EB%A7%A8%20%EB%95%85%EC%97%90%20%ED%97%A4%EB%94%A9%ED%95%98%EA%B8%B0/1.%20%EA%B8%B0%EB%B3%B8%20%EC%84%B8%ED%8C%85%ED%95%98%EA%B8%B0/2%20-%20Paper%20%EC%84%A4%EC%B9%98%ED%95%98%EA%B8%B0/11.png)

좌측의 **Libraries** 클릭, 상단의 **+ 버튼** 클릭, **Java**를 클릭하자.

![](https://raw.githubusercontent.com/MBAPD/mbpd/main/%E2%85%A0.%20%EB%A7%A8%20%EB%95%85%EC%97%90%20%ED%97%A4%EB%94%A9%ED%95%98%EA%B8%B0/1.%20%EA%B8%B0%EB%B3%B8%20%EC%84%B8%ED%8C%85%ED%95%98%EA%B8%B0/2%20-%20Paper%20%EC%84%A4%EC%B9%98%ED%95%98%EA%B8%B0/12.png)

아까 생성했던 `patched_1.16.5.jar` 파일을 선택하고 **OK**를 누른다.

![](https://raw.githubusercontent.com/MBAPD/mbpd/main/%E2%85%A0.%20%EB%A7%A8%20%EB%95%85%EC%97%90%20%ED%97%A4%EB%94%A9%ED%95%98%EA%B8%B0/1.%20%EA%B8%B0%EB%B3%B8%20%EC%84%B8%ED%8C%85%ED%95%98%EA%B8%B0/2%20-%20Paper%20%EC%84%A4%EC%B9%98%ED%95%98%EA%B8%B0/13.png)

방금 추가한 라이브러리를 어느 모듈에 넣을 것이냐고 묻는 창이다. 우린 직접 추가할 것이기 때문에 **Cancel**을 눌러주자.

![](https://raw.githubusercontent.com/MBAPD/mbpd/main/%E2%85%A0.%20%EB%A7%A8%20%EB%95%85%EC%97%90%20%ED%97%A4%EB%94%A9%ED%95%98%EA%B8%B0/1.%20%EA%B8%B0%EB%B3%B8%20%EC%84%B8%ED%8C%85%ED%95%98%EA%B8%B0/2%20-%20Paper%20%EC%84%A4%EC%B9%98%ED%95%98%EA%B8%B0/14.png)

Paper jar 파일을 라이브러리로 등록했다. 하지만 라이브러리로 등록하는 것만으로는 끝나지 않고, 이제 모듈에 라이브러리에 대한 의존성(Dependency)을 붙여야 한다.

![](https://raw.githubusercontent.com/MBAPD/mbpd/main/%E2%85%A0.%20%EB%A7%A8%20%EB%95%85%EC%97%90%20%ED%97%A4%EB%94%A9%ED%95%98%EA%B8%B0/1.%20%EA%B8%B0%EB%B3%B8%20%EC%84%B8%ED%8C%85%ED%95%98%EA%B8%B0/2%20-%20Paper%20%EC%84%A4%EC%B9%98%ED%95%98%EA%B8%B0/15.png)

좌측 **Modules** > 중앙 상단 **Dependencies** > 하단 **+ 버튼** > **2 Library...** 를 클릭한다.

![](https://raw.githubusercontent.com/MBAPD/mbpd/main/%E2%85%A0.%20%EB%A7%A8%20%EB%95%85%EC%97%90%20%ED%97%A4%EB%94%A9%ED%95%98%EA%B8%B0/1.%20%EA%B8%B0%EB%B3%B8%20%EC%84%B8%ED%8C%85%ED%95%98%EA%B8%B0/2%20-%20Paper%20%EC%84%A4%EC%B9%98%ED%95%98%EA%B8%B0/16.png)

아까 생성한 라이브러리를 선택하고 **Add Selected**를 클릭한다.

![](https://raw.githubusercontent.com/MBAPD/mbpd/main/%E2%85%A0.%20%EB%A7%A8%20%EB%95%85%EC%97%90%20%ED%97%A4%EB%94%A9%ED%95%98%EA%B8%B0/1.%20%EA%B8%B0%EB%B3%B8%20%EC%84%B8%ED%8C%85%ED%95%98%EA%B8%B0/2%20-%20Paper%20%EC%84%A4%EC%B9%98%ED%95%98%EA%B8%B0/17.png)

정상적을 라이브러리를 모듈에 등록했으면 위와 같은 모습이 나오면 된다!

-----

그럼 이렇게 Paper 라이브러리를 프로젝트에 등록하고, 메인 모듈에 의존성을 등록했다. 이제 거의 모든 준비 과정이 끝났다!