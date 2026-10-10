---
title: "Método Aspose::Words::Border::get_LineStyle"
linktitle: "get_LineStyle"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Border::get_LineStyle. Obtiene o establece el estilo del borde en C++."
type: docs
weight: 7000
url: /es/cpp/aspose.words/border/get_linestyle/
---
## Border::get_LineStyle method


Obtiene o establece el estilo del borde.

```cpp
Aspose::Words::LineStyle Aspose::Words::Border::get_LineStyle()
```

## Observaciones


Si establece el estilo de línea en ninguno, entonces el ancho de línea se cambia automáticamente a cero.

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

* Enum [LineStyle](../../linestyle/)
* Class [Border](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
