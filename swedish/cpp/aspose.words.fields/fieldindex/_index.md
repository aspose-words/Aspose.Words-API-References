---
title: "Aspose::Words::Fields::FieldIndex-klass"
linktitle: "FieldIndex"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::FieldIndex-klass. Implementerar INDEX-fältet. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 59000
url: /sv/cpp/aspose.words.fields/fieldindex/
---
## FieldIndex class


Implementerar INDEX-fältet. För att lära dig mer, besök dokumentationsartikeln [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldIndex : public Aspose::Words::Fields::Field,
                   public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_BookmarkName](./get_bookmarkname/)() | Hämtar eller anger namnet på bokmärket som markerar den del av dokumentet som används för att bygga indexet. |
| [get_CrossReferenceSeparator](./get_crossreferenceseparator/)() | Hämtar eller anger teckensekvensen som används för att separera korsreferenser och andra poster. |
| [get_DisplayResult](../field/get_displayresult/)() | Hämtar texten som representerar det visade fältresultatet. |
| [get_End](../field/get_end/)() const | Hämtar noden som representerar fältets slut. |
| [get_EntryType](./get_entrytype/)() | Hämtar eller anger en indexposttyp som används för att bygga indexet. |
| [get_FieldEnd](../field/get_fieldend/)() const | Hämtar noden som representerar fältets slut. |
| [get_FieldStart](../field/get_fieldstart/)() const | Hämtar noden som representerar fältets början. |
| [get_Format](../field/get_format/)() | Hämtar ett [FieldFormat](../fieldformat/) objekt som ger typad åtkomst till fältets formatering. |
| [get_HasPageNumberSeparator](./get_haspagenumberseparator/)() | Hämtar ett värde som indikerar om en sidnummeravgränsare har åsidosatts via fältets kod. |
| [get_HasSequenceName](./get_hassequencename/)() | Hämtar ett värde som indikerar om en sekvens ska användas under fältets resultatbyggnad. |
| [get_Heading](./get_heading/)() | Hämtar eller anger en rubrik som visas i början av varje uppsättning poster för en given bokstav. |
| [get_IsDirty](../field/get_isdirty/)() | Hämtar eller anger om det aktuella resultatet av fältet inte längre är korrekt (föråldrat) på grund av andra ändringar som gjorts i dokumentet. |
| [get_IsLocked](../field/get_islocked/)() | Hämtar eller anger om fältet är låst (bör inte beräkna om sitt resultat). |
| [get_LanguageId](./get_languageid/)() | Hämtar eller anger språk-ID som används för att generera indexet. |
| [get_LetterRange](./get_letterrange/)() | Hämtar eller anger ett intervall av bokstäver som indexet ska begränsas till. |
| [get_LocaleId](../field/get_localeid/)() | Hämtar eller anger LCID för fältet. |
| [get_NumberOfColumns](./get_numberofcolumns/)() | Hämtar eller anger antalet kolumner per sida som används när indexet byggs. |
| [get_PageNumberListSeparator](./get_pagenumberlistseparator/)() | Hämtar eller anger teckensekvensen som används för att separera två sidnummer i en sidnumreringslista. |
| [get_PageNumberSeparator](./get_pagenumberseparator/)() | Hämtar eller anger teckensekvensen som används för att separera ett indexpost och dess sidnummer. |
| [get_PageRangeSeparator](./get_pagerangeseparator/)() | Hämtar eller anger teckensekvensen som används för att separera början och slutet av ett sidintervall. |
| [get_Result](../field/get_result/)() | Hämtar eller anger text som ligger mellan fältavgränsaren och fältets slut. |
| [get_RunSubentriesOnSameLine](./get_runsubentriesonsameline/)() | Hämtar eller anger om underposter ska köras på samma rad som huvudposten. |
| [get_Separator](../field/get_separator/)() | Hämtar noden som representerar fältavgränsaren. Kan vara **null**. |
| [get_SequenceName](./get_sequencename/)() | Hämtar eller anger namnet på en sekvens vars nummer inkluderas med sidnumret. |
| [get_SequenceSeparator](./get_sequenceseparator/)() | Hämtar eller anger teckensekvensen som används för att separera sekvensnummer och sidnummer. |
| [get_Start](../field/get_start/)() const | Hämtar noden som representerar fältets början. |
| virtual [get_Type](../field/get_type/)() const | Hämtar Microsoft Word-fälttypen. |
| [get_UseYomi](./get_useyomi/)() | Hämtar eller anger om användning av yomi‑text för indexposter ska aktiveras. |
| [GetFieldCode](../field/getfieldcode/)() | Returnerar text mellan fältets början och fältavgränsaren (eller fältets slut om det inte finns någon avgränsare). Både fältkod och fältresultat för underfält inkluderas. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Returnerar text mellan fältets början och fältavgränsaren (eller fältets slut om det inte finns någon avgränsare). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Tar bort fältet från dokumentet. Returnerar en nod precis efter fältet. Om fältets slut är det sista barnet till dess föräldranod, returneras dess föräldrapparagraf. Om fältet redan har tagits bort, returneras **null**. |
| [set_BookmarkName](./set_bookmarkname/)(const System::String\&) | Sättare för [Aspose::Words::Fields::FieldIndex::get_BookmarkName](./get_bookmarkname/). |
| [set_CrossReferenceSeparator](./set_crossreferenceseparator/)(const System::String\&) | Sättare för [Aspose::Words::Fields::FieldIndex::get_CrossReferenceSeparator](./get_crossreferenceseparator/). |
| [set_EntryType](./set_entrytype/)(const System::String\&) | Sättare för [Aspose::Words::Fields::FieldIndex::get_EntryType](./get_entrytype/). |
| [set_Heading](./set_heading/)(const System::String\&) | Sättare för [Aspose::Words::Fields::FieldIndex::get_Heading](./get_heading/). |
| [set_IsDirty](../field/set_isdirty/)(bool) | Sättare för [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Sättare för [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LanguageId](./set_languageid/)(const System::String\&) | Sättare för [Aspose::Words::Fields::FieldIndex::get_LanguageId](./get_languageid/). |
| [set_LetterRange](./set_letterrange/)(const System::String\&) | Sättare för [Aspose::Words::Fields::FieldIndex::get_LetterRange](./get_letterrange/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Sättare för [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_NumberOfColumns](./set_numberofcolumns/)(const System::String\&) | Sättare för [Aspose::Words::Fields::FieldIndex::get_NumberOfColumns](./get_numberofcolumns/). |
| [set_PageNumberListSeparator](./set_pagenumberlistseparator/)(const System::String\&) | Sättare för [Aspose::Words::Fields::FieldIndex::get_PageNumberListSeparator](./get_pagenumberlistseparator/). |
| [set_PageNumberSeparator](./set_pagenumberseparator/)(const System::String\&) | Sättare för [Aspose::Words::Fields::FieldIndex::get_PageNumberSeparator](./get_pagenumberseparator/). |
| [set_PageRangeSeparator](./set_pagerangeseparator/)(const System::String\&) | Sättare för [Aspose::Words::Fields::FieldIndex::get_PageRangeSeparator](./get_pagerangeseparator/). |
| [set_Result](../field/set_result/)(const System::String\&) | Sättare för [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_RunSubentriesOnSameLine](./set_runsubentriesonsameline/)(bool) | Sättare för [Aspose::Words::Fields::FieldIndex::get_RunSubentriesOnSameLine](./get_runsubentriesonsameline/). |
| [set_SequenceName](./set_sequencename/)(const System::String\&) | Sättare för [Aspose::Words::Fields::FieldIndex::get_SequenceName](./get_sequencename/). |
| [set_SequenceSeparator](./set_sequenceseparator/)(const System::String\&) | Sättare för [Aspose::Words::Fields::FieldIndex::get_SequenceSeparator](./get_sequenceseparator/). |
| [set_UseYomi](./set_useyomi/)(bool) | Sättare för [Aspose::Words::Fields::FieldIndex::get_UseYomi](./get_useyomi/). |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Utför avlänkning av fältet. |
| [Update](../field/update/)() | Utför fältuppdateringen. Kastar ett undantag om fältet redan uppdateras. |
| [Update](../field/update/)(bool) | Utför en fältuppdatering. Kastar ett undantag om fältet redan uppdateras. |

## Exempel



Visar hur man skapar ett INDEX-fält och sedan använder XE-fält för att fylla det med poster.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Skapa ett INDEX-fält som visar en post för varje XE-fält som hittas i dokumentet.
// Varje post kommer att visa XE-fältets Text-egenskapsvärde på vänster sida
// och sidan som innehåller XE-fältet på höger sida.
// Om XE-fälten har samma värde i deras \"Text\"-egenskap,
// kommer INDEX-fältet att gruppera dem till en post.
auto index = System::ExplicitCast<Aspose::Words::Fields::FieldIndex>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndex, true));

