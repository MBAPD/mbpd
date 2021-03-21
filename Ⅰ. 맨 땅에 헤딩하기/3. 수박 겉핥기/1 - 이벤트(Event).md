[TOC]

# 이벤트(Event)란?

이벤트(Event)의 사전적 정의는 다음과 같다.

- **event** [명]  
	- (특히 중요한) 사건[일]    
	- 행사  

우리는 1번 의미에 집중하면 된다. Bukkit API에서 이벤트란 **마인크래프트 내에서 일어나는 모든 사건**을 의미한다.

즉, 마인크래프트 서버 측에서 어떤 사건이 일어났을 때, Bukkit API는 이를 이벤트 형태로 처리하여 외부 플러그인이 이벤트에 대한 정보를 가공할 수 있게 한다. 

**플레이어가 접속했을 때 발생**하는 이벤트인 `PlayerJoinEvent`를 예로 들어보겠다.

`PlayerJoinEvent`는 플레이어가 서버에 성공적으로 접속하여 월드에 플레이어가 들어왔을 때 호출된다. 

해당 이벤트에서는 다음과 같은 기능을 제공한다.  
- 어떤 플레이어가 들어왔는지(`getPlayer()`)  
- 플레이어가 들어왔을 때 서버 전체에 전송되는 채팅(`<플레이어 이름> joined the game.`)을 얻어오거나(`getJoinMessage()`) 원하는 대로 설정(`setJoinMessage(String message)`)

여기서 플레이어가 들어왔을 때 전송되는 메시지를 수정하고 싶다면 `PlayerJoinEvent` 객체에 대해 `setJoinMessage(String message)`를 호출하여 변경하면, Bukkit API는 변경된 입장 메시지를 전체 플레이어에게 전송할 것이다. 정리하면 다음 이미지와 같다.

