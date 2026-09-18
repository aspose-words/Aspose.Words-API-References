---
title: "Aspose::Words::Lists::ListFormat::get_List Methode"
linktitle: "get_List"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Lists::ListFormat::get_List Methode. Ruft die Liste ab, zu der dieser Absatz gehört, oder legt sie fest in C++."
type: docs
weight: 5000
url: /de/cpp/aspose.words.lists/listformat/get_list/
---
## ListFormat::get_List method


Liest oder setzt die Liste, zu der dieser Absatz gehört.

```cpp
System::SharedPtr<Aspose::Words::Lists::List> Aspose::Words::Lists::ListFormat::get_List()
```

## Hinweise


Die Liste, die dieser Eigenschaft zugewiesen wird, muss zum aktuellen Dokument gehören.

Die Liste, die dieser Eigenschaft zugewiesen wird, darf keine Listenvorlagendefinition sein.

Das Setzen dieser Eigenschaft auf **null** entfernt Aufzählungszeichen und Nummerierung aus dem Absatz und setzt die Listenebenennummer auf Null. Das Setzen dieser Eigenschaft auf **null** ist gleichbedeutend mit dem Aufruf von [RemoveNumbers](../removenumbers/).

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


Zeigt, wie man eine Liste in einer anderen Liste verschachtelt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Eine Liste ermöglicht es uns, Absatzgruppen mit Präfixsymbolen und Einzügen zu organisieren und zu formatieren.
// Wir können verschachtelte Listen erstellen, indem wir die Einzugsebene erhöhen.
// Wir können eine Liste beginnen und beenden, indem wir die "ListFormat"-Eigenschaft eines Document Builders verwenden.
// Jeder Absatz, den wir zwischen dem Beginn und dem Ende einer Liste einfügen, wird zu einem Element in der Liste.
// Erstelle eine Gliederungsliste für die Überschriften.
System::SharedPtr<Aspose::Words::Lists::List> outlineList = doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::OutlineNumbers);
builder->get_ListFormat()->set_List(outlineList);
builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading1);
builder->Writeln(u"This is my Chapter 1");

// Erstelle eine nummerierte Liste.
System::SharedPtr<Aspose::Words::Lists::List> numberedList = doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberDefault);
builder->get_ListFormat()->set_List(numberedList);
builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Normal);
builder->Writeln(u"Numbered list item 1.");

// Jeder Absatz, der eine Liste enthält, hat dieses Flag.
ASSERT_TRUE(builder->get_CurrentParagraph()->get_IsListItem());
ASSERT_TRUE(builder->get_ParagraphFormat()->get_IsListItem());

// Erstelle eine Aufzählungsliste.
System::SharedPtr<Aspose::Words::Lists::List> bulletedList = doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::BulletDefault);
builder->get_ListFormat()->set_List(bulletedList);
builder->get_ParagraphFormat()->set_LeftIndent(72);
builder->Writeln(u"Bulleted list item 1.");
builder->Writeln(u"Bulleted list item 2.");
builder->get_ParagraphFormat()->ClearFormatting();

// Zurück zur nummerierten Liste.
builder->get_ListFormat()->set_List(numberedList);
builder->Writeln(u"Numbered list item 2.");
builder->Writeln(u"Numbered list item 3.");

// Zurück zur Gliederungsliste.
builder->get_ListFormat()->set_List(outlineList);
builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading1);
builder->Writeln(u"This is my Chapter 2");

builder->get_ParagraphFormat()->ClearFormatting();

builder->get_Document()->Save(get_ArtifactsDir() + u"Lists.NestedLists.docx");
```

## Siehe auch

* Class [List](../../list/)
* Class [ListFormat](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
