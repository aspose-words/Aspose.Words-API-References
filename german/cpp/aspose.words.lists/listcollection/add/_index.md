---
title: "Aspose::Words::Lists::ListCollection::Add Methode"
linktitle: "Add"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Lists::ListCollection::Add Methode. Erstellt eine neue Liste basierend auf einer vordefinierten Vorlage und fügt sie der Sammlung von Listen im Dokument in C++ hinzu."
type: docs
weight: 2000
url: /de/cpp/aspose.words.lists/listcollection/add/
---
## ListCollection::Add(Aspose::Words::Lists::ListTemplate) method


Erstellt eine neue Liste basierend auf einer vordefinierten Vorlage und fügt sie der Listensammlung im Dokument hinzu.

```cpp
System::SharedPtr<Aspose::Words::Lists::List> Aspose::Words::Lists::ListCollection::Add(Aspose::Words::Lists::ListTemplate listTemplate)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| listTemplate | Aspose::Words::Lists::ListTemplate | Die Vorlage der Liste. |

### ReturnValue

Die neu erstellte Liste.
## Hinweise


Aspose.Words-Listenvorlagen entsprechen den 21 Listenvorlagen, die im Dialogfeld Aufzählungszeichen und Nummerierung in Microsoft Word 2003 verfügbar sind.

Alle mit dieser Methode erstellten Listen haben 9 Listenebenen.

## Beispiele



Zeigt, wie man mit Listenebenen arbeitet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

ASSERT_FALSE(builder->get_ListFormat()->get_IsListItem());

// Eine Liste ermöglicht es uns, Absatzgruppen mit Präfixsymbolen und Einzügen zu organisieren und zu formatieren.
// Wir können verschachtelte Listen erstellen, indem wir die Einzugsebene erhöhen.
// Wir können eine Liste beginnen und beenden, indem wir die "ListFormat"-Eigenschaft eines Document Builders verwenden.
// Jeder Absatz, den wir zwischen dem Beginn und dem Ende einer Liste einfügen, wird zu einem Element in der Liste.
// Unten sind zwei Listentypen, die wir mit einem Dokumenten‑Builder erstellen können.
// 1 -  Eine nummerierte Liste:
// Nummerierte Listen erzeugen eine logische Reihenfolge für ihre Absätze, indem sie jedes Element nummerieren.
builder->get_ListFormat()->set_List(doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberDefault));

ASSERT_TRUE(builder->get_ListFormat()->get_IsListItem());

// Durch das Setzen der Eigenschaft "ListLevelNumber" können wir die Listentiefe erhöhen
// um eine eigenständige Unterliste beim aktuellen Listenelement zu beginnen.
// Die Microsoft‑Word-Listenvorlage mit dem Namen "NumberDefault" verwendet Zahlen, um Listenniveaus für das erste Listenniveau zu erstellen.
// Tiefere Listenniveaus verwenden Buchstaben und kleine römische Ziffern.
for (int32_t i = 0; i < 9; i++)
{
    builder->get_ListFormat()->set_ListLevelNumber(i);
    builder->Writeln(System::String(u"Level ") + i);
}

// 2 -  Eine Aufzählungsliste:
// Diese Liste fügt vor jedem Absatz einen Einzug und ein Aufzählungszeichen ("•") ein.
// Tiefere Ebenen dieser Liste verwenden unterschiedliche Symbole, wie "■" und "○".
builder->get_ListFormat()->set_List(doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::BulletDefault));

for (int32_t i = 0; i < 9; i++)
{
    builder->get_ListFormat()->set_ListLevelNumber(i);
    builder->Writeln(System::String(u"Level ") + i);
}

// Wir können die Listformatierung deaktivieren, um nachfolgende Absätze nicht als Listen zu formatieren, indem wir das "List"‑Flag zurücksetzen.
builder->get_ListFormat()->set_List(nullptr);

ASSERT_FALSE(builder->get_ListFormat()->get_IsListItem());

doc->Save(get_ArtifactsDir() + u"Lists.SpecifyListLevel.docx");
```


