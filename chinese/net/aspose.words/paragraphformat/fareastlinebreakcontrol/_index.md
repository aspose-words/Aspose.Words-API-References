---
title: FarEastLineBreakControl
second_title: Aspose.Words for .NET API 参考
description: 获取或设置一个标志指示是否将东亚换行规则应用于当前段落
type: docs
weight: 100
url: /zh/net/aspose.words/paragraphformat/fareastlinebreakcontrol/
---
## ParagraphFormat.FarEastLineBreakControl property

获取或设置一个标志，指示是否将东亚换行规则应用于当前段落。

```csharp
public bool FarEastLineBreakControl { get; set; }
```

### 例子

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

* class [ParagraphFormat](../../paragraphformat)
* 命名空间 [Aspose.Words](../../paragraphformat)
* 部件 [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->