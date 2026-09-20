---
title: "Aspose::Words::Fields::FieldIndex::get_EntryType método"
linktitle: "get_EntryType"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fields::FieldIndex::get_EntryType método. Obtiene o establece un tipo de entrada de índice utilizado para crear el índice en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words.fields/fieldindex/get_entrytype/
---
## FieldIndex::get_EntryType method


Obtiene o establece un tipo de entrada de índice utilizado para crear el índice.

```cpp
System::String Aspose::Words::Fields::FieldIndex::get_EntryType()
```


## Ejemplos



Muestra cómo crear un campo INDEX y luego usar campos XE para poblarlo con entradas.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Crea un campo INDEX que mostrará una entrada por cada campo XE encontrado en el documento.
// Cada entrada mostrará el valor de la propiedad Text del campo XE en el lado izquierdo
// y la página que contiene el campo XE a la derecha.
// Si los campos XE tienen el mismo valor en su propiedad "Text",
// el campo INDEX los agrupará en una sola entrada.
auto index = System::ExplicitCast<Aspose::Words::Fields::FieldIndex>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndex, true));

// Configura el campo INDEX para que solo muestre los campos XE que estén dentro de los límites
// de un marcador llamado "MainBookmark", y cuyas propiedades "EntryType" tengan un valor de "A".
// Para los campos INDEX y XE, la propiedad "EntryType" solo utiliza el primer carácter de su valor de cadena.
index->set_BookmarkName(u"MainBookmark");
index->set_EntryType(u"A");

ASSERT_EQ(u" INDEX  \\b MainBookmark \\f A", index->GetFieldCode());

// En una página nueva, inicia el marcador con un nombre que coincida con el valor
// de la propiedad "BookmarkName" del campo INDEX.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->StartBookmark(u"MainBookmark");

// El campo INDEX capturará esta entrada porque está dentro del marcador,
// y su tipo de entrada también coincide con el tipo de entrada del campo INDEX.
auto indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Index entry 1");
indexEntry->set_EntryType(u"A");

ASSERT_EQ(u" XE  \"Index entry 1\" \\f A", indexEntry->GetFieldCode());

// Inserta un campo XE que no aparecerá en el INDEX porque los tipos de entrada no coinciden.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Index entry 2");
indexEntry->set_EntryType(u"B");

// Finaliza el marcador e inserta un campo XE después.
// Es del mismo tipo que el campo INDEX, pero no aparecerá
// ya que está fuera de los límites del marcador.
builder->EndBookmark(u"MainBookmark");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Index entry 3");
indexEntry->set_EntryType(u"A");

doc->UpdatePageLayout();
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.INDEX.XE.Filtering.docx");
```

## Ver también

* Class [FieldIndex](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
