---
title: ControlChar.Cr
linktitle: Cr
articleTitle: Cr
second_title: Aspose.Words for .NET
description: 探索 ControlChar Cr，即回车符（x000d 或 r），它可以增强文本格式。使用我们独特的解决方案简化您的编码！
type: docs
weight: 50
url: /zh/net/aspose.words/controlchar/cr/
---
## ControlChar.Cr field

回车符：“\x000d”或“\r”。与[`ParagraphBreak`](../paragraphbreak/).

```csharp
public static readonly string Cr;
```

## 例子

展示如何使用控制字符。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 使用 DocumentBuilder 插入带有文本的段落。
builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

// 将文档转换为文本形式显示控制字符
// 表示文档的一些结构元素，例如分页符。
Assert.AreEqual($"Hello world!{ControlChar.Cr}" +
                $"Hello again!{ControlChar.Cr}" +
                ControlChar.PageBreak, doc.GetText());

// 将文档转换为字符串形式时，
// 我们可以使用 Trim 方法省略一些控制字符。
Assert.AreEqual($"Hello world!{ControlChar.Cr}" +
                "Hello again!", doc.GetText().Trim());
```

### 也可以看看

* class [ControlChar](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
