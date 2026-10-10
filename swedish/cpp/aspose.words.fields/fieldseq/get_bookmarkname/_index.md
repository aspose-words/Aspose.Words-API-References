---
title: "Aspose::Words::Fields::FieldSeq::get_BookmarkName metod"
linktitle: "get_BookmarkName"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::FieldSeq::get_BookmarkName metod. Hämtar eller anger ett bokmärkesnamn som refererar till ett objekt någon annanstans i dokumentet snarare än på den aktuella platsen i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words.fields/fieldseq/get_bookmarkname/
---
## FieldSeq::get_BookmarkName method


Hämtar eller anger ett bokmärkesnamn som refererar till ett objekt någon annanstans i dokumentet snarare än på den aktuella platsen.

```cpp
System::String Aspose::Words::Fields::FieldSeq::get_BookmarkName()
```


## Exempel



Visar hur man kombinerar innehållsförteckning och sekvensfält.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Ett TOC-fält kan skapa en post i dess innehållsförteckning för varje SEQ-fält som hittas i dokumentet.
// Varje post innehåller stycket som innehåller SEQ-fältet,
// och sidnumret där fältet visas.
auto fieldToc = System::ExplicitCast<Aspose::Words::Fields::FieldToc>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldTOC, true));

// Konfigurera detta TOC-fält så att det har egenskapen SequenceIdentifier med värdet "MySequence".
fieldToc->set_TableOfFiguresLabel(u"MySequence");

// Konfigurera detta TOC-fält så att det bara plockar upp SEQ-fält som ligger inom gränserna för ett bokmärke
// med namnet "TOCBookmark".
fieldToc->set_BookmarkName(u"TOCBookmark");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

ASSERT_EQ(u" TOC  \\c MySequence \\b TOCBookmark", fieldToc->GetFieldCode());

// SEQ-fält visar ett antal som ökas vid varje SEQ-fält.
// Dessa fält upprätthåller också separata räknare för varje unikt namngivet sekvens
// identifierade av SEQ-fältets "SequenceIdentifier"-egenskap.
// Infoga ett SEQ-fält som har en sekvensidentifierare som matchar TOC:ns
// TableOfFiguresLabel-egenskap. Detta fält kommer inte att skapa en post i TOC eftersom det är utanför
// bokmärkets gränser som anges av "BookmarkName".
builder->Write(u"MySequence #");
auto fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
builder->Writeln(u", will not show up in the TOC because it is outside of the bookmark.");

builder->StartBookmark(u"TOCBookmark");

// Detta SEQ-fälts sekvens matchar TOC:ns "TableOfFiguresLabel"-egenskap och ligger inom bokmärkets gränser.
// Stycket som innehåller detta fält kommer att visas i TOC som en post.
builder->Write(u"MySequence #");
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
builder->Writeln(u", will show up in the TOC next to the entry for the above caption.");

// Detta SEQ-fälts sekvens matchar inte TOC:ns "TableOfFiguresLabel"-egenskap,
// och ligger inom bokmärkets gränser. Dess stycke kommer inte att visas i TOC som en post.
builder->Write(u"MySequence #");
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"OtherSequence");
builder->Writeln(u", will not show up in the TOC because it's from a different sequence identifier.");

// Denna SEQ-fälts sekvens matchar TOC:s "TableOfFiguresLabel"-egenskap och ligger inom bokmärkets gränser.
// Detta fält refererar också till ett annat bokmärke. Innehållet i det bokmärket kommer att visas i TOC-posten för detta SEQ-fält.
// SEQ-fältet självt kommer inte att visa innehållet i det bokmärket.
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
fieldSeq->set_BookmarkName(u"SEQBookmark");
ASSERT_EQ(u" SEQ  MySequence SEQBookmark", fieldSeq->GetFieldCode());

// Skapa ett bokmärke med innehåll som kommer att visas i TOC-posten på grund av att ovanstående SEQ-fält refererar till det.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->StartBookmark(u"SEQBookmark");
builder->Write(u"MySequence #");
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
builder->Writeln(u", text from inside SEQBookmark.");
builder->EndBookmark(u"SEQBookmark");

builder->EndBookmark(u"TOCBookmark");

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.SEQ.Bookmark.docx");
```

## Se även

* Class [FieldSeq](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
