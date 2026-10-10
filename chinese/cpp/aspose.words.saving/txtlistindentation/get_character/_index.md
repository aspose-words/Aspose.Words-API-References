---
title: "Aspose::Words::Saving::TxtListIndentation::get_Character 方法"
linktitle: "get_Character"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::TxtListIndentation::get_Character 方法。获取或设置用于缩进列表级别的字符。默认值为 ''\\\\0''，表示在 C++ 中没有缩进。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words.saving/txtlistindentation/get_character/
---
## TxtListIndentation::get_Character method


获取或设置用于缩进列表级别的字符。默认值为 '\0'，这表示没有缩进。

```cpp
char16_t Aspose::Words::Saving::TxtListIndentation::get_Character() const
```


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

* Class [TxtListIndentation](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
