---
title: "Aspose::Words::Fields::FieldFileSize::get_IsInMegabytes método"
linktitle: "get_IsInMegabytes"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fields::FieldFileSize::get_IsInMegabytes método. Obtiene o establece si se muestra el tamaño del archivo en megabytes en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words.fields/fieldfilesize/get_isinmegabytes/
---
## FieldFileSize::get_IsInMegabytes method


Obtiene o establece si se debe mostrar el tamaño del archivo en megabytes.

```cpp
bool Aspose::Words::Fields::FieldFileSize::get_IsInMegabytes()
```


## Ejemplos



Muestra cómo mostrar el tamaño del archivo de un documento con un campo FILESIZE.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

ASSERT_EQ(18105, doc->get_BuiltInDocumentProperties()->get_Bytes());

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->MoveToDocumentEnd();
builder->InsertParagraph();

// A continuación se presentan tres unidades de medida diferentes
// con las que los campos FILESIZE pueden mostrar el tamaño del archivo del documento.
// 1 -  Bytes:
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldFileSize>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldFileSize, true));
field->Update();

ASSERT_EQ(u" FILESIZE ", field->GetFieldCode());
ASSERT_EQ(u"18105", field->get_Result());

// 2 -  Kilobytes:
builder->InsertParagraph();
field = System::ExplicitCast<Aspose::Words::Fields::FieldFileSize>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldFileSize, true));
field->set_IsInKilobytes(true);
field->Update();

ASSERT_EQ(u" FILESIZE  \\k", field->GetFieldCode());
ASSERT_EQ(u"18", field->get_Result());

// 3 -  Megabytes:
builder->InsertParagraph();
field = System::ExplicitCast<Aspose::Words::Fields::FieldFileSize>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldFileSize, true));
field->set_IsInMegabytes(true);
field->Update();

ASSERT_EQ(u" FILESIZE  \\m", field->GetFieldCode());
ASSERT_EQ(u"0", field->get_Result());

// Para actualizar los valores de estos campos mientras se edita en Microsoft Word,
// debemos primero guardar los cambios y luego actualizar manualmente estos campos.
doc->Save(get_ArtifactsDir() + u"Field.FILESIZE.docx");
```

## Ver también

* Class [FieldFileSize](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
