---
title: "Aspose::Words::Fields::FieldSubject::get_Text-metod"
linktitle: "get_Text"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::FieldSubject::get_Text-metod. Hämtar eller anger texten för ämnet i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words.fields/fieldsubject/get_text/
---
## FieldSubject::get_Text method


Hämtar eller anger texten för ämnet.

```cpp
System::String Aspose::Words::Fields::FieldSubject::get_Text()
```


## Exempel



Visar hur man använder SUBJECT-fältet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Ange ett värde för dokumentets inbyggda egenskap "Subject".
doc->get_BuiltInDocumentProperties()->set_Subject(u"My subject");

// Skapa ett SUBJECT-fält för att visa värdet av den inbyggda egenskapen.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldSubject>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSubject, true));
field->Update();

ASSERT_EQ(u" SUBJECT ", field->GetFieldCode());
ASSERT_EQ(u"My subject", field->get_Result());

// Om vi ger SUBJECT-fältets Text-egenskap ett värde och uppdaterar det, kommer fältet att
// skriva över det aktuella värdet för den inbyggda egenskapen "Subject" med värdet från dess Text-egenskap,
// och sedan visa det nya värdet.
field->set_Text(u"My new subject");
field->Update();

ASSERT_EQ(u" SUBJECT  \"My new subject\"", field->GetFieldCode());
ASSERT_EQ(u"My new subject", field->get_Result());

ASSERT_EQ(u"My new subject", doc->get_BuiltInDocumentProperties()->get_Subject());

doc->Save(get_ArtifactsDir() + u"Field.SUBJECT.docx");
```

## Se även

* Class [FieldSubject](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
