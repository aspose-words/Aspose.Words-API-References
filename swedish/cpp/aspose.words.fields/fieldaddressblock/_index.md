---
title: "Aspose::Words::Fields::FieldAddressBlock class"
linktitle: "FieldAddressBlock"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::FieldAddressBlock class. Implementerar ADDRESSBLOCK‑fältet. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 7000
url: /sv/cpp/aspose.words.fields/fieldaddressblock/
---
## FieldAddressBlock class


Implementerar ADDRESSBLOCK-fältet. För att lära dig mer, besök [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) dokumentationsartikel.

```cpp
class FieldAddressBlock : public Aspose::Words::Fields::Field,
                          public Aspose::Words::Fields::IFieldCodeTokenInfoProvider,
                          public Aspose::Words::Fields::IFormattableMergeField
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [FieldAddressBlock](./fieldaddressblock/)() |  |
| [get_DisplayResult](../field/get_displayresult/)() | Hämtar texten som representerar det visade fältresultatet. |
| [get_End](../field/get_end/)() const | Hämtar noden som representerar fältets slut. |
| [get_ExcludedCountryOrRegionName](./get_excludedcountryorregionname/)() | Hämtar eller anger det uteslutna land-/regionsnamnet. |
| [get_FieldEnd](../field/get_fieldend/)() const | Hämtar noden som representerar fältets slut. |
| [get_FieldStart](../field/get_fieldstart/)() const | Hämtar noden som representerar fältets början. |
| [get_Format](../field/get_format/)() | Hämtar ett [FieldFormat](../fieldformat/) objekt som ger typad åtkomst till fältets formatering. |
| [get_FormatAddressOnCountryOrRegion](./get_formataddressoncountryorregion/)() | Hämtar eller anger om adressen ska formateras enligt mottagarens land/region enligt POST*CODE (Universal Postal Union 2006). |
| [get_IncludeCountryOrRegionName](./get_includecountryorregionname/)() | Hämtar eller anger om land-/regionsnamnet ska inkluderas. |
| [get_IsDirty](../field/get_isdirty/)() | Hämtar eller anger om det aktuella resultatet av fältet inte längre är korrekt (föråldrat) på grund av andra ändringar som gjorts i dokumentet. |
| [get_IsLocked](../field/get_islocked/)() | Hämtar eller anger om fältet är låst (bör inte beräkna om sitt resultat). |
| [get_LanguageId](./get_languageid/)() | Hämtar eller anger språk‑ID som används för att formatera adressen. |
| [get_LocaleId](../field/get_localeid/)() | Hämtar eller anger LCID för fältet. |
| [get_NameAndAddressFormat](./get_nameandaddressformat/)() | Hämtar eller anger namn‑ och adressformatet. |
| [get_Result](../field/get_result/)() | Hämtar eller anger text som ligger mellan fältavgränsaren och fältets slut. |
| [get_Separator](../field/get_separator/)() | Hämtar noden som representerar fältavgränsaren. Kan vara **null**. |
| [get_Start](../field/get_start/)() const | Hämtar noden som representerar fältets början. |
| virtual [get_Type](../field/get_type/)() const | Hämtar Microsoft Word-fälttypen. |
| [GetFieldCode](../field/getfieldcode/)() | Returnerar text mellan fältets början och fältavgränsaren (eller fältets slut om det inte finns någon avgränsare). Både fältkod och fältresultat för underfält inkluderas. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Returnerar text mellan fältets början och fältavgränsaren (eller fältets slut om det inte finns någon avgränsare). |
| [GetFieldNames](./getfieldnames/)() override | Returnerar en samling av namn på mail‑sammanfogningsfält som används av fältet. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Tar bort fältet från dokumentet. Returnerar en nod precis efter fältet. Om fältets slut är det sista barnet till dess föräldranod, returneras dess föräldrapparagraf. Om fältet redan har tagits bort, returneras **null**. |
| [set_ExcludedCountryOrRegionName](./set_excludedcountryorregionname/)(const System::String\&) | Inställare för [Aspose::Words::Fields::FieldAddressBlock::get_ExcludedCountryOrRegionName](./get_excludedcountryorregionname/). |
| [set_FormatAddressOnCountryOrRegion](./set_formataddressoncountryorregion/)(bool) | Inställare för [Aspose::Words::Fields::FieldAddressBlock::get_FormatAddressOnCountryOrRegion](./get_formataddressoncountryorregion/). |
| [set_IncludeCountryOrRegionName](./set_includecountryorregionname/)(const System::String\&) | Inställare för [Aspose::Words::Fields::FieldAddressBlock::get_IncludeCountryOrRegionName](./get_includecountryorregionname/). |
| [set_IsDirty](../field/set_isdirty/)(bool) | Sättare för [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Sättare för [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LanguageId](./set_languageid/)(const System::String\&) | Inställare för [Aspose::Words::Fields::FieldAddressBlock::get_LanguageId](./get_languageid/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Sättare för [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_NameAndAddressFormat](./set_nameandaddressformat/)(const System::String\&) | Inställare för [Aspose::Words::Fields::FieldAddressBlock::get_NameAndAddressFormat](./get_nameandaddressformat/). |
| [set_Result](../field/set_result/)(const System::String\&) | Sättare för [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Utför avlänkning av fältet. |
| [Update](../field/update/)() | Utför fältuppdateringen. Kastar ett undantag om fältet redan uppdateras. |
| [Update](../field/update/)(bool) | Utför en fältuppdatering. Kastar ett undantag om fältet redan uppdateras. |
## Se även

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
