---
title: ParagraphFormat.BaselineAlignment
second_title: Aspose.Words for .NET API 参考
description: ParagraphFormat 财产. 获取或设置字体在一行上的垂直位置
type: docs
weight: 40
url: /zh/net/aspose.words/paragraphformat/baselinealignment/
---
## ParagraphFormat.BaselineAlignment property

获取或设置字体在一行上的垂直位置。

```csharp
public BaselineAlignment BaselineAlignment { get; set; }
```

### 例子

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
* 命名空间 [Aspose.Words](../../paragraphformat/)
* 部件 [Aspose.Words](../../../)


