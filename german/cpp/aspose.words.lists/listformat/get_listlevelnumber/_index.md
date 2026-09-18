---
title: "Aspose::Words::Lists::ListFormat::get_ListLevelNumber method"
linktitle: "get_ListLevelNumber"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Lists::ListFormat::get_ListLevelNumber method. Liest oder setzt die Listentiefe (0 bis 8) für den Absatz in C++."
type: docs
weight: 7000
url: /de/cpp/aspose.words.lists/listformat/get_listlevelnumber/
---
## ListFormat::get_ListLevelNumber method


Liest oder setzt die Listenebenennummer (0 bis 8) für den Absatz.

```cpp
int32_t Aspose::Words::Lists::ListFormat::get_ListLevelNumber()
```

## Hinweise


In Word-Dokumenten können Listen aus 1 bis 9 Ebenen bestehen, nummeriert von 0 bis 8.

Wirkt nur, wenn die Eigenschaft [List](../get_list/) auf eine gültige Liste verweist.

## Beispiele



Zeigt, wie man Aufzählungs‑ und Nummerierungslisten erstellt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Aspose.Words main advantages are:");

// Eine Liste ermöglicht es uns, Absatzgruppen mit Präfixsymbolen und Einzügen zu organisieren und zu formatieren.
// Wir können verschachtelte Listen erstellen, indem wir die Einzugsebene erhöhen.
// Wir können eine Liste beginnen und beenden, indem wir die "ListFormat"-Eigenschaft eines Document Builders verwenden.
// Jeder Absatz, den wir zwischen dem Beginn und dem Ende einer Liste einfügen, wird zu einem Element in der Liste.
// Unten sind zwei Arten von Listen, die wir mit einem Document Builder erstellen können.
// 1 -  Eine Aufzählungsliste:
// Diese Liste fügt vor jedem Absatz einen Einzug und ein Aufzählungszeichen ("•") ein.
builder->get_ListFormat()->ApplyBulletDefault();
builder->Writeln(u"Great performance");
builder->Writeln(u"High reliability");
builder->Writeln(u"Quality code and working");
builder->Writeln(u"Wide variety of features");
builder->Writeln(u"Easy to understand API");

// Beende die Aufzählungsliste.
builder->get_ListFormat()->RemoveNumbers();

builder->InsertBreak(Aspose::Words::BreakType::ParagraphBreak);
builder->Writeln(u"Aspose.Words allows:");

// 2 -  Eine nummerierte Liste:
// Nummerierte Listen erzeugen eine logische Reihenfolge für ihre Absätze, indem sie jedes Element nummerieren.
builder->get_ListFormat()->ApplyNumberDefault();

// Dieser Absatz ist das erste Element. Das erste Element einer nummerierten Liste hat ein "1." als Listenelementsymbol.
builder->Writeln(u"Opening documents from different formats:");

ASSERT_EQ(0, builder->get_ListFormat()->get_ListLevelNumber());

// Rufen Sie die Methode "ListIndent" auf, um die aktuelle Listentiefe zu erhöhen,
// was eine neue eigenständige Liste mit größerer Einrückung beim aktuellen Element der ersten Listentiefe startet.
builder->get_ListFormat()->ListIndent();

ASSERT_EQ(1, builder->get_ListFormat()->get_ListLevelNumber());

// Dies sind die ersten drei Listenelemente der zweiten Listentiefe, die einen Zähler beibehalten
// unabhängig vom Zähler der ersten Listentiefe. Gemäß dem aktuellen Listenformat,
// haben sie Symbole "a.", "b." und "c.".
builder->Writeln(u"DOC");
builder->Writeln(u"PDF");
builder->Writeln(u"HTML");

// Rufen Sie die Methode "ListOutdent" auf, um zur vorherigen Listentiefe zurückzukehren.
builder->get_ListFormat()->ListOutdent();

ASSERT_EQ(0, builder->get_ListFormat()->get_ListLevelNumber());

// Diese beiden Absätze setzen den Zähler der ersten Listentiefe fort.
// Diese Elemente haben die Symbole "2." und "3."
builder->Writeln(u"Processing documents");
builder->Writeln(u"Saving documents in different formats:");

// Wenn wir die Listentiefe auf ein Niveau erhöhen, zu dem wir bereits zuvor Elemente hinzugefügt haben,
// wird die verschachtelte Liste von der vorherigen getrennt sein und ihre Nummerierung beginnt von vorne.
// Diese Listenelemente haben die Symbole "a.", "b.", "c.", "d." und "e".
builder->get_ListFormat()->ListIndent();
builder->Writeln(u"DOC");
builder->Writeln(u"PDF");
builder->Writeln(u"HTML");
builder->Writeln(u"MHTML");
builder->Writeln(u"Plain text");

// Rücken Sie die Listentiefe erneut zurück.
builder->get_ListFormat()->ListOutdent();
builder->Writeln(u"Doing many other things!");

// Beenden Sie die nummerierte Liste.
builder->get_ListFormat()->RemoveNumbers();

doc->Save(get_ArtifactsDir() + u"Lists.ApplyDefaultBulletsAndNumbers.docx");
```


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

* Class [ListFormat](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
