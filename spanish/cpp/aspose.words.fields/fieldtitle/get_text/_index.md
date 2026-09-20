---
title: "Aspose::Words::Fields::FieldTitle::get_Text método"
linktitle: "get_Text"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Fields::FieldTitle::get_Text. Obtiene o establece el texto del título en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words.fields/fieldtitle/get_text/
---
## FieldTitle::get_Text method


Obtiene o establece el texto del título.

```cpp
System::String Aspose::Words::Fields::FieldTitle::get_Text()
```


## Ejemplos



Muestra cómo usar el campo TITLE.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Establece un valor para la propiedad incorporada del documento "Title".
doc->get_BuiltInDocumentProperties()->set_Title(u"My Title");

// Podemos usar el campo TITLE para mostrar el valor de esta propiedad en el documento.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldTitle>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldTitle, false));
field->Update();

ASSERT_EQ(u" TITLE ", field->GetFieldCode());
ASSERT_EQ(u"My Title", field->get_Result());

// Estableciendo un valor para la propiedad Text del campo,
// y luego actualizar el campo también sobrescribirá la propiedad incorporada correspondiente con el nuevo valor.
builder->Writeln();
field = System::ExplicitCast<Aspose::Words::Fields::FieldTitle>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldTitle, false));
field->set_Text(u"My New Title");
field->Update();

ASSERT_EQ(u" TITLE  \"My New Title\"", field->GetFieldCode());
ASSERT_EQ(u"My New Title", field->get_Result());
ASSERT_EQ(u"My New Title", doc->get_BuiltInDocumentProperties()->get_Title());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.TITLE.docx");
```

## Ver también

* Class [FieldTitle](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
