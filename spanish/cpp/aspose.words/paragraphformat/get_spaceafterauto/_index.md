---
title: "Aspose::Words::ParagraphFormat::get_SpaceAfterAuto método"
linktitle: "get_SpaceAfterAuto"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::ParagraphFormat::get_SpaceAfterAuto método. Verdadero si la cantidad de espacio después del párrafo se establece automáticamente en C++."
type: docs
weight: 32000
url: /es/cpp/aspose.words/paragraphformat/get_spaceafterauto/
---
## ParagraphFormat::get_SpaceAfterAuto method


True si la cantidad de espacio después del párrafo se establece automáticamente.

```cpp
bool Aspose::Words::ParagraphFormat::get_SpaceAfterAuto()
```

## Observaciones


Cuando se establece en **true**, sobrescribe el efecto de [SpaceAfter](../get_spaceafter/).

Cuando configuras el Espacio Antes y el Espacio Después del párrafo en Auto, **Microsoft** Word agrega automáticamente un espaciado de 14 puntos entre párrafos según las siguientes reglas:

* Normally, spacing is added after all paragraphs.
* In a bulleted or numbered list, spacing is added only after the last item in the list. Spacing is not added between the list items.
* In a nested bulleted or numbered list spacing is not added.
* Spacing is normally added after a table.
* Spacing is not added after a table if it is the last block in a table cell.
* Spacing is not added after the last paragraph in a table cell.



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

## Ver también

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
