---
title: RtfLoadOptions.RecognizeUtf8Text
linktitle: RecognizeUtf8Text
articleTitle: RecognizeUtf8Text
second_title: Aspose.Words for .NET
description: 了解 RtfLoadOptions RecognizeUtf8Text 属性如何在导入期间保留 UTF-8 字符，以确保准确的文本表示和无缝集成。
type: docs
weight: 20
url: /zh/net/aspose.words.loading/rtfloadoptions/recognizeutf8text/
---
## RtfLoadOptions.RecognizeUtf8Text property

当设置为`真的`，将尝试检测 UTF8 字符， 它们将在导入期间被保留。

```csharp
public bool RecognizeUtf8Text { get; set; }
```

## 评论

默认值为`错误的`。

## 例子

展示如何在加载 RTF 文档时检测 UTF-8 字符。

```csharp
// 创建一个“RtfLoadOptions”对象来修改我们加载 RTF 文档的方式。
RtfLoadOptions loadOptions = new RtfLoadOptions();

// 将“RecognizeUtf8Text”属性设置为“false”，以假定文档使用 ISO 8859-1 字符集
// 并加载文档中的每个字符。
// 将“RecognizeUtf8Text”属性设置为“true”以解析文本中可能出现的任何可变长度字符。
loadOptions.RecognizeUtf8Text = recognizeUtf8Text;

Document doc = new Document(MyDir + "UTF-8 characters.rtf", loadOptions);

Assert.AreEqual(
    recognizeUtf8Text
        ? "“John Doe´s list of currency symbols”™\r" +
          "€, ¢, £, ¥, ¤"
        : "â€œJohn DoeÂ´s list of currency symbolsâ€\u009dâ„¢\r" +
          "â‚¬, Â¢, Â£, Â¥, Â¤",
    doc.FirstSection.Body.GetText().Trim());
```

### 也可以看看

* class [RtfLoadOptions](../)
* 命名空间 [Aspose.Words.Loading](../../../aspose.words.loading/)
* 部件 [Aspose.Words](../../../)
