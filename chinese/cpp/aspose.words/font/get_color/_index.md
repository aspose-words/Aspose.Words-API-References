---
title: "Aspose::Words::Font::get_Color 方法"
linktitle: "get_Color"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Font::get_Color 方法。获取或设置 C++ 中字体的颜色。"
type: docs
weight: 9000
url: /zh/cpp/aspose.words/font/get_color/
---
## Font::get_Color method


获取或设置字体颜色。

```cpp
System::Drawing::Color Aspose::Words::Font::get_Color()
```


## 示例



展示如何使用 [DocumentBuilder](../../documentbuilder/) 插入格式化文本。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 指定字体格式，然后添加文本。
System::SharedPtr<Aspose::Words::Font> font = builder->get_Font();
font->set_Size(16);
font->set_Bold(true);
font->set_Color(System::Drawing::Color::get_Blue());
font->set_Name(u"Courier New");
font->set_Underline(Aspose::Words::Underline::Dash);

builder->Write(u"Hello world!");
```


展示如何插入超链接字段。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"For more information, please visit the ");

// 插入超链接并使用自定义格式进行强调。
// 该超链接将是可点击的文本，能够将我们带到 URL 中指定的位置。
builder->get_Font()->set_Color(System::Drawing::Color::get_Blue());
builder->get_Font()->set_Underline(Aspose::Words::Underline::Single);
builder->InsertHyperlink(u"Google website", u"https://www.google.com", false);
builder->get_Font()->ClearFormatting();
builder->Writeln(u".");

// 在 Microsoft Word 中按 Ctrl 并左键单击文本中的链接，将通过新建的网页浏览器窗口打开该 URL。
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertHyperlink.docx");
```

## 另见

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
