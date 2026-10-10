---
title: "Aspose::Words::Saving::TxtSaveOptions::get_ListIndentation 方法"
linktitle: "get_ListIndentation"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::TxtSaveOptions::get_ListIndentation 方法。获取一个 TxtListIndentation 对象，该对象指定在列表级别缩进时使用多少个以及哪种字符。默认情况下，字符 ''\\\\0'' 的计数为零，这意味着在 C++ 中没有缩进。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words.saving/txtsaveoptions/get_listindentation/
---
## TxtSaveOptions::get_ListIndentation method


获取一个 [TxtListIndentation](../../txtlistindentation/) 对象，该对象指定在列表级别缩进时使用多少个以及哪种字符。默认情况下，字符 '\\0' 的计数为零，这意味着没有缩进。

```cpp
System::SharedPtr<Aspose::Words::Saving::TxtListIndentation> Aspose::Words::Saving::TxtSaveOptions::get_ListIndentation() const
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

* Class [TxtListIndentation](../../txtlistindentation/)
* Class [TxtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
