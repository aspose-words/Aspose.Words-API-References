---
title: "Aspose::Words::Fields::FieldRef::get_BookmarkName metod"
linktitle: "get_BookmarkName"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::FieldRef::get_BookmarkName metod. Hämtar eller anger namnet på det refererade bokmärket i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words.fields/fieldref/get_bookmarkname/
---
## FieldRef::get_BookmarkName method


Hämtar eller anger namnet på den refererade bokmärket.

```cpp
System::String Aspose::Words::Fields::FieldRef::get_BookmarkName()
```


## Exempel



Visar hur man skapar bokmärkt text med ett SET-fält, och sedan visar den i dokumentet med ett REF-fält.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Namnge bokmärkt text med ett SET-fält.
// Detta fält refererar till "bookmark" och inte en bokmärkesstruktur som visas i texten, utan en namngiven variabel.
auto fieldSet = System::ExplicitCast<Aspose::Words::Fields::FieldSet>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSet, false));
fieldSet->set_BookmarkName(u"MyBookmark");
fieldSet->set_BookmarkText(u"Hello world!");
fieldSet->Update();

ASSERT_EQ(u" SET  MyBookmark \"Hello world!\"", fieldSet->GetFieldCode());

// Referera till bokmärket med namn i ett REF-fält och visa dess innehåll.
auto fieldRef = System::ExplicitCast<Aspose::Words::Fields::FieldRef>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldRef, true));
fieldRef->set_BookmarkName(u"MyBookmark");
fieldRef->Update();

ASSERT_EQ(u" REF  MyBookmark", fieldRef->GetFieldCode());
ASSERT_EQ(u"Hello world!", fieldRef->get_Result());

doc->Save(get_ArtifactsDir() + u"Field.SET.REF.docx");
```

## Se även

* Class [FieldRef](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
