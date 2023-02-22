---
title: ControlChar.Cr
second_title: Aspose.Words for .NET API 参考
description: ControlChar 场地. 回车符x000d或r如同ParagraphBreak.
type: docs
weight: 50
url: /zh/net/aspose.words/controlchar/cr/
---
## ControlChar.Cr field

回车符：“\x000d”或“\r”。如同[`ParagraphBreak`](../paragraphbreak/).

```csharp
public static readonly string Cr;
```

### 例子

显示如何使用控制字符。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 使用 DocumentBuilder 插入带有文本的段落。
builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

// 将文档转换为文本形式显示控制字符
// 表示文档的一些结构元素，比如分页符。
Assert.AreEqual($"Hello world!{ControlChar.Cr}" +
                $"Hello again!{ControlChar.Cr}" +
                ControlChar.PageBreak, doc.GetText());

// 将文档转换为字符串形式时，
// 我们可以用 Trim 方法省略一些控制字符。
Assert.AreEqual($"Hello world!{ControlChar.Cr}" +
                "Hello again!", doc.GetText().Trim());
```

### 也可以看看

* class [ControlChar](../)
* 命名空间 [Aspose.Words](../../controlchar/)
* 部件 [Aspose.Words](../../../)


