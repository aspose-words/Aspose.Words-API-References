---
title: ParagraphFormat.BaselineAlignment
linktitle: BaselineAlignment
articleTitle: BaselineAlignment
second_title: 用于 .NET 的 Aspose.Words
description: ParagraphFormat BaselineAlignment 财产. 获取或设置字体在一行上的垂直位置 在 C#.
type: docs
weight: 40
url: /zh/net/aspose.words/paragraphformat/baselinealignment/
---
## ParagraphFormat.BaselineAlignment property

获取或设置字体在一行上的垂直位置。

```csharp
public BaselineAlignment BaselineAlignment { get; set; }
```

## 例子

演示如何设置字体在一行上的垂直位置。

```csharp
Document doc = new Document(MyDir + "Office math.docx");

ParagraphFormat format = doc.FirstSection.Body.Paragraphs[0].ParagraphFormat;
if (format.BaselineAlignment == BaselineAlignment.Auto)
{                
    format.BaselineAlignment = BaselineAlignment.Top;
}

doc.Save(ArtifactsDir + "ParagraphFormat.ParagraphBaselineAlignment.docx");
```

### 也可以看看

* enum [BaselineAlignment](../../baselinealignment/)
* class [ParagraphFormat](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
