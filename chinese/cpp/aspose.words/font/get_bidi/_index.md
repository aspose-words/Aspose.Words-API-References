---
title: "Aspose::Words::Font::get_Bidi 方法"
linktitle: "get_Bidi"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Font::get_Bidi 方法。指定此运行的内容是否具有从右到左的特性（在 C++ 中）。"
type: docs
weight: 5000
url: /zh/cpp/aspose.words/font/get_bidi/
---
## Font::get_Bidi method


指定此运行的内容是否应具有从右到左的特性。

```cpp
bool Aspose::Words::Font::get_Bidi()
```

## 备注


当此属性开启时，不应与强左到右文本一起使用。在此情况下的任何行为均未定义。当此属性关闭时，不应与强右到左文本一起使用。在此情况下的任何行为亦未定义。

当显示此运行的内容时，所有字符应被视为复杂脚本字符进行格式化。这意味着在渲染此运行时，将使用 [BoldBi](../get_boldbi/)、[ItalicBi](../get_italicbi/)、[SizeBi](../get_sizebi/) 以及相应的字体名称。

此外，当显示此运行的内容时，此属性对被归类为“弱类型”和“中性类型”的字符起到从右到左的覆盖作用。

## 示例



展示如何为从右到左文本以及从右到左文本定义独立的字体设置集合。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 为从左到右文本定义一组字体设置。
builder->get_Font()->set_Name(u"Courier New");
builder->get_Font()->set_Size(16);
builder->get_Font()->set_Italic(false);
builder->get_Font()->set_Bold(false);
builder->get_Font()->set_LocaleId(System::MakeObject<System::Globalization::CultureInfo>(u"en-US", false)->get_LCID());

// 为从右到左的文本定义另一组字体设置。
builder->get_Font()->set_NameBi(u"Andalus");
builder->get_Font()->set_SizeBi(24);
builder->get_Font()->set_ItalicBi(true);
builder->get_Font()->set_BoldBi(true);
builder->get_Font()->set_LocaleIdBi(System::MakeObject<System::Globalization::CultureInfo>(u"ar-AR", false)->get_LCID());

// 我们可以使用 Bidi 标志来指示即将添加的文本是否
// 使用文档生成器时为从右到左。当我们将此标志设置为 true 时添加文本，
// 它将使用从右到左的字体设置进行格式化。
builder->get_Font()->set_Bidi(true);
builder->Write(u"مرحبًا");

// 将标志设置为 false，然后添加从左到右的文本。
// 文档生成器将使用从左到右的字体设置对这些文本进行格式化。
builder->get_Font()->set_Bidi(false);
builder->Write(u" Hello world!");

doc->Save(get_ArtifactsDir() + u"Font.Bidi.docx");
```

## 另见

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
