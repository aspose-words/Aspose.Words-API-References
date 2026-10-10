---
title: "Aspose::Words::LowCode::Comparer class"
linktitle: "Comparer"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::LowCode::Comparer class. 提供用于在 C++ 中比较文档的方法。"
type: docs
weight: 500
url: /zh/cpp/aspose.words.lowcode/comparer/
---
## Comparer class


提供用于比较文档的方法。

```cpp
class Comparer : public Aspose::Words::LowCode::Processor
```

## 方法

| 方法 | 描述 |
| --- | --- |
| static [Compare](./compare/)(const System::String\&, const System::String\&, const System::String\&, const System::String\&, System::DateTime) | 比较两个文档并使用附加选项，将差异保存到指定的输出文件中，以编辑和格式修订的数量形式生成更改。 |
| static [Compare](./compare/)(const System::String\&, const System::String\&, const System::String\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) | 比较两个文档并使用附加选项，将差异保存到指定的输出文件中，以编辑和格式修订的数量形式生成更改。 |
| static [Compare](./compare/)(const System::String\&, const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, System::DateTime) | 比较两个文档并使用附加选项，将差异保存到指定的输出文件中，使用提供的保存格式，以编辑和格式修订的数量形式生成更改。 |
| static [Compare](./compare/)(const System::String\&, const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) | 比较两个文档并使用附加选项，将差异保存到指定的输出文件中，使用提供的保存格式，以编辑和格式修订的数量形式生成更改。 |
| static [Compare](./compare/)(const System::String\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, System::DateTime) | 比较两个文档并使用附加选项，将差异保存到指定的输出文件中，使用提供的保存格式，以编辑和格式修订的数量形式生成更改。 |
| static [Compare](./compare/)(const System::String\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) | 比较两个文档并使用附加选项，将差异保存到指定的输出文件中，使用提供的保存格式，以编辑和格式修订的数量形式生成更改。 |
| static [Compare](./compare/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&, System::DateTime) | 比较从流加载的两个文档并使用附加选项，将差异保存到提供的输出流中，使用指定的保存格式，以编辑和格式修订的数量形式生成更改。 |
| static [Compare](./compare/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) | 比较从流加载的两个文档并使用附加选项，将差异保存到提供的输出流中，使用指定的保存格式，以编辑和格式修订的数量形式生成更改。 |
| static [Compare](./compare/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, System::DateTime) | 比较从流加载的两个文档并使用附加选项，将差异保存到提供的输出流中，使用指定的保存格式，以编辑和格式修订的数量形式生成更改。 |
| static [Compare](./compare/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) | 比较从流加载的两个文档并使用附加选项，将差异保存到提供的输出流中，使用指定的保存格式，以编辑和格式修订的数量形式生成更改。 |
| static [CompareToImages](./comparetoimages/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, System::DateTime) | 比较两个文档并将差异保存为图像。返回数组中的每个项表示输出的单页渲染图像。 |
| static [CompareToImages](./comparetoimages/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) | 比较两个文档并将差异保存为图像。返回数组中的每个项表示输出的单页渲染图像。 |
| static [CompareToImages](./comparetoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, System::DateTime) | 比较两个文档并将差异保存为图像。返回数组中的每个项表示输出的单页渲染图像。 |
| static [CompareToImages](./comparetoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) | 比较两个文档并将差异保存为图像。返回数组中的每个项表示输出的单页渲染图像。 |
| static [Create](./create/)() | 创建转换处理器的新实例。 |
| static [Create](./create/)(const System::SharedPtr\<Aspose::Words::LowCode::ComparerContext\>\&) | 创建比较处理器的新实例。 |
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
## 另见

* Class [Processor](../processor/)
* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
