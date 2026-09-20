---
title: "Aspose::Words::LineSpacingRule enum"
linktitle: "LineSpacingRule"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::LineSpacingRule enum. Especifica los valores de interlineado para un párrafo en C++."
type: docs
weight: 95000
url: /es/cpp/aspose.words/linespacingrule/
---
## LineSpacingRule enum


Especifica los valores de interlineado para un párrafo.

```cpp
enum class LineSpacingRule
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| AtLeast | 0 | El interlineado puede ser mayor o igual, pero nunca menor, que el valor especificado en la propiedad [LineSpacing](../paragraphformat/get_linespacing/). |
| Exactly | 1 | El interlineado nunca cambia del valor especificado en la propiedad [LineSpacing](../paragraphformat/get_linespacing/), incluso si se usa una fuente más grande dentro del párrafo. |
| Multiple | 2 | El interlineado se especifica en la propiedad [LineSpacing](../paragraphformat/get_linespacing/) como el número de líneas. Una línea equivale a 12 puntos. |


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
