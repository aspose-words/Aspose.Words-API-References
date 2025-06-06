---
title: Font.NameOther
linktitle: NameOther
articleTitle: NameOther
second_title: Aspose.Words for .NET
description: 探索字体名称其他。轻松自定义字符代码 128-255 的字体，提升文本风格和可读性。立即提升您的设计！
type: docs
weight: 270
url: /zh/net/aspose.words/font/nameother/
---
## Font.NameOther property

返回或设置字符代码从 128 到 255 的字符使用的字体。

```csharp
public string NameOther { get; set; }
```

## 例子

展示 Microsoft Word 如何在一次运行中组合两种不同的字体。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 假设我们在使用此字体配置时使用构建器插入运行
// 包含 ASCII 字符范围内的字符。在这种情况下，
// 它将使用这种字体显示这些字符。
builder.Font.NameAscii = "Calibri";

// 如果未指定其他字体，构建器也会将此字体应用于其插入的所有字符。
Assert.AreEqual("Calibri", builder.Font.Name);

// 指定用于 ASCII 范围之外的所有字符的字体。
// 理想情况下，此字体应该为每个必需的非 ASCII 字符代码提供一个字形。
builder.Font.NameOther = "Courier New";

// 插入一个由 ASCII 字符组成的单词和一个由该范围之外的所有字符组成的单词。
// 每个字符将使用任一字体显示，具体取决于。
builder.Writeln("Hello, Привет");

doc.Save(ArtifactsDir + "Font.NameAscii.docx");
```

### 也可以看看

* property [Name](../name/)
* class [Font](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
