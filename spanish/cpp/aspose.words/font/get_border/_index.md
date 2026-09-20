---
title: "Método Aspose::Words::Font::get_Border"
linktitle: "get_Border"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Font::get_Border. Devuelve un objeto Border que especifica el borde para la fuente en C++."
type: docs
weight: 8000
url: /es/cpp/aspose.words/font/get_border/
---
## Font::get_Border method


Devuelve un objeto [Border](../../border/) que especifica el borde para la fuente.

```cpp
System::SharedPtr<Aspose::Words::Border> Aspose::Words::Font::get_Border()
```


## Ejemplos



Muestra cómo insertar una cadena rodeada por un borde en un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->get_Border()->set_Color(System::Drawing::Color::get_Green());
builder->get_Font()->get_Border()->set_LineWidth(2.5);
builder->get_Font()->get_Border()->set_LineStyle(Aspose::Words::LineStyle::DashDotStroker);

builder->Write(u"Text surrounded by green border.");

doc->Save(get_ArtifactsDir() + u"Border.FontBorder.docx");
```

## Ver también

* Class [Border](../../border/)
* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
