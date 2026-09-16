---
title: "Aspose::Words::Border::get_LineWidth 方法"
linktitle: "get_LineWidth"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Border::get_LineWidth 方法。获取或设置 C++ 中以点为单位的边框宽度。"
type: docs
weight: 8000
url: /zh/cpp/aspose.words/border/get_linewidth/
---
## Border::get_LineWidth method


获取或设置以点为单位的边框宽度。

```cpp
double Aspose::Words::Border::get_LineWidth()
```

## 备注


如果在行样式为 none 时将线宽设置为大于零，行样式会自动更改为单线。

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

* Class [Border](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
