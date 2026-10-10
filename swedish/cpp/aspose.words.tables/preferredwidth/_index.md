---
title: "Aspose::Words::Tables::PreferredWidth class"
linktitle: "PreferredWidth"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Tables::PreferredWidth class. Representerar ett värde och dess måttenhet som används för att specificera den föredragna bredden för en tabell eller en cell. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 4000
url: /sv/cpp/aspose.words.tables/preferredwidth/
---
## PreferredWidth class


Representerar ett värde och dess måttenhet som används för att ange den föredragna bredden på en tabell eller en cell. För att lära dig mer, besök dokumentationsartikeln [Working with Tables](https://docs.aspose.com/words/cpp/working-with-tables/).

```cpp
class PreferredWidth : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| static [Auto](./auto/)() | Returnerar en instans som representerar värdet "preferred width is not specified". |
| [Equals](./equals/)(const System::SharedPtr\<Aspose::Words::Tables::PreferredWidth\>\&) | Bestämmer om den angivna [PreferredWidth](./) är lika i värde med den aktuella [PreferredWidth](./). |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | Bestämmer om det angivna objektet är lika i värde med det aktuella objektet. |
| static [FromPercent](./frompercent/)(double) | En skapande metod som returnerar en ny instans som representerar en föredragen bredd angiven som procent. |
| static [FromPoints](./frompoints/)(double) | En skapande metod som returnerar en ny instans som representerar en föredragen bredd angiven med ett antal punkter. |
| [get_Type](./get_type/)() const | Hämtar måttenheten som används för detta föredragna breddvärde. |
| [get_Value](./get_value/)() const | Hämtar det föredragna breddvärdet. Måttenheten anges i egenskapen [Type](./get_type/). |
| [GetHashCode](./gethashcode/)() const override | Fungerar som en hash-funktion för denna typ. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [ToString](./tostring/)() const override | Returnerar en användarvänlig sträng som visar värdet för detta objekt. |
| static [Type](./type/)() |  |
## Anmärkningar


Föredragen bredd kan anges som procent, antal punkter eller ett speciellt värde "none/auto".

Instanserna av den här klassen är oföränderliga.

## Exempel



Visar hur man ställer in en tabell så att den automatiskt anpassas till 50 % av sidans bredd.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Cell #1");
builder->InsertCell();
builder->Write(u"Cell #2");
builder->InsertCell();
builder->Write(u"Cell #3");

table->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPercent(50));

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertTableWithPreferredWidth.docx");
```


Visar hur man anger en föredragen bredd för tabellceller.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();

// Det finns två sätt att tillämpa klassen "PreferredWidth" på tabellceller.
// 1 -  Ställ in en absolut föredragen bredd baserad på punkter:
builder->InsertCell();
builder->get_CellFormat()->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(40));
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightYellow());
builder->Writeln(System::String::Format(u"Cell with a width of {0}.", builder->get_CellFormat()->get_PreferredWidth()));

// 2 -  Ställ in en relativ föredragen bredd baserad på procent av tabellens bredd:
builder->InsertCell();
builder->get_CellFormat()->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPercent(20));
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightBlue());
builder->Writeln(System::String::Format(u"Cell with a width of {0}.", builder->get_CellFormat()->get_PreferredWidth()));

builder->InsertCell();

// En cell utan angiven föredragen bredd kommer att ta upp resten av det tillgängliga utrymmet.
builder->get_CellFormat()->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::Auto());

// Varje konfiguration av egenskapen "PreferredWidth" skapar ett nytt objekt.
ASSERT_NE(System::ObjectExt::GetHashCode(table->get_FirstRow()->get_Cells()->idx_get(1)->get_CellFormat()->get_PreferredWidth()), System::ObjectExt::GetHashCode(builder->get_CellFormat()->get_PreferredWidth()));

builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightGreen());
builder->Writeln(u"Automatically sized cell.");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertCellsWithPreferredWidths.docx");
```

## Se även

* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
