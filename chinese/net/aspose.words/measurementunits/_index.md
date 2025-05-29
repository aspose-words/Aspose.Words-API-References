---
title: MeasurementUnits Enum
linktitle: MeasurementUnits
articleTitle: MeasurementUnits
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.MeasurementUnits 枚举，在文档处理中实现精确的单位选择。使用精准的测量选项增强您的工作流程！
type: docs
weight: 4840
url: /zh/net/aspose.words/measurementunits/
---
## MeasurementUnits enumeration

指定测量单位。

```csharp
public enum MeasurementUnits
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Inches | `0` | 英寸. |
| Centimeters | `1` | 厘米. |
| Millimeters | `2` | 毫米. |
| Points | `3` | 分. |
| Picas | `4` | Picas（常用于传统打字机字体间距）。 |

## 例子

展示如何使保存的文档符合旧的 ODT 模式。

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

OdtSaveOptions saveOptions = new OdtSaveOptions
{
    MeasureUnit = OdtSaveMeasureUnit.Centimeters,
    IsStrictSchema11 = exportToOdt11Specs
};

doc.Save(ArtifactsDir + "OdtSaveOptions.Odt11Schema.odt", saveOptions);
```

### 也可以看看

* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
