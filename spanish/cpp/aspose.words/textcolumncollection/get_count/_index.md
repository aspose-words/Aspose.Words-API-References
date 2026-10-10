---
title: "Aspose::Words::TextColumnCollection::get_Count método"
linktitle: "get_Count"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::TextColumnCollection::get_Count método. Obtiene el número de columnas en la sección de un documento en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words/textcolumncollection/get_count/
---
## TextColumnCollection::get_Count method


Obtiene el número de columnas en la sección de un documento.

```cpp
int32_t Aspose::Words::TextColumnCollection::get_Count()
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

* Class [TextColumnCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
