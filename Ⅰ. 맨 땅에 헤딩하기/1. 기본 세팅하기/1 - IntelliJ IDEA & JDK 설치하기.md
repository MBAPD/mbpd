**IntelliJ IDEA**는 JetBrains 사에서 개발한 Java 전문 **IDE**(Integrated Development Environment, 통합 개발 환경)이다. 인터넷에서 찾아볼 수 있는 대부분의 *(옛날)* 강좌에서는 Eclipse를 기반으로 작성되어 있을 것이다. 원한다면 Eclipse를 사용해도 되지만, 본 강좌는 IntelliJ IDEA를 기반으로 작성될 것이다. 또한 Eclipse보다 자동완성, 인덱싱 기능 등이 월등히 강력하여 필자는 IntelliJ IDEA를 사용하는 것을 추천한다.

또한 본 설치 과정에서 JDK(Java Development Kit) 또한 설치할 것이다. 기존에는 따로따로 설치해야 했으나 IntelliJ IDEA의 기초 설정 과정에서 직접 JDK를 다운로드할 수 있도록 지원하므로 해당 기능을 사용한다. 만약 해당 기능을 사용하지 않을 경우, 본 강좌가 사용할 JDK 기반은 **AdoptOpenJDK 11.0, HotSpot** 버전이다.

# IntelliJ IDEA & JDK 설치

