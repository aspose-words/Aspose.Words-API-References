---
title: "Aspose::Words::Saving::OdtSaveOptions::get_IsStrictSchema11 方法"
linktitle: "get_IsStrictSchema11"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::OdtSaveOptions::get_IsStrictSchema11 方法。指定导出是否严格符合 ODT 规范 1.1。OOo 3.0 在文件包含 ODT 1.2 的元素和属性时能够正确显示。使用 \"false\" 以实现此目的，或使用 \"true\" 以严格符合规范 1.1。默认值在 C++ 中为 false。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words.saving/odtsaveoptions/get_isstrictschema11/
---
## OdtSaveOptions::get_IsStrictSchema11 method


指定导出是否严格符合 ODT 规范 1.1。OOo 3.0 在文件包含 ODT 1.2 的元素和属性时能够正确显示。为此请使用 "false"，或使用 "true" 以严格符合规范 1.1。默认值为 **false**。

```cpp
bool Aspose::Words::Saving::OdtSaveOptions::get_IsStrictSchema11() const
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

* Class [OdtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
