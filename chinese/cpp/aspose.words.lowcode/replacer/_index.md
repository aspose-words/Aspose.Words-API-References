---
title: "Aspose::Words::LowCode::Replacer class"
linktitle: "Replacer"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::LowCode::Replacer class. 提供用于在 C++ 中查找和替换文档文本的方法。"
type: docs
weight: 1250
url: /zh/cpp/aspose.words.lowcode/replacer/
---
## Replacer class


提供用于在文档中查找和替换文本的方法。

```cpp
class Replacer : public Aspose::Words::LowCode::Processor
```

## 方法

| 方法 | 描述 |
| --- | --- |
| static [Create](./create/)(const System::SharedPtr\<Aspose::Words::LowCode::ReplacerContext\>\&) | 创建 replacer 处理器的新实例。 |
| [Execute](../processor/execute/)() | 执行处理器操作。 |
| [Execute](../processor/execute/)(System::Threading::CancellationToken) | 执行处理器操作，允许使用指定的取消令牌取消文档处理任务。 |
| [From](../processor/from/)(const System::String\&) | 指定用于处理的输入文档。 |
| [From](../processor/from/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | 指定用于处理的输入文档。 |
| [From](../processor/from/)(const System::SharedPtr\<System::IO::Stream\>\&) | 指定用于处理的输入文档。 |
| [From](../processor/from/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | 指定用于处理的输入文档。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Replace](./replace/)(const System::String\&, const System::String\&, const System::String\&, const System::String\&) | 在输入文件中将指定的字符字符串模式的所有出现替换为替换字符串。 |
| static [Replace](./replace/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, const System::String\&) | 在输入文件中将指定的字符字符串模式的所有出现替换为替换字符串，并使用指定的保存格式和其他选项。 |
| static [Replace](./replace/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) | 在输入文件中将指定的字符字符串模式的所有出现替换为替换字符串，并使用指定的保存格式和其他选项。 |
| static [Replace](./replace/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::String\&) | 在输入文件中将指定的字符字符串模式的所有出现替换为替换字符串，并使用指定的保存格式和其他选项。 |
| static [Replace](./replace/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) | 在输入文件中将指定的字符字符串模式的所有出现替换为替换字符串，并使用指定的保存格式和其他选项。 |
| static [Replace](./replace/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&, const System::String\&) | 在输入流中将指定的字符字符串模式的所有出现替换为替换字符串，并使用指定的保存格式和其他选项。 |
| static [Replace](./replace/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) | 在输入流中将指定的字符字符串模式的所有出现替换为替换字符串，并使用指定的保存格式和其他选项。 |
| static [Replace](./replace/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::String\&) | 在输入流中将指定的字符字符串模式的所有出现替换为替换字符串，并使用指定的保存格式和其他选项。 |
| static [Replace](./replace/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) | 在输入流中将指定的字符字符串模式的所有出现替换为替换字符串，并使用指定的保存格式和其他选项。 |
| static [Replace](./replace/)(const System::String\&, const System::String\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) | 在输入文件中使用正则表达式将指定的字符字符串模式的所有出现替换为替换字符串。 |
| static [Replace](./replace/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) | 在输入文件中使用正则表达式将指定的字符字符串模式的所有出现替换为替换字符串，并使用指定的保存格式和其他选项。 |
| static [Replace](./replace/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) | 在输入文件中使用正则表达式将指定的字符字符串模式的所有出现替换为替换字符串，并使用指定的保存格式和其他选项。 |
| static [Replace](./replace/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) | 在输入文件中使用正则表达式将指定的字符字符串模式的所有出现替换为替换字符串，并使用指定的保存格式和其他选项。 |
| static [Replace](./replace/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) | 在输入文件中使用正则表达式将指定的字符字符串模式的所有出现替换为替换字符串，并使用指定的保存格式和其他选项。 |
| static [Replace](./replace/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) | 在输入流中使用正则表达式将指定的字符字符串模式的所有出现替换为替换字符串，并使用指定的保存格式和其他选项。 |
| static [Replace](./replace/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) | 在输入流中使用正则表达式将指定的字符字符串模式的所有出现替换为替换字符串，并使用指定的保存格式和其他选项。 |
| static [Replace](./replace/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) | 在输入流中使用正则表达式将指定的字符字符串模式的所有出现替换为替换字符串，并使用指定的保存格式和其他选项。 |
| static [Replace](./replace/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) | 在输入流中使用正则表达式将指定的字符字符串模式的所有出现替换为替换字符串，并使用指定的保存格式和其他选项。 |
| static [ReplaceToImages](./replacetoimages/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, const System::String\&) | 在输入文件中将指定的字符字符串模式的所有出现替换为替换字符串。将输出渲染为图像。 |
| static [ReplaceToImages](./replacetoimages/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) | 在输入文件中将指定的字符字符串模式的所有出现替换为替换字符串。将输出渲染为图像。 |
| static [ReplaceToImages](./replacetoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, const System::String\&) | 在输入文件中将指定的字符字符串模式的所有出现替换为替换字符串。将输出渲染为图像。 |
| static [ReplaceToImages](./replacetoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) | 在输入文件中将指定的字符字符串模式的所有出现替换为替换字符串。将输出渲染为图像。 |
| static [ReplaceToImages](./replacetoimages/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) | 在输入文件中将指定的正则表达式模式的所有出现替换为替换字符串。将输出渲染为图像。 |
| static [ReplaceToImages](./replacetoimages/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) | 在输入文件中将指定的正则表达式模式的所有出现替换为替换字符串。将输出渲染为图像。 |
| static [ReplaceToImages](./replacetoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) | 在输入文件中将指定的正则表达式模式的所有出现替换为替换字符串。将输出渲染为图像。 |
| static [ReplaceToImages](./replacetoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) | 在输入文件中将指定的正则表达式模式的所有出现替换为替换字符串。将输出渲染为图像。 |
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
