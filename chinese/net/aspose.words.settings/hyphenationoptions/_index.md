---
title: HyphenationOptions Class
linktitle: HyphenationOptions
articleTitle: HyphenationOptions
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Settings.HyphenationOptions 班级. 允许配置文档断字选项 在 C#.
type: docs
weight: 5790
url: /zh/net/aspose.words.settings/hyphenationoptions/
---
## HyphenationOptions class

允许配置文档断字选项。

```csharp
public class HyphenationOptions
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [HyphenationOptions](hyphenationoptions/)() | 默认构造函数。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [AutoHyphenation](../../aspose.words.settings/hyphenationoptions/autohyphenation/) { get; set; } | 获取或设置确定是否为文档打开自动断字的值。 此属性的默认值为**错误的**. |
| [ConsecutiveHyphenLimit](../../aspose.words.settings/hyphenationoptions/consecutivehyphenlimit/) { get; set; } | 获取或设置可以以连字符结尾的最大连续行数。 此属性的默认值为 0。 |
| [HyphenateCaps](../../aspose.words.settings/hyphenationoptions/hyphenatecaps/) { get; set; } | 获取或设置确定所有大写字母的单词是否连字符的值。 此属性的默认值为**真的**. |
| [HyphenationZone](../../aspose.words.settings/hyphenationoptions/hyphenationzone/) { get; set; } | 获取或设置距离右边距不希望连字的点的 1/20 的距离。 此属性的默认值为 360（0.25 英寸）。 |

## 例子

显示如何配置自动断字。

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

* 命名空间 [Aspose.Words.Settings](../../aspose.words.settings/)
* 部件 [Aspose.Words](../../)
