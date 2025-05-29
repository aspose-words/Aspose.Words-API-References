---
title: ParagraphFormat.BaselineAlignment
linktitle: BaselineAlignment
articleTitle: BaselineAlignment
second_title: Aspose.Words for .NET
description: 使用 ParagraphFormat BaselineAlignment 属性优化文本布局，可以精确控制字体垂直定位，从而增强可读性。
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

展示如何设置一行上的字体垂直位置。

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
