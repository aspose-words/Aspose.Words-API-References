---
title: "Aspose::Words::Font::get_Size 方法"
linktitle: "get_Size"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Font::get_Size 方法。获取或设置 C++ 中以点为单位的字体大小。"
type: docs
weight: 36000
url: /zh/cpp/aspose.words/font/get_size/
---
## Font::get_Size method


获取或设置字体大小（磅）。

```cpp
double Aspose::Words::Font::get_Size()
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


展示如何使用其字体属性格式化文本运行。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto run = System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!");

System::SharedPtr<Aspose::Words::Font> font = run->get_Font();
font->set_Name(u"Courier New");
font->set_Size(36);
font->set_HighlightColor(System::Drawing::Color::get_Yellow());

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);
doc->Save(get_ArtifactsDir() + u"Font.CreateFormattedRun.docx");
```

## 另见

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
