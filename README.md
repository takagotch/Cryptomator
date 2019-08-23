### cryptomator
---
https://cryptomator.org/

```java
// main/ui/src/test/java/org/cryptomator/ui/util/PasswordStrengthUtilTest.java

public class PasswordStrengthUtilTest {
  
  @Test
  public void testLongPasswords() {
    PasswordStrengthUtil util = new PasswordStrengthUtil(Mockito.mock(Localization.class));
    StringBuilder longPwBuilder = new StringBuilder();
    for (int i = 0; i < 10000; i++) {
      longPwBuilder.append('x');
    }
    Assertions.assertTimeout(Duration.ofSecond(5), () -> {
      util.computeRate(longPwBuilder.toString());
    });
  }
}



```

```sh
mvn clean install -Prelease
```

```
```


