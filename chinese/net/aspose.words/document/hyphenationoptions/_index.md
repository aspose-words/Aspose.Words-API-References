---
title: Document.HyphenationOptions
linktitle: HyphenationOptions
articleTitle: HyphenationOptions
second_title: Aspose.Words for .NET
description: 探索 Document HyphenationOptions 属性来自定义连字设置，增强可读性并改善文档的呈现效果。
type: docs
weight: 220
url: /zh/net/aspose.words/document/hyphenationoptions/
---
## Document.HyphenationOptions property

提供对文档连字选项的访问。

```csharp
public HyphenationOptions HyphenationOptions { get; }
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

* class [HyphenationOptions](../../../aspose.words.settings/hyphenationoptions/)
* class [Document](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
