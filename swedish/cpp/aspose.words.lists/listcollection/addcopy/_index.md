---
title: "Aspose::Words::Lists::ListCollection::AddCopy method"
linktitle: "AddCopy"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Lists::ListCollection::AddCopy method. Skapar en ny lista genom att kopiera den angivna listan och lägga till den i samlingen av listor i dokumentet i C++."
type: docs
weight: 3000
url: /sv/cpp/aspose.words.lists/listcollection/addcopy/
---
## ListCollection::AddCopy method


Skapar en ny lista genom att kopiera den angivna listan och lägga till den i samlingen av listor i dokumentet.

```cpp
System::SharedPtr<Aspose::Words::Lists::List> Aspose::Words::Lists::ListCollection::AddCopy(const System::SharedPtr<Aspose::Words::Lists::List> &srcList)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| srcList | const System::SharedPtr\<Aspose::Words::Lists::List\>\& | Källistan att kopiera från. |

### ReturnValue

Den nyss skapade listan.
## Anmärkningar


Källistan kan komma från vilket dokument som helst. Om källistan tillhör ett annat dokument skapas en kopia av listan och läggs till i det aktuella dokumentet.

Om källistan är en referens till eller en definition av en liststil är den nyss skapade listan inte relaterad till den ursprungliga liststilen.

## Exempel



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

* Class [List](../../list/)
* Class [ListCollection](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
