---
title: "Aspose::Words::Fields::FieldQuote::get_Text-metod"
linktitle: "get_Text"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::FieldQuote::get_Text-metod. Hämtar eller anger texten att hämta i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words.fields/fieldquote/get_text/
---
## FieldQuote::get_Text method


Hämtar eller anger texten som ska hämtas.

```cpp
System::String Aspose::Words::Fields::FieldQuote::get_Text()
```


## Exempel



Visar hur man använder QUOTE-fältet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Infoga ett QUOTE-fält, som kommer att visa värdet av dess Text-egenskap.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldQuote>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldQuote, true));
field->set_Text(u"\"Quoted text\"");

ASSERT_EQ(u" QUOTE  \"\\\"Quoted text\\\"\"", field->GetFieldCode());

// Infoga ett QUOTE-fält och nästla ett DATE-fält inuti det.
// DATE-fält uppdaterar sitt värde till aktuellt datum varje gång vi öppnar dokumentet med Microsoft Word.
// Att nästla DATE-fältet inuti QUOTE-fältet på detta sätt kommer att frysa dess värde
// till datumet då vi skapade dokumentet.
builder->Write(u"\nDocument creation date: ");
field = System::ExplicitCast<Aspose::Words::Fields::FieldQuote>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldQuote, true));
builder->MoveTo(field->get_Separator());
builder->InsertField(Aspose::Words::Fields::FieldType::FieldDate, true);

ASSERT_EQ(System::String(u" QUOTE \u0013 DATE \u0014") + System::DateTime::get_Now().get_Date().ToShortDateString() + u"\u0015", field->GetFieldCode());

// Uppdatera alla fält så att de visar sina korrekta resultat.
doc->UpdateFields();

ASSERT_EQ(u"\"Quoted text\"", doc->get_Range()->get_Fields()->idx_get(0)->get_Result());

doc->Save(get_ArtifactsDir() + u"Field.QUOTE.docx");
```

## Se även

* Class [FieldQuote](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
