---
title: "Aspose::Words::Font::get_Bold 方法"
linktitle: "get_Bold"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Font::get_Bold 方法。如果在 C++ 中字体被设置为粗体，则返回 true。"
type: docs
weight: 6000
url: /zh/cpp/aspose.words/font/get_bold/
---
## Font::get_Bold method


如果字体设置为粗体，则为 True。

```cpp
bool Aspose::Words::Font::get_Bold()
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

## 另见

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
