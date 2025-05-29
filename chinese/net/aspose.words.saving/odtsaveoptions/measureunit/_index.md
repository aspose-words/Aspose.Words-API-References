---
title: OdtSaveOptions.MeasureUnit
linktitle: MeasureUnit
articleTitle: MeasureUnit
second_title: Aspose.Words for .NET
description: 使用 OdtSaveOptions 自定义文档的 MeasureUnit。选择您喜欢的精度测量单位——默认为厘米。
type: docs
weight: 40
url: /zh/net/aspose.words.saving/odtsaveoptions/measureunit/
---
## OdtSaveOptions.MeasureUnit property

允许指定应用于文档内容的计量单位。 默认值为Centimeters

```csharp
public OdtSaveMeasureUnit MeasureUnit { get; set; }
```

## 评论

Open Office 在文档中指定长度、宽度和其他可测量格式和内容属性时使用厘米，而 MS Office 使用英寸。

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

* enum [OdtSaveMeasureUnit](../../odtsavemeasureunit/)
* class [OdtSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