Zeigt, wie man die Nummerierung in einer Liste durch Kopieren einer Liste neu startet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Eine Liste ermöglicht es uns, Absatzgruppen mit Präfixsymbolen und Einzügen zu organisieren und zu formatieren.
// Wir können verschachtelte Listen erstellen, indem wir die Einzugsebene erhöhen.
// Wir können eine Liste beginnen und beenden, indem wir die "ListFormat"-Eigenschaft eines Document Builders verwenden.
// Jeder Absatz, den wir zwischen dem Beginn und dem Ende einer Liste einfügen, wird zu einem Element in der Liste.
// Erstellen Sie eine Liste aus einer Microsoft‑Word-Vorlage und passen Sie ihr erstes Listenniveau an.
System::SharedPtr<Aspose::Words::Lists::List> list1 = doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberArabicParenthesis);
list1->get_ListLevels()->idx_get(0)->get_Font()->set_Color(System::Drawing::Color::get_Red());
list1->get_ListLevels()->idx_get(0)->set_Alignment(Aspose::Words::Lists::ListLevelAlignment::Right);

// Wenden Sie unsere Liste auf einige Absätze an.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"List 1 starts below:");
builder->get_ListFormat()->set_List(list1);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");
builder->get_ListFormat()->RemoveNumbers();

// Wir können eine Kopie einer bestehenden Liste zur Listensammlung des Dokuments hinzufügen
// um eine ähnliche Liste zu erstellen, ohne das Original zu ändern.
System::SharedPtr<Aspose::Words::Lists::List> list2 = doc->get_Lists()->AddCopy(list1);
list2->get_ListLevels()->idx_get(0)->get_Font()->set_Color(System::Drawing::Color::get_Blue());
list2->get_ListLevels()->idx_get(0)->set_StartAt(10);

// Wenden Sie die zweite Liste auf neue Absätze an.
builder->Writeln(u"List 2 starts below:");
builder->get_ListFormat()->set_List(list2);
builder->Writeln(u"Item 1");
builder->Writeln(u"Item 2");
builder->get_ListFormat()->RemoveNumbers();

doc->Save(get_ArtifactsDir() + u"Lists.RestartNumberingUsingListCopy.docx");
```


Zeigt, wie man eine Liste erstellt, indem man ein neues Listenformat auf eine Sammlung von Absätzen anwendet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Paragraph 1");
builder->Writeln(u"Paragraph 2");
builder->Write(u"Paragraph 3");

System::SharedPtr<Aspose::Words::NodeCollection> paras = doc->GetChildNodes(Aspose::Words::NodeType::Paragraph, true);

ASSERT_EQ(0, paras->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> n)>>([](System::SharedPtr<Aspose::Words::Node> n) -> bool
{
    return (System::ExplicitCast<Aspose::Words::Paragraph>(n))->get_ListFormat()->get_IsListItem();
}))));

System::SharedPtr<Aspose::Words::Lists::List> list = doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberUppercaseLetterDot);

for (auto&& paragraph : System::IterateOver(paras->LINQ_OfType<System::SharedPtr<Aspose::Words::Paragraph> >()))
{
    paragraph->get_ListFormat()->set_List(list);
    paragraph->get_ListFormat()->set_ListLevelNumber(1);
}

ASSERT_EQ(3, paras->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> n)>>([](System::SharedPtr<Aspose::Words::Node> n) -> bool
{
    return (System::ExplicitCast<Aspose::Words::Paragraph>(n))->get_ListFormat()->get_IsListItem();
}))));
```

## Siehe auch

* Class [List](../../list/)
* Enum [ListTemplate](../../listtemplate/)
* Class [ListCollection](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
## ListCollection::Add(const System::SharedPtr\<Aspose::Words::Style\>\&) method


Erstellt eine neue Liste, die einen Listenvorlage‑Stil referenziert, und fügt sie der Listensammlung im Dokument hinzu.

```cpp
System::SharedPtr<Aspose::Words::Lists::List> Aspose::Words::Lists::ListCollection::Add(const System::SharedPtr<Aspose::Words::Style> &listStyle)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| listStyle | const System::SharedPtr\<Aspose::Words::Style\>\& | Der Liststil. |

### ReturnValue

Die neu erstellte Liste.
## Hinweise


Die neu erstellte Liste verweist auf den Liststil. Wenn Sie die Eigenschaften des Liststils ändern, werden sie in den Eigenschaften der Liste widergespiegelt. Umgekehrt, wenn Sie die Eigenschaften der Liste ändern, werden sie in den Eigenschaften des Liststils widergespiegelt.

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

* Class [List](../../list/)
* Class [Style](../../../aspose.words/style/)
* Class [ListCollection](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
