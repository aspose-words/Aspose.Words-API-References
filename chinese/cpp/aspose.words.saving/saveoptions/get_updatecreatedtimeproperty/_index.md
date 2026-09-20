---
title: "Aspose::Words::Saving::SaveOptions::get_UpdateCreatedTimeProperty 方法"
linktitle: "get_UpdateCreatedTimeProperty"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::SaveOptions::get_UpdateCreatedTimeProperty 方法。获取或设置一个值，以确定在保存之前是否更新 CreatedTime 属性。默认值为 false；在 C++ 中。"
type: docs
weight: 16000
url: /zh/cpp/aspose.words.saving/saveoptions/get_updatecreatedtimeproperty/
---
## SaveOptions::get_UpdateCreatedTimeProperty method


获取或设置一个值，以确定在保存之前是否更新 [CreatedTime](../../../aspose.words.properties/builtindocumentproperties/get_createdtime/) 属性。默认值为 **false**；

```cpp
bool Aspose::Words::Saving::SaveOptions::get_UpdateCreatedTimeProperty() const
```


## 示例



展示如何在保存时更新文档的 "CreatedTime" 属性。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::DateTime createdTime(2019, 12, 20);
doc->get_BuiltInDocumentProperties()->set_CreatedTime(createdTime);

// 此标志决定是否更新创建时间，该时间是内置属性。
// 如果是，则使用文档最近一次保存操作的日期
// 将此 SaveOptions 对象作为参数传递时，用作创建时间。
auto saveOptions = System::MakeObject<Aspose::Words::Saving::DocSaveOptions>();
saveOptions->set_UpdateCreatedTimeProperty(isUpdateCreatedTimeProperty);

doc->Save(get_ArtifactsDir() + u"DocSaveOptions.UpdateCreatedTimeProperty.docx", saveOptions);

// 打开已保存的文档，然后验证该属性的值。
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"DocSaveOptions.UpdateCreatedTimeProperty.docx");

if (isUpdateCreatedTimeProperty)
{
    ASSERT_NE(createdTime, doc->get_BuiltInDocumentProperties()->get_CreatedTime());
}
else
{
    ASSERT_EQ(createdTime, doc->get_BuiltInDocumentProperties()->get_CreatedTime());
}
```

## 另见

* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
