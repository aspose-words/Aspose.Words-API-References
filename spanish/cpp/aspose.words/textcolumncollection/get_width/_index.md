---
title: "Aspose::Words::TextColumnCollection::get_Width método"
linktitle: "get_Width"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::TextColumnCollection::get_Width método. Cuando las columnas están espaciadas uniformemente, obtiene el ancho de las columnas en C++."
type: docs
weight: 6000
url: /es/cpp/aspose.words/textcolumncollection/get_width/
---
## TextColumnCollection::get_Width method


Cuando las columnas están espaciadas uniformemente, obtiene el ancho de las columnas.

```cpp
double Aspose::Words::TextColumnCollection::get_Width()
```

## Observaciones


Tiene efecto solo cuando [EvenlySpaced](../get_evenlyspaced/) está establecido en **true**.

## Ejemplos



Muestra cómo crear múltiples columnas espaciadas uniformemente en una sección.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::TextColumnCollection> columns = builder->get_PageSetup()->get_TextColumns();
columns->set_Spacing(100);
columns->SetCount(2);

builder->Writeln(u"Column 1.");
builder->InsertBreak(Aspose::Words::BreakType::ColumnBreak);
builder->Writeln(u"Column 2.");

doc->Save(get_ArtifactsDir() + u"PageSetup.ColumnsSameWidth.docx");
```

## Ver también

* Class [TextColumnCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
