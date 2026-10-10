---
title: "Aspose::Words::LowCode::Processor 类"
linktitle: "Processor"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::LowCode::Processor 类。用于在 C++ 中执行不同文档处理操作的处理器类。"
type: docs
weight: 1126
url: /zh/cpp/aspose.words.lowcode/processor/
---
## Processor class


[Processor](./) class for performing different document processing actions.

```cpp
class Processor : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [Execute](./execute/)() | 执行处理器操作。 |
| [Execute](./execute/)(System::Threading::CancellationToken) | 执行处理器操作，允许使用指定的取消令牌取消文档处理任务。 |
| [From](./from/)(const System::String\&) | 指定用于处理的输入文档。 |
| [From](./from/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | 指定用于处理的输入文档。 |
| [From](./from/)(const System::SharedPtr\<System::IO::Stream\>\&) | 指定用于处理的输入文档。 |
| [From](./from/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | 指定用于处理的输入文档。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [To](./to/)(const System::String\&) | 指定处理器的输出文件。 |
| [To](./to/)(const System::String\&, System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>) | 指定处理器的输出文件。 |
| [To](./to/)(const System::String\&, Aspose::Words::SaveFormat) | 指定处理器的输出文件。 |
| [To](./to/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | 指定处理器的输出流。 |
| [To](./to/)(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) | 指定处理器的输出流。 |
| [To](./to/)(const System::SharedPtr\<System::Collections::Generic::List\<System::SharedPtr\<System::IO::Stream\>\>\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) |  |
| [To](./to/)(const System::SharedPtr\<System::Collections::Generic::List\<System::SharedPtr\<System::IO::Stream\>\>\>\&, Aspose::Words::SaveFormat) |  |
| static [Type](./type/)() |  |
## 另见

* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
