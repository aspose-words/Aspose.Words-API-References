---
title: ListFormat.ListLevelNumber
linktitle: ListLevelNumber
articleTitle: ListLevelNumber
second_title: Aspose.Words für .NET
description: Entdecken Sie die ListFormat-Eigenschaft „ListLevelNumber“ und verwalten Sie mühelos Absatzlistenebenen von 0 bis 8 für eine verbesserte Dokumentorganisation und Übersichtlichkeit.
type: docs
weight: 40
url: /de/net/aspose.words.lists/listformat/listlevelnumber/
---
## ListFormat.ListLevelNumber property

Ruft die Listenebenennummer (0 bis 8) für den Absatz ab oder legt sie fest.

```csharp
public int ListLevelNumber { get; set; }
```

## Bemerkungen

In Word-Dokumenten können Listen aus 1 oder 9 Ebenen bestehen, die von 0 bis 8 nummeriert sind.

Wirkt sich nur aus, wenn[`List`](../list/) Die Eigenschaft ist so eingestellt, dass sie auf eine gültige Liste verweist.

## Beispiele

Zeigt, wie mit Listenebenen gearbeitet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.False(builder.ListFormat.IsListItem);

// Eine Liste ermöglicht es uns, Absatzsätze mit Präfixsymbolen und Einzügen zu organisieren und zu dekorieren.
    // Wir können verschachtelte Listen erstellen, indem wir die Einrückungsebene erhöhen.
    // Wir können eine Liste beginnen und beenden, indem wir die Eigenschaft „ListFormat“ eines Dokument-Generators verwenden.
// Jeder Absatz, den wir zwischen dem Anfang und dem Ende einer Liste hinzufügen, wird zu einem Element in der Liste.
// Unten sind zwei Arten von Listen, die wir mit einem Dokumentgenerator erstellen können.
// 1 - Eine nummerierte Liste:
// Nummerierte Listen erstellen eine logische Reihenfolge ihrer Absätze, indem sie jedes Element nummerieren.
builder.ListFormat.List = doc.Lists.Add(ListTemplate.NumberDefault);

Assert.True(builder.ListFormat.IsListItem);

// Durch Setzen der Eigenschaft „ListLevelNumber“ können wir die Listenebene erhöhen
// um eine in sich geschlossene Unterliste beim aktuellen Listenelement zu beginnen.
// Die Microsoft Word-Listenvorlage mit dem Namen „NumberDefault“ verwendet Zahlen, um Listenebenen für die erste Listenebene zu erstellen.
    // Tiefere Listenebenen verwenden Buchstaben und römische Ziffern in Kleinbuchstaben.
for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// 2 - Eine Aufzählungsliste:
// Diese Liste wendet vor jedem Absatz einen Einzug und ein Aufzählungszeichen („•“) an.
// Tiefere Ebenen dieser Liste verwenden andere Symbole, wie „■“ und „○“.
builder.ListFormat.List = doc.Lists.Add(ListTemplate.BulletDefault);

for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// Wir können die Listenformatierung deaktivieren, um nachfolgende Absätze nicht als Listen zu formatieren, indem wir das Flag „Liste“ deaktivieren.
builder.ListFormat.List = null;

Assert.False(builder.ListFormat.IsListItem);

doc.Save(ArtifactsDir + "Lists.SpecifyListLevel.docx");
```

Zeigt, wie Aufzählungs- und nummerierte Listen erstellt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Aspose.Words main advantages are:");

// Eine Liste ermöglicht es uns, Absatzsätze mit Präfixsymbolen und Einzügen zu organisieren und zu dekorieren.
    // Wir können verschachtelte Listen erstellen, indem wir die Einrückungsebene erhöhen.
    // Wir können eine Liste beginnen und beenden, indem wir die Eigenschaft „ListFormat“ eines Dokument-Generators verwenden.
// Jeder Absatz, den wir zwischen dem Anfang und dem Ende einer Liste hinzufügen, wird zu einem Element in der Liste.
// Unten sind zwei Arten von Listen, die wir mit einem Dokumentgenerator erstellen können.
// 1 - Eine Aufzählungsliste:
// Diese Liste wendet vor jedem Absatz einen Einzug und ein Aufzählungszeichen („•“) an.
builder.ListFormat.ApplyBulletDefault();
builder.Writeln("Great performance");
builder.Writeln("High reliability");
builder.Writeln("Quality code and working");
builder.Writeln("Wide variety of features");
builder.Writeln("Easy to understand API");

// Beenden Sie die Aufzählungsliste.
builder.ListFormat.RemoveNumbers();

builder.InsertBreak(BreakType.ParagraphBreak);
builder.Writeln("Aspose.Words allows:");

// 2 - Eine nummerierte Liste:
// Nummerierte Listen erstellen eine logische Reihenfolge ihrer Absätze, indem sie jedes Element nummerieren.
builder.ListFormat.ApplyNumberDefault();

// Dieser Absatz ist das erste Element. Das erste Element einer nummerierten Liste hat eine „1.“ als Listenelementsymbol.
builder.Writeln("Opening documents from different formats:");

Assert.AreEqual(0, builder.ListFormat.ListLevelNumber);

// Rufen Sie die Methode „ListIndent“ auf, um die aktuelle Listenebene zu erhöhen,
// Dadurch wird eine neue, in sich geschlossene Liste mit einer tieferen Einrückung beim aktuellen Element der ersten Listenebene gestartet.
builder.ListFormat.ListIndent();

Assert.AreEqual(1, builder.ListFormat.ListLevelNumber);

// Dies sind die ersten drei Listenelemente der zweiten Listenebene, die eine Zählung verwalten
// unabhängig von der Anzahl der ersten Listenebenen. Je nach aktuellem Listenformat
// Sie werden die Symbole „a.“, „b.“ und „c.“ haben.
builder.Writeln("DOC");
builder.Writeln("PDF");
builder.Writeln("HTML");

// Rufen Sie die Methode „ListOutdent“ auf, um zur vorherigen Listenebene zurückzukehren.
builder.ListFormat.ListOutdent();

Assert.AreEqual(0, builder.ListFormat.ListLevelNumber);

// Diese beiden Absätze setzen die Zählung der ersten Listenebene fort.
// Diese Elemente haben die Symbole „2.“ und „3.“
builder.Writeln("Processing documents");
builder.Writeln("Saving documents in different formats:");

// Wenn wir die Listenebene auf eine Ebene erhöhen, zu der wir zuvor Elemente hinzugefügt haben,
    // Die verschachtelte Liste wird von der vorherigen getrennt und ihre Nummerierung beginnt von vorne.
// Diese Listenelemente haben die Symbole „a.“, „b.“, „c.“, „d.“ und „e.“
builder.ListFormat.ListIndent();
builder.Writeln("DOC");
builder.Writeln("PDF");
builder.Writeln("HTML");
builder.Writeln("MHTML");
builder.Writeln("Plain text");

// Die Listenebene erneut ausrücken.
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
