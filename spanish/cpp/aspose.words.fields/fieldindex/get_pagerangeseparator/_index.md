---
title: "Método Aspose::Words::Fields::FieldIndex::get_PageRangeSeparator"
linktitle: "get_PageRangeSeparator"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Fields::FieldIndex::get_PageRangeSeparator. Obtiene o establece la secuencia de caracteres que se usa para separar el inicio y el fin de un rango de páginas en C++."
type: docs
weight: 13000
url: /es/cpp/aspose.words.fields/fieldindex/get_pagerangeseparator/
---
## FieldIndex::get_PageRangeSeparator method


Obtiene o establece la secuencia de caracteres que se usa para separar el inicio y el fin de un rango de páginas.

```cpp
System::String Aspose::Words::Fields::FieldIndex::get_PageRangeSeparator()
```


## Ejemplos



Muestra cómo especificar las páginas abarcadas por un marcador como un rango de páginas para una entrada de campo INDEX.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Crea un campo INDEX que mostrará una entrada por cada campo XE encontrado en el documento.
// Cada entrada mostrará el valor de la propiedad Text del campo XE en el lado izquierdo,
// y el número de la página que contiene el campo XE a la derecha.
// La entrada INDEX recopilará todos los campos XE con valores coincidentes en la propiedad "Text"
// en una sola entrada en lugar de crear una entrada para cada campo XE.
auto index = System::ExplicitCast<Aspose::Words::Fields::FieldIndex>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndex, true));

// Para las entradas INDEX que muestran rangos de páginas, podemos especificar una cadena separadora
// que aparecerá entre el número de la primera página y el número de la última.
index->set_PageNumberSeparator(u", on page(s) ");
index->set_PageRangeSeparator(u" to ");

ASSERT_EQ(u" INDEX  \\e \", on page(s) \" \\g \" to \"", index->GetFieldCode());

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
auto indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"My entry");

// Si un campo XE nombra un marcador usando la propiedad PageRangeBookmarkName,
// su entrada INDEX mostrará el rango de páginas que abarca el marcador
// en lugar del número de la página que contiene el campo XE.
indexEntry->set_PageRangeBookmarkName(u"MyBookmark");

ASSERT_EQ(u" XE  \"My entry\" \\r MyBookmark", indexEntry->GetFieldCode());
ASSERT_EQ(u"MyBookmark", indexEntry->get_PageRangeBookmarkName());

// Inserte un marcador que comience en la página 3 y termine en la página 5.
// La entrada INDEX para el campo XE que hace referencia a este marcador mostrará este rango de páginas.
// En nuestra tabla, la entrada INDEX mostrará "Mi entrada, en la(s) página(s) 3 a 5".
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->StartBookmark(u"MyBookmark");
builder->Write(u"Start of MyBookmark");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Write(u"End of MyBookmark");
builder->EndBookmark(u"MyBookmark");

doc->UpdatePageLayout();
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.INDEX.XE.PageRangeBookmark.docx");
```

## Ver también

* Class [FieldIndex](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
