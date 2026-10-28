---
title: Aspose::Words::Border::set_LineWidth method
linktitle: set_LineWidth
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Border::set_LineWidth method. Sets the border width in points in C++.'
type: docs
weight: 18000
url: /cpp/aspose.words/border/set_linewidth/
---
## Border::set_LineWidth method


Sets the border width in points.

```cpp
void Aspose::Words::Border::set_LineWidth(double value)
```

## Remarks


If you set line width greater than zero when line style is none, the line style is automatically changed to single line.
## Examples


Shows how to insert a string surrounded by a border into a document.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->get_Border()->set_Color(System::Drawing::Color::get_Green());
builder->get_Font()->get_Border()->set_LineWidth(2.5);
builder->get_Font()->get_Border()->set_LineStyle(LineStyle::DashDotStroker);

builder->Write(u"Text surrounded by green border.");

doc->Save(get_ArtifactsDir() + u"Border.FontBorder.docx");
```
## See Also

* Class [Border](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
