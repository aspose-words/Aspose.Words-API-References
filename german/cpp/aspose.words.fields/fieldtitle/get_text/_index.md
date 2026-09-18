---
title: "Aspose::Words::Fields::FieldTitle::get_Text-Methode"
linktitle: "get_Text"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::FieldTitle::get_Text-Methode. Gibt den Text des Titels in C++ zurück oder setzt ihn."
type: docs
weight: 2000
url: /de/cpp/aspose.words.fields/fieldtitle/get_text/
---
## FieldTitle::get_Text method


Liest oder setzt den Text des Titels.

```cpp
System::String Aspose::Words::Fields::FieldTitle::get_Text()
```


## Beispiele



Zeigt, wie das TITLE-Feld verwendet wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Setzt einen Wert für die integrierte Dokumenteigenschaft "Title".
doc->get_BuiltInDocumentProperties()->set_Title(u"My Title");

// Wir können das TITLE-Feld verwenden, um den Wert dieser Eigenschaft im Dokument anzuzeigen.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldTitle>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldTitle, false));
field->Update();

ASSERT_EQ(u" TITLE ", field->GetFieldCode());
ASSERT_EQ(u"My Title", field->get_Result());

// Setzen eines Werts für die Text-Eigenschaft des Feldes,
// und das Aktualisieren des Feldes überschreibt dann auch die entsprechende integrierte Eigenschaft mit dem neuen Wert.
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

## Siehe auch

* Class [FieldTitle](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
