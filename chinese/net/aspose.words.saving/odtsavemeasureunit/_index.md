---
title: Enum OdtSaveMeasureUnit
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.Saving.OdtSaveMeasureUnit 枚举. 指定的测量单位应用于保存期间可测量的文档内容例如形状宽度和其他
type: docs
weight: 5040
url: /zh/net/aspose.words.saving/odtsavemeasureunit/
---
## OdtSaveMeasureUnit enumeration

指定的测量单位应用于保存期间可测量的文档内容，例如形状、宽度和其他。

```csharp
public enum OdtSaveMeasureUnit
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Centimeters | `0` | 指定以厘米为单位保存文档内容。 |
| Inches | `1` | 指定使用英寸保存文档内容。 |

### 例子

展示如何使用不同的测量单位来定义保存的 ODT 文档的样式参数。

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// 当我们将文档导出为 .odt 时，我们可以使用 OdtSaveOptions 对象来修改我们保存文档的方式。
// 我们可以将“MeasureUnit”属性设置为“OdtSaveMeasureUnit.Centimeters”
// 使用 Open Office 使用的公制系统定义样式参数等内容。 
// 我们可以将“MeasureUnit”属性设置为“OdtSaveMeasureUnit.Inches”
// 使用 Microsoft Word 使用的英制系统定义样式参数等内容。
OdtSaveOptions saveOptions = new OdtSaveOptions
{
    MeasureUnit = odtSaveMeasureUnit
};

doc.Save(ArtifactsDir + "OdtSaveOptions.Odt11Schema.odt", saveOptions);
```

### 也可以看看

* 命名空间 [Aspose.Words.Saving](../../aspose.words.saving/)
* 部件 [Aspose.Words](../../)


