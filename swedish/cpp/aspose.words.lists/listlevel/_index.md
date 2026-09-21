---
title: "Aspose::Words::Lists::ListLevel klass"
linktitle: "ListLevel"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Lists::ListLevel klass. Definierar formatering för en listnivå. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 5000
url: /sv/cpp/aspose.words.lists/listlevel/
---
## ListLevel class


Definierar formatering för en listnivå. För att lära dig mer, besök dokumentationsartikeln [Working with Lists](https://docs.aspose.com/words/cpp/working-with-lists/).

```cpp
class ListLevel : public Aspose::Words::IRunAttrSource
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [CreatePictureBullet](./createpicturebullet/)() | Skapar bildpunktsform för den aktuella listnivån. |
| [DeletePictureBullet](./deletepicturebullet/)() | Tar bort bildpunkt för den aktuella listnivån. |
| [Equals](./equals/)(const System::SharedPtr\<Aspose::Words::Lists::ListLevel\>\&) | Jämför med den angivna [ListLevel](./). |
| [get_Alignment](./get_alignment/)() const | Hämtar eller anger justeringen av det faktiska numret för listobjektet. |
| [get_CustomNumberStyleFormat](./get_customnumberstyleformat/)() | Hämtar eller anger det anpassade talstilsformatet för denna listnivå. Till exempel: "a, ç, ĝ, ...". |
| [get_Font](./get_font/)() | Anger teckenformatering som används för listetiketten. |
| [get_ImageData](./get_imagedata/)() | Returnerar bilddata för bildpunktsformen för den aktuella listnivån. |
| [get_IsLegal](./get_islegal/)() const | Sant om nivån omvandlar alla ärvda nummer till arabiska, falskt om den behåller deras talstil. |
| [get_LinkedStyle](./get_linkedstyle/)() | Hämtar eller anger styckeformatet som är länkat till denna listnivå. |
| [get_NumberFormat](./get_numberformat/)() const | Returnerar eller anger talformatet för listnivån. |
| [get_NumberPosition](./get_numberposition/)() const | Returnerar eller anger positionen (i punkter) för numret eller punkten för listnivån. |
| [get_NumberStyle](./get_numberstyle/)() const | Returnerar eller anger talstilen för denna listnivå. |
| [get_RestartAfterLevel](./get_restartafterlevel/)() const | Anger eller returnerar listnivån som måste visas innan den angivna listnivån startar om numreringen. |
| [get_StartAt](./get_startat/)() | Returnerar eller anger startnumret för denna listnivå. |
| [get_TabPosition](./get_tabposition/)() const | Returnerar eller anger tabbpositionen (i punkter) för listnivån. |
| [get_TextPosition](./get_textposition/)() const | Returnerar eller anger positionen (i punkter) för den andra raden av omslagstext för listnivån. |
| [get_TrailingCharacter](./get_trailingcharacter/)() const | Returnerar eller anger tecknet som infogas efter numret för listnivån. |
| static [GetEffectiveValue](./geteffectivevalue/)(int32_t, Aspose::Words::NumberStyle, const System::String\&) | Rapporterar strängrepresentationen av objektet [ListLevel](./) för det angivna indexet för listobjektet. Parametrar specificerar [NumberStyle](../../aspose.words/numberstyle/) och en valfri formatsträng som används när [Custom](../../aspose.words/numberstyle/) anges. |
| [GetHashCode](./gethashcode/)() const override | Beräknar hashkod för detta objekt. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [RemoveTabStop](./removetabstop/)() | Tar bort tabbstopp från listnivån. |
| [set_Alignment](./set_alignment/)(Aspose::Words::Lists::ListLevelAlignment) | Inställare för [Aspose::Words::Lists::ListLevel::get_Alignment](./get_alignment/). |
| [set_CustomNumberStyleFormat](./set_customnumberstyleformat/)(const System::String\&) | Inställare för [Aspose::Words::Lists::ListLevel::get_CustomNumberStyleFormat](./get_customnumberstyleformat/). |
| [set_IsLegal](./set_islegal/)(bool) | Inställare för [Aspose::Words::Lists::ListLevel::get_IsLegal](./get_islegal/). |
| [set_LinkedStyle](./set_linkedstyle/)(const System::SharedPtr\<Aspose::Words::Style\>\&) | Inställare för [Aspose::Words::Lists::ListLevel::get_LinkedStyle](./get_linkedstyle/). |
| [set_NumberFormat](./set_numberformat/)(const System::String\&) | Inställare för [Aspose::Words::Lists::ListLevel::get_NumberFormat](./get_numberformat/). |
| [set_NumberPosition](./set_numberposition/)(double) | Inställare för [Aspose::Words::Lists::ListLevel::get_NumberPosition](./get_numberposition/). |
| [set_NumberStyle](./set_numberstyle/)(Aspose::Words::NumberStyle) | Inställare för [Aspose::Words::Lists::ListLevel::get_NumberStyle](./get_numberstyle/). |
| [set_RestartAfterLevel](./set_restartafterlevel/)(int32_t) | Inställare för [Aspose::Words::Lists::ListLevel::get_RestartAfterLevel](./get_restartafterlevel/). |
| [set_StartAt](./set_startat/)(int32_t) | Inställare för [Aspose::Words::Lists::ListLevel::get_StartAt](./get_startat/). |
| [set_TabPosition](./set_tabposition/)(double) | Inställare för [Aspose::Words::Lists::ListLevel::get_TabPosition](./get_tabposition/). |
| [set_TextPosition](./set_textposition/)(double) | Inställare för [Aspose::Words::Lists::ListLevel::get_TextPosition](./get_textposition/). |
| [set_TrailingCharacter](./set_trailingcharacter/)(Aspose::Words::Lists::ListTrailingCharacter) | Inställare för [Aspose::Words::Lists::ListLevel::get_TrailingCharacter](./get_trailingcharacter/). |
| static [Type](./type/)() |  |
## Anmärkningar


Du skapar inte objekt av den här klassen. [List](../list/) nivåobjekt skapas automatiskt när en lista skapas. Du får åtkomst till [ListLevel](./) objekt via samlingen [ListLevelCollection](../listlevelcollection/).

Använd egenskaperna i [ListLevel](./) för att ange listformatering för enskilda listnivåer.

## Exempel



Visar hur man tillämpar anpassad listformatering på stycken när man använder [DocumentBuilder](../../aspose.words/documentbuilder/).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// En lista låter oss organisera och dekorera uppsättningar av stycken med prefixsymboler och indrag.
// Vi kan skapa nästlade listor genom att öka indragnivån.
// Vi kan börja och avsluta en lista genom att använda en dokumentbyggares egenskap "ListFormat".
// Varje stycke som vi lägger till mellan en listas början och slut blir ett objekt i listan.
// Skapa en lista från en Microsoft Word‑mall och anpassa de två första nivåerna i dess lista.
System::SharedPtr<Aspose::Words::Lists::List> list = doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberDefault);

System::SharedPtr<Aspose::Words::Lists::ListLevel> listLevel = list->get_ListLevels()->idx_get(0);
listLevel->get_Font()->set_Color(System::Drawing::Color::get_Red());
listLevel->get_Font()->set_Size(24);
listLevel->set_NumberStyle(Aspose::Words::NumberStyle::OrdinalText);
listLevel->set_StartAt(21);
listLevel->set_NumberFormat(u"\x0000");

listLevel->set_NumberPosition(-36);
listLevel->set_TextPosition(144);
listLevel->set_TabPosition(144);

listLevel = list->get_ListLevels()->idx_get(1);
listLevel->set_Alignment(Aspose::Words::Lists::ListLevelAlignment::Right);
listLevel->set_NumberStyle(Aspose::Words::NumberStyle::Bullet);
listLevel->get_Font()->set_Name(u"Wingdings");
listLevel->get_Font()->set_Color(System::Drawing::Color::get_Blue());
listLevel->get_Font()->set_Size(24);

// Detta NumberFormat‑värde kommer att skapa stjärnformade punktlistsymboler.
listLevel->set_NumberFormat(u"\xf0af");
listLevel->set_TrailingCharacter(Aspose::Words::Lists::ListTrailingCharacter::Space);
listLevel->set_NumberPosition(144);

// Skapa stycken och tillämpa båda listnivåerna i vår anpassade listformatering på dem.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_ListFormat()->set_List(list);
builder->Writeln(u"The quick brown fox...");
builder->Writeln(u"The quick brown fox...");

builder->get_ListFormat()->ListIndent();
builder->Writeln(u"jumped over the lazy dog.");
builder->Writeln(u"jumped over the lazy dog.");

builder->get_ListFormat()->ListOutdent();
builder->Writeln(u"The quick brown fox...");

builder->get_ListFormat()->RemoveNumbers();

builder->get_Document()->Save(get_ArtifactsDir() + u"Lists.CreateCustomList.docx");
```

## Se även

* Namespace [Aspose::Words::Lists](../)
* Library [Aspose.Words for C++](../../)
