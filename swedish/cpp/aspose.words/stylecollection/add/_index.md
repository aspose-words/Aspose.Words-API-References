---
title: "Aspose::Words::StyleCollection::Add metod"
linktitle: "Add"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::StyleCollection::Add metod. Skapar en ny användardefinierad stil och lägger till den i samlingen i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words/stylecollection/add/
---
## StyleCollection::Add method


Skapar en ny användardefinierad stil och lägger till den i samlingen.

```cpp
System::SharedPtr<Aspose::Words::Style> Aspose::Words::StyleCollection::Add(Aspose::Words::StyleType type, const System::String &name)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| type | Aspose::Words::StyleType | Ett [StyleType](../../styletype/)‑värde som specificerar typen av stil att skapa. |
| namn | const System::String\& | Skiftlägeskänsligt namn på den stil som ska skapas. |
## Anmärkningar


Du kan skapa tecken-, stycke- eller liststil.

När du skapar en liststil skapas stilen med standardformatering för numrerade listor (1 \\ a \\ i).

Kastar ett undantag om en stil med detta namn redan finns.

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


Visar hur man lägger till en [Style](../../style/) i ett dokuments stilsamling.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::StyleCollection> styles = doc->get_Styles();
// Ställ in standardparametrar för nya stilar som vi senare kan lägga till i denna samling.
styles->get_DefaultFont()->set_Name(u"Courier New");
// Om vi lägger till en stil av typen "StyleType.Paragraph" kommer samlingen att tillämpa värdena av
// dess egenskap "DefaultParagraphFormat" på stilens egenskap "ParagraphFormat".
styles->get_DefaultParagraphFormat()->set_FirstLineIndent(15.0);
// Lägg till en stil och verifiera sedan att den har standardinställningarna.
styles->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle");

ASSERT_EQ(u"Courier New", styles->idx_get(4)->get_Font()->get_Name());
ASPOSE_ASSERT_EQ(15.0, styles->idx_get(u"MyStyle")->get_ParagraphFormat()->get_FirstLineIndent());
```

## Se även

* Class [Style](../../style/)
* Enum [StyleType](../../styletype/)
* Class [StyleCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
