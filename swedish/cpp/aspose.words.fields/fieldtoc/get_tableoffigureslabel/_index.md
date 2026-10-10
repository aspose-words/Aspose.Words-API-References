---
title: "Aspose::Words::Fields::FieldToc::get_TableOfFiguresLabel metod"
linktitle: "get_TableOfFiguresLabel"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::FieldToc::get_TableOfFiguresLabel metod. Hämtar eller anger namnet på sekvensidentifieraren som används när en figurförteckning byggs i C++."
type: docs
weight: 19000
url: /sv/cpp/aspose.words.fields/fieldtoc/get_tableoffigureslabel/
---
## FieldToc::get_TableOfFiguresLabel method


Hämtar eller anger namnet på sekvensidentifieraren som används när en figurlista byggs.

```cpp
System::String Aspose::Words::Fields::FieldToc::get_TableOfFiguresLabel()
```


## Exempel



Visar hur man fyller ett TOC‑fält med poster med hjälp av SEQ‑fält.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Ett TOC-fält kan skapa en post i dess innehållsförteckning för varje SEQ-fält som hittas i dokumentet.
// Varje post innehåller det stycke som inkluderar SEQ-fältet och sidnumret där fältet visas.
auto fieldToc = System::ExplicitCast<Aspose::Words::Fields::FieldToc>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldTOC, true));

// SEQ-fält visar ett antal som ökas vid varje SEQ-fält.
// Dessa fält upprätthåller också separata räknare för varje unikt namngivet sekvens
// identifierade av SEQ-fältets "SequenceIdentifier"-egenskap.
// Använd egenskapen "TableOfFiguresLabel" för att namnge en huvudsekvens för TOC.
// Nu kommer detta TOC endast att skapa poster från SEQ-fält med deras "SequenceIdentifier" satt till "MySequence".
fieldToc->set_TableOfFiguresLabel(u"MySequence");

// Vi kan namnge en annan SEQ-fältsekvens i egenskapen "PrefixedSequenceIdentifier".
// SEQ-fält från detta prefixsekvens kommer inte att skapa TOC-poster.
// Varje TOC-post som skapas från ett huvudsekvens SEQ-fält kommer nu också att visa räknaren som
// prefixsekvensen för närvarande har vid det primära sekvens SEQ-fältet som skapade posten.
fieldToc->set_PrefixedSequenceIdentifier(u"PrefixSequence");

// Varje TOC-post kommer att visa prefixsekvensens räknare omedelbart till vänster
// på sidnumret där huvudsekvensens SEQ-fält visas.
// Vi kan ange en anpassad avgränsare som kommer att visas mellan dessa två siffror.
fieldToc->set_SequenceSeparator(u">");

ASSERT_EQ(u" TOC  \\c MySequence \\s PrefixSequence \\d >", fieldToc->GetFieldCode());

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// Det finns två sätt att använda SEQ-fält för att fylla i detta TOC.
// 1 -  Infoga ett SEQ-fält som tillhör TOC:s prefixsekvens:
// Detta fält kommer att öka SEQ-sekvensens räknare för "PrefixSequence" med 1.
// Eftersom detta fält inte tillhör huvudsekvensen som identifieras
// av TOC:s "TableOfFiguresLabel"-egenskap, kommer det inte att visas som en post.
auto fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"PrefixSequence");
builder->InsertParagraph();

ASSERT_EQ(u" SEQ  PrefixSequence", fieldSeq->GetFieldCode());

// 2 -  Infoga ett SEQ-fält som tillhör TOC:s huvudsekvens:
// Detta SEQ-fält kommer att skapa en post i TOC.
// TOC-posten kommer att innehålla det stycke som SEQ-fältet är i och sidnumret där det visas.
// Denna post kommer också att visa räknaren som prefixsekvensen för närvarande har,
// separerad från sidnumret av värdet i TOC:s "SeqenceSeparator"-egenskap.
// Räknaren för "PrefixSequence" är 1, detta huvudsekvens SEQ-fält är på sida 2,
// och separatorn är ">", så posten kommer att visas som "1>2".
builder->Write(u"First TOC entry, MySequence #");
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");

ASSERT_EQ(u" SEQ  MySequence", fieldSeq->GetFieldCode());

// Infoga en sida, öka prefixsekvensen med 2 och infoga ett SEQ-fält för att skapa ett innehållsförteckningspost efteråt.
// Prefixsekvensen är nu på 2, och huvudsekvensens SEQ-fält är på sida 3,
// så innehållsförteckningsposten kommer att visa "2>3" i sidantalet.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"PrefixSequence");
builder->InsertParagraph();
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
builder->Write(u"Second TOC entry, MySequence #");
fieldSeq->set_SequenceIdentifier(u"MySequence");

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.TOC.SEQ.docx");
```

## Se även

* Class [FieldToc](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
