---
title: "Aspose::Words::Fields::FieldGoToButton::get_Location-Methode"
linktitle: "get_Location"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::FieldGoToButton::get_Location-Methode. Gibt den Namen eines Lesezeichens, einer Seitenzahl oder eines anderen Elements zurück oder legt ihn fest, zu dem in C++ gesprungen werden soll."
type: docs
weight: 3000
url: /de/cpp/aspose.words.fields/fieldgotobutton/get_location/
---
## FieldGoToButton::get_Location method


Liest oder setzt den Namen eines Lesezeichens, einer Seitenzahl oder eines anderen Elements, zu dem gesprungen werden soll.

```cpp
System::String Aspose::Words::Fields::FieldGoToButton::get_Location()
```


## Beispiele



Zeigt, wie man ein GOTOBUTTON-Feld einfügt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Fügen Sie ein GOTOBUTTON-Feld hinzu. Wenn wir dieses Feld in Microsoft Word doppelklicken,
// wird der Textcursor zum Lesezeichen springen, dessen Name von der Location-Eigenschaft referenziert wird.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldGoToButton>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldGoToButton, true));
field->set_DisplayText(u"My Button");
field->set_Location(u"MyBookmark");

ASSERT_EQ(u" GOTOBUTTON  MyBookmark My Button", field->GetFieldCode());

// Fügen Sie ein gültiges Lesezeichen ein, auf das das Feld verweisen kann.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->StartBookmark(field->get_Location());
builder->Writeln(u"Bookmark text contents.");
builder->EndBookmark(field->get_Location());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.GOTOBUTTON.docx");
```

## Siehe auch

* Class [FieldGoToButton](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
