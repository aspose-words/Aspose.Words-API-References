---
title: Aspose::Words::Font::get_Border method
linktitle: get_Border
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Font::get_Border method. Returns a Border object that specifies border for the font in C++.'
type: docs
weight: 8000
url: /cpp/aspose.words/font/get_border/
---
## Font::get_Border method


Returns a [Border](../../border/) object that specifies border for the font.

```cpp
System::SharedPtr<Aspose::Words::Border> Aspose::Words::Font::get_Border()
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

* Class [Border](../../border/)
* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
