---
title: get_LineWidth
second_title: Aspose.Words for C++ API Reference
description: Gets or sets the border width in points.
type: docs
weight: 92
url: /cpp/aspose.words/border/get_linewidth/
---
## Border::get_LineWidth method


Gets or sets the border width in points.

```cpp
double Aspose::Words::Border::get_LineWidth()
```

## Remarks


If you set line width greater than zero when line style is none, the line style is automatically changed to single line.

## Examples



Shows how to insert a string surrounded by a border into a document. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->get_Font()->get_Border()->set_Color(System::Drawing::Color::get_Green());
builder->get_Font()->get_Border()->set_LineWidth(2.5);
builder->get_Font()->get_Border()->set_LineStyle(LineStyle::DashDotStroker);

builder->Write(u"Text surrounded by green border.");

doc->Save(ArtifactsDir + u"Border.FontBorder.docx");
```

## See Also

* Class [Border](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
