---
title: ListFormat.ApplyBulletDefault
linktitle: ApplyBulletDefault
articleTitle: ApplyBulletDefault
second_title: Aspose.Words für .NET
description: ListFormat ApplyBulletDefault methode. Startet eine neue Standardliste mit Aufzählungszeichen und wendet sie auf den Absatz an in C#.
type: docs
weight: 50
url: /de/net/aspose.words.lists/listformat/applybulletdefault/
---
## ListFormat.ApplyBulletDefault method

Startet eine neue Standardliste mit Aufzählungszeichen und wendet sie auf den Absatz an.

```csharp
public void ApplyBulletDefault()
```

## Bemerkungen

Hierbei handelt es sich um eine Verknüpfungsmethode, die mithilfe der Standardvorlage „bulleted “ eine neue Liste erstellt, diese auf den Absatz anwendet und die 1. Listenebene auswählt.

## Beispiele

Zeigt, wie Aufzählungslisten und nummerierte Listen erstellt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Aspose.Words main advantages are:");

// Eine Liste ermöglicht es uns, Absätze mit Präfixsymbolen und Einzügen zu organisieren und zu dekorieren.
 // Wir können verschachtelte Listen erstellen, indem wir die Einrückungsebene erhöhen.
 // Wir können eine Liste beginnen und beenden, indem wir die „ListFormat“-Eigenschaft eines Document Builders verwenden.
// Jeder Absatz, den wir zwischen dem Anfang und dem Ende einer Liste hinzufügen, wird zu einem Element in der Liste.
// Nachfolgend finden Sie zwei Arten von Listen, die wir mit einem Document Builder erstellen können.
// 1 – Eine Liste mit Aufzählungszeichen:
// Diese Liste fügt vor jedem Absatz einen Einzug und ein Aufzählungszeichen („•“) ein.
builder.ListFormat.ApplyBulletDefault();
builder.Writeln("Great performance");
builder.Writeln("High reliability");
builder.Writeln("Quality code and working");
builder.Writeln("Wide variety of features");
builder.Writeln("Easy to understand API");

// Beende die Aufzählungsliste.
builder.ListFormat.RemoveNumbers();

builder.InsertBreak(BreakType.ParagraphBreak);
builder.Writeln("Aspose.Words allows:");

// 2 - Eine nummerierte Liste:
// Nummerierte Listen erstellen eine logische Reihenfolge für ihre Absätze, indem sie jedes Element nummerieren.
builder.ListFormat.ApplyNumberDefault();

// Dieser Absatz ist das erste Element. Das erste Element einer nummerierten Liste hat eine „1“. als Listenelementsymbol.
builder.Writeln("Opening documents from different formats:");

Assert.AreEqual(0, builder.ListFormat.ListLevelNumber);

// Rufen Sie die Methode „ListIndent“ auf, um die aktuelle Listenebene zu erhöhen,
// wodurch eine neue in sich geschlossene Liste mit einem tieferen Einzug beim aktuellen Element der ersten Listenebene beginnt.
builder.ListFormat.ListIndent();

Assert.AreEqual(1, builder.ListFormat.ListLevelNumber);

// Dies sind die ersten drei Listenelemente der zweiten Listenebene, die gezählt werden
// unabhängig von der Anzahl der ersten Listenebene. Gemäß dem aktuellen Listenformat
// Sie werden die Symbole „a“, „b“ und „c“ haben.
builder.Writeln("DOC");
builder.Writeln("PDF");
builder.Writeln("HTML");

// Rufen Sie die Methode „ListOutdent“ auf, um zur vorherigen Listenebene zurückzukehren.
builder.ListFormat.ListOutdent();

Assert.AreEqual(0, builder.ListFormat.ListLevelNumber);

// Diese beiden Absätze führen die Zählung der ersten Listenebene fort.
// Diese Elemente haben die Symbole „2.“ und „3“.
builder.Writeln("Processing documents");
builder.Writeln("Saving documents in different formats:");

// Wenn wir die Listenebene auf eine Ebene erhöhen, zu der wir zuvor Elemente hinzugefügt haben,
 // Die verschachtelte Liste ist von der vorherigen getrennt und ihre Nummerierung beginnt von vorne.
// Diese Listenelemente enthalten die Symbole „a“, „b“, „c“, „d“ und „e“.
builder.ListFormat.ListIndent();
builder.Writeln("DOC");
builder.Writeln("PDF");
builder.Writeln("HTML");
builder.Writeln("MHTML");
builder.Writeln("Plain text");

// Listenebene erneut ausrücken.
builder.ListFormat.ListOutdent();
builder.Writeln("Doing many other things!");

// Beende die nummerierte Liste.
builder.ListFormat.RemoveNumbers();

doc.Save(ArtifactsDir + "Lists.ApplyDefaultBulletsAndNumbers.docx");
```

### Siehe auch

* class [ListFormat](../)
* namensraum [Aspose.Words.Lists](../../../aspose.words.lists/)
* Montage [Aspose.Words](../../../)
