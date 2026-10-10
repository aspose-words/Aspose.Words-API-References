---
title: "Aspose::Words::Saving::SaveOptions::get_UpdateLastPrintedProperty 方法"
linktitle: "get_UpdateLastPrintedProperty"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::SaveOptions::get_UpdateLastPrintedProperty 方法。获取或设置决定在 C++ 中保存前是否更新 LastPrinted 属性的值。"
type: docs
weight: 18000
url: /zh/cpp/aspose.words.saving/saveoptions/get_updatelastprintedproperty/
---
## SaveOptions::get_UpdateLastPrintedProperty method


获取或设置决定在保存前是否更新 [LastPrinted](../../../aspose.words.properties/builtindocumentproperties/get_lastprinted/) 属性的值。

```cpp
bool Aspose::Words::Saving::SaveOptions::get_UpdateLastPrintedProperty() const
```


## 示例



展示如何在保存时更新文档的 “Last printed” 属性。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::DateTime lastPrinted(2019, 12, 20);
doc->get_BuiltInDocumentProperties()->set_LastPrinted(lastPrinted);

// 此标志决定是否更新作为内置属性的最后打印日期。
// 如果是，则使用文档最近一次保存操作的日期
// 将此 SaveOptions 对象作为参数传入时，用作打印日期。
auto saveOptions = System::MakeObject<Aspose::Words::Saving::DocSaveOptions>();
saveOptions->set_UpdateLastPrintedProperty(isUpdateLastPrintedProperty);

// 在 Microsoft Word 2003 中，可通过 文件 -> 属性 -> 统计信息 -> 已打印 来找到此属性。
// 也可以通过使用 PRINTDATE 域将其显示在文档正文中。
doc->Save(get_ArtifactsDir() + u"DocSaveOptions.UpdateLastPrintedProperty.doc", saveOptions);

// 打开已保存的文档，然后验证该属性的值。
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"DocSaveOptions.UpdateLastPrintedProperty.doc");

if (isUpdateLastPrintedProperty)
{
    ASSERT_NE(lastPrinted, doc->get_BuiltInDocumentProperties()->get_LastPrinted());
}
else
{
    ASSERT_EQ(lastPrinted, doc->get_BuiltInDocumentProperties()->get_LastPrinted());
}
```

## 另见

* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
