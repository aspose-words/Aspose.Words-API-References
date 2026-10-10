---
title: "Método Aspose::Words::Fields::FieldSet::get_BookmarkText"
linktitle: "get_BookmarkText"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Fields::FieldSet::get_BookmarkText. Obtiene o establece el nuevo texto del marcador en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words.fields/fieldset/get_bookmarktext/
---
## FieldSet::get_BookmarkText method


Obtiene o establece el nuevo texto del marcador.

```cpp
System::String Aspose::Words::Fields::FieldSet::get_BookmarkText()
```


## Ejemplos



Muestra cómo crear texto marcado con un campo SET y luego mostrarlo en el documento usando un campo REF.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Nombra el texto marcado con un campo SET.
// Este campo se refiere al "bookmark" no a una estructura de marcador que aparece dentro del texto, sino a una variable con nombre.
auto fieldSet = System::ExplicitCast<Aspose::Words::Fields::FieldSet>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSet, false));
fieldSet->set_BookmarkName(u"MyBookmark");
fieldSet->set_BookmarkText(u"Hello world!");
fieldSet->Update();

ASSERT_EQ(u" SET  MyBookmark \"Hello world!\"", fieldSet->GetFieldCode());

// Refiérase al marcador por su nombre en un campo REF y muestre su contenido.
auto fieldRef = System::ExplicitCast<Aspose::Words::Fields::FieldRef>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldRef, true));
fieldRef->set_BookmarkName(u"MyBookmark");
fieldRef->Update();

ASSERT_EQ(u" REF  MyBookmark", fieldRef->GetFieldCode());
ASSERT_EQ(u"Hello world!", fieldRef->get_Result());

doc->Save(get_ArtifactsDir() + u"Field.SET.REF.docx");
```

## Ver también

* Class [FieldSet](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
