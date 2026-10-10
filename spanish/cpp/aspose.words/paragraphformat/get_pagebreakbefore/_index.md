---
title: "Aspose::Words::ParagraphFormat::get_PageBreakBefore método"
linktitle: "get_PageBreakBefore"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::ParagraphFormat::get_PageBreakBefore método. True si se fuerza un salto de página antes del párrafo en C++."
type: docs
weight: 27000
url: /es/cpp/aspose.words/paragraphformat/get_pagebreakbefore/
---
## ParagraphFormat::get_PageBreakBefore method


Verdadero si se fuerza un salto de página antes del párrafo.

```cpp
bool Aspose::Words::ParagraphFormat::get_PageBreakBefore()
```


## Ejemplos



Muestra cómo crear párrafos con saltos de página al inicio.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Establece esta bandera a "true" para aplicar un salto de página al inicio de cada párrafo
// que el generador de documentos creará bajo esta configuración de ParagraphFormat.
// El primer párrafo no recibirá un salto de página.
// Deja esta bandera como "false" para iniciar cada nuevo párrafo en la misma página
// como el anterior, siempre que haya suficiente espacio.
builder->get_ParagraphFormat()->set_PageBreakBefore(pageBreakBefore);

builder->Writeln(u"Paragraph 1.");
builder->Writeln(u"Paragraph 2.");

auto layoutCollector = System::MakeObject<Aspose::Words::Layout::LayoutCollector>(doc);
System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();

if (pageBreakBefore)
{
    ASSERT_EQ(1, layoutCollector->GetStartPageIndex(paragraphs->idx_get(0)));
    ASSERT_EQ(2, layoutCollector->GetStartPageIndex(paragraphs->idx_get(1)));
}
else
{
    ASSERT_EQ(1, layoutCollector->GetStartPageIndex(paragraphs->idx_get(0)));
    ASSERT_EQ(1, layoutCollector->GetStartPageIndex(paragraphs->idx_get(1)));
}

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.PageBreakBefore.docx");
```

## Ver también

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
