---
title: ParagraphFormat.WordWrap
second_title: Aspose.Words for .NET API 参考
description: ParagraphFormat 财产. 如果此属性是错误的 单词中间的拉丁文本可以换行 for 当前段落否则拉丁文本将被整个单词包围
type: docs
weight: 410
url: /zh/net/aspose.words/paragraphformat/wordwrap/
---
## ParagraphFormat.WordWrap property

如果此属性是`错误的` 单词中间的拉丁文本可以换行 for 当前段落。否则拉丁文本将被整个单词包围。

```csharp
public bool WordWrap { get; set; }
```

### 例子

展示如何设置亚洲版式的特殊属性。

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
* 命名空间 [Aspose.Words](../../paragraphformat/)
* 部件 [Aspose.Words](../../../)


