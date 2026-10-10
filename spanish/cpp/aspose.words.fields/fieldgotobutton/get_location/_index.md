---
title: "Método get_Location de Aspose::Words::Fields::FieldGoToButton"
linktitle: "get_Location"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método get_Location de Aspose::Words::Fields::FieldGoToButton. Obtiene o establece el nombre de un marcador, un número de página u otro elemento al que saltar en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words.fields/fieldgotobutton/get_location/
---
## FieldGoToButton::get_Location method


Obtiene o establece el nombre de un marcador, un número de página o algún otro elemento al que saltar.

```cpp
System::String Aspose::Words::Fields::FieldGoToButton::get_Location()
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
