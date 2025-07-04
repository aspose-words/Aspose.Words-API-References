---
title: Aspose::Words::Border::get_LineStyle method
linktitle: get_LineStyle
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Border::get_LineStyle method. Gets or sets the border style in C++.'
type: docs
weight: 7000
url: /cpp/aspose.words/border/get_linestyle/
---
## Border::get_LineStyle method


Gets or sets the border style.

```cpp
Aspose::Words::LineStyle Aspose::Words::Border::get_LineStyle()
```

## Remarks


If you set line style to none, then line width is automatically changed to zero.

## Examples



Shows how to insert a string surrounded by a border into a document. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->get_Border()->set_Color(System::Drawing::Color::get_Green());
builder->get_Font()->get_Border()->set_LineWidth(2.5);
builder->get_Font()->get_Border()->set_LineStyle(Aspose::Words::LineStyle::DashDotStroker);

builder->Write(u"Text surrounded by green border.");

doc->Save(get_ArtifactsDir() + u"Border.FontBorder.docx");
```

## See Also

* Enum [LineStyle](../../linestyle/)
* Class [Border](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
