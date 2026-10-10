---
title: "Aspose::Words::Font::get_Border 方法"
linktitle: "get_Border"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Font::get_Border 方法。返回一个在 C++ 中指定字体边框的 Border 对象。"
type: docs
weight: 8000
url: /zh/cpp/aspose.words/font/get_border/
---
## Font::get_Border method


返回一个指定字体边框的 [Border](../../border/) 对象。

```cpp
System::SharedPtr<Aspose::Words::Border> Aspose::Words::Font::get_Border()
```


## 示例



展示如何在文档中插入被边框包围的字符串。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->get_Border()->set_Color(System::Drawing::Color::get_Green());
builder->get_Font()->get_Border()->set_LineWidth(2.5);
builder->get_Font()->get_Border()->set_LineStyle(Aspose::Words::LineStyle::DashDotStroker);

builder->Write(u"Text surrounded by green border.");

doc->Save(get_ArtifactsDir() + u"Border.FontBorder.docx");
```

## 另见

* Class [Border](../../border/)
* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
