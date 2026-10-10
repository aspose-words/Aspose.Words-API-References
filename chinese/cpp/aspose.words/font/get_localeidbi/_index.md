---
title: "Aspose::Words::Font::get_LocaleIdBi 方法"
linktitle: "get_LocaleIdBi"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Font::get_LocaleIdBi 方法。获取或设置 C++ 中格式化的从右到左字符的区域标识符（语言）。"
type: docs
weight: 23000
url: /zh/cpp/aspose.words/font/get_localeidbi/
---
## Font::get_LocaleIdBi method


获取或设置已格式化的从右到左字符的区域标识符（语言）。

```cpp
int32_t Aspose::Words::Font::get_LocaleIdBi()
```


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
