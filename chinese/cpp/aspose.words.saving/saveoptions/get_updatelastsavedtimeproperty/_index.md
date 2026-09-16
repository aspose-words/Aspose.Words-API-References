---
title: "Aspose::Words::Saving::SaveOptions::get_UpdateLastSavedTimeProperty 方法"
linktitle: "get_UpdateLastSavedTimeProperty"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::SaveOptions::get_UpdateLastSavedTimeProperty 方法。获取或设置一个值，以确定在 C++ 中保存之前是否更新 LastSavedTime 属性。"
type: docs
weight: 19000
url: /zh/cpp/aspose.words.saving/saveoptions/get_updatelastsavedtimeproperty/
---
## SaveOptions::get_UpdateLastSavedTimeProperty method


获取或设置一个值，以确定在保存之前是否更新 [LastSavedTime](../../../aspose.words.properties/builtindocumentproperties/get_lastsavedtime/) 属性。

```cpp
bool Aspose::Words::Saving::SaveOptions::get_UpdateLastSavedTimeProperty() const
```


## 示例



展示如何确定在保存时是否保留文档的 “Last saved time” 属性。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

ASSERT_EQ(System::DateTime(2021, 5, 11, 6, 32, 0), doc->get_BuiltInDocumentProperties()->get_LastSavedTime());

// 当我们将文档保存为 OOXML 格式时，可以创建一个 OoxmlSaveOptions 对象
// 然后将其传递给文档的保存方法，以修改文档的保存方式。
// 将 “UpdateLastSavedTimeProperty” 属性设置为 “true” 以
// 将输出文档的 “Last saved time” 内置属性设置为当前日期/时间。
// 将 “UpdateLastSavedTimeProperty” 属性设置为 “false” 以
// 保留输入文档的 “Last saved time” 内置属性的原始值。
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_UpdateLastSavedTimeProperty(updateLastSavedTimeProperty);

doc->Save(get_ArtifactsDir() + u"OoxmlSaveOptions.LastSavedTime.docx", saveOptions);

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OoxmlSaveOptions.LastSavedTime.docx");
System::DateTime lastSavedTimeNew = doc->get_BuiltInDocumentProperties()->get_LastSavedTime();

if (updateLastSavedTimeProperty)
{
    ASSERT_TRUE((System::DateTime::get_Now() - lastSavedTimeNew).get_Days() < 1);
}
else
{
    ASSERT_EQ(System::DateTime(2021, 5, 11, 6, 32, 0), lastSavedTimeNew);
}
```

## 另见

* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
