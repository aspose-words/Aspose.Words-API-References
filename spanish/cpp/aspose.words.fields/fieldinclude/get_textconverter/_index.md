---
title: "Aspose::Words::Fields::FieldInclude::get_TextConverter método"
linktitle: "get_TextConverter"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fields::FieldInclude::get_TextConverter método. Obtiene o establece el nombre del convertidor de texto para el formato del archivo incluido en C++."
type: docs
weight: 5000
url: /es/cpp/aspose.words.fields/fieldinclude/get_textconverter/
---
## FieldInclude::get_TextConverter method


Obtiene o establece el nombre del convertidor de texto para el formato del archivo incluido.

```cpp
System::String Aspose::Words::Fields::FieldInclude::get_TextConverter() override
```


## Ejemplos



Muestra cómo crear un campo INCLUDE y establecer sus propiedades.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Podemos usar un campo INCLUDE para importar una parte de otro documento en el sistema de archivos local.
// El marcador del otro documento que referenciamos con este campo contiene esta porción importada.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldInclude>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldInclude, true));
field->set_SourceFullName(get_MyDir() + u"Bookmarks.docx");
field->set_BookmarkName(u"MyBookmark1");
field->set_LockFields(false);
field->set_TextConverter(u"Microsoft Word");

ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(field->GetFieldCode(), u" INCLUDE .* MyBookmark1 \\\\c \"Microsoft Word\"")->get_Success());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.INCLUDE.docx");
```

## Ver también

* Class [FieldInclude](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
