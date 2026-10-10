---
title: "Aspose::Words::DocumentBase::get_Lists Methode"
linktitle: "get_Lists"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::DocumentBase::get_Lists Methode. Bietet Zugriff auf die im Dokument verwendete Listformatierung in C++."
type: docs
weight: 5000
url: /de/cpp/aspose.words/documentbase/get_lists/
---
## DocumentBase::get_Lists method


Stellt Zugriff auf die im Dokument verwendete Listformatierung bereit.

```cpp
System::SharedPtr<Aspose::Words::Lists::ListCollection> Aspose::Words::DocumentBase::get_Lists() const
```

## Hinweise


Weitere Informationen finden Sie in der Beschreibung der Klasse [ListCollection](../../../aspose.words.lists/listcollection/).

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

## Siehe auch

* Class [ListCollection](../../../aspose.words.lists/listcollection/)
* Class [DocumentBase](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
