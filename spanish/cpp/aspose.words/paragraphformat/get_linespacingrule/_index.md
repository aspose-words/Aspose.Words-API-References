---
title: "Aspose::Words::ParagraphFormat::get_LineSpacingRule método"
linktitle: "get_LineSpacingRule"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::ParagraphFormat::get_LineSpacingRule método. Obtiene o establece el interlineado del párrafo en C++."
type: docs
weight: 21000
url: /es/cpp/aspose.words/paragraphformat/get_linespacingrule/
---
## ParagraphFormat::get_LineSpacingRule method


Obtiene o establece el interlineado para el párrafo.

```cpp
Aspose::Words::LineSpacingRule Aspose::Words::ParagraphFormat::get_LineSpacingRule()
```


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

* Enum [LineSpacingRule](../../linespacingrule/)
* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
