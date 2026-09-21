---
title: "Aspose::Words::Fields::FieldDatabase class"
linktitle: "FieldDatabase"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::FieldDatabase class. Implementerar DATABASE-fältet. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 28000
url: /sv/cpp/aspose.words.fields/fielddatabase/
---
## FieldDatabase class


Implementerar DATABASE-fältet. För att lära dig mer, besök [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) dokumentationsartikel.

```cpp
class FieldDatabase : public Aspose::Words::Fields::Field,
                      public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [FieldDatabase](./fielddatabase/)() |  |
| [get_Connection](./get_connection/)() | Hämtar en anslutning till data. |
| [get_DisplayResult](../field/get_displayresult/)() | Hämtar texten som representerar det visade fältresultatet. |
| [get_End](../field/get_end/)() const | Hämtar noden som representerar fältets slut. |
| [get_FieldEnd](../field/get_fieldend/)() const | Hämtar noden som representerar fältets slut. |
| [get_FieldStart](../field/get_fieldstart/)() const | Hämtar noden som representerar fältets början. |
| [get_FileName](./get_filename/)() | Hämtar den fullständiga sökvägen och filnamnet för databasen. |
| [get_FirstRecord](./get_firstrecord/)() | Hämtar det heltalsbaserade postnumret för den första dataposten som ska infogas. |
| [get_Format](../field/get_format/)() | Hämtar ett [FieldFormat](../fieldformat/) objekt som ger typad åtkomst till fältets formatering. |
| [get_FormatAttributes](./get_formatattributes/)() | Hämtar vilka attribut i formatet som ska tillämpas på tabellen. |
| [get_InsertHeadings](./get_insertheadings/)() | Hämtar om fältnamnen från databasen ska infogas som kolumnrubriker i den resulterande tabellen. |
| [get_InsertOnceOnMailMerge](./get_insertonceonmailmerge/)() | Hämtar om data ska infogas i början av en sammanslagning. |
| [get_IsDirty](../field/get_isdirty/)() | Hämtar eller anger om det aktuella resultatet av fältet inte längre är korrekt (föråldrat) på grund av andra ändringar som gjorts i dokumentet. |
| [get_IsLocked](../field/get_islocked/)() | Hämtar eller anger om fältet är låst (bör inte beräkna om sitt resultat). |
| [get_LastRecord](./get_lastrecord/)() | Hämtar det heltalsbaserade postnumret för den sista dataposten som ska infogas. |
| [get_LocaleId](../field/get_localeid/)() | Hämtar eller anger LCID för fältet. |
| [get_Query](./get_query/)() | Hämtar en uppsättning SQL-instruktioner som frågar databasen. |
| [get_Result](../field/get_result/)() | Hämtar eller anger text som ligger mellan fältavgränsaren och fältets slut. |
| [get_Separator](../field/get_separator/)() | Hämtar noden som representerar fältavgränsaren. Kan vara **null**. |
| [get_Start](../field/get_start/)() const | Hämtar noden som representerar fältets början. |
| [get_TableFormat](./get_tableformat/)() | Hämtar formatet som ska tillämpas på resultatet av databasfrågan. |
| virtual [get_Type](../field/get_type/)() const | Hämtar Microsoft Word-fälttypen. |
| [GetFieldCode](../field/getfieldcode/)() | Returnerar text mellan fältets början och fältavgränsaren (eller fältets slut om det inte finns någon avgränsare). Både fältkod och fältresultat för underfält inkluderas. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Returnerar text mellan fältets början och fältavgränsaren (eller fältets slut om det inte finns någon avgränsare). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Tar bort fältet från dokumentet. Returnerar en nod precis efter fältet. Om fältets slut är det sista barnet till dess föräldranod, returneras dess föräldrapparagraf. Om fältet redan har tagits bort, returneras **null**. |
| [set_Connection](./set_connection/)(const System::String\&) | Ställer in en anslutning till data. |
| [set_FileName](./set_filename/)(const System::String\&) | Ställer in den fullständiga sökvägen och filnamnet för databasen. |
| [set_FirstRecord](./set_firstrecord/)(const System::String\&) | Ställer in det heltalsbaserade postnumret för den första dataposten som ska infogas. |
| [set_FormatAttributes](./set_formatattributes/)(const System::String\&) | Ställer in vilka attribut i formatet som ska tillämpas på tabellen. |
| [set_InsertHeadings](./set_insertheadings/)(bool) | Anger om fältnamnen från databasen ska infogas som kolumnrubriker i den resulterande tabellen. |
| [set_InsertOnceOnMailMerge](./set_insertonceonmailmerge/)(bool) | Anger om data ska infogas i början av en sammanslagning. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Sättare för [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Sättare för [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LastRecord](./set_lastrecord/)(const System::String\&) | Anger det heltaliga postnumret för den sista dataposten som ska infogas. |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Sättare för [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_Query](./set_query/)(const System::String\&) | Anger en uppsättning SQL‑instruktioner som frågar databasen. |
| [set_Result](../field/set_result/)(const System::String\&) | Sättare för [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_TableFormat](./set_tableformat/)(const System::String\&) | Anger det format som ska tillämpas på resultatet av databasfrågan. |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Utför avlänkning av fältet. |
| [Update](../field/update/)() | Utför fältuppdateringen. Kastar ett undantag om fältet redan uppdateras. |
| [Update](../field/update/)(bool) | Utför en fältuppdatering. Kastar ett undantag om fältet redan uppdateras. |
## Se även

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
