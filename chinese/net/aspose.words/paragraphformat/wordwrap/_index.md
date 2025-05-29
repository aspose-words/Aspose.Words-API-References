---
title: ParagraphFormat.WordWrap
linktitle: WordWrap
articleTitle: WordWrap
second_title: Aspose.Words for .NET
description: 了解 ParagraphFormat WordWrap 属性如何影响 Word 中的文本换行。学习如何控制拉丁文本的换行方式，从而提高文档的可读性。
type: docs
weight: 420
url: /zh/net/aspose.words/paragraphformat/wordwrap/
---
## ParagraphFormat.WordWrap property

如果此属性是`错误的`，单词中间的拉丁文本可以按 当前段落换行。否则，拉丁文本将按整个单词换行。

```csharp
public bool WordWrap { get; set; }
```

## 例子

展示如何设置亚洲字体的特殊属性。

```csharp
Document doc = new Document(MyDir + "Document.docx");

ParagraphFormat format = doc.FirstSection.Body.FirstParagraph.ParagraphFormat;
format.FarEastLineBreakControl = true;
format.WordWrap = false;
format.HangingPunctuation = true;

doc.Save(ArtifactsDir + "ParagraphFormat.AsianTypographyProperties.docx");
```

### 也可以看看

* class [ParagraphFormat](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
