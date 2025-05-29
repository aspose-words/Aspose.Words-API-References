---
title: ListFormat.IsListItem
linktitle: IsListItem
articleTitle: IsListItem
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die ListFormat-Eigenschaft „IsListItem“ die Struktur Ihres Dokuments verbessert, indem sie Absätze mit Aufzählungszeichen oder Nummerierungen zur besseren Lesbarkeit kennzeichnet.
type: docs
weight: 10
url: /de/net/aspose.words.lists/listformat/islistitem/
---
## ListFormat.IsListItem property

Wahr, wenn auf den Absatz Aufzählungszeichen oder Nummerierungen angewendet wurden.

```csharp
public bool IsListItem { get; }
```

## Beispiele

Zeigt, wie alle Absätze in einem Dokument ausgegeben werden, die Listenelemente sind.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ListFormat.ApplyNumberDefault();
builder.Writeln("Numbered list item 1");
builder.Writeln("Numbered list item 2");
builder.Writeln("Numbered list item 3");
builder.ListFormat.RemoveNumbers();

builder.ListFormat.ApplyBulletDefault();
builder.Writeln("Bulleted list item 1");
builder.Writeln("Bulleted list item 2");
builder.Writeln("Bulleted list item 3");
builder.ListFormat.RemoveNumbers();

NodeCollection paras = doc.GetChildNodes(NodeType.Paragraph, true);

foreach (Paragraph para in paras.OfType<Paragraph>().Where(p => p.ListFormat.IsListItem).ToList())
{ 
    Console.WriteLine($"This paragraph belongs to list ID# {para.ListFormat.List.ListId}, number style \"{para.ListFormat.ListLevel.NumberStyle}\"");
    Console.WriteLine($"\t\"{para.GetText().Trim()}\"");
}
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

* class [ListFormat](../)
* namensraum [Aspose.Words.Lists](../../../aspose.words.lists/)
* Montage [Aspose.Words](../../../)
