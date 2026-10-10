---
title: "Aspose::Words::FileFormatUtil 类"
linktitle: "FileFormatUtil"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::FileFormatUtil 类。提供用于处理文件格式的实用方法，例如检测文件格式或在文件扩展名与文件格式枚举之间相互转换。欲了解更多，请访问 C++ 文档文章。"
type: docs
weight: 28000
url: /zh/cpp/aspose.words/fileformatutil/
---
## FileFormatUtil class


提供处理文件格式的实用方法，例如检测文件格式或在文件扩展名与文件格式枚举之间相互转换。要了解更多信息，请访问 [Detect File Format and Check Format Compatibility](https://docs.aspose.com/words/cpp/detect-file-format-and-check-format-compatibility/) 文档文章。

```cpp
class FileFormatUtil
```

## 方法

| 方法 | 描述 |
| --- | --- |
| static [ContentTypeToLoadFormat](./contenttypetoloadformat/)(const System::String\&) | 将 IANA 内容类型转换为加载格式枚举值。 |
| static [ContentTypeToSaveFormat](./contenttypetosaveformat/)(const System::String\&) | 将 IANA 内容类型转换为保存格式枚举值。 |
| static [DetectFileFormat](./detectfileformat/)(const System::String\&) | 检测并返回存储在磁盘文件中的文档格式信息。 |
| static [DetectFileFormat](./detectfileformat/)(const System::SharedPtr\<System::IO::Stream\>\&) | 检测并返回存储在流中的文档格式信息。 |
| static [DetectFileFormat](./detectfileformat/)(std::basic_istream\<CharType, Traits\>\&) |  |
| static [ExtensionToSaveFormat](./extensiontosaveformat/)(const System::String\&) | 将文件名扩展名转换为 [SaveFormat](../saveformat/) 值。 |
| [FileFormatUtil](./fileformatutil/)() |  |
| static [ImageTypeToExtension](./imagetypetoextension/)(Aspose::Words::Drawing::ImageType) | 将 Aspose.Words 图像类型枚举值转换为文件扩展名。返回的扩展名是带前导点的小写字符串。 |
| static [LoadFormatToExtension](./loadformattoextension/)(Aspose::Words::LoadFormat) | 将加载格式枚举值转换为文件扩展名。返回的扩展名是带前导点的小写字符串。 |
| static [LoadFormatToSaveFormat](./loadformattosaveformat/)(Aspose::Words::LoadFormat) | 如果可能，将 [LoadFormat](../loadformat/) 值转换为 [SaveFormat](../saveformat/) 值。 |
| static [SaveFormatToExtension](./saveformattoextension/)(Aspose::Words::SaveFormat) | 将保存格式枚举值转换为文件扩展名。返回的扩展名是带前导点的小写字符串。 |
| static [SaveFormatToLoadFormat](./saveformattoloadformat/)(Aspose::Words::SaveFormat) | 如果可能，将 [SaveFormat](../saveformat/) 值转换为 [LoadFormat](../loadformat/) 值。 |

## 示例



展示如何检测 html 文件的编码。
```cpp
System::SharedPtr<Aspose::Words::FileFormatInfo> info = Aspose::Words::FileFormatUtil::DetectFileFormat(get_MyDir() + u"Document.html");

ASSERT_EQ(Aspose::Words::LoadFormat::Html, info->get_LoadFormat());

// Encoding 属性仅在我们为 html 文档创建 FileFormatInfo 对象时使用。
ASSERT_EQ(u"Western European (Windows)", info->get_Encoding()->get_EncodingName());
ASSERT_EQ(1252, info->get_Encoding()->get_CodePage());
```

## 另见

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
