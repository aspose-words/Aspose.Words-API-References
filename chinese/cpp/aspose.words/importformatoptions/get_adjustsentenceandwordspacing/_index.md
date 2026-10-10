---
title: "Aspose::Words::ImportFormatOptions::get_AdjustSentenceAndWordSpacing method"
linktitle: "get_AdjustSentenceAndWordSpacing"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::ImportFormatOptions::get_AdjustSentenceAndWordSpacing 方法。获取或设置一个布尔值，指定是否自动调整句子和单词间距。默认值在 C++ 中为 false。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words/importformatoptions/get_adjustsentenceandwordspacing/
---
## ImportFormatOptions::get_AdjustSentenceAndWordSpacing method


获取或设置一个布尔值，指定是否自动调整句子和单词间距。默认值为 **false**。

```cpp
bool Aspose::Words::ImportFormatOptions::get_AdjustSentenceAndWordSpacing() const
```


## 示例



展示如何自动调整句子和单词间距。
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::Document>();
auto dstDoc = System::MakeObject<Aspose::Words::Document>();

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(srcDoc);
builder->Write(u"Dolor sit amet.");

builder = System::MakeObject<Aspose::Words::DocumentBuilder>(dstDoc);
builder->Write(u"Lorem ipsum.");

auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();
options->set_AdjustSentenceAndWordSpacing(true);
builder->InsertDocument(srcDoc, Aspose::Words::ImportFormatMode::UseDestinationStyles, options);

ASSERT_EQ(u"Lorem ipsum. Dolor sit amet.", dstDoc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetText().Trim());
```

## 另见

* Class [ImportFormatOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