![](https://raw.githubusercontent.com/MBAPD/mbpd/main/%E2%85%A0.%20%EB%A7%A8%20%EB%95%85%EC%97%90%20%ED%97%A4%EB%94%A9%ED%95%98%EA%B8%B0/3.%20%EC%88%98%EB%B0%95%20%EA%B2%89%ED%95%A5%EA%B8%B0/1%20-%20%EC%9D%B4%EB%B2%A4%ED%8A%B8%28Event%29/1.png)

# 이벤트 겉핥기

위에서 설명한 대로 PlayerJoinEvent를 받아서 가공, 서버 접속 시 출력되는 메시지를 수정해볼 것이다.

## 이벤트 리스너 클래스

`MBPDPlugin`과 같은 패키지에 `EventListener` 클래스를 만들어 주자.

![](https://raw.githubusercontent.com/MBAPD/mbpd/main/%E2%85%A0.%20%EB%A7%A8%20%EB%95%85%EC%97%90%20%ED%97%A4%EB%94%A9%ED%95%98%EA%B8%B0/3.%20%EC%88%98%EB%B0%95%20%EA%B2%89%ED%95%A5%EA%B8%B0/1%20-%20%EC%9D%B4%EB%B2%A4%ED%8A%B8%28Event%29/2.png)
![](https://raw.githubusercontent.com/MBAPD/mbpd/main/%E2%85%A0.%20%EB%A7%A8%20%EB%95%85%EC%97%90%20%ED%97%A4%EB%94%A9%ED%95%98%EA%B8%B0/3.%20%EC%88%98%EB%B0%95%20%EA%B2%89%ED%95%A5%EA%B8%B0/1%20-%20%EC%9D%B4%EB%B2%A4%ED%8A%B8%28Event%29/3.png)
![](https://raw.githubusercontent.com/MBAPD/mbpd/main/%E2%85%A0.%20%EB%A7%A8%20%EB%95%85%EC%97%90%20%ED%97%A4%EB%94%A9%ED%95%98%EA%B8%B0/3.%20%EC%88%98%EB%B0%95%20%EA%B2%89%ED%95%A5%EA%B8%B0/1%20-%20%EC%9D%B4%EB%B2%A4%ED%8A%B8%28Event%29/4.png)

**2.1 - 메인 클래스 생성하기** 에서 했던 것 처럼, 클래스 이름 뒤에 `implements Listener`를 입력해주자. `Listener`가 빨갛게 표시된다면 `Listener` 뒤에 커서를 두고 **Ctrl+Space**로 자동 `import` 명령을 실행하자.

주의할 점은 `import`해야 하는 `Listener`는 `org.bukkit.event` 패키지의 `Listener`이다. 워낙 범용되는 이름이라 다른 Java 라이브러리에도 동일한 이름의 클래스가 몇몇 있다. 낚이지 말고 잘 고르자.

클래스가 다음과 같이 구성됐으면 합격이다.

```java
package net.wikidocs.mbpd;

import org.bukkit.event.Listener;

public class EventListener implements Listener {
    
    
    
}
```

우리가 방금 작성한 `implements` 명령은 `extends`와 비슷한 맥락이다. 단, `extends`는 다른 클래스로부터 기능을 물려받지만, `implements`는 다른 **인터페이스(Interface)** 로부터 기능 구현을 강요받게 만든다. 즉, Listener는 사실 클래스가 아니라 인터페이스이다.

따라서 원래 인터페이스를 가져오면 클래스 이름 밑에 빨간 줄이 뜨면서, 필수로 구현해야 하는 메소드들을 알려주는데, 이상하게도 그렇지 않다. 그 이유는 `Listener`의 코드를 보면 알 수 있다.

![](https://raw.githubusercontent.com/MBAPD/mbpd/main/%E2%85%A0.%20%EB%A7%A8%20%EB%95%85%EC%97%90%20%ED%97%A4%EB%94%A9%ED%95%98%EA%B8%B0/3.%20%EC%88%98%EB%B0%95%20%EA%B2%89%ED%95%A5%EA%B8%B0/1%20-%20%EC%9D%B4%EB%B2%A4%ED%8A%B8%28Event%29/5.png)

`Listener`의 코드를 보려면 `Listener` 위에 마우스를 대고 **Ctrl+클릭**하여 해당 클래스의 정의로 찾아갈 수 있다.

그런데 우리는 사실 Paper의 소스 코드를 다운로드 받은 적이 없다. 그래서 `Listener`를 Ctrl+클릭 하면 IntelliJ가 알아서 **디컴파일(Decompile)** 하여 보여준다(처음 사용하면 JetBrains의 디컴파일러 사용 EULA를 동의하라고 한다).

> 원래 Java의 프로그램을 빌드(컴파일)하면 소스 하나가 하나의 .class 파일 형태로 변환되어, 일반적으로 읽을 수 없게 변한다(바이트코드). 그런데 Java는 바이트코드를 역으로 해석하여 원본 소스를 유추하기 쉬운 구조로 되어있다. 따라서 IntelliJ IDEA에서도 이 기능을 기본적으로 제공한다.  
> Paper 및 Bukkit API는 소스가 공개된 것에 가깝기 때문에 대놓고 디컴파일해도 상관이 없고, 개인적으로 상용 플러그인을 다운받아 디컴파일하여 조용히 공부 용도로 사용하는 것도 상관이 없다. 하지만 디컴파일한 소스를 원 개발자의 허락 없이 그대로 사용하면 문제가 생길 수 있으니 그러한 행동은 지양하자. 

설명이 길었지만 Listener는 다음과 같은 구조로 이루어져 있다.

```java
package org.bukkit.event;

public interface Listener {
}
```

***"엥? 이거 완전 빈 껍데기 아닌가?"*** 라는 생각이 들 것이고, 실제로도 맞다. 완전히 빈 인터페이스라, 아무런 구현을 강요하지 않는다. 단순히 Bukkit API가 이벤트 리스너를 등록할 때 아무 객체나 받으면 문제가 생길 것 같으니, 이벤트를 받으려는 객체들은 빈 껍데기 인터페이스인 `Listener`를 구현하도록 한 것일 뿐이다.

## 이벤트 가공 메소드

다음과 같은 코드를 `EventListener` 클래스 중괄호 안에 작성하자.

```java
    @EventHandler
    public void onJoin(PlayerJoinEvent e){
        
    }
```
자동완성은 굳이 설명하지 않아도 이미 잘 사용하고 있으리라 믿는다. 작성 중에 `import`가 필요한 부분은 `EventHandler`, `PlayerJoinEvent`이다.

뭔가 익숙한 것 같으면서도 익숙하지 않은 구조이다. 이 구조는 이벤트 가공 메소드를 만드는 기본적인 형태이므로 앞으로도 자주 보게 될 것이다. 위 메소드는 `PlayerJoinEvent` 이벤트 객체를 가공할 수 있는 메소드이다.

코드의 각 부분들에 대해 설명을 하자면 다음과 같다.

### `@EventHandler`
Java의 **어노테이션(Annotation)** 이라는 기능으로, 클래스나 메소드 등에 주석을 다는 것과 비슷한 역할을 한다. Bukkit API에서는 이 `@EventHandler`라는 어노테이션은 메소드 앞에 달 수 있으며, Bukkit API에서 이벤트 리스너 클래스를 읽을 때 이 메소드가 이벤트를 가공하는 메소드임을 인식하게 하는 매개체이다.

### `public void onJoin(PlayerJoinEvent e)`
메소드를 정의하는 부분이다. 메소드는 다음과 같이 정의한다.
```java
[public/protected/private] <반환할 타입> <메소드 이름>(인자 ...) {}
```

`public`은 이 클래스나 패키지 뿐만 아니라 다른 곳에서도 이 메소드에 접근할 수 있게 하는 **접근 제어자(Access Modifier)** 이다. public으로 해 두지 않으면 나중에 Bukkit API가 접근하지 못할 수 있다.

`void`는 이전 강좌에서도 설명했지만 아무것도 반환하지 않는다는 뜻이다. 이 메소드는 단순히 이벤트를 가공할 뿐이라 별도의 값을 반환할 필요가 없다.

`onJoin`은 임의로 정한 메소드 이름이다. Bukkit API는 이벤트 가공 메소드에 대해서 이름에 딱히 제한을 두지 않았기 때문에, 메소드의 이름이 될 수 없는 경우, 메소드 이름과 형태가 완전히 중복되는 경우가 아니면 어떤 단어라도 들어갈 수 있다.

`(PlayerJoinEvent e)`는 이 메소드가 받아들일 인자값을 정의하는 부분이다. 즉, 인자를 통해 이벤트 객체를 받아들이고, 메소드 안에서 이 이벤트 객체를 참조하여 수정하면 된다. 이벤트 가공 메소드는 이벤트 객체 하나만을 인자로 받아야 한다. 그 이외의 형태로 작성하면 Bukkit API가 읽어들이지 못한다.

## 이벤트 가공

이벤트 가공 메소드의 중괄호 안에 다음과 같이 작성하자.

```java
e.setJoinMessage(e.getPlayer().getName()+"(이)가 서버에 접속했습니다.");
```

살짝 머리가 어질어질해질 수 있지만, 자세히 들여다 보면 별 거 아니다.

### `e.`

먼저 이벤트 객체 (`PlayerJoinEvent e`)에 점(`.`)을 붙여서, `PlayerJoinEvent`의 메소드에 접근한다. 이전에 Logger 객체를 가져올 때 getLogger() 메소드를 사용했었는데, 여기서는 메소드 인자값으로 `PlayerJoinEvent e` 라는 변수(Variable) 에 객체를 이미 받아둔 상태에서 코드를 실행하기 때문에, 단순히 `e` 뒤에 `.`을 붙여서 사용하면 된다.

### `setJoinMessage();`

PlayerJoinEvent 객체에 접근했으므로, 객체의 `void setJoinMessage(String message);` 메소드를 실행한다. `setJoinMessage()` 의 괄호 사이에는 인자값이 들어가므로 `e.getPlayer().getName()+"(이)가 서버에 접속했습니다."` 가 하나의 문자열로 취급되는 것이다.

### `e.getPlayer().getName()+"(이)가 서버에 접속했습니다."`

근데 분명 문자열은 큰따옴표 안에 넣는 것이 아니었나? `e.getPlayer().getName()`은 뭐고, 그 사이에 `+`는 무엇인가?

기본 설정 상의 플레이어 접속 메시지는 `<플레이어 이름> joined the game.` 이다. 즉, 항상 같은 문자열이 아닌, 플레이어의 닉네임마다 다른 문자열 값을 출력해야 한다. 하지만 큰따옴표 안에는 항상 고정된 문자열밖에 담을 수 없다.

여기서 눈치가 빠르면 이해했겠지만, `e.getPlayer().getName()` 은 이벤트에서 접속한 플레이어의 객체(`Player`)를 얻어오고, 거기서 다시 `getName()`을 호출하여 플레이어의 16자 이내 닉네임을 가져오는 명령이다. 그리고 `getName()` 메소드는 문자열(String)을 반환하는데, 큰따옴표 안에는 고정된 문자열밖에 담을 수 없다고 했으니, 두 문자열을 합치는 `+` 연산자를 통해 두 문자열을 합친 것이다(당연히 두 문자열을 합치면 문자열이다).

즉, 접속한 플레이어의 닉네임이 `MinecraftPlayer` 라면, 해당 명령은 `MinecraftPlayer(이)가 서버에 접속했습니다.` 라는 하나의 문자열을 뽑아내는 명령이 되는 것이다. 그리고 그 결과를 `setJoinMessage(String message)`의 인자값으로 설정하여, 최종적으로 해당 문자열이 서버 접속 메시지로 설정되는 것이다.

여기까지 잘 따라왔다면, 최종적으로 `EventListener`는 다음과 같이 생겼을 것이다.

```java
package net.wikidocs.mbpd;

import org.bukkit.event.EventHandler;
import org.bukkit.event.Listener;
import org.bukkit.event.player.PlayerJoinEvent;

public class EventListener implements Listener {

    @EventHandler
    public void onJoin(PlayerJoinEvent e){
        e.setJoinMessage(e.getPlayer().getName()+"(이)가 서버에 접속했습니다.");
    }

}
```

성공적으로 이벤트를 가공하는 메소드를 만들었다.

## onEnable에서 이벤트 리스너 등록

이벤트 가공 메소드를 만드는 것 만으로는 저 메소드를 호출하지 못한다. 우리가 만든 `EventListner` 클래스를 Bukkit API한테 등록해 주어야 클래스를 읽고 이벤트 호출 시 이벤트 가공 메소드를 호출해줄 것이다.

다시 플러그인 메인 클래스로 돌아와, `onEnable()` 메소드를 다음과 같이 수정하자.

```java
    @Override
    public void onEnable() {
        getServer().getPluginManager().registerEvents(new EventListener(), this);
        getLogger().info("MBPD Plugin Enabled.");
    }
```

메시지 출력 위에 무언가 더 생겼을 것이다.

```java
getServer().getPluginManager().registerEvents(new EventListener(), this);
```

`JavaPlugin#getServer()`를 통해 Server 객체를 얻고, `Server#getPluginManager()`를 통해 PluginManager 객체를 얻고, PluginManager 객채에서 `PluginManager#registerEvents(new EventListener(), this);`를 얻어 최종적으로 이벤트 리스너 객체를 Bukkit API에 등록했다. 이제 PlayerJoinEvent가 발생하면 이벤트 리스너 안의 이벤트 가공 메소드를 호출할 것이다.

근데 여기서 처음 보는 단어가 보이는데, `new EventListener()`와 `this`는 뭘까? `registerEvents()` 메소드의 정의를 보자.

```java
void registerEvents(Listener listener, Plugin plugin);
```

`registerEvents()` 메소드는 두 개의 인자를 받는다. 보다시피 메소드는 여러 개의 인자를 받을 수 있으며, 그 구분은 쉼표(`,`)로 한다. 여기서는 Listener 객체와 Plugin 객체를 받는다. 근데 왜 각각 `new EventListener()`와 `this`가 사용된 걸까?

### `new EventListener()`

메소드에 인자로 넘길 때 그냥 `EventListener`만 써도 될 것 같지만, 앞뒤에 뭔가 이상한게 주렁주렁 붙어있다.

`new` 키워드는 새로운 객체를 생성한다는 뜻이다. 어? 객체와 클래스는 같은 것 아니었나?

사실 **클래스는 도장틀**이고, **객체는 도장틀로 찍어낸 도장**이다. 즉, 클래스는 객체의 설계도를 정의해둔 것이고, 객체는 그 설계도대로 메모리 상에 존재하는 데이터이다.

인자로 넘길 때는 클래스가 아니라 객체 형태로 넘겨야 하므로, 도장틀에서 도장을 찍어내야 하는데, 바로 도장틀에서 도장을 찍어내는 명령이 `new <클래스 이름>()` 명령이다.

근데 뒤에 붙은 `()`는 메소드에서나 붙어있던 것 아닌가? 여기에 대체 왜 들어가 있을까?

바로 `new <클래스 이름>()`도 일종의 객체를 생성하는 메소드, 즉 생성자(Constructor)이기 때문이다. 클래스마다 최소한 한 개는 정의되어 있으며, 별도로 정의하지 않을 경우 기본적으로 인자가 없는 형태로 정의된다.

즉, `new EventListener()`라는 명령은 새로운 `EventListener` 객체를 생성하라는 명령이다. 그리고 그렇게 생성된 객체를 바로 인자에 넣은 것이다.

### `this`

이것, 즉 메소드를 실행하고 있는 객체 자신을 가리키는 키워드이다. onEnable()을 실행하고 있는 객체는 바로 Bukkit API로부터 생성된 `JavaPlugin` 객체(정확히는 `MBPDPlugin`)를 가리킨다. `JavaPlugin`은 `Plugin`을 상속하고 있어 `Plugin`을 인자로 받는 곳에 넣을 수 있다.

## 작동 테스트

이벤트의 작동 구조는 대략 파악했고, Bukkit API에도 이를 등록했으니 이제 그 결과를 볼 차례다. 뭔가 엄청나게 많은 내용이 있었던 것 같지만, 우린 고작 플레이어가 접속할 때 나오는 메시지를 변경한 것 밖에 없다. 그래도 너무 쫄지 말자. 이 관문만 넘어서면 당신도 훌륭한 플러그인 개발자가 될 수 있다.

이전에 했던 것 처럼, **Build** > **Build Artifacts...** 를 눌러 jar 파일을 생성하고, open_server.bat 파일을 더블클릭 해 서버를 열자.

그리고 마인크래프트를 켜서 직접 자신의 서버로 들어가보자. 우리가 일구어낸 건 **"플레이어가 서버에 접속할 때 뜨는 메시지를 수정"** 한 것이니, 이를 테스트하려면 서버에 들어가보는 수밖에 없다.

플러그인 개발한다는 사람 치고 멀티플레이 한 번 안해본 사람은 없으리라 생각하지만, 서버를 직접 열어본 경험이 없을 수도 있으니 설명하자면, 마인크래프트를 킨 후 화면 중앙의 **멀티플레이** > 하단 중앙의 **직접 연결** > **서버 주소란**에 서버 주소 입력 > 하단 **서버 참여**를 클릭하면 된다.

서버 주소는 `localhost` 또는 `127.0.0.1` 으로 설정하면 자신의 컴퓨터에서 연 서버를 접속할 수 있다.

![](https://raw.githubusercontent.com/MBAPD/mbpd/main/%E2%85%A0.%20%EB%A7%A8%20%EB%95%85%EC%97%90%20%ED%97%A4%EB%94%A9%ED%95%98%EA%B8%B0/3.%20%EC%88%98%EB%B0%95%20%EA%B2%89%ED%95%A5%EA%B8%B0/1%20-%20%EC%9D%B4%EB%B2%A4%ED%8A%B8%28Event%29/6.png)
![](https://raw.githubusercontent.com/MBAPD/mbpd/main/%E2%85%A0.%20%EB%A7%A8%20%EB%95%85%EC%97%90%20%ED%97%A4%EB%94%A9%ED%95%98%EA%B8%B0/3.%20%EC%88%98%EB%B0%95%20%EA%B2%89%ED%95%A5%EA%B8%B0/1%20-%20%EC%9D%B4%EB%B2%A4%ED%8A%B8%28Event%29/7.png)

기본 서버 접속 메시지가 영어에서 한글로 변한 것을 볼 수 있다!
