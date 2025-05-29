---
title: ParagraphFormat.FarEastLineBreakControl
linktitle: FarEastLineBreakControl
articleTitle: FarEastLineBreakControl
second_title: Aspose.Words for .NET
description: 发现 ParagraphFormat FarEastLineBreakControl 属性，启用东亚换行规则，以便在文档中实现精确的文本格式。
type: docs
weight: 110
url: /zh/net/aspose.words/paragraphformat/fareastlinebreakcontrol/
---
## ParagraphFormat.FarEastLineBreakControl property

获取或设置一个标志，指示东亚换行规则是否适用于当前段落。

```csharp
public bool FarEastLineBreakControl { get; set; }
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