// Konfigurera INDEX-fältet så att det endast visar XE-fält som ligger inom gränserna
// för ett bokmärke med namnet \"MainBookmark\" och vars \"EntryType\"-egenskaper har värdet \"A\".
// För både INDEX- och XE-fält använder \"EntryType\"-egenskapen endast det första tecknet i dess strängvärde.
index->set_BookmarkName(u"MainBookmark");
index->set_EntryType(u"A");

ASSERT_EQ(u" INDEX  \\b MainBookmark \\f A", index->GetFieldCode());

// På en ny sida, starta bokmärket med ett namn som matchar värdet
// för INDEX-fältets \"BookmarkName\"-egenskap.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->StartBookmark(u"MainBookmark");

// INDEX-fältet kommer att plocka upp den här posten eftersom den ligger inom bokmärket,
// och dess posttyp matchar också INDEX-fältets posttyp.
auto indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Index entry 1");
indexEntry->set_EntryType(u"A");

ASSERT_EQ(u" XE  \"Index entry 1\" \\f A", indexEntry->GetFieldCode());

// Infoga ett XE-fält som inte kommer att visas i INDEX eftersom posttyperna inte matchar.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Index entry 2");
indexEntry->set_EntryType(u"B");

// Avsluta bokmärket och infoga ett XE-fält efteråt.
// Det är av samma typ som INDEX-fältet, men kommer inte att visas
// eftersom det är utanför bokmärkets gränser.
builder->EndBookmark(u"MainBookmark");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Index entry 3");
indexEntry->set_EntryType(u"A");

