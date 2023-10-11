---
title: ListFormat.List
second_title: Aspose.Words für .NET-API-Referenz
description: ListFormat eigendom. Ruft die Liste ab zu der dieser Absatz gehört oder legt sie fest.
type: docs
weight: 20
url: /de/net/aspose.words.lists/listformat/list/
---
## ListFormat.List property

Ruft die Liste ab, zu der dieser Absatz gehört, oder legt sie fest.

```csharp
public List List { get; set; }
```

### Bemerkungen

Die Liste, die dieser Eigenschaft zugewiesen wird, muss zum aktuellen Dokument gehören.

Die Liste, die dieser Eigenschaft zugewiesen wird, darf keine Listenstildefinition sein.

Diese Eigenschaft festlegen auf`Null` Entfernt Aufzählungszeichen und Nummerierungen aus „paragraph “ und setzt die Nummer der Listenebene auf Null. Diese Eigenschaft festlegen auf`Null` entspricht dem Aufruf[`RemoveNumbers`](../removenumbers/).

### Beispiele

Zeigt, wie eine Liste in einer anderen Liste verschachtelt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Eine Liste ermöglicht es uns, Absätze mit Präfixsymbolen und Einzügen zu organisieren und zu dekorieren.
 // Wir können verschachtelte Listen erstellen, indem wir die Einrückungsebene erhöhen.
 // Wir können eine Liste beginnen und beenden, indem wir die „ListFormat“-Eigenschaft eines Document Builders verwenden.
// Jeder Absatz, den wir zwischen dem Anfang und dem Ende einer Liste hinzufügen, wird zu einem Element in der Liste.
// Eine Übersichtsliste für die Überschriften erstellen.
List outlineList = doc.Lists.Add(ListTemplate.OutlineNumbers);
builder.ListFormat.List = outlineList;
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("This is my Chapter 1");

// Erstelle eine nummerierte Liste.
List numberedList = doc.Lists.Add(ListTemplate.NumberDefault);
builder.ListFormat.List = numberedList;
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Normal;
builder.Writeln("Numbered list item 1.");

// Jeder Absatz, der eine Liste enthält, hat dieses Flag.
Assert.True(builder.CurrentParagraph.IsListItem);
Assert.True(builder.ParagraphFormat.IsListItem);

// Eine Liste mit Aufzählungszeichen erstellen.
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

// Eine Liste ermöglicht es uns, Absätze mit Präfixsymbolen und Einzügen zu organisieren und zu dekorieren.
 // Wir können verschachtelte Listen erstellen, indem wir die Einrückungsebene erhöhen.
 // Wir können eine Liste beginnen und beenden, indem wir die „ListFormat“-Eigenschaft eines Document Builders verwenden.
// Jeder Absatz, den wir zwischen dem Anfang und dem Ende einer Liste hinzufügen, wird zu einem Element in der Liste.
// Nachfolgend finden Sie zwei Arten von Listen, die wir mit einem Document Builder erstellen können.
// 1 – Eine nummerierte Liste:
// Nummerierte Listen erstellen eine logische Reihenfolge für ihre Absätze, indem sie jedes Element nummerieren.
builder.ListFormat.List = doc.Lists.Add(ListTemplate.NumberDefault);

Assert.True(builder.ListFormat.IsListItem);

// Durch Setzen der Eigenschaft „ListLevelNumber“ können wir die Listenebene erhöhen
// um eine eigenständige Unterliste beim aktuellen Listenelement zu beginnen.
// Die Microsoft Word-Listenvorlage namens „NumberDefault“ verwendet Zahlen, um Listenebenen für die erste Listenebene zu erstellen.
 // Tiefere Listenebenen verwenden Buchstaben und römische Kleinbuchstaben.
for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// 2 – Eine Liste mit Aufzählungszeichen:
// Diese Liste fügt vor jedem Absatz einen Einzug und ein Aufzählungszeichen („•“) ein.
// Auf tieferen Ebenen dieser Liste werden andere Symbole verwendet, z. B. „■“ und „○“.
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
* namensraum [Aspose.Words.Lists](../../listformat/)
* Montage [Aspose.Words](../../../)


