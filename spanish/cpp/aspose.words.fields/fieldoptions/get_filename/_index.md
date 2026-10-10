---
title: "Aspose::Words::Fields::FieldOptions::get_FileName método"
linktitle: "get_FileName"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Fields::FieldOptions::get_FileName. Obtiene o establece el nombre de archivo del documento en C++."
type: docs
weight: 14000
url: /es/cpp/aspose.words.fields/fieldoptions/get_filename/
---
## FieldOptions::get_FileName method


Obtiene o establece el nombre de archivo del documento.

```cpp
System::String Aspose::Words::Fields::FieldOptions::get_FileName() const
```

## Observaciones


Esta propiedad es utilizada por el campo [FieldFileName](../../fieldfilename/) con mayor prioridad que la propiedad [OriginalFileName](../../../aspose.words/document/get_originalfilename/).

## Ejemplos



Muestra cómo usar [FieldOptions](../) para sobrescribir el valor predeterminado del campo FILENAME.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->MoveToDocumentEnd();
builder->Writeln();

// Este campo FILENAME mostrará el nombre del archivo del sistema local del documento que cargamos.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldFileName>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldFileName, true));
field->Update();

ASSERT_EQ(u" FILENAME ", field->GetFieldCode());
ASSERT_EQ(u"Document.docx", field->get_Result());

builder->Writeln();

// Por defecto, el campo FILENAME muestra el nombre del archivo, pero no su ruta completa en el sistema de archivos local.
// Podemos establecer una bandera para que muestre la ruta completa del archivo.
field = System::ExplicitCast<Aspose::Words::Fields::FieldFileName>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldFileName, true));
field->set_IncludeFullPath(true);
field->Update();

ASSERT_EQ(get_MyDir() + u"Document.docx", field->get_Result());

// También podemos establecer un valor para esta propiedad a
// sobrescribir el valor que muestra el campo FILENAME.
doc->get_FieldOptions()->set_FileName(u"FieldOptions.FILENAME.docx");
field->Update();

ASSERT_EQ(u" FILENAME  \\p", field->GetFieldCode());
ASSERT_EQ(u"FieldOptions.FILENAME.docx", field->get_Result());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + doc->get_FieldOptions()->get_FileName());
```

## Ver también

* Class [FieldOptions](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
