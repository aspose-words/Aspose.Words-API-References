---
title: ParagraphFormat.WordWrap
linktitle: WordWrap
articleTitle: WordWrap
second_title: 用于 .NET 的 Aspose.Words
description: ParagraphFormat WordWrap 财产. 如果这个属性是错误的 单词中间的拉丁文字可以换成 当前段落否则拉丁文字会被整个单词包裹起来 在 C#.
type: docs
weight: 410
url: /zh/net/aspose.words/paragraphformat/wordwrap/
---
## ParagraphFormat.WordWrap property

如果这个属性是**错误的** 单词中间的拉丁文字可以换成 当前段落。否则拉丁文字会被整个单词包裹起来。

```csharp
public bool WordWrap { get; set; }
```

## 例子

展示如何为亚洲字体设置特殊属性。

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
