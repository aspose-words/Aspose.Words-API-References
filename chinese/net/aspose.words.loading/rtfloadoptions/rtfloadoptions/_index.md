---
title: RtfLoadOptions
linktitle: RtfLoadOptions
articleTitle: RtfLoadOptions
second_title: 用于 .NET 的 Aspose.Words
description: RtfLoadOptions 构造函数. 使用默认值初始化此类的新实例 在 C#.
type: docs
weight: 10
url: /zh/net/aspose.words.loading/rtfloadoptions/rtfloadoptions/
---
## RtfLoadOptions constructor

使用默认值初始化此类的新实例。

```csharp
public RtfLoadOptions()
```

## 例子

展示如何在加载 RTF 文档时检测 UTF-8 字符。

```csharp
// 创建一个“RtfLoadOptions”对象来修改我们加载 RTF 文档的方式。
RtfLoadOptions loadOptions = new RtfLoadOptions();

// 将“RecognizeUtf8Text”属性设置为“false”以假定文档使用 ISO 8859-1 字符集
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
