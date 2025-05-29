---
title: HyphenationOptions Class
linktitle: HyphenationOptions
articleTitle: HyphenationOptions
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Settings.HyphenationOptions 类，轻松自定义文档的连字设置并增强文本呈现。
type: docs
weight: 6620
url: /zh/net/aspose.words.settings/hyphenationoptions/
---
## HyphenationOptions class

允许配置文档连字选项。

要了解更多信息，请访问[使用连字符](https://docs.aspose.com/words/net/working-with-hyphenation/)文档文章。

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
| [AutoHyphenation](../../aspose.words.settings/hyphenationoptions/autohyphenation/) { get; set; } | 获取或设置确定文档是否启用自动连字的值。 此属性的默认值为`错误的`. |
| [ConsecutiveHyphenLimit](../../aspose.words.settings/hyphenationoptions/consecutivehyphenlimit/) { get; set; } | 获取或设置可以以连字符结尾的连续行的最大数量。 此属性的默认值为 0。 |
| [HyphenateCaps](../../aspose.words.settings/hyphenationoptions/hyphenatecaps/) { get; set; } | 获取或设置确定全部大写字母的单词是否带连字符的值。 此属性的默认值为`真的`. |
| [HyphenationZone](../../aspose.words.settings/hyphenationoptions/hyphenationzone/) { get; set; } | 获取或设置距离右边距 1/20 点的距离，在该距离内您不希望 对单词进行连字。 此属性的默认值为 360（0.25 英寸）。 |

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

* 命名空间 [Aspose.Words.Settings](../../aspose.words.settings/)
* 部件 [Aspose.Words](../../)
