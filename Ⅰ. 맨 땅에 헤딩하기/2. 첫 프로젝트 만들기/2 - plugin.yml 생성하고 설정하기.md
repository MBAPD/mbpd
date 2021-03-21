상위 문서에서 언급한 대로, plugin.yml은 Bukkit API가 이 플러그인을 정상적으로 인식할 수 있도록 플러그인의 정보를 기재하는 파일이다. Bukkit API에서 플러그인을 불러올 때, jar 파일 내부의 plugin.yml을 찾아 내부에 기재된 내용을 기준으로 플러그인을 불러온다.

plugin.yml 내에 필수로 기재해야 하는 것은 이름(name), 버전(version), 메인 클래스의 경로(main)이다. 세 개 항목 중 하나라도 빠지면 플러그인을 정상적으로 로드하지 못한다.

[https://bukkit.fandom.com/wiki/Plugin_YAML](https://bukkit.fandom.com/wiki/Plugin_YAML) - plugin.yml에 기재할 수 있는 내용들을 정리한 공식 문서

세 가지 필수 항목을 포함해 여러가지 기재할 수 있는 항목들을 정리한 문서이다. 이후에도 Bukkit API의 기능을 소개하면서 자주 참고하게 될 것이다.

[TOC]

# plugin.yml 파일 생성하기
## 파일 만들기

![](https://raw.githubusercontent.com/MBAPD/mbpd/main/%E2%85%A0.%20%EB%A7%A8%20%EB%95%85%EC%97%90%20%ED%97%A4%EB%94%A9%ED%95%98%EA%B8%B0/2.%20%EC%B2%AB%20%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8%20%EB%A7%8C%EB%93%A4%EA%B8%B0/2%20-%20plugin.yml%20%EC%83%9D%EC%84%B1%ED%95%98%EA%B3%A0%20%EC%84%A4%EC%A0%95%ED%95%98%EA%B8%B0/1.png)

먼저 `plugin.yml`을 넣을 폴더를 생성한다. 바로 프로젝트 경로 밑에 `plugin.yml`을 생성해도 되지만, 이후에 플러그인에 포함할 여러 리소스 파일들이 생길지도 모르니 미리 폴더를 만들어 두자.

![](https://raw.githubusercontent.com/MBAPD/mbpd/main/%E2%85%A0.%20%EB%A7%A8%20%EB%95%85%EC%97%90%20%ED%97%A4%EB%94%A9%ED%95%98%EA%B8%B0/2.%20%EC%B2%AB%20%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8%20%EB%A7%8C%EB%93%A4%EA%B8%B0/2%20-%20plugin.yml%20%EC%83%9D%EC%84%B1%ED%95%98%EA%B3%A0%20%EC%84%A4%EC%A0%95%ED%95%98%EA%B8%B0/2.png)

폴더 이름은 `resources`로 정한다.

![](https://raw.githubusercontent.com/MBAPD/mbpd/main/%E2%85%A0.%20%EB%A7%A8%20%EB%95%85%EC%97%90%20%ED%97%A4%EB%94%A9%ED%95%98%EA%B8%B0/2.%20%EC%B2%AB%20%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8%20%EB%A7%8C%EB%93%A4%EA%B8%B0/2%20-%20plugin.yml%20%EC%83%9D%EC%84%B1%ED%95%98%EA%B3%A0%20%EC%84%A4%EC%A0%95%ED%95%98%EA%B8%B0/3.png)

방금 생성된 `resources` 폴더를 다시 우클릭하여 파일을 생성한다.

![](https://raw.githubusercontent.com/MBAPD/mbpd/main/%E2%85%A0.%20%EB%A7%A8%20%EB%95%85%EC%97%90%20%ED%97%A4%EB%94%A9%ED%95%98%EA%B8%B0/2.%20%EC%B2%AB%20%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8%20%EB%A7%8C%EB%93%A4%EA%B8%B0/2%20-%20plugin.yml%20%EC%83%9D%EC%84%B1%ED%95%98%EA%B3%A0%20%EC%84%A4%EC%A0%95%ED%95%98%EA%B8%B0/4.png)

파일 이름은 `plugin.yml`으로 정한다.

![](https://raw.githubusercontent.com/MBAPD/mbpd/main/%E2%85%A0.%20%EB%A7%A8%20%EB%95%85%EC%97%90%20%ED%97%A4%EB%94%A9%ED%95%98%EA%B8%B0/2.%20%EC%B2%AB%20%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8%20%EB%A7%8C%EB%93%A4%EA%B8%B0/2%20-%20plugin.yml%20%EC%83%9D%EC%84%B1%ED%95%98%EA%B3%A0%20%EC%84%A4%EC%A0%95%ED%95%98%EA%B8%B0/5.png)

방금 생성한 `plugin.yml`이 오른쪽 텍스트 에디터에 열렸을 것이다. 이제 여기에 내용을 작성하면 된다.

## 내용 적기

다음을 그대로 받아적거나 복사 붙여넣기 하자.

```yml
name: MBPD
version: 1.0.0
main: net.wikidocs.mbpd.MBPDPlugin
```

눈치가 빠르면 이해했겠지만, 이 파일의 핵심은 바로 메인 클래스의 경로를 지정하는 `main` 항목이다. Bukkit API가 플러그인을 인식하고 불러올 때, 여기에 기재된 `main` 항목을 따라 들어가 해당 클래스를 불러오게 된다. 반대로 `main` 항목이 잘못 기재된 경우 플러그인을 인식할 수 없게 된다.

이름(`name`)이나 버전(`version`)은 자유롭게 기재해도 된다. 이름은 적당히 다른 플러그인의 이름이랑 충돌이 나지 않을 정도로, 버전은 자유롭게 작성해도 좋다(YAML 파일 형태를 깨지게 하지 않을 정도로).
