---
title: "Aspose::Words::Fields::FieldFileSize::get_IsInMegabytes metod"
linktitle: "get_IsInMegabytes"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::FieldFileSize::get_IsInMegabytes metod. Hämtar eller anger om filstorleken ska visas i megabyte i C++."
type: docs
weight: 3000
url: /sv/cpp/aspose.words.fields/fieldfilesize/get_isinmegabytes/
---
## FieldFileSize::get_IsInMegabytes method


Hämtar eller anger om filstorleken ska visas i megabyte.

```cpp
bool Aspose::Words::Fields::FieldFileSize::get_IsInMegabytes()
```


## Exempel



Visar hur man visar filstorleken för ett dokument med ett FILESIZE-fält.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

ASSERT_EQ(18105, doc->get_BuiltInDocumentProperties()->get_Bytes());

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->MoveToDocumentEnd();
builder->InsertParagraph();

// Nedan är tre olika måttenheter
// som FILESIZE-fält kan använda för att visa dokumentets filstorlek.
// 1 -  Byte:
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldFileSize>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldFileSize, true));
field->Update();

ASSERT_EQ(u" FILESIZE ", field->GetFieldCode());
ASSERT_EQ(u"18105", field->get_Result());

// 2 -  Kilobyte:
builder->InsertParagraph();
field = System::ExplicitCast<Aspose::Words::Fields::FieldFileSize>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldFileSize, true));
field->set_IsInKilobytes(true);
field->Update();

ASSERT_EQ(u" FILESIZE  \\k", field->GetFieldCode());
ASSERT_EQ(u"18", field->get_Result());

// 3 -  Megabyte:
builder->InsertParagraph();
field = System::ExplicitCast<Aspose::Words::Fields::FieldFileSize>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldFileSize, true));
field->set_IsInMegabytes(true);
field->Update();

ASSERT_EQ(u" FILESIZE  \\m", field->GetFieldCode());
ASSERT_EQ(u"0", field->get_Result());

// För att uppdatera värdena i dessa fält medan du redigerar i Microsoft Word,
// måste vi först spara ändringarna och sedan manuellt uppdatera dessa fält.
doc->Save(get_ArtifactsDir() + u"Field.FILESIZE.docx");
```

## Se även

* Class [FieldFileSize](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
