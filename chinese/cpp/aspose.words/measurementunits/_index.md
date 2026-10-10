---
title: "Aspose::Words::MeasurementUnits 枚举"
linktitle: "MeasurementUnits"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::MeasurementUnits 枚举。指定 C++ 中的测量单位。"
type: docs
weight: 100000
url: /zh/cpp/aspose.words/measurementunits/
---
## MeasurementUnits enum


指定计量单位。

```cpp
enum class MeasurementUnits
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| 英寸 | 0 | 英寸。 |
| 厘米 | 1 | 厘米。 |
| 毫米 | 2 | 毫米。 |
| 磅 | 3 | 磅。 |
| 派卡 | 4 | 派卡（常用于传统打字机字体间距）。 |


## 示例



展示如何使已保存的文档符合旧的 ODT 架构。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::OdtSaveOptions>();
saveOptions->set_MeasureUnit(Aspose::Words::Saving::OdtSaveMeasureUnit::Centimeters);
saveOptions->set_IsStrictSchema11(exportToOdt11Specs);

doc->Save(get_ArtifactsDir() + u"OdtSaveOptions.Odt11Schema.odt", saveOptions);

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OdtSaveOptions.Odt11Schema.odt");
ASSERT_EQ(Aspose::Words::MeasurementUnits::Centimeters, doc->get_LayoutOptions()->get_RevisionOptions()->get_MeasurementUnit());
```

## 另见

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
