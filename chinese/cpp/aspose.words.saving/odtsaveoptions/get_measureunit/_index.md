---
title: "Aspose::Words::Saving::OdtSaveOptions::get_MeasureUnit 方法"
linktitle: "get_MeasureUnit"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::OdtSaveOptions::get_MeasureUnit 方法。允许指定用于文档内容的度量单位。默认值是 C++ 中的厘米。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words.saving/odtsaveoptions/get_measureunit/
---
## OdtSaveOptions::get_MeasureUnit method


允许指定用于文档内容的度量单位。默认值是 [厘米](../../odtsavemeasureunit/)

```cpp
Aspose::Words::Saving::OdtSaveMeasureUnit Aspose::Words::Saving::OdtSaveOptions::get_MeasureUnit() const
```


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

* Enum [OdtSaveMeasureUnit](../../odtsavemeasureunit/)
* Class [OdtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
