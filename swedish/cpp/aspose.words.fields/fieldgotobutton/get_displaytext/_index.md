---
title: "Aspose::Words::Fields::FieldGoToButton::get_DisplayText metod"
linktitle: "get_DisplayText"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::FieldGoToButton::get_DisplayText metod. Hämtar eller anger texten för \"knappen\" som visas i dokumentet, så att den kan väljas för att aktivera hoppet i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words.fields/fieldgotobutton/get_displaytext/
---
## FieldGoToButton::get_DisplayText method


Hämtar eller anger texten för \"knappen\" som visas i dokumentet, så att den kan väljas för att aktivera hoppet.

```cpp
System::String Aspose::Words::Fields::FieldGoToButton::get_DisplayText()
```


## Exempel



Visar hur man infogar ett GOTOBUTTON-fält.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Lägg till ett GOTOBUTTON-fält. När vi dubbelklickar på detta fält i Microsoft Word,
// kommer den att flytta textmarkören till bokmärket vars namn Location-egenskapen refererar till.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldGoToButton>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldGoToButton, true));
field->set_DisplayText(u"My Button");
field->set_Location(u"MyBookmark");

ASSERT_EQ(u" GOTOBUTTON  MyBookmark My Button", field->GetFieldCode());

// Infoga ett giltigt bokmärke som fältet kan referera till.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->StartBookmark(field->get_Location());
builder->Writeln(u"Bookmark text contents.");
builder->EndBookmark(field->get_Location());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.GOTOBUTTON.docx");
```

## Se även

* Class [FieldGoToButton](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
