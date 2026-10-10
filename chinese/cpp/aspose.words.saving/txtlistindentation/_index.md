---
title: "Aspose::Words::Saving::TxtListIndentation 类"
linktitle: "TxtListIndentation"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::TxtListIndentation 类。指定文档导出为 Text 格式时列表级别的缩进方式。要了解更多，请访问 C++ 文档文章。"
type: docs
weight: 32000
url: /zh/cpp/aspose.words.saving/txtlistindentation/
---
## TxtListIndentation class


指定文档导出为 [Text](../../aspose.words/saveformat/) 格式时列表级别的缩进方式。要了解更多，请访问 [Save a Document](https://docs.aspose.com/words/cpp/save-a-document/) 文档文章。

```cpp
class TxtListIndentation : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_Character](./get_character/)() const | 获取或设置用于缩进列表级别的字符。默认值为 '\0'，这表示没有缩进。 |
| [get_Count](./get_count/)() const | 获取或设置每个列表级别使用多少个 [Character](./get_character/) 作为缩进。默认值为 0，表示没有缩进。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Character](./set_character/)(char16_t) | 用于设置 [Aspose::Words::Saving::TxtListIndentation::get_Character](./get_character/) 的 setter。 |
| [set_Count](./set_count/)(int32_t) | 用于设置 [Aspose::Words::Saving::TxtListIndentation::get_Count](./get_count/) 的 setter。 |
| [TxtListIndentation](./txtlistindentation/)() |  |
| static [Type](./type/)() |  |

## 示例



展示如何在将文档保存为纯文本时配置列表缩进。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 创建一个具有三级缩进的列表。
builder->get_ListFormat()->ApplyNumberDefault();
builder->Writeln(u"Item 1");
builder->get_ListFormat()->ListIndent();
builder->Writeln(u"Item 2");
builder->get_ListFormat()->ListIndent();
builder->Write(u"Item 3");

// 创建一个 "TxtSaveOptions" 对象，可将其传递给文档的 "Save" 方法
// 以修改我们保存文档为纯文本的方式。
auto txtSaveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();

// 设置 "Character" 属性以指定要使用的字符
// 用于填充，以在纯文本中模拟列表缩进。
txtSaveOptions->get_ListIndentation()->set_Character(u' ');

// 设置 "Count" 属性以指定次数
// 为每个列表缩进级别放置填充字符。
txtSaveOptions->get_ListIndentation()->set_Count(3);

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.TxtListIndentation.txt", txtSaveOptions);

System::String docText = System::IO::File::ReadAllText(get_ArtifactsDir() + u"TxtSaveOptions.TxtListIndentation.txt");
System::String newLine = System::Environment::get_NewLine();

ASSERT_EQ(System::String::Format(u"1. Item 1{0}", newLine) + System::String::Format(u"   a. Item 2{0}", newLine) + System::String::Format(u"      i. Item 3{0}", newLine), docText);
```

## 另见

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
