---
title: "Aspose::Words::Saving::ResourceSavingArgs class"
linktitle: "ResourceSavingArgs"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::ResourceSavingArgs 类。提供 ResourceSaving() 事件的数据。要了解更多信息，请访问 C++ 文档文章。"
type: docs
weight: 27000
url: /zh/cpp/aspose.words.saving/resourcesavingargs/
---
## ResourceSavingArgs class


提供 [ResourceSaving()](../iresourcesavingcallback/resourcesaving/) 事件的数据。要了解更多信息，请访问 [Save a Document](https://docs.aspose.com/words/cpp/save-a-document/) 文档文章。

```cpp
class ResourceSavingArgs : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_Document](./get_document/)() const | 获取当前正在保存的文档对象。 |
| [get_KeepResourceStreamOpen](./get_keepresourcestreamopen/)() const | 指定 Aspose.Words 在保存资源后是保持流打开还是关闭。 |
| [get_ResourceFileName](./get_resourcefilename/)() const | 获取或设置资源将被保存到的文件名（不含路径）。 |
| [get_ResourceFileUri](./get_resourcefileuri/)() const | 获取或设置用于从文档引用资源文件的统一资源标识符（URI）。 |
| [get_ResourceStream](./get_resourcestream/)() const | 允许指定资源将要保存的流。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_KeepResourceStreamOpen](./set_keepresourcestreamopen/)(bool) | 用于设置 [Aspose::Words::Saving::ResourceSavingArgs::get_KeepResourceStreamOpen](./get_keepresourcestreamopen/)。 |
| [set_ResourceFileName](./set_resourcefilename/)(const System::String\&) | 用于设置 [Aspose::Words::Saving::ResourceSavingArgs::get_ResourceFileName](./get_resourcefilename/)。 |
| [set_ResourceFileUri](./set_resourcefileuri/)(const System::String\&) | 用于设置 [Aspose::Words::Saving::ResourceSavingArgs::get_ResourceFileUri](./get_resourcefileuri/)。 |
| [set_ResourceStream](./set_resourcestream/)(const System::SharedPtr\<System::IO::Stream\>\&) | 用于设置 [Aspose::Words::Saving::ResourceSavingArgs::get_ResourceStream](./get_resourcestream/)。 |
| [set_ResourceStream](./set_resourcestream/)(std::basic_ostream\<CharType, Traits\>\&) |  |
| static [Type](./type/)() |  |
## 备注


默认情况下，当 Aspose.Words 将文档保存为固定页面的 HTML、SVG 或 Markdown 时，它会将每个资源保存到单独的文件中。Aspose.Words 使用文档文件名和唯一编号为文档中找到的每个资源生成唯一的文件名。

[ResourceSavingArgs](./) allows to redefine how resource file names are generated or to completely circumvent saving of resources into files by providing your own stream objects.

要应用您自己的资源文件名生成逻辑，请使用 [ResourceFileName](./get_resourcefilename/) 属性。

要将资源保存到流而不是文件，请使用 [ResourceStream](./get_resourcestream/) 属性。
## 另见

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
