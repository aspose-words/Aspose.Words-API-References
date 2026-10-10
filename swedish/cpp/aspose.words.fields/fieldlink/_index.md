---
title: "Aspose::Words::Fields::FieldLink klass"
linktitle: "FieldLink"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::FieldLink klass. Implementerar LINK-fältet. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 63000
url: /sv/cpp/aspose.words.fields/fieldlink/
---
## FieldLink class


Implementerar LINK-fältet. För att lära dig mer, besök dokumentationsartikeln [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldLink : public Aspose::Words::Fields::Field,
                  public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_AutoUpdate](./get_autoupdate/)() | Hämtar om detta fält ska uppdateras automatiskt. |
| [get_DisplayResult](../field/get_displayresult/)() | Hämtar texten som representerar det visade fältresultatet. |
| [get_End](../field/get_end/)() const | Hämtar noden som representerar fältets slut. |
| [get_FieldEnd](../field/get_fieldend/)() const | Hämtar noden som representerar fältets slut. |
| [get_FieldStart](../field/get_fieldstart/)() const | Hämtar noden som representerar fältets början. |
| [get_Format](../field/get_format/)() | Hämtar ett [FieldFormat](../fieldformat/) objekt som ger typad åtkomst till fältets formatering. |
| [get_FormatUpdateType](./get_formatupdatetype/)() | Hämtar ett sätt som det länkade objektet uppdaterar sin formatering. |
| [get_InsertAsBitmap](./get_insertasbitmap/)() | Hämtar om det länkade objektet ska infogas som en bitmap. |
| [get_InsertAsHtml](./get_insertashtml/)() | Hämtar om det länkade objektet ska infogas som HTML-formaterad text. |
| [get_InsertAsPicture](./get_insertaspicture/)() | Hämtar om det länkade objektet ska infogas som en bild. |
| [get_InsertAsRtf](./get_insertasrtf/)() | Hämtar om det länkade objektet ska infogas i rich-text-format (RTF). |
| [get_InsertAsText](./get_insertastext/)() | Hämtar om det länkade objektet ska infogas i endast-text-format. |
| [get_InsertAsUnicode](./get_insertasunicode/)() | Hämtar om det länkade objektet ska infogas som Unicode-text. |
| [get_IsDirty](../field/get_isdirty/)() | Hämtar eller anger om det aktuella resultatet av fältet inte längre är korrekt (föråldrat) på grund av andra ändringar som gjorts i dokumentet. |
| [get_IsLinked](./get_islinked/)() | Hämtar om filstorleken ska minskas genom att inte lagra grafikdata med dokumentet. |
| [get_IsLocked](../field/get_islocked/)() | Hämtar eller anger om fältet är låst (bör inte beräkna om sitt resultat). |
| [get_LocaleId](../field/get_localeid/)() | Hämtar eller anger LCID för fältet. |
| [get_ProgId](./get_progid/)() | Hämtar applikationstypen för länkinformationen. |
| [get_Result](../field/get_result/)() | Hämtar eller anger text som ligger mellan fältavgränsaren och fältets slut. |
| [get_Separator](../field/get_separator/)() | Hämtar noden som representerar fältavgränsaren. Kan vara **null**. |
| [get_SourceFullName](./get_sourcefullname/)() | Hämtar namn och plats för källfilen. |
| [get_SourceItem](./get_sourceitem/)() | Hämtar den del av källfilen som länkas. |
| [get_Start](../field/get_start/)() const | Hämtar noden som representerar fältets början. |
| virtual [get_Type](../field/get_type/)() const | Hämtar Microsoft Word-fälttypen. |
| [GetFieldCode](../field/getfieldcode/)() | Returnerar text mellan fältets början och fältavgränsaren (eller fältets slut om det inte finns någon avgränsare). Både fältkod och fältresultat för underfält inkluderas. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Returnerar text mellan fältets början och fältavgränsaren (eller fältets slut om det inte finns någon avgränsare). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Tar bort fältet från dokumentet. Returnerar en nod precis efter fältet. Om fältets slut är det sista barnet till dess föräldranod, returneras dess föräldrapparagraf. Om fältet redan har tagits bort, returneras **null**. |
| [set_AutoUpdate](./set_autoupdate/)(bool) | Ställer in om detta fält ska uppdateras automatiskt. |
| [set_FormatUpdateType](./set_formatupdatetype/)(const System::String\&) | Ställer in ett sätt som det länkade objektet uppdaterar sin formatering. |
| [set_InsertAsBitmap](./set_insertasbitmap/)(bool) | Ställer in om det länkade objektet ska infogas som en bitmap. |
| [set_InsertAsHtml](./set_insertashtml/)(bool) | Anger om den länkade objektet ska infogas som HTML-formattext. |
| [set_InsertAsPicture](./set_insertaspicture/)(bool) | Anger om den länkade objektet ska infogas som en bild. |
| [set_InsertAsRtf](./set_insertasrtf/)(bool) | Anger om den länkade objektet ska infogas i rich-text-format (RTF). |
| [set_InsertAsText](./set_insertastext/)(bool) | Anger om den länkade objektet ska infogas i endast-textformat. |
| [set_InsertAsUnicode](./set_insertasunicode/)(bool) | Anger om den länkade objektet ska infogas som Unicode-text. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Sättare för [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLinked](./set_islinked/)(bool) | Anger om filstorleken ska minskas genom att inte lagra grafikdata med dokumentet. |
| [set_IsLocked](../field/set_islocked/)(bool) | Sättare för [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Sättare för [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_ProgId](./set_progid/)(const System::String\&) | Anger applikationstypen för länkinformationen. |
| [set_Result](../field/set_result/)(const System::String\&) | Sättare för [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_SourceFullName](./set_sourcefullname/)(const System::String\&) | Anger namn och plats för källfilen. |
| [set_SourceItem](./set_sourceitem/)(const System::String\&) | Anger den del av källfilen som länkas. |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Utför avlänkning av fältet. |
| [Update](../field/update/)() | Utför fältuppdateringen. Kastar ett undantag om fältet redan uppdateras. |
| [Update](../field/update/)(bool) | Utför en fältuppdatering. Kastar ett undantag om fältet redan uppdateras. |
## Se även

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
