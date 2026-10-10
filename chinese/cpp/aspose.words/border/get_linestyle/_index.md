---
title: "Aspose::Words::Border::get_LineStyle 方法"
linktitle: "get_LineStyle"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Border::get_LineStyle 方法。获取或设置 C++ 中的边框样式。"
type: docs
weight: 7000
url: /zh/cpp/aspose.words/border/get_linestyle/
---
## Border::get_LineStyle method


获取或设置边框样式。

```cpp
Aspose::Words::LineStyle Aspose::Words::Border::get_LineStyle()
```

## 备注


如果将线样式设置为 none，则线宽会自动更改为零。

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

* Enum [LineStyle](../../linestyle/)
* Class [Border](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