doc->UpdatePageLayout();
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.INDEX.XE.Filtering.docx");
```


Visar hur man fyller ett INDEX-fält med poster med hjälp av XE-fält, och även ändrar dess utseende.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Skapa ett INDEX-fält som visar en post för varje XE-fält som hittas i dokumentet.
// Varje post kommer att visa XE-fältets Text-egenskapsvärde på vänster sida,
// och sidnumret som innehåller XE-fältet på höger sida.
// Om XE-fälten har samma värde i deras \"Text\"-egenskap,
// kommer INDEX-fältet att gruppera dem till en post.
auto index = System::ExplicitCast<Aspose::Words::Fields::FieldIndex>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndex, true));
index->set_LanguageId(u"1033");

// Om du sätter detta egenskapsvärde till "A" kommer alla poster att grupperas efter deras första bokstav,
// och placera den bokstaven i versaler ovanför varje grupp.
index->set_Heading(u"A");

// Ställ in tabellen som skapats av INDEX-fältet så att den sträcker sig över 2 kolumner.
index->set_NumberOfColumns(u"2");

// Ställ in att alla poster med startbokstäver utanför teckenområdet "a-c" ska utelämnas.
index->set_LetterRange(u"a-c");

ASSERT_EQ(u" INDEX  \\z 1033 \\h A \\c 2 \\p a-c", index->GetFieldCode());

// Dessa två nästa XE-fält kommer att visas under rubriken "A",
// med deras respektive textstilar också tillämpade på deras sidnummer.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
auto indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Apple");
indexEntry->set_IsItalic(true);

ASSERT_EQ(u" XE  Apple \\i", indexEntry->GetFieldCode());

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Apricot");
indexEntry->set_IsBold(true);

ASSERT_EQ(u" XE  Apricot \\b", indexEntry->GetFieldCode());

// Båda de två nästa XE-fälten kommer att vara under rubrikerna "B" och "C" i INDEX-fälten innehållsförteckning.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Banana");

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Cherry");

// INDEX-fält sorterar alla poster alfabetiskt, så denna post kommer att visas under "A" tillsammans med de andra två.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Avocado");

// Denna post kommer inte att visas eftersom den börjar med bokstaven "D",
// vilket ligger utanför teckenområdet "a-c" som INDEX-fältets LetterRange-egenskap definierar.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
indexEntry = System::ExplicitCast<Aspose::Words::Fields::FieldXE>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIndexEntry, true));
indexEntry->set_Text(u"Durian");

doc->UpdatePageLayout();
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.INDEX.XE.Formatting.docx");
```

## Se även

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
