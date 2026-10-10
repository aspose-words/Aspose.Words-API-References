---
title: "Aspose::Words::LowCode::Converter 类"
linktitle: "Converter"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::LowCode::Converter 类。表示一组方法，旨在使用 C++ 中的一行代码转换各种不同类型的文档。"
type: docs
weight: 600
url: /zh/cpp/aspose.words.lowcode/converter/
---
## Converter class


表示一组旨在使用单行代码转换各种不同类型文档的方法。

```cpp
class Converter : public Aspose::Words::LowCode::Processor
```

## 方法

| 方法 | 描述 |
| --- | --- |
| static [Convert](./convert/)(const System::String\&, const System::String\&) | 使用指定的输入输出文件名及其扩展名，将给定的输入文档转换为输出文档。 |
| static [Convert](./convert/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat) | 使用指定的输入输出文件名和最终文档格式，将给定的输入文档转换为输出文档。 |
| static [Convert](./convert/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | 使用指定的输入输出文件名和保存选项，将给定的输入文档转换为输出文档。 |
| static [Convert](./convert/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | 使用指定的输入输出文件名及其加载/保存选项，将给定的输入文档转换为输出文档。 |
| static [Convert](./convert/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) | 使用指定的输入和输出流，将给定的输入文档转换为单个输出文档。 |
| static [Convert](./convert/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | 使用指定的输入和输出流，将给定的输入文档转换为单个输出文档。 |
| static [Convert](./convert/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | 使用指定的输入和输出流，将给定的输入文档转换为单个输出文档。 |
| static [ConvertToImages](./converttoimages/)(const System::String\&, const System::String\&) | 将指定输入文件的页面转换为图像文件。 |
| static [ConvertToImages](./converttoimages/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat) | 将指定输入文件的页面转换为指定格式的图像文件。 |
| static [ConvertToImages](./converttoimages/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) | 使用指定的保存选项，将指定输入文件的页面转换为图像文件。 |
| static [ConvertToImages](./converttoimages/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) | 使用提供的加载和保存选项，将指定输入文件的页面转换为图像文件。 |
| static [ConvertToImages](./converttoimages/)(const System::String\&, Aspose::Words::SaveFormat) | 将指定输入文件的页面转换为指定格式的图像，并返回包含这些图像的流数组。 |
| static [ConvertToImages](./converttoimages/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) | 使用指定的保存选项，将指定输入文件的页面转换为图像，并返回包含这些图像的流数组。 |
| static [ConvertToImages](./converttoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) | 将指定输入流的页面转换为指定格式的图像，并返回包含这些图像的流数组。 |
| static [ConvertToImages](./converttoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) | 使用指定的保存选项，将指定输入流的页面转换为图像，并返回包含这些图像的流数组。 |
| static [ConvertToImages](./converttoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) | 使用提供的加载和保存选项，将指定输入流的页面转换为图像，并返回包含这些图像的流数组。 |
| static [ConvertToImages](./converttoimages/)(const System::SharedPtr\<Aspose::Words::Document\>\&, Aspose::Words::SaveFormat) | 将指定文档的页面转换为指定格式的图像，并返回包含这些图像的流数组。 |
| static [ConvertToImages](./converttoimages/)(const System::SharedPtr\<Aspose::Words::Document\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) | 使用指定的保存选项，将指定文档的页面转换为图像，并返回包含这些图像的流数组。 |
| static [Create](./create/)() | 创建转换处理器的新实例。 |
| static [Create](./create/)(const System::SharedPtr\<Aspose::Words::LowCode::ConverterContext\>\&) | 创建转换处理器的新实例。 |
| [Execute](../processor/execute/)() | 执行处理器操作。 |
| [Execute](../processor/execute/)(System::Threading::CancellationToken) | 执行处理器操作，允许使用指定的取消令牌取消文档处理任务。 |
| [From](../processor/from/)(const System::String\&) | 指定用于处理的输入文档。 |
| [From](../processor/from/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | 指定用于处理的输入文档。 |
| [From](../processor/from/)(const System::SharedPtr\<System::IO::Stream\>\&) | 指定用于处理的输入文档。 |
| [From](../processor/from/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | 指定用于处理的输入文档。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [To](../processor/to/)(const System::String\&) | 指定处理器的输出文件。 |
| [To](../processor/to/)(const System::String\&, System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>) | 指定处理器的输出文件。 |
| [To](../processor/to/)(const System::String\&, Aspose::Words::SaveFormat) | 指定处理器的输出文件。 |
| [To](../processor/to/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | 指定处理器的输出流。 |
| [To](../processor/to/)(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) | 指定处理器的输出流。 |
| [To](../processor/to/)(const System::SharedPtr\<System::Collections::Generic::List\<System::SharedPtr\<System::IO::Stream\>\>\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) |  |
| [To](../processor/to/)(const System::SharedPtr\<System::Collections::Generic::List\<System::SharedPtr\<System::IO::Stream\>\>\>\&, Aspose::Words::SaveFormat) |  |
| static [Type](./type/)() |  |
## 备注


使用指定的输入和输出文件或流以及所需的保存格式，将给定的输入文档（一种格式）转换为另一种指定格式的输出文档。

转换功能支持超过 35 种不同的文件格式。

使用 [ConvertToImages()](../) 方法组将文档转换为图像，每页都会转换为单独的图像文件。这些方法还可以直接将 PDF 文档转换为固定页格式，而无需将其加载到文档模型中，从而提升性能和准确性。

使用 [PageSet](../../aspose.words.saving/imagesaveoptions/get_pageset/)，您可以指定要转换为图像的特定页面集合。
## 另见

* Class [Processor](../processor/)
* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
