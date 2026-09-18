---
title: "Aspose::Words::Lists::ListFormat::ApplyBulletDefault Methode"
linktitle: "ApplyBulletDefault"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Lists::ListFormat::ApplyBulletDefault Methode. Startet eine neue Standard‑Aufzählungsliste und wendet sie auf den Absatz in C++ an."
type: docs
weight: 2000
url: /de/cpp/aspose.words.lists/listformat/applybulletdefault/
---
## ListFormat::ApplyBulletDefault method


Startet eine neue Standard-Aufzählungsliste und wendet sie auf den Absatz an.

```cpp
void Aspose::Words::Lists::ListFormat::ApplyBulletDefault()
```

## Hinweise


Dies ist eine Kurzmethoden‑Funktion, die eine neue Liste mit der Standard‑Aufzählungsvorlage erstellt, sie auf den Absatz anwendet und die erste Listenebene auswählt.

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

## Siehe auch

* Class [ListFormat](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
