---
title: "Aspose::Words::TextColumnCollection::SetCount método"
linktitle: "SetCount"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::TextColumnCollection::SetCount método. Organiza el texto en el número especificado de columnas de texto en C++."
type: docs
weight: 13000
url: /es/cpp/aspose.words/textcolumncollection/setcount/
---
## TextColumnCollection::SetCount method


Organiza el texto en el número especificado de columnas de texto.

```cpp
void Aspose::Words::TextColumnCollection::SetCount(int32_t newCount)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| newCount | int32_t | El número de columnas en las que se organizará el texto. |
## Observaciones


Cuando [EvenlySpaced](../get_evenlyspaced/) es **false** y aumenta el número de columnas, se crean nuevos objetos [TextColumn](../../textcolumn/) con ancho y espaciado cero. Necesita establecer el ancho y el espaciado para las nuevas columnas.

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
