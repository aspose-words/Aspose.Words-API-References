---
title: "Aspose::Words::Fields::FieldQuote::get_Text Methode"
linktitle: "get_Text"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::FieldQuote::get_Text Methode. Gibt den Text zurück oder legt ihn fest, der in C++ abgerufen wird."
type: docs
weight: 2000
url: /de/cpp/aspose.words.fields/fieldquote/get_text/
---
## FieldQuote::get_Text method


Ermittelt oder legt den abzurufenden Text fest.

```cpp
System::String Aspose::Words::Fields::FieldQuote::get_Text()
```


## Beispiele



Zeigt die Verwendung des QUOTE-Feldes.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Fügt ein QUOTE-Feld ein, das den Wert seiner Text-Eigenschaft anzeigt.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldQuote>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldQuote, true));
field->set_Text(u"\"Quoted text\"");

ASSERT_EQ(u" QUOTE  \"\\\"Quoted text\\\"\"", field->GetFieldCode());

// Fügt ein QUOTE-Feld ein und verschachtelt darin ein DATE-Feld.
// DATE-Felder aktualisieren ihren Wert auf das aktuelle Datum jedes Mal, wenn wir das Dokument mit Microsoft Word öffnen.
// Das Verschachteln des DATE-Feldes innerhalb des QUOTE-Feldes auf diese Weise friert seinen Wert ein.
// auf das Datum, an dem wir das Dokument erstellt haben.
builder->Write(u"\nDocument creation date: ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldQuote>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldQuote, true));
builder->MoveTo(field->get_Separator());
builder->InsertField(Aspose::Words::Fields::FieldType::FieldDate, true);

ASSERT_EQ(System::String(u" QUOTE \u0013 DATE \u0014") + System::DateTime::get_Now().get_Date().ToShortDateString() + u"\u0015", field->GetFieldCode());

// Aktualisieren Sie alle Felder, um ihre korrekten Ergebnisse anzuzeigen.
doc->UpdateFields();

ASSERT_EQ(u"\"Quoted text\"", doc->get_Range()->get_Fields()->idx_get(0)->get_Result());

doc->Save(get_ArtifactsDir() + u"Field.QUOTE.docx");
```

## Siehe auch

* Class [FieldQuote](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
