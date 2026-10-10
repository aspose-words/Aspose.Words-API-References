---
title: "Método Aspose::Words::ParagraphFormat::get_LineSpacing"
linktitle: "get_LineSpacing"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::ParagraphFormat::get_LineSpacing. Obtiene o establece el interlineado (en puntos) para el párrafo en C++."
type: docs
weight: 20000
url: /es/cpp/aspose.words/paragraphformat/get_linespacing/
---
## ParagraphFormat::get_LineSpacing method


Obtiene o establece el interlineado (en puntos) para el párrafo.

```cpp
double Aspose::Words::ParagraphFormat::get_LineSpacing()
```

## Observaciones


Cuando la propiedad [LineSpacingRule](../get_linespacingrule/) se establece en [AtLeast](../../linespacingrule/), el interlineado puede ser mayor o igual, pero nunca menor que el valor especificado de [LineSpacing](./).

Cuando la propiedad [LineSpacingRule](../get_linespacingrule/) se establece en [Exactly](../../linespacingrule/), el interlineado nunca cambia del valor especificado de [LineSpacing](./), incluso si se usa una fuente más grande dentro del párrafo.

## Ejemplos



Muestra cómo trabajar con el interlineado.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// A continuación se presentan tres reglas de interlineado que podemos definir usando el
// propiedad "LineSpacingRule" del párrafo para configurar el espaciado entre párrafos.
// 1 -  Establecer una cantidad mínima de espaciado.
// Esto proporcionará un relleno vertical a líneas de texto de cualquier tamaño
// que son demasiado pequeñas para mantener la altura mínima de línea.
builder->get_ParagraphFormat()->set_LineSpacingRule(Aspose::Words::LineSpacingRule::AtLeast);
builder->get_ParagraphFormat()->set_LineSpacing(20);

builder->Writeln(u"Minimum line spacing of 20.");
builder->Writeln(u"Minimum line spacing of 20.");

// 2 -  Establecer espaciado exacto.
// Usar tamaños de fuente demasiado grandes para el espaciado truncará el texto.
builder->get_ParagraphFormat()->set_LineSpacingRule(Aspose::Words::LineSpacingRule::Exactly);
builder->get_ParagraphFormat()->set_LineSpacing(5);

builder->Writeln(u"Line spacing of exactly 5.");
builder->Writeln(u"Line spacing of exactly 5.");

// 3 -  Establecer el espaciado como múltiplo del espaciado de línea predeterminado, que es 12 puntos por defecto.
// Este tipo de espaciado se escalará a diferentes tamaños de fuente.
builder->get_ParagraphFormat()->set_LineSpacingRule(Aspose::Words::LineSpacingRule::Multiple);
builder->get_ParagraphFormat()->set_LineSpacing(18);

builder->Writeln(u"Line spacing of 1.5 default lines.");
builder->Writeln(u"Line spacing of 1.5 default lines.");

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.LineSpacing.docx");
```

## Ver también

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
