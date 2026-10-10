---
title: "Aspose::Words::Fields::FieldSeq klass"
linktitle: "FieldSeq"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::FieldSeq klass. Implementerar SEQ‑fältet. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 91000
url: /sv/cpp/aspose.words.fields/fieldseq/
---
## FieldSeq class


Implementerar SEQ-fältet. För att lära dig mer, besök dokumentationsartikeln [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldSeq : public Aspose::Words::Fields::Field,
                 public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_BookmarkName](./get_bookmarkname/)() | Hämtar eller anger ett bokmärkesnamn som refererar till ett objekt någon annanstans i dokumentet snarare än på den aktuella platsen. |
| [get_DisplayResult](../field/get_displayresult/)() | Hämtar texten som representerar det visade fältresultatet. |
| [get_End](../field/get_end/)() const | Hämtar noden som representerar fältets slut. |
| [get_FieldEnd](../field/get_fieldend/)() const | Hämtar noden som representerar fältets slut. |
| [get_FieldStart](../field/get_fieldstart/)() const | Hämtar noden som representerar fältets början. |
| [get_Format](../field/get_format/)() | Hämtar ett [FieldFormat](../fieldformat/) objekt som ger typad åtkomst till fältets formatering. |
| [get_InsertNextNumber](./get_insertnextnumber/)() | Hämtar eller anger om nästa sekvensnummer ska infogas för det angivna objektet. |
| [get_IsDirty](../field/get_isdirty/)() | Hämtar eller anger om det aktuella resultatet av fältet inte längre är korrekt (föråldrat) på grund av andra ändringar som gjorts i dokumentet. |
| [get_IsLocked](../field/get_islocked/)() | Hämtar eller anger om fältet är låst (bör inte beräkna om sitt resultat). |
| [get_LocaleId](../field/get_localeid/)() | Hämtar eller anger LCID för fältet. |
| [get_ResetHeadingLevel](./get_resetheadinglevel/)() | Hämtar eller anger ett heltal som representerar en rubriknivå att återställa sekvensnumret till. Returnerar -1 om numret saknas. |
| [get_ResetNumber](./get_resetnumber/)() | Hämtar eller anger ett heltal att återställa sekvensnumret till. Returnerar -1 om numret saknas. |
| [get_Result](../field/get_result/)() | Hämtar eller anger text som ligger mellan fältavgränsaren och fältets slut. |
| [get_Separator](../field/get_separator/)() | Hämtar noden som representerar fältavgränsaren. Kan vara **null**. |
| [get_SequenceIdentifier](./get_sequenceidentifier/)() | Hämtar eller anger namnet som tilldelas serien av objekt som ska numreras. |
| [get_Start](../field/get_start/)() const | Hämtar noden som representerar fältets början. |
| virtual [get_Type](../field/get_type/)() const | Hämtar Microsoft Word-fälttypen. |
| [GetFieldCode](../field/getfieldcode/)() | Returnerar text mellan fältets början och fältavgränsaren (eller fältets slut om det inte finns någon avgränsare). Både fältkod och fältresultat för underfält inkluderas. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Returnerar text mellan fältets början och fältavgränsaren (eller fältets slut om det inte finns någon avgränsare). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Tar bort fältet från dokumentet. Returnerar en nod precis efter fältet. Om fältets slut är det sista barnet till dess föräldranod, returneras dess föräldrapparagraf. Om fältet redan har tagits bort, returneras **null**. |
| [set_BookmarkName](./set_bookmarkname/)(const System::String\&) | Sättare för [Aspose::Words::Fields::FieldSeq::get_BookmarkName](./get_bookmarkname/). |
| [set_InsertNextNumber](./set_insertnextnumber/)(bool) | Sättare för [Aspose::Words::Fields::FieldSeq::get_InsertNextNumber](./get_insertnextnumber/). |
| [set_IsDirty](../field/set_isdirty/)(bool) | Sättare för [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Sättare för [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Sättare för [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_ResetHeadingLevel](./set_resetheadinglevel/)(const System::String\&) | Sättare för [Aspose::Words::Fields::FieldSeq::get_ResetHeadingLevel](./get_resetheadinglevel/). |
| [set_ResetNumber](./set_resetnumber/)(const System::String\&) | Sättare för [Aspose::Words::Fields::FieldSeq::get_ResetNumber](./get_resetnumber/). |
| [set_Result](../field/set_result/)(const System::String\&) | Sättare för [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_SequenceIdentifier](./set_sequenceidentifier/)(const System::String\&) | Sättare för [Aspose::Words::Fields::FieldSeq::get_SequenceIdentifier](./get_sequenceidentifier/). |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Utför avlänkning av fältet. |
| [Update](../field/update/)() | Utför fältuppdateringen. Kastar ett undantag om fältet redan uppdateras. |
| [Update](../field/update/)(bool) | Utför en fältuppdatering. Kastar ett undantag om fältet redan uppdateras. |

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


Visar hur man skapar numrering med SEQ-fält.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// SEQ-fält visar ett antal som ökas vid varje SEQ-fält.
// Dessa fält upprätthåller också separata räknare för varje unikt namngivet sekvens
// identifierade av SEQ-fältets "SequenceIdentifier"-egenskap.
// Infoga ett SEQ-fält som kommer att visa det aktuella räknarvärdet för "MySequence",
// efter att ha använt egenskapen "ResetNumber" för att sätta den till 100.
builder->Write(u"#");
auto fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
fieldSeq->set_ResetNumber(u"100");
fieldSeq->Update();

ASSERT_EQ(u" SEQ  MySequence \\r 100", fieldSeq->GetFieldCode());
ASSERT_EQ(u"100", fieldSeq->get_Result());

// Visa nästa nummer i denna sekvens med ett annat SEQ-fält.
builder->Write(u", #");
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
fieldSeq->Update();

ASSERT_EQ(u"101", fieldSeq->get_Result());

// Infoga en rubrik på nivå 1.
builder->InsertBreak(Aspose::Words::BreakType::ParagraphBreak);
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Heading 1"));
builder->Writeln(u"This level 1 heading will reset MySequence to 1");
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Normal"));

// Infoga ett annat SEQ-fält från samma sekvens och konfigurera det så att räknaren återställs till 1 vid varje rubrik.
builder->Write(u"\n#");
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
fieldSeq->set_ResetHeadingLevel(u"1");
fieldSeq->Update();

// Ovanstående rubrik är en rubrik på nivå 1, så räknaren för denna sekvens återställs till 1.
ASSERT_EQ(u" SEQ  MySequence \\s 1", fieldSeq->GetFieldCode());
ASSERT_EQ(u"1", fieldSeq->get_Result());

// Gå till nästa nummer i denna sekvens.
builder->Write(u", #");
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
fieldSeq->set_InsertNextNumber(true);
fieldSeq->Update();

ASSERT_EQ(u" SEQ  MySequence \\n", fieldSeq->GetFieldCode());
ASSERT_EQ(u"2", fieldSeq->get_Result());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.SEQ.ResetNumbering.docx");
```


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

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
