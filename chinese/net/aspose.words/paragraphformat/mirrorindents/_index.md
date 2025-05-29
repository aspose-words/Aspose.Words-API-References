---
title: ParagraphFormat.MirrorIndents
linktitle: MirrorIndents
articleTitle: MirrorIndents
second_title: Aspose.Words for .NET
description: 了解 ParagraphFormat MirrorIndents 属性如何通过确保左右缩进一致以获得美观的外观来增强文档格式。
type: docs
weight: 240
url: /zh/net/aspose.words/paragraphformat/mirrorindents/
---
## ParagraphFormat.MirrorIndents property

获取或设置一个标志，指示左右缩进是否具有相同的宽度。

```csharp
public bool MirrorIndents { get; set; }
```

## 例子

展示如何使左缩进和右缩进相同。

```csharp
Document doc = new Document(MyDir + "Document.docx");
ParagraphFormat format = doc.FirstSection.Body.Paragraphs[0].ParagraphFormat;

format.MirrorIndents = true;

doc.Save(ArtifactsDir + "ParagraphFormat.MirrorIndents.docx");
```

### 也可以看看

* class [ParagraphFormat](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
