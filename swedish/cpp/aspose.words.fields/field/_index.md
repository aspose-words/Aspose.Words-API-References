---
title: "Aspose::Words::Fields::Field klass"
linktitle: "Fält"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::Field klass. Representerar ett Microsoft Word-dokumentfält. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 5000
url: /sv/cpp/aspose.words.fields/field/
---
## Field class


Representerar ett Microsoft Word-dokumentfält. För att lära dig mer, besök dokumentationsartikeln.

```cpp
class Field : public virtual System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_DisplayResult](./get_displayresult/)() | Hämtar texten som representerar det visade fältresultatet. |
| [get_End](./get_end/)() const | Hämtar noden som representerar fältets slut. |
| [get_FieldEnd](./get_fieldend/)() const | Hämtar noden som representerar fältets slut. |
| [get_FieldStart](./get_fieldstart/)() const | Hämtar noden som representerar fältets början. |
| [get_Format](./get_format/)() | Hämtar ett [FieldFormat](../fieldformat/) objekt som ger typad åtkomst till fältets formatering. |
| [get_IsDirty](./get_isdirty/)() | Hämtar eller anger om det aktuella resultatet av fältet inte längre är korrekt (föråldrat) på grund av andra ändringar som gjorts i dokumentet. |
| [get_IsLocked](./get_islocked/)() | Hämtar eller anger om fältet är låst (bör inte beräkna om sitt resultat). |
| [get_LocaleId](./get_localeid/)() | Hämtar eller anger LCID för fältet. |
| [get_Result](./get_result/)() | Hämtar eller anger text som ligger mellan fältavgränsaren och fältets slut. |
| [get_Separator](./get_separator/)() | Hämtar noden som representerar fältavgränsaren. Kan vara **null**. |
| [get_Start](./get_start/)() const | Hämtar noden som representerar fältets början. |
| virtual [get_Type](./get_type/)() const | Hämtar Microsoft Word-fälttypen. |
| [GetFieldCode](./getfieldcode/)() | Returnerar text mellan fältets början och fältavgränsaren (eller fältets slut om det inte finns någon avgränsare). Både fältkod och fältresultat för underfält inkluderas. |
| [GetFieldCode](./getfieldcode/)(bool) | Returnerar text mellan fältets början och fältavgränsaren (eller fältets slut om det inte finns någon avgränsare). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](./remove/)() | Tar bort fältet från dokumentet. Returnerar en nod precis efter fältet. Om fältets slut är det sista barnet till dess föräldranod, returneras dess föräldrapparagraf. Om fältet redan har tagits bort, returneras **null**. |
| [set_IsDirty](./set_isdirty/)(bool) | Sättare för [Aspose::Words::Fields::Field::get_IsDirty](./get_isdirty/). |
| [set_IsLocked](./set_islocked/)(bool) | Sättare för [Aspose::Words::Fields::Field::get_IsLocked](./get_islocked/). |
| [set_LocaleId](./set_localeid/)(int32_t) | Sättare för [Aspose::Words::Fields::Field::get_LocaleId](./get_localeid/). |
| [set_Result](./set_result/)(const System::String\&) | Sättare för [Aspose::Words::Fields::Field::get_Result](./get_result/). |
| static [Type](./type/)() |  |
| [Unlink](./unlink/)() | Utför avlänkning av fältet. |
| [Update](./update/)() | Utför fältuppdateringen. Kastar ett undantag om fältet redan uppdateras. |
| [Update](./update/)(bool) | Utför en fältuppdatering. Kastar ett undantag om fältet redan uppdateras. |
## Anmärkningar


Ett fält i ett Word-dokument är en komplex struktur bestående av flera noder som inkluderar fältstart, fältkod, fältseparator, fältresultat och fältslut. [Fields](../) kan vara nästlade, innehålla rikt innehåll och sträcka sig över flera stycken eller sektioner i ett dokument. Klassen [Field](./) är ett \"facade\"-objekt som tillhandahåller egenskaper och metoder som möjliggör arbete med ett fält som ett enda objekt.

Egenskaperna [Start](./get_start/), [Separator](./get_separator/) och [End](./get_end/) pekar på fältets start-, separator- och slutnoder respektive.

Innehållet mellan fältets start och separator är fältkoden. Innehållet mellan fältseparatorn och fältets slut är fältresultatet. Fältkoden består vanligtvis av ett eller flera [Run](../../aspose.words/run/)-objekt som specificerar instruktioner. Bearbetningsapplikationen förväntas köra fältkoden för att beräkna fältresultatet.

Processen för att beräkna fältresultat kallas fältuppdatering. Aspose.Words kan uppdatera fältresultat för de flesta fälttyper på exakt samma sätt som Microsoft Word gör det. Särskilt kan Aspose.Words beräkna resultat för även de mest komplexa formelfälten. För att beräkna fältresultatet för ett enskilt fält, använd metoden [Update](./update/). För att uppdatera fält i hela dokumentet, använd [UpdateFields](../../aspose.words/document/updatefields/).

Du kan hämta den rena textversionen av fältkoden med metoden [GetFieldCode()](./getfieldcode/). Du kan hämta och sätta den rena textversionen av fältresultatet med egenskapen [Result](./get_result/). Både fältkoden och fältresultatet kan innehålla komplext innehåll, såsom nästlade fält, stycken, former, tabeller och i detta fall kan du vilja arbeta direkt med fältnoderna om du behöver mer kontroll.

Du skapar inte instanser av klassen [Field](./) direkt. För att skapa ett nytt fält, använd metoden [InsertField()](../).

## Exempel



Visar hur man infogar ett fält i ett dokument med en fältkod.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u"DATE \\@ \"dddd, MMMM dd, yyyy\"");

ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldDate, field->get_Type());
ASSERT_EQ(u"DATE \\@ \"dddd, MMMM dd, yyyy\"", field->GetFieldCode());

// Denna överlagring av InsertField‑metoden uppdaterar automatiskt infogade fält.
ASSERT_TRUE((System::DateTime::get_Today() - System::DateTime::Parse(field->get_Result())).get_Days() <= 1);
```

## Se även

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
