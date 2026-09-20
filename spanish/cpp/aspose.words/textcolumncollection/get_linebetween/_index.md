---
title: "Aspose::Words::TextColumnCollection::get_LineBetween método"
linktitle: "get_LineBetween"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::TextColumnCollection::get_LineBetween método. Cuando es true, agrega una línea vertical entre columnas en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words/textcolumncollection/get_linebetween/
---
## TextColumnCollection::get_LineBetween method


Cuando **true**, agrega una línea vertical entre columnas.

```cpp
bool Aspose::Words::TextColumnCollection::get_LineBetween()
```


## Ejemplos



Muestra cómo separar columnas con una línea vertical.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Configure el objeto PageSetup de la sección actual para dividir el texto en varias columnas.
// Establezca la propiedad "LineBetween" en "true" para colocar una línea divisoria entre columnas.
// Establezca la propiedad "LineBetween" en "false" para dejar el espacio entre columnas en blanco.
System::SharedPtr<Aspose::Words::TextColumnCollection> columns = builder->get_PageSetup()->get_TextColumns();
columns->set_LineBetween(lineBetween);
columns->SetCount(3);

builder->Writeln(u"Column 1.");
builder->InsertBreak(Aspose::Words::BreakType::ColumnBreak);
builder->Writeln(u"Column 2.");
builder->InsertBreak(Aspose::Words::BreakType::ColumnBreak);
builder->Writeln(u"Column 3.");

doc->Save(get_ArtifactsDir() + u"PageSetup.VerticalLineBetweenColumns.docx");
```

## Ver también

* Class [TextColumnCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
