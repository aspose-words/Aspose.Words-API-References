---
title: Font.NameOther
linktitle: NameOther
articleTitle: NameOther
second_title: 用于 .NET 的 Aspose.Words
description: Font NameOther 财产. 返回或设置字符代码从 128 到 255 的字符所使用的字体 在 C#.
type: docs
weight: 270
url: /zh/net/aspose.words/font/nameother/
---
## Font.NameOther property

返回或设置字符代码从 128 到 255 的字符所使用的字体。

```csharp
public string NameOther { get; set; }
```

## 例子

展示 Microsoft Word 如何在一次运行中组合两种不同的字体。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 假设我们使用构建器在使用此字体配置时插入运行
// 包含 ASCII 字符范围内的字符。在这种情况下，
// 它将使用此字体显示这些字符。
builder.Font.NameAscii = "Calibri";

// 如果没有指定其他字体，构建器也会将此字体应用于它插入的所有字符。
Assert.AreEqual("Calibri", builder.Font.Name);

// 指定 ASCII 范围之外的所有字符使用的字体。
// 理想情况下，此字体应该为每个所需的非 ASCII 字符代码都有一个字形。
builder.Font.NameOther = "Courier New";

// 插入一个包含 ASCII 字符的单词和一个包含该范围之外的所有字符的单词的运行。
// 每个字符将使用其中一种字体显示，具体取决于。
builder.Writeln("Hello, Привет");

doc.Save(ArtifactsDir + "Font.NameAscii.docx");
```

### 也可以看看

* property [Name](../name/)
* class [Font](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
