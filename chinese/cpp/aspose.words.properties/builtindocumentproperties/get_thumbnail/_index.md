---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_Thumbnail 方法"
linktitle: "get_Thumbnail"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::get_Thumbnail 方法。获取或设置文档的缩略图（C++）。"
type: docs
weight: 28000
url: /zh/cpp/aspose.words.properties/builtindocumentproperties/get_thumbnail/
---
## BuiltInDocumentProperties::get_Thumbnail method


获取或设置文档的缩略图。

```cpp
System::ArrayPtr<uint8_t> Aspose::Words::Properties::BuiltInDocumentProperties::get_Thumbnail()
```

## 备注


目前此属性仅在文档导出为 ePub 时使用，未在其他文档格式中读取或写入。

可以将任意格式的图像设置到此属性，但在导出时会检查其格式。

仅可使用 gif、jpeg 和 png 图像进行 ePub 发布。

## 示例



展示如何向保存为 Epub 的文档添加缩略图。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// 如果我们将一个文档，其 \"Thumbnail\" 属性包含我们添加的图像数据，保存为 Epub，
// 打开该文档的阅读器可能会在第一页之前显示该图像。
System::SharedPtr<Aspose::Words::Properties::BuiltInDocumentProperties> properties = doc->get_BuiltInDocumentProperties();

System::ArrayPtr<uint8_t> thumbnailBytes = System::IO::File::ReadAllBytes(get_ImageDir() + u"Logo.jpg");
properties->set_Thumbnail(thumbnailBytes);

doc->Save(get_ArtifactsDir() + u"DocumentProperties.Thumbnail.epub");

// 我们可以提取文档的缩略图并将其保存到本地文件系统。
System::SharedPtr<Aspose::Words::Properties::DocumentProperty> thumbnail = doc->get_BuiltInDocumentProperties()->idx_get(u"Thumbnail");
System::IO::File::WriteAllBytes(get_ArtifactsDir() + u"DocumentProperties.Thumbnail.gif", thumbnail->ToByteArray());
```

## 另见

* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
