---
title: "Aspose::Words::ParagraphFormat::get_NoSpaceBetweenParagraphsOfSameStyle método"
linktitle: "get_NoSpaceBetweenParagraphsOfSameStyle"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::ParagraphFormat::get_NoSpaceBetweenParagraphsOfSameStyle método. Cuando **true**, SpaceBefore y SpaceAfter se ignorarán entre los párrafos del mismo estilo en C++."
type: docs
weight: 25000
url: /es/cpp/aspose.words/paragraphformat/get_nospacebetweenparagraphsofsamestyle/
---
## ParagraphFormat::get_NoSpaceBetweenParagraphsOfSameStyle method


Cuando **true**, [SpaceBefore](../get_spacebefore/) y [SpaceAfter](../get_spaceafter/) se ignorarán entre los párrafos del mismo estilo.

```cpp
bool Aspose::Words::ParagraphFormat::get_NoSpaceBetweenParagraphsOfSameStyle()
```

## Observaciones


Esta configuración solo tiene efecto cuando se aplica a un estilo de párrafo. Si se aplica directamente a un párrafo, no tiene ningún efecto.

## Ejemplos



Muestra cómo aplicar sin espaciado entre párrafos con el mismo estilo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Aplica una gran cantidad de espaciado antes y después de los párrafos que este generador creará.
builder->get_ParagraphFormat()->set_SpaceBefore(24);
builder->get_ParagraphFormat()->set_SpaceAfter(24);

// Establece la bandera "NoSpaceBetweenParagraphsOfSameStyle" a "true" para aplicar
// sin espaciado entre párrafos con el mismo estilo, lo que agrupará párrafos similares.
// Deja la bandera "NoSpaceBetweenParagraphsOfSameStyle" como "false"
// para aplicar uniformemente espaciado a cada párrafo.
builder->get_ParagraphFormat()->set_NoSpaceBetweenParagraphsOfSameStyle(noSpaceBetweenParagraphsOfSameStyle);

builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Normal"));
builder->Writeln(System::String::Format(u"Paragraph in the \"{0}\" style.", builder->get_ParagraphFormat()->get_Style()->get_Name()));
builder->Writeln(System::String::Format(u"Paragraph in the \"{0}\" style.", builder->get_ParagraphFormat()->get_Style()->get_Name()));
builder->Writeln(System::String::Format(u"Paragraph in the \"{0}\" style.", builder->get_ParagraphFormat()->get_Style()->get_Name()));
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Quote"));
builder->Writeln(System::String::Format(u"Paragraph in the \"{0}\" style.", builder->get_ParagraphFormat()->get_Style()->get_Name()));
builder->Writeln(System::String::Format(u"Paragraph in the \"{0}\" style.", builder->get_ParagraphFormat()->get_Style()->get_Name()));
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Normal"));
builder->Writeln(System::String::Format(u"Paragraph in the \"{0}\" style.", builder->get_ParagraphFormat()->get_Style()->get_Name()));
builder->Writeln(System::String::Format(u"Paragraph in the \"{0}\" style.", builder->get_ParagraphFormat()->get_Style()->get_Name()));

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.ParagraphSpacingSameStyle.docx");
```

## Ver también

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
