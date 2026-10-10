---
title: "Aspose::Words::ParagraphFormat::get_SpaceBefore método"
linktitle: "get_SpaceBefore"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::ParagraphFormat::get_SpaceBefore método. Obtiene o establece la cantidad de espacio (en puntos) antes del párrafo en C++."
type: docs
weight: 33000
url: /es/cpp/aspose.words/paragraphformat/get_spacebefore/
---
## ParagraphFormat::get_SpaceBefore method


Obtiene o establece la cantidad de espacio (en puntos) antes del párrafo.

```cpp
double Aspose::Words::ParagraphFormat::get_SpaceBefore()
```

## Observaciones


No tiene efecto cuando [SpaceBeforeAuto](../get_spacebeforeauto/) es **true**.

Los valores válidos van de 0 a 1584 inclusive.

## Ejemplos



Muestra cómo establecer el espaciado automático de párrafos.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Aplica una gran cantidad de espaciado antes y después de los párrafos que este generador creará.
builder->get_ParagraphFormat()->set_SpaceBefore(24);
builder->get_ParagraphFormat()->set_SpaceAfter(24);

// Establezca estos indicadores a "true" para aplicar el espaciado automático,
// ignorando efectivamente el espaciado en las propiedades que establecimos arriba.
// Dejarlos como "false" aplicará nuestro espaciado personalizado de párrafos.
builder->get_ParagraphFormat()->set_SpaceAfterAuto(autoSpacing);
builder->get_ParagraphFormat()->set_SpaceBeforeAuto(autoSpacing);

// Inserte dos párrafos que tendrán espaciado arriba y abajo y guarde el documento.
builder->Writeln(u"Paragraph 1.");
builder->Writeln(u"Paragraph 2.");

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.ParagraphSpacingAuto.docx");
```


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
