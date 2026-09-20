---
title: "Aspose::Words::LineStyle enum"
linktitle: "LineStyle"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::LineStyle enum. Especifica el estilo de línea de un Border en C++."
type: docs
weight: 96000
url: /es/cpp/aspose.words/linestyle/
---
## LineStyle enum


Especifica el estilo de línea de un [Border](../border/).

```cpp
enum class LineStyle
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| None | 0 |  |
| Single | 1 |  |
| Thick | 2 |  |
| Double | 3 |  |
| Hairline | 5 |  |
| Dot | 6 |  |
| DashLargeGap | 7 |  |
| DotDash | 8 |  |
| DotDotDash | 9 |  |
| Triple | 10 |  |
| ThinThickSmallGap | 11 |  |
| ThickThinSmallGap | 12 |  |
| ThinThickThinSmallGap | 13 |  |
| ThinThickMediumGap | 14 |  |
| ThickThinMediumGap | 15 |  |
| ThinThickThinMediumGap | 16 |  |
| ThinThickLargeGap | 17 |  |
| ThickThinLargeGap | 18 |  |
| ThinThickThinLargeGap | 19 |  |
| Wave | 20 |  |
| DoubleWave | 21 |  |
| DashSmallGap | 22 |  |
| DashDotStroker | 23 |  |
| Emboss3D | 24 |  |
| Engrave3D | 25 |  |
| Outset | 26 |  |
| Inset | 27 |  |


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
