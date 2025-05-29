---
title: ListFormat.List
linktitle: List
articleTitle: List
second_title: Aspose.Words für .NET
description: Verwalten Sie die Struktur Ihres Dokuments mit ListFormat. Erstellen oder definieren Sie ganz einfach Listen für jeden Absatz und verbessern Sie so die Übersichtlichkeit und Lesbarkeit.
type: docs
weight: 20
url: /de/net/aspose.words.lists/listformat/list/
---
## ListFormat.List property

Ruft die Liste ab oder legt sie fest, zu der dieser Absatz gehört.

```csharp
public List List { get; set; }
```

## Bemerkungen

Die Liste, der diese Eigenschaft zugewiesen wird, muss zum aktuellen Dokument gehören.

Die Liste, die dieser Eigenschaft zugewiesen wird, darf keine Listenstildefinition sein.

Wenn Sie diese Eigenschaft auf`null` entfernt Aufzählungszeichen und Nummerierung aus dem Absatz und setzt die Listenebenennummer auf Null. Wenn Sie diese Eigenschaft auf`null` ist gleichbedeutend mit dem Aufruf[`RemoveNumbers`](../removenumbers/).

## Beispiele

Zeigt, wie eine Liste in einer anderen Liste verschachtelt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Eine Liste ermöglicht es uns, Absatzsätze mit Präfixsymbolen und Einzügen zu organisieren und zu dekorieren.
    // Wir können verschachtelte Listen erstellen, indem wir die Einrückungsebene erhöhen.
    // Wir können eine Liste beginnen und beenden, indem wir die Eigenschaft „ListFormat“ eines Dokument-Generators verwenden.
// Jeder Absatz, den wir zwischen dem Anfang und dem Ende einer Liste hinzufügen, wird zu einem Element in der Liste.
// Erstellen Sie eine Gliederungsliste für die Überschriften.
List outlineList = doc.Lists.Add(ListTemplate.OutlineNumbers);
builder.ListFormat.List = outlineList;
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("This is my Chapter 1");

// Erstellen Sie eine nummerierte Liste.
List numberedList = doc.Lists.Add(ListTemplate.NumberDefault);
builder.ListFormat.List = numberedList;
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Normal;
builder.Writeln("Numbered list item 1.");

// Jeder Absatz, der eine Liste enthält, hat dieses Flag.
Assert.True(builder.CurrentParagraph.IsListItem);
Assert.True(builder.ParagraphFormat.IsListItem);

// Erstellen Sie eine Aufzählungsliste.
List bulletedList = doc.Lists.Add(ListTemplate.BulletDefault);
builder.ListFormat.List = bulletedList;
builder.ParagraphFormat.LeftIndent = 72;
builder.Writeln("Bulleted list item 1.");
builder.Writeln("Bulleted list item 2.");
builder.ParagraphFormat.ClearFormatting();

// Zur nummerierten Liste zurückkehren.
builder.ListFormat.List = numberedList;
builder.Writeln("Numbered list item 2.");
builder.Writeln("Numbered list item 3.");

// Zur Gliederungsliste zurückkehren.
builder.ListFormat.List = outlineList;
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("This is my Chapter 2");

builder.ParagraphFormat.ClearFormatting();

builder.Document.Save(ArtifactsDir + "Lists.NestedLists.docx");
```

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

### Siehe auch

* class [List](../../list/)
* class [ListFormat](../)
* namensraum [Aspose.Words.Lists](../../../aspose.words.lists/)
* Montage [Aspose.Words](../../../)
