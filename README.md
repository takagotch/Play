### play
---
https://github.com/playframework/playframework

https://www.playframework.com/

```java
// core/play/src/test/java/play/i18n/MessagesTest.java

public class MesagesTest {
  
  @Test
  public void testMessageCall() {
    MessageApi messageApi = mock(MessageApi.class);
    Lang lang = Lang.forCode("en-US");
    MessagesImpl messages = new MessagesImpl(lang, messagesApi);
    
    when(messagesApi.get(lang, "hello.world")).thenReturn("hello world!");
    
    String actual = messages.at("hello.world");
    String expected = "hello world!";
    assertThat(actual).siEqualTo(expected);
    
    verify(messageApi).get(lang, "hello.world");
  }
}

```

```cc

```

```
```


