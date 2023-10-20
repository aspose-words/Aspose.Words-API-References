---
title: HyphenationOptions.HyphenationZone
linktitle: HyphenationZone
articleTitle: HyphenationZone
second_title: 用于 .NET 的 Aspose.Words
description: HyphenationOptions HyphenationZone 财产. 获取或设置距右边距 1/20 的点的距离在该距离内您不希望 对单词进行连字符 此属性的默认值为 3600.25 英寸 在 C#.
type: docs
weight: 50
url: /zh/net/aspose.words.settings/hyphenationoptions/hyphenationzone/
---
## HyphenationOptions.HyphenationZone property

获取或设置距右边距 1/20 的点的距离，在该距离内您不希望 对单词进行连字符。 此属性的默认值为 360（0.25 英寸）。

```csharp
public int HyphenationZone { get; set; }
```

## 例子

展示如何配置自动连字。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Size = 24;
builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc.HyphenationOptions.AutoHyphenation = true;
doc.HyphenationOptions.ConsecutiveHyphenLimit = 2;
doc.HyphenationOptions.HyphenationZone = 720;
doc.HyphenationOptions.HyphenateCaps = true;

doc.Save(ArtifactsDir + "Document.HyphenationOptions.docx");
```

### 也可以看看

* class [HyphenationOptions](../)
* 命名空间 [Aspose.Words.Settings](../../../aspose.words.settings/)
* 部件 [Aspose.Words](../../../)
