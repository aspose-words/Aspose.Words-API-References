---
title: "Aspose::Words::Fields::FieldComments::get_Text método"
linktitle: "get_Text"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fields::FieldComments::get_Text método. Obtiene o establece el texto de los comentarios en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words.fields/fieldcomments/get_text/
---
## FieldComments::get_Text method


Obtiene o establece el texto de los comentarios.

```cpp
System::String Aspose::Words::Fields::FieldComments::get_Text()
```


## Ejemplos



Muestra cómo usar el campo COMMENTS.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Establece un valor para la propiedad incorporada "Comments" del documento.
doc->get_BuiltInDocumentProperties()->set_Comments(u"My comment.");

// Crea un campo COMMENTS para mostrar el valor de esa propiedad incorporada.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldComments>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldComments, true));
field->Update();

ASSERT_EQ(u" COMMENTS ", field->GetFieldCode());
ASSERT_EQ(u"My comment.", field->get_Result());

// Si asignamos un valor a la propiedad Text del campo COMMENTS y lo actualizamos, el campo
// sobrescribirá el valor actual de la propiedad incorporada "Comments" con el valor de su propiedad Text,
// y luego mostrará el nuevo valor.
field->set_Text(u"My overriding comment.");
field->Update();

ASSERT_EQ(u" COMMENTS  \"My overriding comment.\"", field->GetFieldCode());
ASSERT_EQ(u"My overriding comment.", field->get_Result());

doc->Save(get_ArtifactsDir() + u"Field.COMMENTS.docx");
```

## Ver también

* Class [FieldComments](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
