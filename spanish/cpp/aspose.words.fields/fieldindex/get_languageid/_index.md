---
title: "Aspose::Words::Fields::FieldIndex::get_LanguageId método"
linktitle: "get_LanguageId"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fields::FieldIndex::get_LanguageId método. Obtiene o establece el ID de idioma utilizado para generar el índice en C++."
type: docs
weight: 8000
url: /es/cpp/aspose.words.fields/fieldindex/get_languageid/
---
## FieldIndex::get_LanguageId method


Obtiene o establece el ID de idioma utilizado para generar el índice.

```cpp
System::String Aspose::Words::Fields::FieldIndex::get_LanguageId()
```


## Ejemplos



Muestra cómo poblar un campo INDEX con entradas usando campos XE y también modificar su apariencia.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Crea un campo INDEX que mostrará una entrada por cada campo XE encontrado en el documento.
// Cada entrada mostrará el valor de la propiedad Text del campo XE en el lado izquierdo,
// y el número de la página que contiene el campo XE a la derecha.
// Si los campos XE tienen el mismo valor en su propiedad "Text",
// el campo INDEX los agrupará en una sola entrada.
auto index = System::ExplicitCast<Aspose::Words::Fields::FieldIndex>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndex, true));
index->set_LanguageId(u"1033");

// Establecer el valor de esta propiedad a "A" agrupará todas las entradas por su primera letra,
// y colocará esa letra en mayúsculas sobre cada grupo.
index->set_Heading(u"A");

// Configure la tabla creada por el campo INDEX para que abarque 2 columnas.
index->set_NumberOfColumns(u"2");

// Configure cualquier entrada con letras iniciales fuera del rango de caracteres "a-c" para que se omita.
index->set_LetterRange(u"a-c");

ASSERT_EQ(u" INDEX  \\z 1033 \\h A \\c 2 \\p a-c", index->GetFieldCode());

// Los siguientes dos campos XE aparecerán bajo el encabezado "A",
// con sus respectivos estilos de texto también aplicados a sus números de página.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
auto indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Apple");
indexEntry->set_IsItalic(true);

ASSERT_EQ(u" XE  Apple \\i", indexEntry->GetFieldCode());

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Apricot");
indexEntry->set_IsBold(true);

ASSERT_EQ(u" XE  Apricot \\b", indexEntry->GetFieldCode());

// Los dos siguientes campos XE estarán bajo los encabezados "B" y "C" en el índice de contenidos de los campos INDEX.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Banana");

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Cherry");

// Los campos INDEX ordenan todas las entradas alfabéticamente, por lo que esta entrada aparecerá bajo "A" con las otras dos.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Avocado");

// Esta entrada no aparecerá porque comienza con la letra "D",
// que está fuera del rango de caracteres "a-c" que define la propiedad LetterRange del campo INDEX.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Durian");

doc->UpdatePageLayout();
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.INDEX.XE.Formatting.docx");
```

## Ver también

* Class [FieldIndex](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
