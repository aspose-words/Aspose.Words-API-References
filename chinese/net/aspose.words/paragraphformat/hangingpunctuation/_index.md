---
title: ParagraphFormat.HangingPunctuation
linktitle: HangingPunctuation
articleTitle: HangingPunctuation
second_title: 用于 .NET 的 Aspose.Words
description: ParagraphFormat HangingPunctuation 财产. 获取或设置是否为当前段落启用悬挂标点的标志 在 C#.
type: docs
weight: 130
url: /zh/net/aspose.words/paragraphformat/hangingpunctuation/
---
## ParagraphFormat.HangingPunctuation property

获取或设置是否为当前段落启用悬挂标点的标志。

```csharp
public bool HangingPunctuation { get; set; }
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