[https://www.jetbrains.com/ko-kr/idea/](https://www.jetbrains.com/ko-kr/idea/) - IntelliJ IDEA 공식 사이트

상기된 링크에 접속한 후, 아래의 이미지에 빨간색 강조 표시를 따른다.

![](https://raw.githubusercontent.com/MBAPD/mbpd/main/%E2%85%A0.%20%EB%A7%A8%20%EB%95%85%EC%97%90%20%ED%97%A4%EB%94%A9%ED%95%98%EA%B8%B0/1.%20%EA%B8%B0%EB%B3%B8%20%EC%84%B8%ED%8C%85%ED%95%98%EA%B8%B0/1%20-%20IntelliJ%20IDEA%20%26%20JDK%20%EC%84%A4%EC%B9%98%ED%95%98%EA%B8%B0/1.png)

![](https://raw.githubusercontent.com/MBAPD/mbpd/main/%E2%85%A0.%20%EB%A7%A8%20%EB%95%85%EC%97%90%20%ED%97%A4%EB%94%A9%ED%95%98%EA%B8%B0/1.%20%EA%B8%B0%EB%B3%B8%20%EC%84%B8%ED%8C%85%ED%95%98%EA%B8%B0/1%20-%20IntelliJ%20IDEA%20%26%20JDK%20%EC%84%A4%EC%B9%98%ED%95%98%EA%B8%B0/2.png)

다운로드 버튼을 클릭하여 설치 프로그램을 다운로드 받고, 실행한다.

![](https://raw.githubusercontent.com/MBAPD/mbpd/main/%E2%85%A0.%20%EB%A7%A8%20%EB%95%85%EC%97%90%20%ED%97%A4%EB%94%A9%ED%95%98%EA%B8%B0/1.%20%EA%B8%B0%EB%B3%B8%20%EC%84%B8%ED%8C%85%ED%95%98%EA%B8%B0/1%20-%20IntelliJ%20IDEA%20%26%20JDK%20%EC%84%A4%EC%B9%98%ED%95%98%EA%B8%B0/3.png)

![](https://raw.githubusercontent.com/MBAPD/mbpd/main/%E2%85%A0.%20%EB%A7%A8%20%EB%95%85%EC%97%90%20%ED%97%A4%EB%94%A9%ED%95%98%EA%B8%B0/1.%20%EA%B8%B0%EB%B3%B8%20%EC%84%B8%ED%8C%85%ED%95%98%EA%B8%B0/1%20-%20IntelliJ%20IDEA%20%26%20JDK%20%EC%84%A4%EC%B9%98%ED%95%98%EA%B8%B0/4.png)

![](https://raw.githubusercontent.com/MBAPD/mbpd/main/%E2%85%A0.%20%EB%A7%A8%20%EB%95%85%EC%97%90%20%ED%97%A4%EB%94%A9%ED%95%98%EA%B8%B0/1.%20%EA%B8%B0%EB%B3%B8%20%EC%84%B8%ED%8C%85%ED%95%98%EA%B8%B0/1%20-%20IntelliJ%20IDEA%20%26%20JDK%20%EC%84%A4%EC%B9%98%ED%95%98%EA%B8%B0/5.png)

각각의 옵션은 다음과 같으며, 전부 체크하지 않아도 강좌 진행에는 무리가 없다.

* ① 바탕화면에 바로가기 아이콘 설치 여부를 결정한다.
* ② IntelliJ IDEA의 설치 경로를 PATH 환경 변수에 등록한다.
* ③ 폴더를 우클릭할 때 "Open Folder as Project(폴더를 프로젝트로 열기)" 옵션을 제공한다.
* ④ 각각 `.java`, `.groovy`, `.kt`, `.kts` 파일에 연결 프로그램을 IntelliJ로 설정한다.
* ⑤ 32비트 JetBrains 런타임을 설치한다.

![](https://raw.githubusercontent.com/MBAPD/mbpd/main/%E2%85%A0.%20%EB%A7%A8%20%EB%95%85%EC%97%90%20%ED%97%A4%EB%94%A9%ED%95%98%EA%B8%B0/1.%20%EA%B8%B0%EB%B3%B8%20%EC%84%B8%ED%8C%85%ED%95%98%EA%B8%B0/1%20-%20IntelliJ%20IDEA%20%26%20JDK%20%EC%84%A4%EC%B9%98%ED%95%98%EA%B8%B0/6.png)

![](https://raw.githubusercontent.com/MBAPD/mbpd/main/%E2%85%A0.%20%EB%A7%A8%20%EB%95%85%EC%97%90%20%ED%97%A4%EB%94%A9%ED%95%98%EA%B8%B0/1.%20%EA%B8%B0%EB%B3%B8%20%EC%84%B8%ED%8C%85%ED%95%98%EA%B8%B0/1%20-%20IntelliJ%20IDEA%20%26%20JDK%20%EC%84%A4%EC%B9%98%ED%95%98%EA%B8%B0/7.png)

![](https://raw.githubusercontent.com/MBAPD/mbpd/main/%E2%85%A0.%20%EB%A7%A8%20%EB%95%85%EC%97%90%20%ED%97%A4%EB%94%A9%ED%95%98%EA%B8%B0/1.%20%EA%B8%B0%EB%B3%B8%20%EC%84%B8%ED%8C%85%ED%95%98%EA%B8%B0/1%20-%20IntelliJ%20IDEA%20%26%20JDK%20%EC%84%A4%EC%B9%98%ED%95%98%EA%B8%B0/8.png)

체크박스를 누르지 않고 Finish 했어도 그냥 방금 설치한 IntelliJ IDEA를 실행하냐 마냐의 차이이다. 실수로 바로 Finish를 했다면 검색을 통해 IntelliJ IDEA를 실행시켜 주자.

![](https://raw.githubusercontent.com/MBAPD/mbpd/main/%E2%85%A0.%20%EB%A7%A8%20%EB%95%85%EC%97%90%20%ED%97%A4%EB%94%A9%ED%95%98%EA%B8%B0/1.%20%EA%B8%B0%EB%B3%B8%20%EC%84%B8%ED%8C%85%ED%95%98%EA%B8%B0/1%20-%20IntelliJ%20IDEA%20%26%20JDK%20%EC%84%A4%EC%B9%98%ED%95%98%EA%B8%B0/9.png)

기존 설정을 불러오는 창이다. 만약 기존에 사용하던 IntelliJ IDEA 설정값이 있다면 재량껏 불러와주자.

![](https://raw.githubusercontent.com/MBAPD/mbpd/main/%E2%85%A0.%20%EB%A7%A8%20%EB%95%85%EC%97%90%20%ED%97%A4%EB%94%A9%ED%95%98%EA%B8%B0/1.%20%EA%B8%B0%EB%B3%B8%20%EC%84%B8%ED%8C%85%ED%95%98%EA%B8%B0/1%20-%20IntelliJ%20IDEA%20%26%20JDK%20%EC%84%A4%EC%B9%98%ED%95%98%EA%B8%B0/10.png)

![](https://raw.githubusercontent.com/MBAPD/mbpd/main/%E2%85%A0.%20%EB%A7%A8%20%EB%95%85%EC%97%90%20%ED%97%A4%EB%94%A9%ED%95%98%EA%B8%B0/1.%20%EA%B8%B0%EB%B3%B8%20%EC%84%B8%ED%8C%85%ED%95%98%EA%B8%B0/1%20-%20IntelliJ%20IDEA%20%26%20JDK%20%EC%84%A4%EC%B9%98%ED%95%98%EA%B8%B0/11.png)

![](https://raw.githubusercontent.com/MBAPD/mbpd/main/%E2%85%A0.%20%EB%A7%A8%20%EB%95%85%EC%97%90%20%ED%97%A4%EB%94%A9%ED%95%98%EA%B8%B0/1.%20%EA%B8%B0%EB%B3%B8%20%EC%84%B8%ED%8C%85%ED%95%98%EA%B8%B0/1%20-%20IntelliJ%20IDEA%20%26%20JDK%20%EC%84%A4%EC%B9%98%ED%95%98%EA%B8%B0/12.png)

![](https://raw.githubusercontent.com/MBAPD/mbpd/main/%E2%85%A0.%20%EB%A7%A8%20%EB%95%85%EC%97%90%20%ED%97%A4%EB%94%A9%ED%95%98%EA%B8%B0/1.%20%EA%B8%B0%EB%B3%B8%20%EC%84%B8%ED%8C%85%ED%95%98%EA%B8%B0/1%20-%20IntelliJ%20IDEA%20%26%20JDK%20%EC%84%A4%EC%B9%98%ED%95%98%EA%B8%B0/13.png)

![](https://raw.githubusercontent.com/MBAPD/mbpd/main/%E2%85%A0.%20%EB%A7%A8%20%EB%95%85%EC%97%90%20%ED%97%A4%EB%94%A9%ED%95%98%EA%B8%B0/1.%20%EA%B8%B0%EB%B3%B8%20%EC%84%B8%ED%8C%85%ED%95%98%EA%B8%B0/1%20-%20IntelliJ%20IDEA%20%26%20JDK%20%EC%84%A4%EC%B9%98%ED%95%98%EA%B8%B0/14.png)

![](https://raw.githubusercontent.com/MBAPD/mbpd/main/%E2%85%A0.%20%EB%A7%A8%20%EB%95%85%EC%97%90%20%ED%97%A4%EB%94%A9%ED%95%98%EA%B8%B0/1.%20%EA%B8%B0%EB%B3%B8%20%EC%84%B8%ED%8C%85%ED%95%98%EA%B8%B0/1%20-%20IntelliJ%20IDEA%20%26%20JDK%20%EC%84%A4%EC%B9%98%ED%95%98%EA%B8%B0/15.png)

![](https://raw.githubusercontent.com/MBAPD/mbpd/main/%E2%85%A0.%20%EB%A7%A8%20%EB%95%85%EC%97%90%20%ED%97%A4%EB%94%A9%ED%95%98%EA%B8%B0/1.%20%EA%B8%B0%EB%B3%B8%20%EC%84%B8%ED%8C%85%ED%95%98%EA%B8%B0/1%20-%20IntelliJ%20IDEA%20%26%20JDK%20%EC%84%A4%EC%B9%98%ED%95%98%EA%B8%B0/16.png)

![](https://raw.githubusercontent.com/MBAPD/mbpd/main/%E2%85%A0.%20%EB%A7%A8%20%EB%95%85%EC%97%90%20%ED%97%A4%EB%94%A9%ED%95%98%EA%B8%B0/1.%20%EA%B8%B0%EB%B3%B8%20%EC%84%B8%ED%8C%85%ED%95%98%EA%B8%B0/1%20-%20IntelliJ%20IDEA%20%26%20JDK%20%EC%84%A4%EC%B9%98%ED%95%98%EA%B8%B0/17.png)

![](https://raw.githubusercontent.com/MBAPD/mbpd/main/%E2%85%A0.%20%EB%A7%A8%20%EB%95%85%EC%97%90%20%ED%97%A4%EB%94%A9%ED%95%98%EA%B8%B0/1.%20%EA%B8%B0%EB%B3%B8%20%EC%84%B8%ED%8C%85%ED%95%98%EA%B8%B0/1%20-%20IntelliJ%20IDEA%20%26%20JDK%20%EC%84%A4%EC%B9%98%ED%95%98%EA%B8%B0/18.png)

![](https://raw.githubusercontent.com/MBAPD/mbpd/main/%E2%85%A0.%20%EB%A7%A8%20%EB%95%85%EC%97%90%20%ED%97%A4%EB%94%A9%ED%95%98%EA%B8%B0/1.%20%EA%B8%B0%EB%B3%B8%20%EC%84%B8%ED%8C%85%ED%95%98%EA%B8%B0/1%20-%20IntelliJ%20IDEA%20%26%20JDK%20%EC%84%A4%EC%B9%98%ED%95%98%EA%B8%B0/19.png)

IntelliJ IDEA & JDK 설치 끝! 

# 부록 - Java 환경 변수 설정
마인크래프트로 플러그인 개발한다는 사람 치고 컴퓨터에 Java 안 깔린 사람은 드물겠지만, 혹여라도 OpenJDK를 기반으로 Java 환경 변수를 설정하고 싶거나 이전에 Java 환경 변수 설정을 하지 않은 독자는 본 설명을 따를 필요가 있다.

상기 이미지에 설명된 대로 설치됐다면, **JDK가 설치된 경로**는 `C:\Users\<유저 이름>\.jdks\adopt-openjdk-11.0.10\` 이다. 앞으로 `JDK가 설치된 경로`와 같이 강조되면 이 경로를 참조하면 된다. 만약 위에서 JDK를 설치할 때 경로를 바꾸었다면 해당 경로를 참조하면 된다.

![](https://raw.githubusercontent.com/MBAPD/mbpd/main/%E2%85%A0.%20%EB%A7%A8%20%EB%95%85%EC%97%90%20%ED%97%A4%EB%94%A9%ED%95%98%EA%B8%B0/1.%20%EA%B8%B0%EB%B3%B8%20%EC%84%B8%ED%8C%85%ED%95%98%EA%B8%B0/1%20-%20IntelliJ%20IDEA%20%26%20JDK%20%EC%84%A4%EC%B9%98%ED%95%98%EA%B8%B0/20.png)

요즘 세상이 참 편해졌다. 만약 Windows 10이 아닌 경우 **제어판 > 시스템 및 보안 > 시스템 > 좌측의 고급 시스템 설정**을 들어가면 나온다.

![](https://raw.githubusercontent.com/MBAPD/mbpd/main/%E2%85%A0.%20%EB%A7%A8%20%EB%95%85%EC%97%90%20%ED%97%A4%EB%94%A9%ED%95%98%EA%B8%B0/1.%20%EA%B8%B0%EB%B3%B8%20%EC%84%B8%ED%8C%85%ED%95%98%EA%B8%B0/1%20-%20IntelliJ%20IDEA%20%26%20JDK%20%EC%84%A4%EC%B9%98%ED%95%98%EA%B8%B0/21.png)

환경 변수 부분을 클릭해준다.

![](https://raw.githubusercontent.com/MBAPD/mbpd/main/%E2%85%A0.%20%EB%A7%A8%20%EB%95%85%EC%97%90%20%ED%97%A4%EB%94%A9%ED%95%98%EA%B8%B0/1.%20%EA%B8%B0%EB%B3%B8%20%EC%84%B8%ED%8C%85%ED%95%98%EA%B8%B0/1%20-%20IntelliJ%20IDEA%20%26%20JDK%20%EC%84%A4%EC%B9%98%ED%95%98%EA%B8%B0/22.png)

하단의 시스템 환경 변수에서 `Path`를 찾아 **편집(I)...**을 클릭한다.

![](https://raw.githubusercontent.com/MBAPD/mbpd/main/%E2%85%A0.%20%EB%A7%A8%20%EB%95%85%EC%97%90%20%ED%97%A4%EB%94%A9%ED%95%98%EA%B8%B0/1.%20%EA%B8%B0%EB%B3%B8%20%EC%84%B8%ED%8C%85%ED%95%98%EA%B8%B0/1%20-%20IntelliJ%20IDEA%20%26%20JDK%20%EC%84%A4%EC%B9%98%ED%95%98%EA%B8%B0/23.png)

**새로 만들기(N)** 버튼을 클릭하여 텍스트를 입력할 칸이 나타난다면 `JDK가 설치된 경로\bin` 를 입력한다. **절대로 뒤의 `\bin`을 빼먹어서는 안 된다!**


![](https://raw.githubusercontent.com/MBAPD/mbpd/main/%E2%85%A0.%20%EB%A7%A8%20%EB%95%85%EC%97%90%20%ED%97%A4%EB%94%A9%ED%95%98%EA%B8%B0/1.%20%EA%B8%B0%EB%B3%B8%20%EC%84%B8%ED%8C%85%ED%95%98%EA%B8%B0/1%20-%20IntelliJ%20IDEA%20%26%20JDK%20%EC%84%A4%EC%B9%98%ED%95%98%EA%B8%B0/24.png)

**확인** 버튼을 눌러 다시 이전의 환경 변수 창으로 돌아가, 이번에는 편집 버튼 대신 **새로 만들기(W)...** 버튼을 클릭한다.

![](https://raw.githubusercontent.com/MBAPD/mbpd/main/%E2%85%A0.%20%EB%A7%A8%20%EB%95%85%EC%97%90%20%ED%97%A4%EB%94%A9%ED%95%98%EA%B8%B0/1.%20%EA%B8%B0%EB%B3%B8%20%EC%84%B8%ED%8C%85%ED%95%98%EA%B8%B0/1%20-%20IntelliJ%20IDEA%20%26%20JDK%20%EC%84%A4%EC%B9%98%ED%95%98%EA%B8%B0/25.png)

**변수 이름** 란에는 `JAVA_HOME`, **변수 값** 란에는 `JDK가 설치된 경로` 그대로를 입력, **확인** 버튼을 클릭한다.

-----

환경 변수 설정이 정상적으로 되었는지 확인해보자.

![](https://raw.githubusercontent.com/MBAPD/mbpd/main/%E2%85%A0.%20%EB%A7%A8%20%EB%95%85%EC%97%90%20%ED%97%A4%EB%94%A9%ED%95%98%EA%B8%B0/1.%20%EA%B8%B0%EB%B3%B8%20%EC%84%B8%ED%8C%85%ED%95%98%EA%B8%B0/1%20-%20IntelliJ%20IDEA%20%26%20JDK%20%EC%84%A4%EC%B9%98%ED%95%98%EA%B8%B0/26.png)

 `Win+R` 버튼을 눌러 `cmd`를 입력한 후 **확인** 버튼을 눌러 명령 프롬프트 창을 실행한다.

![](https://raw.githubusercontent.com/MBAPD/mbpd/main/%E2%85%A0.%20%EB%A7%A8%20%EB%95%85%EC%97%90%20%ED%97%A4%EB%94%A9%ED%95%98%EA%B8%B0/1.%20%EA%B8%B0%EB%B3%B8%20%EC%84%B8%ED%8C%85%ED%95%98%EA%B8%B0/1%20-%20IntelliJ%20IDEA%20%26%20JDK%20%EC%84%A4%EC%B9%98%ED%95%98%EA%B8%B0/27.png)

실행된 창에 `java -version` 을 입력한다.

![](https://raw.githubusercontent.com/MBAPD/mbpd/main/%E2%85%A0.%20%EB%A7%A8%20%EB%95%85%EC%97%90%20%ED%97%A4%EB%94%A9%ED%95%98%EA%B8%B0/1.%20%EA%B8%B0%EB%B3%B8%20%EC%84%B8%ED%8C%85%ED%95%98%EA%B8%B0/1%20-%20IntelliJ%20IDEA%20%26%20JDK%20%EC%84%A4%EC%B9%98%ED%95%98%EA%B8%B0/28.png)

이미지와 같이 **AdoptOpenJDK, 버전 11**이 정상적으로 출력된다면 환경 변수 설정도 완료된 것이다!

-----

이제 Java 프로그램 개발을 위한 모든 기반이 갖춰졌다. 하지만 우리가 Bukkit API 플러그인을 개발하기 위해선 아직 한 가지 과정이 더 필요하다.