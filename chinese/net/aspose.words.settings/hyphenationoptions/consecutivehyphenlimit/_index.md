---
title: HyphenationOptions.ConsecutiveHyphenLimit
second_title: Aspose.Words for .NET API 参考
description: HyphenationOptions 财产. 获取或设置可以以连字符结尾的最大连续行数 此属性的默认值为 0
type: docs
weight: 30
url: /zh/net/aspose.words.settings/hyphenationoptions/consecutivehyphenlimit/
---
## HyphenationOptions.ConsecutiveHyphenLimit property

获取或设置可以以连字符结尾的最大连续行数。 此属性的默认值为 0。

```csharp
public int ConsecutiveHyphenLimit { get; set; }
```

### 评论

如果此属性的值设置为 0，则任意数量的连续行都可以以连字符结尾。

当保存为固定页面格式（例如 PDF）时，该属性不起作用。

### 例子

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
* 命名空间 [Aspose.Words.Settings](../../hyphenationoptions/)
* 部件 [Aspose.Words](../../../)


