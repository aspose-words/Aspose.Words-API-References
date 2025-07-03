---
title: Aspose::Words::Border::get_Color method
linktitle: get_Color
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Border::get_Color method. Gets or sets the border color in C++.'
type: docs
weight: 4000
url: /cpp/aspose.words/border/get_color/
---
## Border::get_Color method


Gets or sets the border color.

```cpp
System::Drawing::Color Aspose::Words::Border::get_Color()
```


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

* Class [Border](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
