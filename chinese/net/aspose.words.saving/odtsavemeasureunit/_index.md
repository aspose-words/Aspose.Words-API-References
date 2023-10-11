---
title: Enum OdtSaveMeasureUnit
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.Saving.OdtSaveMeasureUnit 枚举. 保存期间应用于可测量文档内容例如形状宽度等的指定测量单位
type: docs
weight: 5320
url: /zh/net/aspose.words.saving/odtsavemeasureunit/
---
## OdtSaveMeasureUnit enumeration

保存期间应用于可测量文档内容（例如形状、宽度等）的指定测量单位。

```csharp
public enum OdtSaveMeasureUnit
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Centimeters | `0` | 指定文档内容以厘米为单位保存。 |
| Inches | `1` | 指定文档内容以英寸为单位保存。 |

### 例子

演示如何使用不同的测量单位来定义已保存 ODT 文档的样式参数。

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// 当我们将文档导出为.odt时，我们可以使用OdtSaveOptions对象来修改保存文档的方式。
// 我们可以将“MeasureUnit”属性设置为“OdtSaveMeasureUnit.Centimeters”
 // 使用 Open Office 使用的公制来定义样式参数等内容。
// 我们可以将“MeasureUnit”属性设置为“OdtSaveMeasureUnit.Inches”
// 使用 Microsoft Word 使用的英制系统来定义样式参数等内容。
OdtSaveOptions saveOptions = new OdtSaveOptions
{
    MeasureUnit = odtSaveMeasureUnit
};

doc.Save(ArtifactsDir + "OdtSaveOptions.Odt11Schema.odt", saveOptions);
```

### 也可以看看

* 命名空间 [Aspose.Words.Saving](../../aspose.words.saving/)
* 部件 [Aspose.Words](../../)


