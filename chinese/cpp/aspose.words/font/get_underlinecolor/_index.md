---
title: "Aspose::Words::Font::get_UnderlineColor 方法"
linktitle: "get_UnderlineColor"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Font::get_UnderlineColor 方法。获取或设置在 C++ 中应用于字体的下划线颜色。"
type: docs
weight: 56000
url: /zh/cpp/aspose.words/font/get_underlinecolor/
---
## Font::get_UnderlineColor method


获取或设置应用于字体的下划线颜色。

```cpp
System::Drawing::Color Aspose::Words::Font::get_UnderlineColor()
```


## 示例



展示如何配置文本下划线的样式和颜色。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Underline(Aspose::Words::Underline::Dotted);
builder->get_Font()->set_UnderlineColor(System::Drawing::Color::get_Red());

builder->Writeln(u"Underlined text.");

doc->Save(get_ArtifactsDir() + u"Font.Underlines.docx");
```

## 另见

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
