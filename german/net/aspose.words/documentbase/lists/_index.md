---
title: DocumentBase.Lists
second_title: Aspose.Words für .NET-API-Referenz
description: DocumentBase eigendom. Bietet Zugriff auf die im Dokument verwendete Listenformatierung.
type: docs
weight: 40
url: /de/net/aspose.words/documentbase/lists/
---
## DocumentBase.Lists property

Bietet Zugriff auf die im Dokument verwendete Listenformatierung.

```csharp
public ListCollection Lists { get; }
```

### Bemerkungen

Weitere Informationen finden Sie in der Beschreibung der[`ListCollection`](../../../aspose.words.lists/listcollection/) Klasse.

### Beispiele

Zeigt, wie mit Listenebenen gearbeitet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.False(builder.ListFormat.IsListItem);

// Eine Liste ermöglicht es uns, Sätze von Absätzen mit Präfixsymbolen und Einzügen zu organisieren und zu dekorieren.
// Wir können verschachtelte Listen erstellen, indem wir die Einrückungsebene erhöhen. 
// Wir können eine Liste beginnen und beenden, indem wir die "ListFormat"-Eigenschaft eines Dokumentenerstellers verwenden. 
// Jeder Absatz, den wir zwischen dem Anfang und dem Ende einer Liste hinzufügen, wird zu einem Element in der Liste.
// Unten sind zwei Arten von Listen, die wir mit einem Document Builder erstellen können.
// 1 - Eine nummerierte Liste:
// Nummerierte Listen schaffen eine logische Reihenfolge für ihre Absätze, indem sie jedes Element nummerieren.
builder.ListFormat.List = doc.Lists.Add(ListTemplate.NumberDefault);

Assert.True(builder.ListFormat.IsListItem);

// Durch Setzen der Eigenschaft "ListLevelNumber" können wir die Listenebene erhöhen
// um eine eigenständige Unterliste am aktuellen Listenelement zu beginnen.
// Die Microsoft Word-Listenvorlage mit dem Namen "NumberDefault" verwendet Zahlen, um Listenebenen für die erste Listenebene zu erstellen.
// Tiefere Listenebenen verwenden Buchstaben und römische Ziffern in Kleinbuchstaben. 
for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// 2 - Eine Liste mit Aufzählungszeichen:
// Diese Liste fügt vor jedem Absatz einen Einzug und ein Aufzählungszeichen ("•") ein.
// Tiefere Ebenen dieser Liste verwenden andere Symbole, wie "■" und "○".
builder.ListFormat.List = doc.Lists.Add(ListTemplate.BulletDefault);

for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// Wir können die Listenformatierung deaktivieren, um nachfolgende Absätze nicht als Listen zu formatieren, indem wir das "List"-Flag deaktivieren.
builder.ListFormat.List = null;

Assert.False(builder.ListFormat.IsListItem);

doc.Save(ArtifactsDir + "Lists.SpecifyListLevel.docx");
```

### Siehe auch

* class [ListCollection](../../../aspose.words.lists/listcollection/)
* class [DocumentBase](../)
* namensraum [Aspose.Words](../../documentbase/)
* Montage [Aspose.Words](../../../)


