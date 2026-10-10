---
title: "Aspose::Words::Fields::FieldToa klass"
linktitle: "FieldToa"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::FieldToa klass. Implementerar TOA-fältet. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 104000
url: /sv/cpp/aspose.words.fields/fieldtoa/
---
## FieldToa class


Implementerar TOA-fältet. För att lära dig mer, besök [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) dokumentationsartikel.

```cpp
class FieldToa : public Aspose::Words::Fields::Field,
                 public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_BookmarkName](./get_bookmarkname/)() | Hämtar namnet på bokmärket som markerar den del av dokumentet som används för att bygga tabellen. |
| [get_DisplayResult](../field/get_displayresult/)() | Hämtar texten som representerar det visade fältresultatet. |
| [get_End](../field/get_end/)() const | Hämtar noden som representerar fältets slut. |
| [get_EntryCategory](./get_entrycategory/)() | Hämtar den integrala kategorin för poster som ingår i tabellen. |
| [get_EntrySeparator](./get_entryseparator/)() | Hämtar teckensekvensen som används för att separera en post i en auktoritetstabell och dess sidnummer. |
| [get_FieldEnd](../field/get_fieldend/)() const | Hämtar noden som representerar fältets slut. |
| [get_FieldStart](../field/get_fieldstart/)() const | Hämtar noden som representerar fältets början. |
| [get_Format](../field/get_format/)() | Hämtar ett [FieldFormat](../fieldformat/) objekt som ger typad åtkomst till fältets formatering. |
| [get_IsDirty](../field/get_isdirty/)() | Hämtar eller anger om det aktuella resultatet av fältet inte längre är korrekt (föråldrat) på grund av andra ändringar som gjorts i dokumentet. |
| [get_IsLocked](../field/get_islocked/)() | Hämtar eller anger om fältet är låst (bör inte beräkna om sitt resultat). |
| [get_LocaleId](../field/get_localeid/)() | Hämtar eller anger LCID för fältet. |
| [get_PageNumberListSeparator](./get_pagenumberlistseparator/)() | Hämtar teckensekvensen som används för att separera två sidnummer i en sidnummerlista. |
| [get_PageRangeSeparator](./get_pagerangeseparator/)() | Hämtar teckensekvensen som används för att separera början och slutet av ett sidintervall. |
| [get_RemoveEntryFormatting](./get_removeentryformatting/)() | Hämtar om formateringen av posttexten i dokumentet ska tas bort från posten i auktoritetstabellen. |
| [get_Result](../field/get_result/)() | Hämtar eller anger text som ligger mellan fältavgränsaren och fältets slut. |
| [get_Separator](../field/get_separator/)() | Hämtar noden som representerar fältavgränsaren. Kan vara **null**. |
| [get_SequenceName](./get_sequencename/)() | Hämtar namnet på en sekvens vars nummer inkluderas med sidnumret. |
| [get_SequenceSeparator](./get_sequenceseparator/)() | Hämtar teckensekvensen som används för att separera sekvensnummer och sidnummer. |
| [get_Start](../field/get_start/)() const | Hämtar noden som representerar fältets början. |
| virtual [get_Type](../field/get_type/)() const | Hämtar Microsoft Word-fälttypen. |
| [get_UseHeading](./get_useheading/)() | Hämtar om kategorirubriken ska inkluderas för posterna i en auktoritetstabell. |
| [get_UsePassim](./get_usepassim/)() | Hämtar om fem eller fler olika sidreferenser till samma auktoritet ska ersättas med "passim", vilket används för att indikera att ett ord eller avsnitt förekommer ofta i det citerade verket. |
| [GetFieldCode](../field/getfieldcode/)() | Returnerar text mellan fältets början och fältavgränsaren (eller fältets slut om det inte finns någon avgränsare). Både fältkod och fältresultat för underfält inkluderas. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Returnerar text mellan fältets början och fältavgränsaren (eller fältets slut om det inte finns någon avgränsare). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Tar bort fältet från dokumentet. Returnerar en nod precis efter fältet. Om fältets slut är det sista barnet till dess föräldranod, returneras dess föräldrapparagraf. Om fältet redan har tagits bort, returneras **null**. |
| [set_BookmarkName](./set_bookmarkname/)(const System::String\&) | Sätter namnet på bokmärket som markerar den del av dokumentet som används för att bygga tabellen. |
| [set_EntryCategory](./set_entrycategory/)(const System::String\&) | Sätter den integrala kategorin för poster som ingår i tabellen. |
| [set_EntrySeparator](./set_entryseparator/)(const System::String\&) | Sätter teckensekvensen som används för att separera en post i en auktoritetstabell och dess sidnummer. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Sättare för [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Sättare för [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Sättare för [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_PageNumberListSeparator](./set_pagenumberlistseparator/)(const System::String\&) | Sätter teckensekvensen som används för att separera två sidnummer i en sidnummerlista. |
| [set_PageRangeSeparator](./set_pagerangeseparator/)(const System::String\&) | Sätter teckensekvensen som används för att separera början och slutet av ett sidintervall. |
| [set_RemoveEntryFormatting](./set_removeentryformatting/)(bool) | Anger om formateringen av posttexten i dokumentet ska tas bort från posten i förteckningen över myndigheter. |
| [set_Result](../field/set_result/)(const System::String\&) | Sättare för [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_SequenceName](./set_sequencename/)(const System::String\&) | Anger namnet på en sekvens vars nummer inkluderas med sidnumret. |
| [set_SequenceSeparator](./set_sequenceseparator/)(const System::String\&) | Anger teckensekvensen som används för att separera sekvensnummer och sidnummer. |
| [set_UseHeading](./set_useheading/)(bool) | Anger om kategorirubriken ska inkluderas för posterna i en förteckning över myndigheter. |
| [set_UsePassim](./set_usepassim/)(bool) | Anger om fem eller fler olika sidreferenser till samma myndighet ska ersättas med "passim", vilket används för att indikera att ett ord eller avsnitt förekommer ofta i det citerade verket. |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Utför avlänkning av fältet. |
| [Update](../field/update/)() | Utför fältuppdateringen. Kastar ett undantag om fältet redan uppdateras. |
| [Update](../field/update/)(bool) | Utför en fältuppdatering. Kastar ett undantag om fältet redan uppdateras. |
## Se även

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
