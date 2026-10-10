---
title: "Aspose::Words::Lists::List::get_Style method"
linktitle: "get_Style"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Lists::List::get_Style metod. Hämtar liststilen som denna lista refererar till eller definierar i C++."
type: docs
weight: 11000
url: /sv/cpp/aspose.words.lists/list/get_style/
---
## List::get_Style method


Hämtar liststilen som den här listan refererar till eller definierar.

```cpp
System::SharedPtr<Aspose::Words::Style> Aspose::Words::Lists::List::get_Style()
```

## Anmärkningar


Om denna lista inte är associerad med en liststil, kommer egenskapen att returnera **null**.

En lista kan vara en referens till en liststil, i så fall kommer [IsListStyleReference](../get_isliststylereference/) att vara **true**.

En lista kan vara en definition av en liststil, i så fall kommer [IsListStyleDefinition](../get_isliststyledefinition/) att vara **true**. En sådan lista kan inte appliceras direkt på stycken i dokumentet.

## Exempel



Visar hur man skapar en liststil och använder den i ett dokument.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// En lista låter oss organisera och dekorera uppsättningar av stycken med prefixsymboler och indrag.
// Vi kan skapa nästlade listor genom att öka indragnivån.
// Vi kan börja och avsluta en lista genom att använda en dokumentbyggares egenskap "ListFormat".
// Varje stycke som vi lägger till mellan en listas början och slut blir ett objekt i listan.
// Vi kan innehålla ett helt List-objekt inom en stil.
System::SharedPtr<Aspose::Words::Style> listStyle = doc->get_Styles()->Add(Aspose::Words::StyleType::List, u"MyListStyle");

System::SharedPtr<Aspose::Words::Lists::List> list1 = listStyle->get_List();

ASSERT_TRUE(list1->get_IsListStyleDefinition());
ASSERT_FALSE(list1->get_IsListStyleReference());
ASSERT_TRUE(list1->get_IsMultiLevel());
ASPOSE_ASSERT_EQ(listStyle, list1->get_Style());

// Ändra utseendet på alla listnivåer i vår lista.
for (auto&& level : list1->get_ListLevels())
{
    level->get_Font()->set_Name(u"Verdana");
    level->get_Font()->set_Color(System::Drawing::Color::get_Blue());
    level->get_Font()->set_Bold(true);
}

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Using list style first time:");

// Skapa en annan lista från en lista inom en stil.
System::SharedPtr<Aspose::Words::Lists::List> list2 = doc->get_Lists()->Add(listStyle);

ASSERT_FALSE(list2->get_IsListStyleDefinition());
ASSERT_TRUE(list2->get_IsListStyleReference());
ASPOSE_ASSERT_EQ(listStyle, list2->get_Style());

// Lägg till några listobjekt som vår lista kommer att formatera.
builder->get_ListFormat()->set_List(list2);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");
builder->get_ListFormat()->RemoveNumbers();

builder->Writeln(u"Using list style second time:");

// Skapa och tillämpa en annan lista baserad på liststilen.
System::SharedPtr<Aspose::Words::Lists::List> list3 = doc->get_Lists()->Add(listStyle);
builder->get_ListFormat()->set_List(list3);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");
builder->get_ListFormat()->RemoveNumbers();

builder->get_Document()->Save(get_ArtifactsDir() + u"Lists.CreateAndUseListStyle.docx");
```

## Se även

* Class [Style](../../../aspose.words/style/)
* Class [List](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
