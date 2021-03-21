Artifact란 IntelliJ IDEA 내에서 Java 프로그램을 jar 파일로 뽑아낼 때, 해당 jar 파일에 어떤 내용이 포함될 것인지, 어디에 저장될 것인지를 정하는 기능이다. 즉, 이번 강좌에서 최종적으로 여태 만든 코드들을 jar 형태로 뽑아내어 서버 내에 적용까지 해볼 것이다.

[TOC]

# Artifact 설정하기

## 내용 구성하기

![](https://raw.githubusercontent.com/MBAPD/mbpd/main/%E2%85%A0.%20%EB%A7%A8%20%EB%95%85%EC%97%90%20%ED%97%A4%EB%94%A9%ED%95%98%EA%B8%B0/2.%20%EC%B2%AB%20%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8%20%EB%A7%8C%EB%93%A4%EA%B8%B0/3%20-%20Artifact%20%EC%84%A4%EC%A0%95%ED%95%98%EA%B3%A0%20%EB%B9%8C%EB%93%9C%2C%20%ED%85%8C%EC%8A%A4%ED%8A%B8%EC%9A%A9%20%EC%84%9C%EB%B2%84%20%EA%B5%AC%EC%B6%95%ED%95%98%EA%B8%B0/1.png)

프로젝트의 모듈 설정을 열어주자. 단축키 F4로도 열 수 있다.

![](https://raw.githubusercontent.com/MBAPD/mbpd/main/%E2%85%A0.%20%EB%A7%A8%20%EB%95%85%EC%97%90%20%ED%97%A4%EB%94%A9%ED%95%98%EA%B8%B0/2.%20%EC%B2%AB%20%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8%20%EB%A7%8C%EB%93%A4%EA%B8%B0/3%20-%20Artifact%20%EC%84%A4%EC%A0%95%ED%95%98%EA%B3%A0%20%EB%B9%8C%EB%93%9C%2C%20%ED%85%8C%EC%8A%A4%ED%8A%B8%EC%9A%A9%20%EC%84%9C%EB%B2%84%20%EA%B5%AC%EC%B6%95%ED%95%98%EA%B8%B0/2.png)

좌측의 **Artifacts** > 상단 **+ 버튼** > **JAR** > **Empty**를 선택한다.

![](https://raw.githubusercontent.com/MBAPD/mbpd/main/%E2%85%A0.%20%EB%A7%A8%20%EB%95%85%EC%97%90%20%ED%97%A4%EB%94%A9%ED%95%98%EA%B8%B0/2.%20%EC%B2%AB%20%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8%20%EB%A7%8C%EB%93%A4%EA%B8%B0/3%20-%20Artifact%20%EC%84%A4%EC%A0%95%ED%95%98%EA%B3%A0%20%EB%B9%8C%EB%93%9C%2C%20%ED%85%8C%EC%8A%A4%ED%8A%B8%EC%9A%A9%20%EC%84%9C%EB%B2%84%20%EA%B5%AC%EC%B6%95%ED%95%98%EA%B8%B0/3.png)

왼쪽에 있는 요소들은 jar 파일에 포함되는 요소들, 오른쪽에 있는 요소들은 jar 파일에 포함 가능한 요소들을 나타낸다.

오른쪽에 **'<모듈 이름>' compile output** 이라고 적혀있는 것을 더블클릭하여 좌측으로 옮겨준다. 그러면 이제 jar 파일을 추출할 때 프로젝트의 컴파일 출력물이 jar 파일 내에 포함될 것이다.

![](https://raw.githubusercontent.com/MBAPD/mbpd/main/%E2%85%A0.%20%EB%A7%A8%20%EB%95%85%EC%97%90%20%ED%97%A4%EB%94%A9%ED%95%98%EA%B8%B0/2.%20%EC%B2%AB%20%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8%20%EB%A7%8C%EB%93%A4%EA%B8%B0/3%20-%20Artifact%20%EC%84%A4%EC%A0%95%ED%95%98%EA%B3%A0%20%EB%B9%8C%EB%93%9C%2C%20%ED%85%8C%EC%8A%A4%ED%8A%B8%EC%9A%A9%20%EC%84%9C%EB%B2%84%20%EA%B5%AC%EC%B6%95%ED%95%98%EA%B8%B0/4.png)

또한, jar 파일 내에는 컴파일 출력물 뿐만 아니라 플러그인임을 인식하게 해 주는 `plugin.yml` 파일도 있어야 한다.

Artifact 기능은 오른쪽에 추가 가능한 요소에 있는 것 말고도 단순 파일이나 폴더를 jar 파일 내에 포함할 수 있다.

따라서 추가 버튼을 눌러 **Directory Content**를 눌러준다. 

![](https://raw.githubusercontent.com/MBAPD/mbpd/main/%E2%85%A0.%20%EB%A7%A8%20%EB%95%85%EC%97%90%20%ED%97%A4%EB%94%A9%ED%95%98%EA%B8%B0/2.%20%EC%B2%AB%20%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8%20%EB%A7%8C%EB%93%A4%EA%B8%B0/3%20-%20Artifact%20%EC%84%A4%EC%A0%95%ED%95%98%EA%B3%A0%20%EB%B9%8C%EB%93%9C%2C%20%ED%85%8C%EC%8A%A4%ED%8A%B8%EC%9A%A9%20%EC%84%9C%EB%B2%84%20%EA%B5%AC%EC%B6%95%ED%95%98%EA%B8%B0/5.png)

**2) plugin.yml 생성하고 설정하기** 에서 만든 프로젝트의 `resources` 폴더를 선택하고 **OK**를 클릭한다.

## 이름과 추출 경로 설정하기

![](https://raw.githubusercontent.com/MBAPD/mbpd/main/%E2%85%A0.%20%EB%A7%A8%20%EB%95%85%EC%97%90%20%ED%97%A4%EB%94%A9%ED%95%98%EA%B8%B0/2.%20%EC%B2%AB%20%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8%20%EB%A7%8C%EB%93%A4%EA%B8%B0/3%20-%20Artifact%20%EC%84%A4%EC%A0%95%ED%95%98%EA%B3%A0%20%EB%B9%8C%EB%93%9C%2C%20%ED%85%8C%EC%8A%A4%ED%8A%B8%EC%9A%A9%20%EC%84%9C%EB%B2%84%20%EA%B5%AC%EC%B6%95%ED%95%98%EA%B8%B0/6.png)

상단의 Artifact 이름을 원하는 대로 바꿔준다. `<Artifact 이름>.jar` 의 형태로 jar 파일이 출력된다.

이후에 오른쪽의 폴더 모양 버튼을 눌러준다.

![](https://raw.githubusercontent.com/MBAPD/mbpd/main/%E2%85%A0.%20%EB%A7%A8%20%EB%95%85%EC%97%90%20%ED%97%A4%EB%94%A9%ED%95%98%EA%B8%B0/2.%20%EC%B2%AB%20%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8%20%EB%A7%8C%EB%93%A4%EA%B8%B0/3%20-%20Artifact%20%EC%84%A4%EC%A0%95%ED%95%98%EA%B3%A0%20%EB%B9%8C%EB%93%9C%2C%20%ED%85%8C%EC%8A%A4%ED%8A%B8%EC%9A%A9%20%EC%84%9C%EB%B2%84%20%EA%B5%AC%EC%B6%95%ED%95%98%EA%B8%B0/7.png)

**1.2) Paper 설치하기**에서 paper 파일을 얻기 위해 사용했던 서버나, 자신이 직접 개인적으로 미리 구축해둔 서버 등의 plugins 폴더 내에 jar 파일을 바로 넣을 것이므로, plugins 폴더가 필요하다. 없는 경우 사진처럼 상단의 **New Folder...** 를 클릭해 주자.

![](https://raw.githubusercontent.com/MBAPD/mbpd/main/%E2%85%A0.%20%EB%A7%A8%20%EB%95%85%EC%97%90%20%ED%97%A4%EB%94%A9%ED%95%98%EA%B8%B0/2.%20%EC%B2%AB%20%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8%20%EB%A7%8C%EB%93%A4%EA%B8%B0/3%20-%20Artifact%20%EC%84%A4%EC%A0%95%ED%95%98%EA%B3%A0%20%EB%B9%8C%EB%93%9C%2C%20%ED%85%8C%EC%8A%A4%ED%8A%B8%EC%9A%A9%20%EC%84%9C%EB%B2%84%20%EA%B5%AC%EC%B6%95%ED%95%98%EA%B8%B0/8.png)

이름은 plugins로 하고 **OK** 버튼을 누르자.

![](https://raw.githubusercontent.com/MBAPD/mbpd/main/%E2%85%A0.%20%EB%A7%A8%20%EB%95%85%EC%97%90%20%ED%97%A4%EB%94%A9%ED%95%98%EA%B8%B0/2.%20%EC%B2%AB%20%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8%20%EB%A7%8C%EB%93%A4%EA%B8%B0/3%20-%20Artifact%20%EC%84%A4%EC%A0%95%ED%95%98%EA%B3%A0%20%EB%B9%8C%EB%93%9C%2C%20%ED%85%8C%EC%8A%A4%ED%8A%B8%EC%9A%A9%20%EC%84%9C%EB%B2%84%20%EA%B5%AC%EC%B6%95%ED%95%98%EA%B8%B0/9.png)

plugins 폴더를 선택하고 **OK** 버튼을 누르자.

![](https://raw.githubusercontent.com/MBAPD/mbpd/main/%E2%85%A0.%20%EB%A7%A8%20%EB%95%85%EC%97%90%20%ED%97%A4%EB%94%A9%ED%95%98%EA%B8%B0/2.%20%EC%B2%AB%20%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8%20%EB%A7%8C%EB%93%A4%EA%B8%B0/3%20-%20Artifact%20%EC%84%A4%EC%A0%95%ED%95%98%EA%B3%A0%20%EB%B9%8C%EB%93%9C%2C%20%ED%85%8C%EC%8A%A4%ED%8A%B8%EC%9A%A9%20%EC%84%9C%EB%B2%84%20%EA%B5%AC%EC%B6%95%ED%95%98%EA%B8%B0/10.png)

이름, 경로, jar 파일 내 포함될 요소가 제대로 적용되었는지 확인하고 **OK** 버튼을 눌러 창을 닫자.

## jar 파일 만들기
모든 준비가 끝났다. 이제 플러그인 파일을 뽑아낼 차례이다!

![](https://raw.githubusercontent.com/MBAPD/mbpd/main/%E2%85%A0.%20%EB%A7%A8%20%EB%95%85%EC%97%90%20%ED%97%A4%EB%94%A9%ED%95%98%EA%B8%B0/2.%20%EC%B2%AB%20%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8%20%EB%A7%8C%EB%93%A4%EA%B8%B0/3%20-%20Artifact%20%EC%84%A4%EC%A0%95%ED%95%98%EA%B3%A0%20%EB%B9%8C%EB%93%9C%2C%20%ED%85%8C%EC%8A%A4%ED%8A%B8%EC%9A%A9%20%EC%84%9C%EB%B2%84%20%EA%B5%AC%EC%B6%95%ED%95%98%EA%B8%B0/11.png)

IntelliJ IDEA 창 상단에 **Build** > **Build Artifacts...** 버튼을 눌러주자.

![](https://raw.githubusercontent.com/MBAPD/mbpd/main/%E2%85%A0.%20%EB%A7%A8%20%EB%95%85%EC%97%90%20%ED%97%A4%EB%94%A9%ED%95%98%EA%B8%B0/2.%20%EC%B2%AB%20%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8%20%EB%A7%8C%EB%93%A4%EA%B8%B0/3%20-%20Artifact%20%EC%84%A4%EC%A0%95%ED%95%98%EA%B3%A0%20%EB%B9%8C%EB%93%9C%2C%20%ED%85%8C%EC%8A%A4%ED%8A%B8%EC%9A%A9%20%EC%84%9C%EB%B2%84%20%EA%B5%AC%EC%B6%95%ED%95%98%EA%B8%B0/12.png)

그럼 창 가운데에 사진처럼 Build Artifact 창이 뜰텐데, 모듈 이름을 클릭하고 우측의 Action 창에서 **Build**를 클릭한다. 

![](https://raw.githubusercontent.com/MBAPD/mbpd/main/%E2%85%A0.%20%EB%A7%A8%20%EB%95%85%EC%97%90%20%ED%97%A4%EB%94%A9%ED%95%98%EA%B8%B0/2.%20%EC%B2%AB%20%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8%20%EB%A7%8C%EB%93%A4%EA%B8%B0/3%20-%20Artifact%20%EC%84%A4%EC%A0%95%ED%95%98%EA%B3%A0%20%EB%B9%8C%EB%93%9C%2C%20%ED%85%8C%EC%8A%A4%ED%8A%B8%EC%9A%A9%20%EC%84%9C%EB%B2%84%20%EA%B5%AC%EC%B6%95%ED%95%98%EA%B8%B0/13.png)

창 하단에 무언가 진행된 후 아래처럼 **Build completed successfully**와 같은 메시지가 뜨면 빌드에 성공한 것이다.

![](https://raw.githubusercontent.com/MBAPD/mbpd/main/%E2%85%A0.%20%EB%A7%A8%20%EB%95%85%EC%97%90%20%ED%97%A4%EB%94%A9%ED%95%98%EA%B8%B0/2.%20%EC%B2%AB%20%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8%20%EB%A7%8C%EB%93%A4%EA%B8%B0/3%20-%20Artifact%20%EC%84%A4%EC%A0%95%ED%95%98%EA%B3%A0%20%EB%B9%8C%EB%93%9C%2C%20%ED%85%8C%EC%8A%A4%ED%8A%B8%EC%9A%A9%20%EC%84%9C%EB%B2%84%20%EA%B5%AC%EC%B6%95%ED%95%98%EA%B8%B0/14.png)

정상적으로 서버의 plugins 폴더에 **MBPD.jar**가 저장되었는지 확인하자.

# 테스트용 서버 구축

## eula.txt 문제 해결하기

서버 최상위 폴더로 돌아오자(강좌에서는 MBPD_Server 폴더이다). paper를 얻어오는 과정에서 `open_server.bat`을 실행해 paper 서버를 열었는데, 직접 창을 닫지 않아도 조금 있으면 자동으로 닫히던 것을 기억할 것이다.

![](https://raw.githubusercontent.com/MBAPD/mbpd/main/%E2%85%A0.%20%EB%A7%A8%20%EB%95%85%EC%97%90%20%ED%97%A4%EB%94%A9%ED%95%98%EA%B8%B0/2.%20%EC%B2%AB%20%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8%20%EB%A7%8C%EB%93%A4%EA%B8%B0/3%20-%20Artifact%20%EC%84%A4%EC%A0%95%ED%95%98%EA%B3%A0%20%EB%B9%8C%EB%93%9C%2C%20%ED%85%8C%EC%8A%A4%ED%8A%B8%EC%9A%A9%20%EC%84%9C%EB%B2%84%20%EA%B5%AC%EC%B6%95%ED%95%98%EA%B8%B0/15.png)

닫히기 직전에 뜬 내용은 위에 떠 있는 것과 같다. 이를 해결하려면 어느샌가 생성된 `eula.txt`를 수정해야 한다. `eula.txt`의 내용은 다음과 같을 것이다. (대충 **파일 우클릭** > **편집**을 통해 열어주자)

```
#By changing the setting below to TRUE you are indicating your agreement to our EULA (https://account.mojang.com/documents/minecraft_eula).
#You also agree that tacos are tasty, and the best food in the world.
#Sun Mar 21 01:27:08 KST 2021
eula=false
```

대충 이런 내용으로 구성되어 있을텐데, 대충 `eula=false` 부분을 `eula=true`로 바꾸어주면 된다. 서버를 여는 사용자가 EULA(End-User License Agreement, 최종 사용자 라이선스 계약)에 동의함을 명시적으로 나타내달라고 모장 측에서 반쯤 강요하고 있는 것이다(Bukkit API 뿐만 아니라 기본 제공되는 Minecraft Server의 기능이다).

수정 및 저장 후, 다시 `open_server.bat`을 통해 서버를 열면, 월드 생성 후 서버가 열릴 것이다.

## onEnable(), onDisable()이 제대로 실행되는지 확인하기

![](https://raw.githubusercontent.com/MBAPD/mbpd/main/%E2%85%A0.%20%EB%A7%A8%20%EB%95%85%EC%97%90%20%ED%97%A4%EB%94%A9%ED%95%98%EA%B8%B0/2.%20%EC%B2%AB%20%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8%20%EB%A7%8C%EB%93%A4%EA%B8%B0/3%20-%20Artifact%20%EC%84%A4%EC%A0%95%ED%95%98%EA%B3%A0%20%EB%B9%8C%EB%93%9C%2C%20%ED%85%8C%EC%8A%A4%ED%8A%B8%EC%9A%A9%20%EC%84%9C%EB%B2%84%20%EA%B5%AC%EC%B6%95%ED%95%98%EA%B8%B0/16.png)

월드를 생성한 이후 서버에 Done! 이라는 메세지가 떴을 때, 그 위를 보면 `onEnable()`에 내가 작성한 메시지가 뜰 것이다.

![](https://raw.githubusercontent.com/MBAPD/mbpd/main/%E2%85%A0.%20%EB%A7%A8%20%EB%95%85%EC%97%90%20%ED%97%A4%EB%94%A9%ED%95%98%EA%B8%B0/2.%20%EC%B2%AB%20%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8%20%EB%A7%8C%EB%93%A4%EA%B8%B0/3%20-%20Artifact%20%EC%84%A4%EC%A0%95%ED%95%98%EA%B3%A0%20%EB%B9%8C%EB%93%9C%2C%20%ED%85%8C%EC%8A%A4%ED%8A%B8%EC%9A%A9%20%EC%84%9C%EB%B2%84%20%EA%B5%AC%EC%B6%95%ED%95%98%EA%B8%B0/17.png)

또한 `stop` 명령어를 통해 서버를 닫으면 마찬가지로 `onDisable()`에 내가 작성했던 메시지가 뜰 것이다.

## 배치 파일 수정하기

사실 처음에 만든 `open_server.bat`은 서버가 그냥 뻗으면 오류 메시지를 볼 틈도 없이 바로 창이 닫혀버린다. 따라서 배치 파일 하단에 `pause` 명령을 설정하여 서버가 뻗었을 때 오류 메시지를 볼 수 있도록 수정하자.

이전과 같이 `open_server.bat`을 **우클릭** > **편집(E)** 을 클릭하여 메모장을 열어주고, 내용을 다음과 같이 수정한다.

```bat
java -jar paper.jar
pause
```

그럼 이제 eula.txt때와 같이 서버가 뻗어도 바로 종료되지 않을 것이다.

-----

플러그인 기능 테스트를 위한 테스트 서버 구축을 완료했다. 이제 순수하게 플러그인 개발에만 집중할 수 있는 환경이 마련됐다.