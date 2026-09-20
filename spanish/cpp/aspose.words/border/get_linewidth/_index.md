---
title: "Método Aspose::Words::Border::get_LineWidth"
linktitle: "get_LineWidth"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Border::get_LineWidth. Obtiene o establece el ancho del borde en puntos en C++."
type: docs
weight: 8000
url: /es/cpp/aspose.words/border/get_linewidth/
---
## Border::get_LineWidth method


Obtiene o establece el ancho del borde en puntos.

```cpp
double Aspose::Words::Border::get_LineWidth()
```

## Observaciones


Si estableces el ancho de línea mayor que cero cuando el estilo de línea es ninguno, el estilo de línea se cambia automáticamente a línea simple.

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

* Class [Border](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
