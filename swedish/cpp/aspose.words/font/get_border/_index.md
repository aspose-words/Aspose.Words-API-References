---
title: "Aspose::Words::Font::get_Border metod"
linktitle: "get_Border"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Font::get_Border metod. Returnerar ett Border-objekt som specificerar kant för teckensnittet i C++."
type: docs
weight: 8000
url: /sv/cpp/aspose.words/font/get_border/
---
## Font::get_Border method


Returnerar ett [Border](../../border/) objekt som specificerar kant för teckensnittet.

```cpp
System::SharedPtr<Aspose::Words::Border> Aspose::Words::Font::get_Border()
```


## Exempel



Visar hur man infogar en sträng omgiven av en kant i ett dokument.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->get_Border()->set_Color(System::Drawing::Color::get_Green());
builder->get_Font()->get_Border()->set_LineWidth(2.5);
builder->get_Font()->get_Border()->set_LineStyle(Aspose::Words::LineStyle::DashDotStroker);

builder->Write(u"Text surrounded by green border.");

doc->Save(get_ArtifactsDir() + u"Border.FontBorder.docx");
```

## Se även

* Class [Border](../../border/)
* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
