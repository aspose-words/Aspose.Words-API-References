---
title: "Aspose::Words::Fields::FieldCitation class"
linktitle: "FieldCitation"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::FieldCitation class. Implementerar CITATION-fältet. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 22000
url: /sv/cpp/aspose.words.fields/fieldcitation/
---
## FieldCitation class


Implementerar CITATION-fältet. För att lära dig mer, besök [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) dokumentationsartikel.

```cpp
class FieldCitation : public Aspose::Words::Fields::Field,
                      public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_AnotherSourceTag](./get_anothersourcetag/)() | Hämtar ett värde som matchar **Tag**-elementets värde från en annan källa som ska inkluderas i citatet. |
| [get_DisplayResult](../field/get_displayresult/)() | Hämtar texten som representerar det visade fältresultatet. |
| [get_End](../field/get_end/)() const | Hämtar noden som representerar fältets slut. |
| [get_FieldEnd](../field/get_fieldend/)() const | Hämtar noden som representerar fältets slut. |
| [get_FieldStart](../field/get_fieldstart/)() const | Hämtar noden som representerar fältets början. |
| [get_Format](../field/get_format/)() | Hämtar ett [FieldFormat](../fieldformat/) objekt som ger typad åtkomst till fältets formatering. |
| [get_FormatLanguageId](./get_formatlanguageid/)() | Hämtar språk-ID:t som används tillsammans med den angivna bibliografiska stilen för att formatera citatet i dokumentet. |
| [get_IsDirty](../field/get_isdirty/)() | Hämtar eller anger om det aktuella resultatet av fältet inte längre är korrekt (föråldrat) på grund av andra ändringar som gjorts i dokumentet. |
| [get_IsLocked](../field/get_islocked/)() | Hämtar eller anger om fältet är låst (bör inte beräkna om sitt resultat). |
| [get_LocaleId](../field/get_localeid/)() | Hämtar eller anger LCID för fältet. |
| [get_PageNumber](./get_pagenumber/)() | Hämtar ett sidnummer som är associerat med citatet. |
| [get_Prefix](./get_prefix/)() | Hämtar ett prefix som läggs till i början av citatet. |
| [get_Result](../field/get_result/)() | Hämtar eller anger text som ligger mellan fältavgränsaren och fältets slut. |
| [get_Separator](../field/get_separator/)() | Hämtar noden som representerar fältavgränsaren. Kan vara **null**. |
| [get_SourceTag](./get_sourcetag/)() | Hämtar ett värde som matchar **Tag**-elementets värde från källan som ska infogas. |
| [get_Start](../field/get_start/)() const | Hämtar noden som representerar fältets början. |
| [get_Suffix](./get_suffix/)() | Hämtar ett suffix som läggs till i slutet av citatet. |
| [get_SuppressAuthor](./get_suppressauthor/)() | Hämtar om författarinformationen undertrycks i citatet. |
| [get_SuppressTitle](./get_suppresstitle/)() | Hämtar om titelinformationen undertrycks i citatet. |
| [get_SuppressYear](./get_suppressyear/)() | Hämtar om årinformationen undertrycks i citatet. |
| virtual [get_Type](../field/get_type/)() const | Hämtar Microsoft Word-fälttypen. |
| [get_VolumeNumber](./get_volumenumber/)() | Hämtar ett volymnummer som är associerat med citatet. |
| [GetFieldCode](../field/getfieldcode/)() | Returnerar text mellan fältets början och fältavgränsaren (eller fältets slut om det inte finns någon avgränsare). Både fältkod och fältresultat för underfält inkluderas. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Returnerar text mellan fältets början och fältavgränsaren (eller fältets slut om det inte finns någon avgränsare). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Tar bort fältet från dokumentet. Returnerar en nod precis efter fältet. Om fältets slut är det sista barnet till dess föräldranod, returneras dess föräldrapparagraf. Om fältet redan har tagits bort, returneras **null**. |
| [set_AnotherSourceTag](./set_anothersourcetag/)(const System::String\&) | Anger ett värde som matchar **Tag**-elementets värde från en annan källa som ska inkluderas i citatet. |
| [set_FormatLanguageId](./set_formatlanguageid/)(const System::String\&) | Anger språk-ID:t som används tillsammans med den angivna bibliografiska stilen för att formatera citatet i dokumentet. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Sättare för [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Sättare för [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Sättare för [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_PageNumber](./set_pagenumber/)(const System::String\&) | Anger ett sidnummer som är associerat med citatet. |
| [set_Prefix](./set_prefix/)(const System::String\&) | Anger ett prefix som läggs till i början av citatet. |
| [set_Result](../field/set_result/)(const System::String\&) | Sättare för [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_SourceTag](./set_sourcetag/)(const System::String\&) | Anger ett värde som matchar **Tag**-elementets värde från källan som ska infogas. |
| [set_Suffix](./set_suffix/)(const System::String\&) | Anger ett suffix som läggs till i slutet av citatet. |
| [set_SuppressAuthor](./set_suppressauthor/)(bool) | Anger om författarinformationen undertrycks i citatet. |
| [set_SuppressTitle](./set_suppresstitle/)(bool) | Ställer in om titelinformationen undertrycks från citatet. |
| [set_SuppressYear](./set_suppressyear/)(bool) | Ställer in om årinformationen undertrycks från citatet. |
| [set_VolumeNumber](./set_volumenumber/)(const System::String\&) | Ställer in ett volymnummer som är associerat med citatet. |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Utför avlänkning av fältet. |
| [Update](../field/update/)() | Utför fältuppdateringen. Kastar ett undantag om fältet redan uppdateras. |
| [Update](../field/update/)(bool) | Utför en fältuppdatering. Kastar ett undantag om fältet redan uppdateras. |
## Se även

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
