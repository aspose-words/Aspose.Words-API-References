---
title: "Aspose::Words::Fields::FieldKeywords::get_Text metod"
linktitle: "get_Text"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::FieldKeywords::get_Text metod. Hämtar eller anger texten för nyckelorden i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words.fields/fieldkeywords/get_text/
---
## FieldKeywords::get_Text method


Hämtar eller anger texten för nyckelorden.

```cpp
System::String Aspose::Words::Fields::FieldKeywords::get_Text()
```


## Exempel



Visar hur man infogar ett KEYWORDS-fält.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Lägg till några nyckelord, även kallade "taggar" i File Explorer.
doc->get_BuiltInDocumentProperties()->set_Keywords(u"Keyword1, Keyword2");

// KEYWORDS-fältet visar värdet på den här egenskapen.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldKeywords>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldKeyword, true));
field->Update();

ASSERT_EQ(u" KEYWORDS ", field->GetFieldCode());
ASSERT_EQ(u"Keyword1, Keyword2", field->get_Result());

// Sätter ett värde för fältets Text-egenskap,
// och sedan kommer en uppdatering av fältet också att skriva över motsvarande inbyggda egenskap med det nya värdet.
field->set_Text(u"OverridingKeyword");
field->Update();

ASSERT_EQ(u" KEYWORDS  OverridingKeyword", field->GetFieldCode());
ASSERT_EQ(u"OverridingKeyword", field->get_Result());
ASSERT_EQ(u"OverridingKeyword", doc->get_BuiltInDocumentProperties()->get_Keywords());

doc->Save(get_ArtifactsDir() + u"Field.KEYWORDS.docx");
```

## Se även

* Class [FieldKeywords](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
