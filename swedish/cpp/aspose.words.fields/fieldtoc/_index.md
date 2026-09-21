---
title: "Aspose::Words::Fields::FieldToc-klass"
linktitle: "FieldToc"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::FieldToc-klass. Implementerar TOC‑fältet. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 105000
url: /sv/cpp/aspose.words.fields/fieldtoc/
---
## FieldToc class


Implementerar TOC-fältet. För att lära dig mer, besök [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) dokumentationsartikel.

```cpp
class FieldToc : public Aspose::Words::Fields::Field,
                 public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [FieldToc](./fieldtoc/)() |  |
| [get_BookmarkName](./get_bookmarkname/)() | Hämtar namnet på bokmärket som markerar den del av dokumentet som används för att bygga tabellen. |
| [get_CaptionlessTableOfFiguresLabel](./get_captionlesstableoffigureslabel/)() | Hämtar eller anger namnet på sekvensidentifieraren som används när en figurlista byggs som inte inkluderar bildtextens etikett och nummer. |
| [get_CustomStyles](./get_customstyles/)() | Hämtar en lista med stilar förutom de inbyggda rubrikstilarna som ska inkluderas i innehållsförteckningen. |
| [get_DisplayResult](../field/get_displayresult/)() | Hämtar texten som representerar det visade fältresultatet. |
| [get_End](../field/get_end/)() const | Hämtar noden som representerar fältets slut. |
| [get_EntryIdentifier](./get_entryidentifier/)() | Hämtar en sträng som ska matcha typidentifierare för TC‑fält som inkluderas. |
| [get_EntryLevelRange](./get_entrylevelrange/)() | Hämtar ett intervall av nivåer för innehållsförteckningens poster som ska inkluderas. |
| [get_EntrySeparator](./get_entryseparator/)() | Hämtar en sekvens av tecken som separerar en post och dess sidnummer. |
| [get_FieldEnd](../field/get_fieldend/)() const | Hämtar noden som representerar fältets slut. |
| [get_FieldStart](../field/get_fieldstart/)() const | Hämtar noden som representerar fältets början. |
| [get_Format](../field/get_format/)() | Hämtar ett [FieldFormat](../fieldformat/) objekt som ger typad åtkomst till fältets formatering. |
| [get_HeadingLevelRange](./get_headinglevelrange/)() | Hämtar ett intervall av rubriknivåer att inkludera. |
| [get_HideInWebLayout](./get_hideinweblayout/)() | Hämtar om tabbläders ledare och sidnummer ska döljas i webblayoutvyn. |
| [get_InsertHyperlinks](./get_inserthyperlinks/)() | Hämtar om innehållsförteckningens poster ska göras till hyperlänkar. |
| [get_IsDirty](../field/get_isdirty/)() | Hämtar eller anger om det aktuella resultatet av fältet inte längre är korrekt (föråldrat) på grund av andra ändringar som gjorts i dokumentet. |
| [get_IsLocked](../field/get_islocked/)() | Hämtar eller anger om fältet är låst (bör inte beräkna om sitt resultat). |
| [get_LocaleId](../field/get_localeid/)() | Hämtar eller anger LCID för fältet. |
| [get_PageNumberOmittingLevelRange](./get_pagenumberomittinglevelrange/)() | Hämtar ett intervall av nivåer för innehållsförteckningens poster från vilka sidnummer ska utelämnas. |
| [get_PrefixedSequenceIdentifier](./get_prefixedsequenceidentifier/)() | Hämtar eller anger identifieraren för en sekvens där ett prefix ska läggas till postens sidnummer. |
| [get_PreserveLineBreaks](./get_preservelinebreaks/)() | Hämtar om radbrytningstecken ska bevaras inom tabellposter. |
| [get_PreserveTabs](./get_preservetabs/)() | Hämtar om tabbposter ska bevaras inom tabellposter. |
| [get_Result](../field/get_result/)() | Hämtar eller anger text som ligger mellan fältavgränsaren och fältets slut. |
| [get_Separator](../field/get_separator/)() | Hämtar noden som representerar fältavgränsaren. Kan vara **null**. |
| [get_SequenceSeparator](./get_sequenceseparator/)() | Hämtar eller anger teckensekvensen som används för att separera sekvensnummer och sidnummer. |
| [get_Start](../field/get_start/)() const | Hämtar noden som representerar fältets början. |
| [get_TableOfFiguresLabel](./get_tableoffigureslabel/)() | Hämtar eller anger namnet på sekvensidentifieraren som används när en figurlista byggs. |
| virtual [get_Type](../field/get_type/)() const | Hämtar Microsoft Word-fälttypen. |
| [get_UseParagraphOutlineLevel](./get_useparagraphoutlinelevel/)() | Hämtar om det tillämpade styckeöversiktsnivån ska användas. |
| [GetFieldCode](../field/getfieldcode/)() | Returnerar text mellan fältets början och fältavgränsaren (eller fältets slut om det inte finns någon avgränsare). Både fältkod och fältresultat för underfält inkluderas. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Returnerar text mellan fältets början och fältavgränsaren (eller fältets slut om det inte finns någon avgränsare). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Tar bort fältet från dokumentet. Returnerar en nod precis efter fältet. Om fältets slut är det sista barnet till dess föräldranod, returneras dess föräldrapparagraf. Om fältet redan har tagits bort, returneras **null**. |
| [set_BookmarkName](./set_bookmarkname/)(const System::String\&) | Sätter namnet på bokmärket som markerar den del av dokumentet som används för att bygga tabellen. |
| [set_CaptionlessTableOfFiguresLabel](./set_captionlesstableoffigureslabel/)(const System::String\&) | Sättare för [Aspose::Words::Fields::FieldToc::get_CaptionlessTableOfFiguresLabel](./get_captionlesstableoffigureslabel/). |
| [set_CustomStyles](./set_customstyles/)(const System::String\&) | Anger en lista med stilar förutom de inbyggda rubrikstilarna som ska inkluderas i innehållsförteckningen. |
| [set_EntryIdentifier](./set_entryidentifier/)(const System::String\&) | Anger en sträng som ska matcha typidentifierare för TC‑fält som inkluderas. |
| [set_EntryLevelRange](./set_entrylevelrange/)(const System::String\&) | Anger ett intervall av nivåer för innehållsförteckningens poster som ska inkluderas. |
| [set_EntrySeparator](./set_entryseparator/)(const System::String\&) | Ställer in en sekvens av tecken som separerar en post och dess sidnummer. |
| [set_HeadingLevelRange](./set_headinglevelrange/)(const System::String\&) | Ställer in ett intervall av rubriknivåer att inkludera. |
| [set_HideInWebLayout](./set_hideinweblayout/)(bool) | Ställer in om tabbledar och sidnummer ska döljas i webblayoutvyn. |
| [set_InsertHyperlinks](./set_inserthyperlinks/)(bool) | Ställer in om innehållsförteckningens poster ska göras till hyperlänkar. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Sättare för [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Sättare för [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Sättare för [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_PageNumberOmittingLevelRange](./set_pagenumberomittinglevelrange/)(const System::String\&) | Ställer in ett intervall av nivåer i innehållsförteckningens poster från vilka sidnummer ska utelämnas. |
| [set_PrefixedSequenceIdentifier](./set_prefixedsequenceidentifier/)(const System::String\&) | Inställare för [Aspose::Words::Fields::FieldToc::get_PrefixedSequenceIdentifier](./get_prefixedsequenceidentifier/). |
| [set_PreserveLineBreaks](./set_preservelinebreaks/)(bool) | Ställer in om radbrytningstecken ska bevaras inom tabellposter. |
| [set_PreserveTabs](./set_preservetabs/)(bool) | Ställer in om tabbposter ska bevaras inom tabellposter. |
| [set_Result](../field/set_result/)(const System::String\&) | Sättare för [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_SequenceSeparator](./set_sequenceseparator/)(const System::String\&) | Inställare för [Aspose::Words::Fields::FieldToc::get_SequenceSeparator](./get_sequenceseparator/). |
| [set_TableOfFiguresLabel](./set_tableoffigureslabel/)(const System::String\&) | Inställare för [Aspose::Words::Fields::FieldToc::get_TableOfFiguresLabel](./get_tableoffigureslabel/). |
| [set_UseParagraphOutlineLevel](./set_useparagraphoutlinelevel/)(bool) | Ställer in om det tillämpade styckeöversiktsnivån ska användas. |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Utför avlänkning av fältet. |
| [Update](../field/update/)() | Utför fältuppdateringen. Kastar ett undantag om fältet redan uppdateras. |
| [Update](../field/update/)(bool) | Utför en fältuppdatering. Kastar ett undantag om fältet redan uppdateras. |
| [UpdatePageNumbers](./updatepagenumbers/)() | Uppdaterar sidnumren för objekt i denna innehållsförteckning. |

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

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
