---
title: "Aspose::Words::Fields::FieldAdvance klass"
linktitle: "FieldAdvance"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::FieldAdvance klass. Implementerar ADVANCE-fältet. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 8000
url: /sv/cpp/aspose.words.fields/fieldadvance/
---
## FieldAdvance class


Implementerar ADVANCE-fältet. För att lära dig mer, besök [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) dokumentationsartikel.

```cpp
class FieldAdvance : public Aspose::Words::Fields::Field,
                     public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_DisplayResult](../field/get_displayresult/)() | Hämtar texten som representerar det visade fältresultatet. |
| [get_DownOffset](./get_downoffset/)() | Hämtar eller anger antalet punkter som texten som följer fältet ska flyttas nedåt. |
| [get_End](../field/get_end/)() const | Hämtar noden som representerar fältets slut. |
| [get_FieldEnd](../field/get_fieldend/)() const | Hämtar noden som representerar fältets slut. |
| [get_FieldStart](../field/get_fieldstart/)() const | Hämtar noden som representerar fältets början. |
| [get_Format](../field/get_format/)() | Hämtar ett [FieldFormat](../fieldformat/) objekt som ger typad åtkomst till fältets formatering. |
| [get_HorizontalPosition](./get_horizontalposition/)() | Hämtar eller anger antalet punkter som texten som följer fältet ska flyttas horisontellt från vänsterkanten av kolumnen, ramen eller textrutan. |
| [get_IsDirty](../field/get_isdirty/)() | Hämtar eller anger om det aktuella resultatet av fältet inte längre är korrekt (föråldrat) på grund av andra ändringar som gjorts i dokumentet. |
| [get_IsLocked](../field/get_islocked/)() | Hämtar eller anger om fältet är låst (bör inte beräkna om sitt resultat). |
| [get_LeftOffset](./get_leftoffset/)() | Hämtar eller anger antalet punkter som texten som följer fältet ska flyttas åt vänster. |
| [get_LocaleId](../field/get_localeid/)() | Hämtar eller anger LCID för fältet. |
| [get_Result](../field/get_result/)() | Hämtar eller anger text som ligger mellan fältavgränsaren och fältets slut. |
| [get_RightOffset](./get_rightoffset/)() | Hämtar eller anger antalet punkter som texten som följer fältet ska flyttas åt höger. |
| [get_Separator](../field/get_separator/)() | Hämtar noden som representerar fältavgränsaren. Kan vara **null**. |
| [get_Start](../field/get_start/)() const | Hämtar noden som representerar fältets början. |
| virtual [get_Type](../field/get_type/)() const | Hämtar Microsoft Word-fälttypen. |
| [get_UpOffset](./get_upoffset/)() | Hämtar eller anger antalet punkter som texten som följer fältet ska flyttas uppåt. |
| [get_VerticalPosition](./get_verticalposition/)() | Hämtar eller anger antalet punkter som texten som följer fältet ska flyttas vertikalt från sidans överkant. |
| [GetFieldCode](../field/getfieldcode/)() | Returnerar text mellan fältets början och fältavgränsaren (eller fältets slut om det inte finns någon avgränsare). Både fältkod och fältresultat för underfält inkluderas. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Returnerar text mellan fältets början och fältavgränsaren (eller fältets slut om det inte finns någon avgränsare). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Tar bort fältet från dokumentet. Returnerar en nod precis efter fältet. Om fältets slut är det sista barnet till dess föräldranod, returneras dess föräldrapparagraf. Om fältet redan har tagits bort, returneras **null**. |
| [set_DownOffset](./set_downoffset/)(const System::String\&) | Sättare för [Aspose::Words::Fields::FieldAdvance::get_DownOffset](./get_downoffset/). |
| [set_HorizontalPosition](./set_horizontalposition/)(const System::String\&) | Sättare för [Aspose::Words::Fields::FieldAdvance::get_HorizontalPosition](./get_horizontalposition/). |
| [set_IsDirty](../field/set_isdirty/)(bool) | Sättare för [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Sättare för [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LeftOffset](./set_leftoffset/)(const System::String\&) | Sättare för [Aspose::Words::Fields::FieldAdvance::get_LeftOffset](./get_leftoffset/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Sättare för [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_Result](../field/set_result/)(const System::String\&) | Sättare för [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_RightOffset](./set_rightoffset/)(const System::String\&) | Sättare för [Aspose::Words::Fields::FieldAdvance::get_RightOffset](./get_rightoffset/). |
| [set_UpOffset](./set_upoffset/)(const System::String\&) | Sättare för [Aspose::Words::Fields::FieldAdvance::get_UpOffset](./get_upoffset/). |
| [set_VerticalPosition](./set_verticalposition/)(const System::String\&) | Sättare för [Aspose::Words::Fields::FieldAdvance::get_VerticalPosition](./get_verticalposition/). |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Utför avlänkning av fältet. |
| [Update](../field/update/)() | Utför fältuppdateringen. Kastar ett undantag om fältet redan uppdateras. |
| [Update](../field/update/)(bool) | Utför en fältuppdatering. Kastar ett undantag om fältet redan uppdateras. |

## Exempel



Visar hur man infogar ett ADVANCE-fält och redigerar dess egenskaper.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"This text is in its normal place.");

// Nedan finns två sätt att använda ADVANCE-fältet för att justera positionen för den text som följer efter det.
// Effekterna av ett ADVANCE-fält fortsätter att tillämpas tills stycket avslutas,
// eller ett annat ADVANCE-fält uppdaterar offset-/koordinatvärdena.
// 1 -  Ange en riktad offset:
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldAdvance>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAdvance, true));
field->set_RightOffset(u"5");
field->set_UpOffset(u"5");

ASSERT_EQ(u" ADVANCE  \\r 5 \\u 5", field->GetFieldCode());

builder->Write(u"This text will be moved up and to the right.");

field = System::ExplicitCast<Aspose::Words::Fields::FieldAdvance>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAdvance, true));
field->set_DownOffset(u"5");
field->set_LeftOffset(u"100");

ASSERT_EQ(u" ADVANCE  \\d 5 \\l 100", field->GetFieldCode());

builder->Writeln(u"This text is moved down and to the left, overlapping the previous text.");

// 2 -  Flytta text till en position som anges av koordinater:
field = System::ExplicitCast<Aspose::Words::Fields::FieldAdvance>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAdvance, true));
field->set_HorizontalPosition(u"-100");
field->set_VerticalPosition(u"200");

ASSERT_EQ(u" ADVANCE  \\x -100 \\y 200", field->GetFieldCode());

builder->Write(u"This text is in a custom position.");

doc->Save(get_ArtifactsDir() + u"Field.ADVANCE.docx");
```

## Se även

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
