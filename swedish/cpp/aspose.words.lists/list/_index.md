---
title: "Aspose::Words::Lists::List-klass"
linktitle: "Lista"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Lists::List-klass. Representerar formatering av en lista. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 1000
url: /sv/cpp/aspose.words.lists/list/
---
## List class


Representerar formatering av en lista. För att lära dig mer, besök dokumentationsartikeln [Working with Lists](https://docs.aspose.com/words/cpp/working-with-lists/).

```cpp
class List : public System::IComparable<System::SharedPtr<Aspose::Words::Lists::List>>
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [CompareTo](./compareto/)(System::SharedPtr\<Aspose::Words::Lists::List\>) override | Jämför den angivna listan med den aktuella listan. |
| [Equals](./equals/)(const System::SharedPtr\<Aspose::Words::Lists::List\>\&) | Jämför med den angivna listan. |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | Bestämmer om det angivna objektet är lika i värde med det aktuella objektet. |
| [get_Document](./get_document/)() const | Hämtar ägardokumentet. |
| [get_IsListStyleDefinition](./get_isliststyledefinition/)() | Returnerar **true** om den här listan är en definition av en liststil. |
| [get_IsListStyleReference](./get_isliststylereference/)() | Returnerar **true** om den här listan är en referens till en liststil. |
| [get_IsMultiLevel](./get_ismultilevel/)() | Returnerar **true** när listan innehåller 9 nivåer; **false** när den har 1 nivå. |
| [get_IsRestartAtEachSection](./get_isrestartateachsection/)() | Anger om listan ska startas om i varje avsnitt. Standardvärdet är **false**. |
| [get_ListId](./get_listid/)() const | Hämtar listans unika identifierare. |
| [get_ListLevels](./get_listlevels/)() | Hämtar samlingen av listnivåer för den här listan. |
| [get_Style](./get_style/)() | Hämtar liststilen som den här listan refererar till eller definierar. |
| [GetHashCode](./gethashcode/)() const override | Beräknar hash‑kod för detta listobjekt. |
| [GetType](./gettype/)() const override |  |
| [HasSameTemplate](./hassametemplate/)(const System::SharedPtr\<Aspose::Words::Lists::List\>\&) | Returnerar true om den aktuella listan och den angivna listan är skapade från samma mall. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_IsRestartAtEachSection](./set_isrestartateachsection/)(bool) | Sättare för [Aspose::Words::Lists::List::get_IsRestartAtEachSection](./get_isrestartateachsection/). |
| static [Type](./type/)() |  |
## Anmärkningar


En lista i ett Microsoft Word‑dokument är en uppsättning formateringsegenskaper för listor. Varje lista kan ha upp till 9 nivåer och formateringsegenskaper, såsom nummerformat, startvärde, indrag, tabbposition osv, definieras separat för varje nivå.

Ett [List](./)‑objekt tillhör alltid [ListCollection](../listcollection/)‑samlingen.

För att skapa en ny lista, använd Add‑metoderna i [ListCollection](../listcollection/)‑samlingen.

För att ändra formatering av en lista, använd [ListLevel](../listlevel/)‑objekt som finns i [ListLevels](./get_listlevels/)‑samlingen.

För att tillämpa eller ta bort listformatering från ett stycke, använd [ListFormat](../listformat/).

## Exempel



Visar hur man arbetar med listnivåer.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

ASSERT_FALSE(builder->get_ListFormat()->get_IsListItem());

// En lista låter oss organisera och dekorera uppsättningar av stycken med prefixsymboler och indrag.
// Vi kan skapa nästlade listor genom att öka indragnivån.
// Vi kan börja och avsluta en lista genom att använda en dokumentbyggares egenskap "ListFormat".
// Varje stycke som vi lägger till mellan en listas början och slut blir ett objekt i listan.
// Nedan finns två typer av listor som vi kan skapa med en dokumentbyggare.
// 1 -  En numrerad lista:
// Numrerade listor skapar en logisk ordning för sina stycken genom att numrera varje objekt.
builder->get_ListFormat()->set_List(doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberDefault));

ASSERT_TRUE(builder->get_ListFormat()->get_IsListItem());

// Genom att sätta egenskapen "ListLevelNumber" kan vi öka listnivån
// för att påbörja en självständig underlista vid det aktuella listobjektet.
// Microsoft Word-listmallen som heter "NumberDefault" använder siffror för att skapa listnivåer för den första listnivån.
// Djupare listnivåer använder bokstäver och gemena romerska siffror.
for (int32_t i = 0; i < 9; i++)
{
    builder->get_ListFormat()->set_ListLevelNumber(i);
    builder->Writeln(System::String(u"Level ") + i);
}

// 2 -  En punktlista:
// Denna lista kommer att applicera ett indrag och en punktsymbol ("•") före varje stycke.
// Djupare nivåer i denna lista kommer att använda olika symboler, såsom "■" och "○".
builder->get_ListFormat()->set_List(doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::BulletDefault));

for (int32_t i = 0; i < 9; i++)
{
    builder->get_ListFormat()->set_ListLevelNumber(i);
    builder->Writeln(System::String(u"Level ") + i);
}

// Vi kan inaktivera listformatering så att inga efterföljande stycken formateras som listor genom att avaktivera flaggan "List".
builder->get_ListFormat()->set_List(nullptr);

ASSERT_FALSE(builder->get_ListFormat()->get_IsListItem());

doc->Save(get_ArtifactsDir() + u"Lists.SpecifyListLevel.docx");
```


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


Visar hur man startar om numrering i en lista genom att kopiera en lista.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// En lista låter oss organisera och dekorera uppsättningar av stycken med prefixsymboler och indrag.
// Vi kan skapa nästlade listor genom att öka indragnivån.
// Vi kan börja och avsluta en lista genom att använda en dokumentbyggares egenskap "ListFormat".
// Varje stycke som vi lägger till mellan en listas början och slut blir ett objekt i listan.
// Skapa en lista från en Microsoft Word-mall och anpassa dess första listnivå.
System::SharedPtr<Aspose::Words::Lists::List> list1 = doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberArabicParenthesis);
list1->get_ListLevels()->idx_get(0)->get_Font()->set_Color(System::Drawing::Color::get_Red());
list1->get_ListLevels()->idx_get(0)->set_Alignment(Aspose::Words::Lists::ListLevelAlignment::Right);

// Applicera vår lista på några stycken.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"List 1 starts below:");
builder->get_ListFormat()->set_List(list1);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");
builder->get_ListFormat()->RemoveNumbers();

// Vi kan lägga till en kopia av en befintlig lista till dokumentets listsamling
// för att skapa en liknande lista utan att ändra originalet.
System::SharedPtr<Aspose::Words::Lists::List> list2 = doc->get_Lists()->AddCopy(list1);
list2->get_ListLevels()->idx_get(0)->get_Font()->set_Color(System::Drawing::Color::get_Blue());
list2->get_ListLevels()->idx_get(0)->set_StartAt(10);

// Applicera den andra listan på nya stycken.
builder->Writeln(u"List 2 starts below:");
builder->get_ListFormat()->set_List(list2);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");
builder->get_ListFormat()->RemoveNumbers();

doc->Save(get_ArtifactsDir() + u"Lists.RestartNumberingUsingListCopy.docx");
```

## Se även

* Namespace [Aspose::Words::Lists](../)
* Library [Aspose.Words for C++](../../)
