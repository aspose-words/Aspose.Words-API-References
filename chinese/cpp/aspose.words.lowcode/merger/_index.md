---
title: "Aspose::Words::LowCode::Merger 类"
linktitle: "Merger"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::LowCode::Merger 类。表示一组用于在 C++ 中将各种不同类型的文档合并为单个输出文档的方法。"
type: docs
weight: 1000
url: /zh/cpp/aspose.words.lowcode/merger/
---
## Merger class


表示一组旨在将各种不同类型文档合并为单个输出文档的方法。

```cpp
class Merger : public Aspose::Words::LowCode::Processor
```

## 方法

| 方法 | 描述 |
| --- | --- |
| static [Create](./create/)() | 创建邮件合并处理器的新实例。 |
| static [Create](./create/)(const System::SharedPtr\<Aspose::Words::LowCode::MergerContext\>\&) | 创建邮件合并处理器的新实例。 |
| [Execute](../processor/execute/)() | 执行处理器操作。 |
| [Execute](../processor/execute/)(System::Threading::CancellationToken) | 执行处理器操作，允许使用指定的取消令牌取消文档处理任务。 |
| [From](../processor/from/)(const System::String\&) | 指定用于处理的输入文档。 |
| [From](../processor/from/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | 指定用于处理的输入文档。 |
| [From](../processor/from/)(const System::SharedPtr\<System::IO::Stream\>\&) | 指定用于处理的输入文档。 |
| [From](../processor/from/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | 指定用于处理的输入文档。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Merge](./merge/)(const System::String\&, const System::ArrayPtr\<System::String\>\&) | 使用指定的输入和输出文件名以及 [KeepSourceFormatting](../mergeformatmode/) 将给定的输入文档合并为单个输出文档。 |
| static [Merge](./merge/)(const System::String\&, const System::ArrayPtr\<System::String\>\&, Aspose::Words::SaveFormat, Aspose::Words::LowCode::MergeFormatMode) | 使用指定的输入输出文件名和最终文档格式将给定的输入文档合并为单个输出文档。 |
| static [Merge](./merge/)(const System::String\&, const System::ArrayPtr\<System::String\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, Aspose::Words::LowCode::MergeFormatMode) | 使用指定的输入输出文件名和保存选项将给定的输入文档合并为单个输出文档。 |
| static [Merge](./merge/)(const System::String\&, const System::ArrayPtr\<System::String\>\&, const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, Aspose::Words::LowCode::MergeFormatMode) | 使用指定的输入输出文件名和保存选项将给定的输入文档合并为单个输出文档。 |
| static [Merge](./merge/)(const System::ArrayPtr\<System::String\>\&, Aspose::Words::LowCode::MergeFormatMode) | 将给定的输入文档合并为单个文档，并返回最终文档的 [Document](../../aspose.words/document/) 实例。 |
| static [Merge](./merge/)(const System::ArrayPtr\<System::String\>\&, const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\>\&, Aspose::Words::LowCode::MergeFormatMode) | 将给定的输入文档合并为单个文档，并返回最终文档的 [Document](../../aspose.words/document/) 实例。 |
| static [Merge](./merge/)(const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Document\>\>\&, Aspose::Words::LowCode::MergeFormatMode) | 将给定的输入文档合并为单个文档，并返回最终文档的 [Document](../../aspose.words/document/) 实例。 |
| static [Merge](./merge/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>\&, Aspose::Words::SaveFormat) | 使用指定的输入输出流和最终文档格式将给定的输入文档合并为单个输出文档。 |
| static [Merge](./merge/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, Aspose::Words::LowCode::MergeFormatMode) | 使用指定的输入输出流和保存选项将给定的输入文档合并为单个输出文档。 |
| static [Merge](./merge/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>\&, const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, Aspose::Words::LowCode::MergeFormatMode) | 使用指定的输入输出流和保存选项将给定的输入文档合并为单个输出文档。 |
| static [Merge](./merge/)(const System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>\&, Aspose::Words::LowCode::MergeFormatMode) | 将给定的输入文档合并为单个文档，并返回最终文档的 [Document](../../aspose.words/document/) 实例。 |
| static [Merge](./merge/)(const System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>\&, const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\>\&, Aspose::Words::LowCode::MergeFormatMode) | 将给定的输入文档合并为单个文档，并返回最终文档的 [Document](../../aspose.words/document/) 实例。 |
| static [MergeToImages](./mergetoimages/)(const System::ArrayPtr\<System::String\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, Aspose::Words::LowCode::MergeFormatMode) | 使用指定的输入输出文件名和保存选项将给定的输入文档合并为单个输出文档。将输出渲染为图像。 |
| static [MergeToImages](./mergetoimages/)(const System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, Aspose::Words::LowCode::MergeFormatMode) | 使用指定的图像保存选项将给定的输入文档流合并为单个输出文档。将输出渲染为图像。 |
| [To](../processor/to/)(const System::String\&) | 指定处理器的输出文件。 |
| [To](../processor/to/)(const System::String\&, System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>) | 指定处理器的输出文件。 |
| [To](../processor/to/)(const System::String\&, Aspose::Words::SaveFormat) | 指定处理器的输出文件。 |
| [To](../processor/to/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | 指定处理器的输出流。 |
| [To](../processor/to/)(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) | 指定处理器的输出流。 |
| [To](../processor/to/)(const System::SharedPtr\<System::Collections::Generic::List\<System::SharedPtr\<System::IO::Stream\>\>\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) |  |
| [To](../processor/to/)(const System::SharedPtr\<System::Collections::Generic::List\<System::SharedPtr\<System::IO::Stream\>\>\>\&, Aspose::Words::SaveFormat) |  |
| static [Type](./type/)() |  |
## 备注


指定的输入和输出文件或流，以及所需的合并和保存选项，用于将给定的输入文档合并为单个输出文档。

合并功能支持超过 35 种不同的文件格式。
## 另见

* Class [Processor](../processor/)
* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
