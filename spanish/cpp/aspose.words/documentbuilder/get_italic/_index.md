---
title: "Método Aspose::Words::DocumentBuilder::get_Italic"
linktitle: "get_Italic"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::DocumentBuilder::get_Italic. Verdadero si la fuente está formateada en cursiva en C++."
type: docs
weight: 21000
url: /es/cpp/aspose.words/documentbuilder/get_italic/
---
## DocumentBuilder::get_Italic method


True si la fuente está formateada en cursiva.

```cpp
bool Aspose::Words::DocumentBuilder::get_Italic()
```


## Ejemplos



Muestra cómo rellenar MERGEFIELDs con datos usando un constructor de documentos en lugar de una combinación de correspondencia.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserte algunos MERGEFIELDS, que aceptan datos de columnas con el mismo nombre en una fuente de datos durante una combinación de correspondencia,
// y luego rellénelos manualmente.
builder->InsertField(u" MERGEFIELD Chairman ");
builder->InsertField(u" MERGEFIELD ChiefFinancialOfficer ");
builder->InsertField(u" MERGEFIELD ChiefTechnologyOfficer ");

builder->MoveToMergeField(u"Chairman");
builder->set_Bold(true);
builder->Writeln(u"John Doe");

builder->MoveToMergeField(u"ChiefFinancialOfficer");
builder->set_Italic(true);
builder->Writeln(u"Jane Doe");

builder->MoveToMergeField(u"ChiefTechnologyOfficer");
builder->set_Italic(true);
builder->Writeln(u"John Bloggs");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.FillMergeFields.docx");
```

## Ver también

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
