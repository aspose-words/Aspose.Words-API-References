---
title: "Aspose::Words::Fields::FieldMergeField-klass"
linktitle: "FieldMergeField"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::FieldMergeField-klass. Implementerar MERGEFIELD-fältet. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 67000
url: /sv/cpp/aspose.words.fields/fieldmergefield/
---
## FieldMergeField class


Implementerar MERGEFIELD-fältet. För att lära dig mer, besök dokumentationsartikeln [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldMergeField : public Aspose::Words::Fields::Field,
                        public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_DisplayResult](../field/get_displayresult/)() | Hämtar texten som representerar det visade fältresultatet. |
| [get_End](../field/get_end/)() const | Hämtar noden som representerar fältets slut. |
| [get_FieldEnd](../field/get_fieldend/)() const | Hämtar noden som representerar fältets slut. |
| [get_FieldName](./get_fieldname/)() | Hämtar namnet på ett datafält. |
| [get_FieldNameNoPrefix](./get_fieldnamenoprefix/)() const | Returnerar endast namnet på datafältet. Eventuellt prefix tas bort till prefix-egenskapen. |
| [get_FieldStart](../field/get_fieldstart/)() const | Hämtar noden som representerar fältets början. |
| [get_Format](../field/get_format/)() | Hämtar ett [FieldFormat](../fieldformat/) objekt som ger typad åtkomst till fältets formatering. |
| [get_IsDirty](../field/get_isdirty/)() | Hämtar eller anger om det aktuella resultatet av fältet inte längre är korrekt (föråldrat) på grund av andra ändringar som gjorts i dokumentet. |
| [get_IsLocked](../field/get_islocked/)() | Hämtar eller anger om fältet är låst (bör inte beräkna om sitt resultat). |
| [get_IsMapped](./get_ismapped/)() | Hämtar om detta fält är ett mappat fält. |
| [get_IsVerticalFormatting](./get_isverticalformatting/)() | Hämtar om teckenomvandling för vertikal formatering ska aktiveras. |
| [get_LocaleId](../field/get_localeid/)() | Hämtar eller anger LCID för fältet. |
| [get_Result](../field/get_result/)() | Hämtar eller anger text som ligger mellan fältavgränsaren och fältets slut. |
| [get_Separator](../field/get_separator/)() | Hämtar noden som representerar fältavgränsaren. Kan vara **null**. |
| [get_Start](../field/get_start/)() const | Hämtar noden som representerar fältets början. |
| [get_TextAfter](./get_textafter/)() | Hämtar texten som ska infogas efter fältet om fältet inte är tomt. |
| [get_TextBefore](./get_textbefore/)() | Hämtar texten som ska infogas före fältet om fältet inte är tomt. |
| [get_Type](./get_type/)() const override | Hämtar Microsoft Word-fälttypen. |
| [GetFieldCode](../field/getfieldcode/)() | Returnerar text mellan fältets början och fältavgränsaren (eller fältets slut om det inte finns någon avgränsare). Både fältkod och fältresultat för underfält inkluderas. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Returnerar text mellan fältets början och fältavgränsaren (eller fältets slut om det inte finns någon avgränsare). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Tar bort fältet från dokumentet. Returnerar en nod precis efter fältet. Om fältets slut är det sista barnet till dess föräldranod, returneras dess föräldrapparagraf. Om fältet redan har tagits bort, returneras **null**. |
| [set_FieldName](./set_fieldname/)(const System::String\&) | Ställer in namnet på ett datafält. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Sättare för [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Sättare för [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_IsMapped](./set_ismapped/)(bool) | Ställer in om detta fält är ett mappat fält. |
| [set_IsVerticalFormatting](./set_isverticalformatting/)(bool) | Ställer in om teckenkonvertering för vertikal formatering ska aktiveras. |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Sättare för [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_Result](../field/set_result/)(const System::String\&) | Sättare för [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_TextAfter](./set_textafter/)(const System::String\&) | Ställer in texten som ska infogas efter fältet om fältet inte är tomt. |
| [set_TextBefore](./set_textbefore/)(const System::String\&) | Ställer in texten som ska infogas före fältet om fältet inte är tomt. |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Utför avlänkning av fältet. |
| [Update](../field/update/)() | Utför fältuppdateringen. Kastar ett undantag om fältet redan uppdateras. |
| [Update](../field/update/)(bool) | Utför en fältuppdatering. Kastar ett undantag om fältet redan uppdateras. |
## Se även

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
