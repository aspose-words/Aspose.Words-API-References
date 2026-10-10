---
title: "Método Aspose::Words::Paragraph::get_BreakIsStyleSeparator"
linktitle: "get_BreakIsStyleSeparator"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Paragraph::get_BreakIsStyleSeparator. True si este salto de párrafo es un Separador de Estilo. Un separador de estilo permite que un párrafo conste de partes que tienen diferentes estilos de párrafo en C++."
type: docs
weight: 5000
url: /es/cpp/aspose.words/paragraph/get_breakisstyleseparator/
---
## Paragraph::get_BreakIsStyleSeparator method


True si este salto de párrafo es un Separador de [Style](../../style/). Un separador de estilo permite que un párrafo conste de partes que tienen diferentes estilos de párrafo.

```cpp
bool Aspose::Words::Paragraph::get_BreakIsStyleSeparator()
```


## Ejemplos



Muestra cómo escribir texto en la misma línea que un encabezado del TOC y que no aparezca en el TOC.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertTableOfContents(u"\\o \\h \\z \\u");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// Inserta un párrafo con un estilo que el TOC reconocerá como una entrada.
builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading1);

// Ambas cadenas están en el mismo párrafo y, por lo tanto, aparecerán en la misma entrada del TOC.
builder->Write(u"Heading 1. ");
builder->Write(u"Will appear in the TOC. ");

// Si insertamos un separador de estilo, podemos escribir más texto en el mismo párrafo
// y usar un estilo diferente sin que aparezca en el TOC.
// Si usamos un estilo de tipo encabezado después del separador, podemos generar múltiples entradas del TOC a partir de una sola línea de texto del documento.
builder->InsertStyleSeparator();
builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Quote);
builder->Write(u"Won't appear in the TOC. ");

ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_BreakIsStyleSeparator());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Paragraph.BreakIsStyleSeparator.docx");
```

## Ver también

* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
