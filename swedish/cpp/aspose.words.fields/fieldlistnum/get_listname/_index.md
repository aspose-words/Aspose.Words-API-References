---
title: "Aspose::Words::Fields::FieldListNum::get_ListName metod"
linktitle: "get_ListName"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::FieldListNum::get_ListName metod. Hämtar eller anger namnet på den abstrakta numreringsdefinitionen som används för numreringen i C++."
type: docs
weight: 4000
url: /sv/cpp/aspose.words.fields/fieldlistnum/get_listname/
---
## FieldListNum::get_ListName method


Hämtar eller anger namnet på den abstrakta numreringsdefinitionen som används för numreringen.

```cpp
System::String Aspose::Words::Fields::FieldListNum::get_ListName()
```


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

* Class [FieldListNum](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
