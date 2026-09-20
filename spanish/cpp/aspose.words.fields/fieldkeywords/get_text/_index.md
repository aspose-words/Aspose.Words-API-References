---
title: "Aspose::Words::Fields::FieldKeywords::get_Text método"
linktitle: "get_Text"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fields::FieldKeywords::get_Text método. Obtiene o establece el texto de las palabras clave en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words.fields/fieldkeywords/get_text/
---
## FieldKeywords::get_Text method


Obtiene o establece el texto de las palabras clave.

```cpp
System::String Aspose::Words::Fields::FieldKeywords::get_Text()
```


## Ejemplos



Muestra cómo insertar un campo KEYWORDS.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Agregue algunas palabras clave, también llamadas "etiquetas" en el Explorador de archivos.
doc->get_BuiltInDocumentProperties()->set_Keywords(u"Keyword1, Keyword2");

// El campo KEYWORDS muestra el valor de esta propiedad.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldKeywords>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldKeyword, true));
field->Update();

ASSERT_EQ(u" KEYWORDS ", field->GetFieldCode());
ASSERT_EQ(u"Keyword1, Keyword2", field->get_Result());

// Estableciendo un valor para la propiedad Text del campo,
// y luego actualizar el campo también sobrescribirá la propiedad incorporada correspondiente con el nuevo valor.
field->set_Text(u"OverridingKeyword");
field->Update();

ASSERT_EQ(u" KEYWORDS  OverridingKeyword", field->GetFieldCode());
ASSERT_EQ(u"OverridingKeyword", field->get_Result());
ASSERT_EQ(u"OverridingKeyword", doc->get_BuiltInDocumentProperties()->get_Keywords());

doc->Save(get_ArtifactsDir() + u"Field.KEYWORDS.docx");
```

## Ver también

* Class [FieldKeywords](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
