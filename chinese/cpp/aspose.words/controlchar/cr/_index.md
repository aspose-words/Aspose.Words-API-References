---
title: "Aspose::Words::ControlChar::Cr 方法"
linktitle: "Cr"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::ControlChar::Cr 方法。回车字符：\"\\x000d\" 或 \"\\r\"。在 C++ 中等同于 ParagraphBreak。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words/controlchar/cr/
---
## ControlChar::Cr method


回车字符："\x000d" 或 "\r"。等同于 [ParagraphBreak](../paragraphbreak/)。

```cpp
static System::String & Aspose::Words::ControlChar::Cr()
```


## 示例



展示如何使用控制字符。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 使用 DocumentBuilder 插入带文本的段落。
builder->Writeln(u"Hello world!");
builder->Writeln(u"Hello again!");

// 将文档转换为文本形式会显示控制字符
// 表示文档的一些结构元素，例如分页符。
ASSERT_EQ(System::String::Format(u"Hello world!{0}", Aspose::Words::ControlChar::Cr()) + System::String::Format(u"Hello again!{0}", Aspose::Words::ControlChar::Cr()) + Aspose::Words::ControlChar::PageBreak(), doc->GetText());

// 在将文档转换为字符串形式时，
// 我们可以使用 Trim 方法省略一些控制字符。
ASSERT_EQ(System::String::Format(u"Hello world!{0}", Aspose::Words::ControlChar::Cr()) + u"Hello again!", doc->GetText().Trim());
```

## 另见

* Class [ControlChar](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
