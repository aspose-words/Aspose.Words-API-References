---
title: "Aspose::Words::Fields::FieldSubject::get_Text método"
linktitle: "get_Text"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fields::FieldSubject::get_Text método. Obtiene o establece el texto del sujeto en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words.fields/fieldsubject/get_text/
---
## FieldSubject::get_Text method


Obtiene o establece el texto del asunto.

```cpp
System::String Aspose::Words::Fields::FieldSubject::get_Text()
```


## Ejemplos



Muestra cómo usar el campo SUBJECT.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Establece un valor para la propiedad incorporada "Subject" del documento.
doc->get_BuiltInDocumentProperties()->set_Subject(u"My subject");

// Crea un campo SUBJECT para mostrar el valor de esa propiedad incorporada.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldSubject>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSubject, true));
field->Update();

ASSERT_EQ(u" SUBJECT ", field->GetFieldCode());
ASSERT_EQ(u"My subject", field->get_Result());

// Si damos el valor de la propiedad Text del campo SUBJECT y lo actualizamos, el campo
// sobrescribe el valor actual de la propiedad incorporada "Subject" con el valor de su propiedad Text,
// y luego mostrará el nuevo valor.
field->set_Text(u"My new subject");
field->Update();

ASSERT_EQ(u" SUBJECT  \"My new subject\"", field->GetFieldCode());
ASSERT_EQ(u"My new subject", field->get_Result());

ASSERT_EQ(u"My new subject", doc->get_BuiltInDocumentProperties()->get_Subject());

doc->Save(get_ArtifactsDir() + u"Field.SUBJECT.docx");
```

## Ver también

* Class [FieldSubject](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
