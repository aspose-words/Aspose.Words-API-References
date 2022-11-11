---
title: I字段UserPromptRespondent
second_title: Aspose.Words for Java API 参考
description:代表字段更新期间用户提示的响应者。
type: docs
weight: 645
url: /zh/java/com.aspose.words/ifielduserpromptrespondent/
---
```
public interface I字段UserPromptRespondent
```

代表字段更新期间用户提示的响应者。 ASK 和 FILLIN 字段是提示用户做出某些响应的字段示例。实现此接口并将其分配给[字段Options.getUserPromptRespondent()](../../com.aspose.words/fieldoptions\#getUserPromptRespondent--) / [字段Options.setUserPromptRespondent(com.aspose.words.I字段UserPromptRespondent)](../../com.aspose.words/fieldoptions\#setUserPromptRespondent-com.aspose.words.I字段UserPromptRespondent-)属性来建立字段更新和用户之间的交互。
## 方法s

| 方法 | 描述 |
| --- | --- |
| [respond(String promptText, String defaultResponse)](#respond-java.lang.String-java.lang.String-) | 实施后，在提示时返回用户的响应。 |
### respond(String promptText, String defaultResponse) {#respond-java.lang.String-java.lang.String-}
```
public abstract String respond(String promptText, String defaultResponse)
```


实施后，在提示时返回用户的响应。你的实现应该返回**null**表示用户没有响应提示（即用户在提示窗口中按下了取消按钮）。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| promptText | java.lang.String | 提示文本（即提示窗口的标题）。 |
| defaultResponse | java.lang.String | 默认用户响应（即提示窗口中包含的初始值）。 |

**退货:**
java.lang.String - 用户响应（即提示窗口中包含的确认值）。