---
title: "Método Aspose::Words::Fields::FieldGoToButton::get_DisplayText"
linktitle: "get_DisplayText"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Fields::FieldGoToButton::get_DisplayText. Obtiene o establece el texto del \"botón\" que aparece en el documento, de modo que pueda ser seleccionado para activar el salto en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words.fields/fieldgotobutton/get_displaytext/
---
## FieldGoToButton::get_DisplayText method


Obtiene o establece el texto del "botón" que aparece en el documento, de modo que pueda seleccionarse para activar el salto.

```cpp
System::String Aspose::Words::Fields::FieldGoToButton::get_DisplayText()
```


## Ejemplos



Muestra cómo insertar un campo GOTOBUTTON.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Agregue un campo GOTOBUTTON. Cuando hacemos doble clic en este campo en Microsoft Word,
// llevará el cursor de texto al marcador cuyo nombre referencia la propiedad Location.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldGoToButton>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldGoToButton, true));
field->set_DisplayText(u"My Button");
field->set_Location(u"MyBookmark");

ASSERT_EQ(u" GOTOBUTTON  MyBookmark My Button", field->GetFieldCode());

// Inserte un marcador válido para que el campo lo referencie.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->StartBookmark(field->get_Location());
builder->Writeln(u"Bookmark text contents.");
builder->EndBookmark(field->get_Location());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.GOTOBUTTON.docx");
```

## Ver también

* Class [FieldGoToButton](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
