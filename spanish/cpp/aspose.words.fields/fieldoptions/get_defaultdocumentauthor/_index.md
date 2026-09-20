---
title: "Aspose::Words::Fields::FieldOptions::get_DefaultDocumentAuthor método"
linktitle: "get_DefaultDocumentAuthor"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fields::FieldOptions::get_DefaultDocumentAuthor método. Obtiene o establece el nombre del autor'' del documento. Si el nombre del autor'' ya está especificado en las propiedades integradas del documento, esta opción no se tiene en cuenta en C++."
type: docs
weight: 7000
url: /es/cpp/aspose.words.fields/fieldoptions/get_defaultdocumentauthor/
---
## FieldOptions::get_DefaultDocumentAuthor method


Obtiene o establece el nombre del autor predeterminado del documento. Si el nombre del autor ya está especificado en las propiedades integradas del documento, esta opción no se considera.

```cpp
System::String Aspose::Words::Fields::FieldOptions::get_DefaultDocumentAuthor() const
```


## Ejemplos



Muestra cómo usar un campo AUTHOR para mostrar el nombre del creador del documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Los campos AUTHOR obtienen sus resultados de la propiedad incorporada del documento llamada \"Author\".
// Si creamos y guardamos un documento en Microsoft Word,
// tendrá nuestro nombre de usuario en esa propiedad.
// Sin embargo, si creamos un documento programáticamente usando Aspose.Words,
// la propiedad \"Author\", por defecto, será una cadena vacía.
ASSERT_EQ(System::String::Empty, doc->get_BuiltInDocumentProperties()->get_Author());

// Establezca un nombre de autor de respaldo para que los campos AUTHOR lo usen
// si la propiedad \"Author\" contiene una cadena vacía.
doc->get_FieldOptions()->set_DefaultDocumentAuthor(u"Joe Bloggs");

builder->Write(u"This document was created by ");
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldAuthor>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAuthor, true));
field->Update();

ASSERT_EQ(u" AUTHOR ", field->GetFieldCode());
ASSERT_EQ(u"Joe Bloggs", field->get_Result());

// Actualizar un campo AUTHOR que contiene un valor
// aplicará ese valor a la propiedad incorporada \"Author\".
ASSERT_EQ(u"Joe Bloggs", doc->get_BuiltInDocumentProperties()->get_Author());

// Cambiar esta propiedad, y luego actualizar el campo AUTHOR aplicará este valor al campo.
doc->get_BuiltInDocumentProperties()->set_Author(u"John Doe");
field->Update();

ASSERT_EQ(u" AUTHOR ", field->GetFieldCode());
ASSERT_EQ(u"John Doe", field->get_Result());

// Si actualizamos un campo AUTHOR después de cambiar su propiedad \"Name\",
// entonces el campo mostrará el nuevo nombre y aplicará el nuevo nombre a la propiedad incorporada.
field->set_AuthorName(u"Jane Doe");
field->Update();

ASSERT_EQ(u" AUTHOR  \"Jane Doe\"", field->GetFieldCode());
ASSERT_EQ(u"Jane Doe", field->get_Result());

// Los campos AUTHOR no afectan la propiedad DefaultDocumentAuthor.
ASSERT_EQ(u"Jane Doe", doc->get_BuiltInDocumentProperties()->get_Author());
ASSERT_EQ(u"Joe Bloggs", doc->get_FieldOptions()->get_DefaultDocumentAuthor());

doc->Save(get_ArtifactsDir() + u"Field.AUTHOR.docx");
```

## Ver también

* Class [FieldOptions](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
