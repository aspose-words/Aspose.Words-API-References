---
title: "Aspose::Words::Font::get_NameOther method"
linktitle: "get_NameOther"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Font::get_NameOther 方法。返回或设置在 C++ 中用于字符代码在 128 到 255 之间的字符的字体。"
type: docs
weight: 29000
url: /zh/cpp/aspose.words/font/get_nameother/
---
## Font::get_NameOther method


返回或设置用于字符代码从 128 到 255 的字符的字体。

```cpp
System::String Aspose::Words::Font::get_NameOther()
```


## 示例



展示 Microsoft Word 如何在同一段落中组合两种不同的字体。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 假设我们使用构建器插入的段落使用此字体配置
// 包含在 ASCII 字符范围内的字符。在这种情况下，
// 它将使用此字体显示这些字符。
builder->get_Font()->set_NameAscii(u"Calibri");

// 如果未指定其他字体，构建器还会将此字体应用于其插入的所有字符。
ASSERT_EQ(u"Calibri", builder->get_Font()->get_Name());

// 指定一种字体用于所有超出 ASCII 范围的字符。
// 理想情况下，此字体应为每个所需的非 ASCII 字符代码提供字形。
builder->get_Font()->set_NameOther(u"Courier New");

// 插入一个段落，其中一个单词由 ASCII 字符组成，另一个单词包含所有超出该范围的字符。
// 每个字符将根据情况使用其中一种字体进行显示。
builder->Writeln(u"Hello, Привет");

doc->Save(get_ArtifactsDir() + u"Font.NameAscii.docx");
```

## 另见

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
