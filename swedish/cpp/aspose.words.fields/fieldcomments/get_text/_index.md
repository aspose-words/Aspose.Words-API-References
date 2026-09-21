---
title: "Aspose::Words::Fields::FieldComments::get_Text-metod"
linktitle: "get_Text"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::FieldComments::get_Text-metod. Hämtar eller anger texten för kommentarerna i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words.fields/fieldcomments/get_text/
---
## FieldComments::get_Text method


Hämtar eller anger texten för kommentarerna.

```cpp
System::String Aspose::Words::Fields::FieldComments::get_Text()
```


## Exempel



Visar hur man använder COMMENTS-fältet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Ange ett värde för dokumentets inbyggda egenskap "Comments".
doc->get_BuiltInDocumentProperties()->set_Comments(u"My comment.");

// Skapa ett COMMENTS-fält för att visa värdet av den inbyggda egenskapen.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldComments>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldComments, true));
field->Update();

ASSERT_EQ(u" COMMENTS ", field->GetFieldCode());
ASSERT_EQ(u"My comment.", field->get_Result());

// Om vi ger COMMENTS-fältets Text-egenskap värde och uppdaterar det, kommer fältet att
// skriva över det aktuella värdet för den inbyggda egenskapen "Comments" med värdet för dess Text-egenskap,
// och sedan visa det nya värdet.
field->set_Text(u"My overriding comment.");
field->Update();

ASSERT_EQ(u" COMMENTS  \"My overriding comment.\"", field->GetFieldCode());
ASSERT_EQ(u"My overriding comment.", field->get_Result());

doc->Save(get_ArtifactsDir() + u"Field.COMMENTS.docx");
```

## Se även

* Class [FieldComments](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
