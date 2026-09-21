---
title: "Aspose::Words::Fields::FieldAuthor::get_AuthorName metod"
linktitle: "get_AuthorName"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::FieldAuthor::get_AuthorName metod. Hämtar eller anger dokumentets författares namn i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words.fields/fieldauthor/get_authorname/
---
## FieldAuthor::get_AuthorName method


Hämtar eller anger dokumentets författarnamn.

```cpp
System::String Aspose::Words::Fields::FieldAuthor::get_AuthorName()
```


## Exempel



Visar hur man använder ett AUTHOR-fält för att visa dokumentets skaparnamn.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// AUTHOR-fält hämtar sina resultat från den inbyggda dokumentegenskapen som heter "Author".
// Om vi skapar och sparar ett dokument i Microsoft Word,
// kommer det att ha vårt användarnamn i den egenskapen.
// Men om vi skapar ett dokument programatiskt med Aspose.Words,
// kommer "Author"-egenskapen som standard att vara en tom sträng.
ASSERT_EQ(System::String::Empty, doc->get_BuiltInDocumentProperties()->get_Author());

// Ange ett reservförfattarnamn för AUTHOR-fält att använda
// om "Author"-egenskapen innehåller en tom sträng.
doc->get_FieldOptions()->set_DefaultDocumentAuthor(u"Joe Bloggs");

builder->Write(u"This document was created by ");
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldAuthor>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAuthor, true));
field->Update();

ASSERT_EQ(u" AUTHOR ", field->GetFieldCode());
ASSERT_EQ(u"Joe Bloggs", field->get_Result());

// Uppdaterar ett AUTHOR-fält som innehåller ett värde
// kommer att tillämpa det värdet på den inbyggda egenskapen "Author".
ASSERT_EQ(u"Joe Bloggs", doc->get_BuiltInDocumentProperties()->get_Author());

// Att ändra den här egenskapen, och sedan uppdatera AUTHOR-fältet, kommer att tillämpa detta värde på fältet.
doc->get_BuiltInDocumentProperties()->set_Author(u"John Doe");
field->Update();

ASSERT_EQ(u" AUTHOR ", field->GetFieldCode());
ASSERT_EQ(u"John Doe", field->get_Result());

// Om vi uppdaterar ett AUTHOR-fält efter att ha ändrat dess "Name"-egenskap,
// kommer fältet att visa det nya namnet och tillämpa det nya namnet på den inbyggda egenskapen.
field->set_AuthorName(u"Jane Doe");
field->Update();

ASSERT_EQ(u" AUTHOR  \"Jane Doe\"", field->GetFieldCode());
ASSERT_EQ(u"Jane Doe", field->get_Result());

// AUTHOR-fält påverkar inte egenskapen DefaultDocumentAuthor.
ASSERT_EQ(u"Jane Doe", doc->get_BuiltInDocumentProperties()->get_Author());
ASSERT_EQ(u"Joe Bloggs", doc->get_FieldOptions()->get_DefaultDocumentAuthor());

doc->Save(get_ArtifactsDir() + u"Field.AUTHOR.docx");
```

## Se även

* Class [FieldAuthor](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
