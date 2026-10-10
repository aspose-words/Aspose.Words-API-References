---
title: "Aspose::Words::Fields::FieldListNum-klass"
linktitle: "FieldListNum"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::FieldListNum-klass. Implementerar LISTNUM-fältet. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 64000
url: /sv/cpp/aspose.words.fields/fieldlistnum/
---
## FieldListNum class


Implementerar LISTNUM-fältet. För att lära dig mer, besök dokumentationsartikeln [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldListNum : public Aspose::Words::Fields::Field,
                     public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_DisplayResult](../field/get_displayresult/)() | Hämtar texten som representerar det visade fältresultatet. |
| [get_End](../field/get_end/)() const | Hämtar noden som representerar fältets slut. |
| [get_FieldEnd](../field/get_fieldend/)() const | Hämtar noden som representerar fältets slut. |
| [get_FieldStart](../field/get_fieldstart/)() const | Hämtar noden som representerar fältets början. |
| [get_Format](../field/get_format/)() | Hämtar ett [FieldFormat](../fieldformat/) objekt som ger typad åtkomst till fältets formatering. |
| [get_HasListName](./get_haslistname/)() | Returnerar ett värde som indikerar om namnet på en abstrakt numreringsdefinition tillhandahålls av fältets kod. |
| [get_IsDirty](../field/get_isdirty/)() | Hämtar eller anger om det aktuella resultatet av fältet inte längre är korrekt (föråldrat) på grund av andra ändringar som gjorts i dokumentet. |
| [get_IsLocked](../field/get_islocked/)() | Hämtar eller anger om fältet är låst (bör inte beräkna om sitt resultat). |
| [get_ListLevel](./get_listlevel/)() | Hämtar eller anger nivån i listan och åsidosätter fältets standardbeteende. |
| [get_ListName](./get_listname/)() | Hämtar eller anger namnet på den abstrakta numreringsdefinitionen som används för numreringen. |
| [get_LocaleId](../field/get_localeid/)() | Hämtar eller anger LCID för fältet. |
| [get_Result](../field/get_result/)() | Hämtar eller anger text som ligger mellan fältavgränsaren och fältets slut. |
| [get_Separator](../field/get_separator/)() | Hämtar noden som representerar fältavgränsaren. Kan vara **null**. |
| [get_Start](../field/get_start/)() const | Hämtar noden som representerar fältets början. |
| [get_StartingNumber](./get_startingnumber/)() | Hämtar eller anger startvärdet för detta fält. |
| virtual [get_Type](../field/get_type/)() const | Hämtar Microsoft Word-fälttypen. |
| [GetFieldCode](../field/getfieldcode/)() | Returnerar text mellan fältets början och fältavgränsaren (eller fältets slut om det inte finns någon avgränsare). Både fältkod och fältresultat för underfält inkluderas. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Returnerar text mellan fältets början och fältavgränsaren (eller fältets slut om det inte finns någon avgränsare). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)() override | Tar bort fältet från dokumentet. Returnerar en nod precis efter fältet. Om fältets slut är det sista barnet till dess föräldranod, returneras dess föräldrapparagraf. Om fältet redan har tagits bort, returneras **null**. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Sättare för [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Sättare för [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_ListLevel](./set_listlevel/)(const System::String\&) | Sättare för [Aspose::Words::Fields::FieldListNum::get_ListLevel](./get_listlevel/). |
| [set_ListName](./set_listname/)(const System::String\&) | Sättare för [Aspose::Words::Fields::FieldListNum::get_ListName](./get_listname/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Sättare för [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_Result](../field/set_result/)(const System::String\&) | Sättare för [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_StartingNumber](./set_startingnumber/)(const System::String\&) | Sättare för [Aspose::Words::Fields::FieldListNum::get_StartingNumber](./get_startingnumber/). |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Utför avlänkning av fältet. |
| [Update](../field/update/)() | Utför fältuppdateringen. Kastar ett undantag om fältet redan uppdateras. |
| [Update](../field/update/)(bool) | Utför en fältuppdatering. Kastar ett undantag om fältet redan uppdateras. |

## Exempel



Visar hur man numrerar stycken med LISTNUM-fält.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// LISTNUM-fält visar ett tal som ökar vid varje LISTNUM-fält.
// Dessa fält har också en mängd alternativ som låter oss använda dem för att efterlikna numrerade listor.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldListNum>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldListNum, true));

// Listor börjar räkna från 1 som standard, men vi kan sätta detta tal till ett annat värde, till exempel 0.
// Detta fält kommer att visa \"0)\".
field->set_StartingNumber(u"0");
builder->Writeln(u"Paragraph 1");

ASSERT_EQ(u" LISTNUM  \\s 0", field->GetFieldCode());

// LISTNUM-fält upprätthåller separata räknare för varje listnivå.
// Att infoga ett LISTNUM-fält i samma stycke som ett annat LISTNUM-fält
// ökar listnivån istället för räknaren.
// Det nästa fältet kommer att fortsätta räknaren som vi startade ovan och visa värdet \"1\" på listnivå 1.
builder->InsertField(Aspose::Words::Fields::FieldType::FieldListNum, true);

// Detta fält kommer att starta en räknare på listnivå 2. Det kommer att visa värdet \"1\".
builder->InsertField(Aspose::Words::Fields::FieldType::FieldListNum, true);

// Detta fält kommer att starta en räknare på listnivå 3. Det kommer att visa värdet \"1\".
// Olika listnivåer har olika formatering,
// så dessa fält kombinerade kommer att visa värdet \"1)a)i)\".
builder->InsertField(Aspose::Words::Fields::FieldType::FieldListNum, true);
builder->Writeln(u"Paragraph 2");

// Det nästa LISTNUM-fältet som vi infogar kommer att fortsätta räknaren på listnivån
// som det föregående LISTNUM-fältet var på.
// Vi kan använda egenskapen \"ListLevel\" för att hoppa till en annan listnivå.
// Om detta LISTNUM-fält förblev på listnivå 3, skulle det visa \"ii)\",
// men, eftersom vi har flyttat den till listnivå 2, fortsätter den räkningen på den nivån och visar "b)".
field = System::ExplicitCast<Aspose::Words::Fields::FieldListNum>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldListNum, true));
field->set_ListLevel(u"2");
builder->Writeln(u"Paragraph 3");

ASSERT_EQ(u" LISTNUM  \\l 2", field->GetFieldCode());

// Vi kan sätta egenskapen ListName för att få fältet att efterlikna en annan AUTONUM-fälttyp.
// "NumberDefault" efterliknar AUTONUM, "OutlineDefault" efterliknar AUTONUMOUT,
// och "LegalDefault" efterliknar AUTONUMLGL-fält.
// Listnamnet "OutlineDefault" med 1 som startnummer kommer att resultera i att visa "I.".
field = System::ExplicitCast<Aspose::Words::Fields::FieldListNum>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldListNum, true));
field->set_StartingNumber(u"1");
field->set_ListName(u"OutlineDefault");
builder->Writeln(u"Paragraph 4");

ASSERT_TRUE(field->get_HasListName());
ASSERT_EQ(u" LISTNUM  OutlineDefault \\s 1", field->GetFieldCode());

// ListName överförs inte från föregående fält, så vi måste sätta den för varje nytt fält.
// Detta fält fortsätter räkningen med det olika listnamnet och visar "II.".
field = System::ExplicitCast<Aspose::Words::Fields::FieldListNum>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldListNum, true));
field->set_ListName(u"OutlineDefault");
builder->Writeln(u"Paragraph 5");

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.LISTNUM.docx");
```

## Se även

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
