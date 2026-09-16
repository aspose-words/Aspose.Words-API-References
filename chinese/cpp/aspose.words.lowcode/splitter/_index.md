---
title: "Aspose::Words::LowCode::Splitter 类"
linktitle: "Splitter"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::LowCode::Splitter 类。提供用于使用不同标准在 C++ 中将文档拆分为多个部分的方法。"
type: docs
weight: 1500
url: /zh/cpp/aspose.words.lowcode/splitter/
---
## Splitter class


提供用于使用不同标准将文档拆分为多个部分的方法。

```cpp
class Splitter : public Aspose::Words::LowCode::Processor
```

## 方法

| 方法 | 描述 |
| --- | --- |
| static [Create](./create/)(const System::SharedPtr\<Aspose::Words::LowCode::SplitterContext\>\&) | 创建拆分处理器的新实例。 |
| [Execute](../processor/execute/)() | 执行处理器操作。 |
| [Execute](../processor/execute/)(System::Threading::CancellationToken) | 执行处理器操作，允许使用指定的取消令牌取消文档处理任务。 |
| static [ExtractPages](./extractpages/)(const System::String\&, const System::String\&, int32_t, int32_t) | 从文档文件中提取指定范围的页面，并将提取的页面保存到新文件中。输出文件格式由输出文件名的扩展名决定。 |
| static [ExtractPages](./extractpages/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, int32_t, int32_t) | 从文档文件中提取指定范围的页面，并使用指定的保存格式将提取的页面保存到新文件中。 |
| static [ExtractPages](./extractpages/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, int32_t, int32_t) | 从文档文件中提取指定范围的页面，并使用指定的保存格式将提取的页面保存到新文件中。 |
| static [ExtractPages](./extractpages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, int32_t, int32_t) | 从文档流中提取指定范围的页面，并使用指定的保存格式将提取的页面保存到输出流中。 |
| static [ExtractPages](./extractpages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, int32_t, int32_t) | 从文档流中提取指定范围的页面，并使用指定的保存格式将提取的页面保存到输出流中。 |
| [From](../processor/from/)(const System::String\&) | 指定用于处理的输入文档。 |
| [From](../processor/from/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | 指定用于处理的输入文档。 |
| [From](../processor/from/)(const System::SharedPtr\<System::IO::Stream\>\&) | 指定用于处理的输入文档。 |
| [From](../processor/from/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | 指定用于处理的输入文档。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [RemoveBlankPages](./removeblankpages/)(const System::String\&, const System::String\&) | 从文档中移除空白页并保存输出。返回被移除的页码列表。 |
| static [RemoveBlankPages](./removeblankpages/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat) | 从文档中移除空白页并以指定格式保存输出。返回被移除的页码列表。 |
| static [RemoveBlankPages](./removeblankpages/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | 从文档中移除空白页并以指定格式保存输出。返回被移除的页码列表。 |
| static [RemoveBlankPages](./removeblankpages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) | 从输入流提供的文档中移除空白页，并以指定的保存格式将更新后的文档保存到输出流中。返回被移除的页码列表。 |
| static [RemoveBlankPages](./removeblankpages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | 从输入流提供的文档中移除空白页，并以指定的保存格式将更新后的文档保存到输出流中。返回被移除的页码列表。 |
| static [Split](./split/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\&) | 根据指定的拆分选项将文档拆分为多个部分，并将生成的部分保存为文件。输出文件格式由输出文件名的扩展名决定。 |
| static [Split](./split/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\&) | 根据指定的拆分选项将文档拆分为多个部分，并以指定的保存格式将生成的部分保存为文件。 |
| static [Split](./split/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\&) | 根据指定的拆分选项将文档拆分为多个部分，并以指定的保存格式将生成的部分保存为文件。 |
| static [Split](./split/)(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\&) | 从输入流中的文档根据指定的拆分选项拆分为多个部分，并以指定的保存格式将生成的部分作为流数组返回。 |
| static [Split](./split/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\&) | 从输入流中的文档根据指定的拆分选项拆分为多个部分，并以指定的保存格式将生成的部分作为流数组返回。 |
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
