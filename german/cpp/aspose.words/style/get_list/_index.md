---
title: "Aspose::Words::Style::get_List‑Methode"
linktitle: "get_List"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Style::get_List‑Methode. Gibt die Liste zurück, die die Formatierung dieses Listenstils in C++ definiert."
type: docs
weight: 12000
url: /de/cpp/aspose.words/style/get_list/
---
## Style::get_List method


Ruft die Liste ab, die die Formatierung dieses Listenstils definiert.

```cpp
System::SharedPtr<Aspose::Words::Lists::List> Aspose::Words::Style::get_List()
```

## Hinweise


Diese Eigenschaft ist nur für Listenstile gültig. Für andere Stiltypen gibt diese Eigenschaft **null** zurück.

## Beispiele



Zeigt, wie man einen List‑Stil erstellt und in einem Dokument verwendet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Eine Liste ermöglicht es uns, Absatzgruppen mit Präfixsymbolen und Einzügen zu organisieren und zu formatieren.
// Wir können verschachtelte Listen erstellen, indem wir die Einzugsebene erhöhen.
// Wir können eine Liste beginnen und beenden, indem wir die "ListFormat"-Eigenschaft eines Document Builders verwenden.
// Jeder Absatz, den wir zwischen dem Beginn und dem Ende einer Liste einfügen, wird zu einem Element in der Liste.
// Wir können ein komplettes List‑Objekt innerhalb eines Stils enthalten.
System::SharedPtr<Aspose::Words::Style> listStyle = doc->get_Styles()->Add(Aspose::Words::StyleType::List, u"MyListStyle");

System::SharedPtr<Aspose::Words::Lists::List> list1 = listStyle->get_List();

ASSERT_TRUE(list1->get_IsListStyleDefinition());
ASSERT_FALSE(list1->get_IsListStyleReference());
ASSERT_TRUE(list1->get_IsMultiLevel());
ASPOSE_ASSERT_EQ(listStyle, list1->get_Style());

// Ändern Sie das Aussehen aller Listenebenen in unserer Liste.
for (auto&& level : list1->get_ListLevels())
{
    level->get_Font()->set_Name(u"Verdana");
    level->get_Font()->set_Color(System::Drawing::Color::get_Blue());
    level->get_Font()->set_Bold(true);
}

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Using list style first time:");

// Erstellen Sie eine weitere Liste aus einer Liste innerhalb eines Stils.
System::SharedPtr<Aspose::Words::Lists::List> list2 = doc->get_Lists()->Add(listStyle);

ASSERT_FALSE(list2->get_IsListStyleDefinition());
ASSERT_TRUE(list2->get_IsListStyleReference());
ASPOSE_ASSERT_EQ(listStyle, list2->get_Style());

// Fügen Sie einige Listenelemente hinzu, die unsere Liste formatieren wird.
builder->get_ListFormat()->set_List(list2);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");
builder->get_ListFormat()->RemoveNumbers();

builder->Writeln(u"Using list style second time:");

// Erstellen und wenden Sie eine weitere Liste basierend auf dem Listenstil an.
System::SharedPtr<Aspose::Words::Lists::List> list3 = doc->get_Lists()->Add(listStyle);
builder->get_ListFormat()->set_List(list3);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");
builder->get_ListFormat()->RemoveNumbers();

builder->get_Document()->Save(get_ArtifactsDir() + u"Lists.CreateAndUseListStyle.docx");
```

## Siehe auch

* Class [List](../../../aspose.words.lists/list/)
* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
