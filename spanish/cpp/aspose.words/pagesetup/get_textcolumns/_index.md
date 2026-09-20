---
title: "Aspose::Words::PageSetup::get_TextColumns método"
linktitle: "get_TextColumns"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::PageSetup::get_TextColumns método. Devuelve una colección que representa el conjunto de columnas de texto en C++."
type: docs
weight: 44000
url: /es/cpp/aspose.words/pagesetup/get_textcolumns/
---
## PageSetup::get_TextColumns method


Devuelve una colección que representa el conjunto de columnas de texto.

```cpp
System::SharedPtr<Aspose::Words::TextColumnCollection> Aspose::Words::PageSetup::get_TextColumns()
```


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

* Class [TextColumnCollection](../../textcolumncollection/)
* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
