---
title: Enum BaselineAlignment
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.BaselineAlignment 枚举. 指定字体在一行上的垂直位置
type: docs
weight: 20
url: /zh/net/aspose.words/baselinealignment/
---
## BaselineAlignment enumeration

指定字体在一行上的垂直位置。

```csharp
public enum BaselineAlignment
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Top | `0` | 沿每个字体的顶部对齐。 |
| Center | `1` | 对齐每种字体的中心点。 |
| Baseline | `2` | 与段落的基线对齐。 |
| Bottom | `3` | 与每种字体的底部对齐。 |
| Auto | `4` | 基线自动调整。 |

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

* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)


