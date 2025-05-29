---
title: OdtSaveMeasureUnit Enum
linktitle: OdtSaveMeasureUnit
articleTitle: OdtSaveMeasureUnit
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.OdtSaveMeasureUnit 枚举，精确控制文档尺寸。轻松增强您的文档格式！
type: docs
weight: 6100
url: /zh/net/aspose.words.saving/odtsavemeasureunit/
---
## OdtSaveMeasureUnit enumeration

指定在保存期间应用于可测量文档内容（如形状、宽度等）的测量单位。

```csharp
public enum OdtSaveMeasureUnit
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Centimeters | `0` | 指定使用厘米保存文档内容。 |
| Inches | `1` | 指定使用英寸保存文档内容。 |

## 例子

展示如何使用不同的测量单位来定义已保存的 ODT 文档的样式参数。

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// 当我们将文档导出为 .odt 时，我们可以使用 OdtSaveOptions 对象来修改我们保存文档的方式。
// 我们可以将“MeasureUnit”属性设置为“OdtSaveMeasureUnit.Centimeters”
 // 使用 Open Office 使用的公制系统来定义样式参数等内容。
// 我们可以将“MeasureUnit”属性设置为“OdtSaveMeasureUnit.Inches”
// 使用 Microsoft Word 所使用的英制系统来定义样式参数等内容。
OdtSaveOptions saveOptions = new OdtSaveOptions
{
    MeasureUnit = odtSaveMeasureUnit
};

doc.Save(ArtifactsDir + "OdtSaveOptions.Odt11Schema.odt", saveOptions);
```

### 也可以看看

* 命名空间 [Aspose.Words.Saving](../../aspose.words.saving/)
* 部件 [Aspose.Words](../../)
