---
title: ListLevelCollection.Item
second_title: Aspose.Words für .NET-API-Referenz
description: ListLevelCollection eigendom. Ruft eine Listenebene nach Index ab.
type: docs
weight: 20
url: /de/net/aspose.words.lists/listlevelcollection/item/
---
## ListLevelCollection indexer

Ruft eine Listenebene nach Index ab.

```csharp
public ListLevel this[int index] { get; set; }
```

### Beispiele

Zeigt, wie ein Listenstil erstellt und in einem Dokument verwendet wird.

```csharp
Document doc = new Document();

// Eine Liste ermöglicht es uns, Sätze von Absätzen mit Präfixsymbolen und Einzügen zu organisieren und zu dekorieren.
// Wir können verschachtelte Listen erstellen, indem wir die Einrückungsebene erhöhen. 
// Wir können eine Liste beginnen und beenden, indem wir die "ListFormat"-Eigenschaft eines Dokumentenerstellers verwenden. 
// Jeder Absatz, den wir zwischen dem Anfang und dem Ende einer Liste hinzufügen, wird zu einem Element in der Liste.
// Wir können ein ganzes List-Objekt in einem Stil enthalten.
Style listStyle = doc.Styles.Add(StyleType.List, "MyListStyle");

List list1 = listStyle.List;

Assert.True(list1.IsListStyleDefinition);
Assert.False(list1.IsListStyleReference);
Assert.True(list1.IsMultiLevel);
Assert.AreEqual(listStyle, list1.Style);

// Ändern Sie das Aussehen aller Listenebenen in unserer Liste.
foreach (ListLevel level in list1.ListLevels)
{
    level.Font.Name = "Verdana";
    level.Font.Color = Color.Blue;
    level.Font.Bold = true;
}

DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Using list style first time:");

// Eine weitere Liste aus einer Liste innerhalb eines Stils erstellen.
List list2 = doc.Lists.Add(listStyle);

Assert.False(list2.IsListStyleDefinition);
Assert.True(list2.IsListStyleReference);
Assert.AreEqual(listStyle, list2.Style);

// Fügen Sie einige Listenelemente hinzu, die unsere Liste formatieren wird.
builder.ListFormat.List = list2;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

builder.Writeln("Using list style second time:");

// Eine weitere Liste basierend auf dem Listenstil erstellen und anwenden.
List list3 = doc.Lists.Add(listStyle);
builder.ListFormat.List = list3;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

builder.Document.Save(ArtifactsDir + "Lists.CreateAndUseListStyle.docx");
```

Zeigt, wie Sie benutzerdefinierte Listenformatierungen auf Absätze anwenden, wenn Sie DocumentBuilder verwenden.

```csharp
Document doc = new Document();

// Eine Liste ermöglicht es uns, Sätze von Absätzen mit Präfixsymbolen und Einzügen zu organisieren und zu dekorieren.
// Wir können verschachtelte Listen erstellen, indem wir die Einrückungsebene erhöhen. 
// Wir können eine Liste beginnen und beenden, indem wir die "ListFormat"-Eigenschaft eines Dokumentenerstellers verwenden. 
// Jeder Absatz, den wir zwischen dem Anfang und dem Ende einer Liste hinzufügen, wird zu einem Element in der Liste.
// Erstellen Sie eine Liste aus einer Microsoft Word-Vorlage und passen Sie die ersten beiden Listenebenen an.
List list = doc.Lists.Add(ListTemplate.NumberDefault);

ListLevel listLevel = list.ListLevels[0];
listLevel.Font.Color = Color.Red;
listLevel.Font.Size = 24;
listLevel.NumberStyle = NumberStyle.OrdinalText;
listLevel.StartAt = 21;
listLevel.NumberFormat = "\x0000";

listLevel.NumberPosition = -36;
listLevel.TextPosition = 144;
listLevel.TabPosition = 144;

listLevel = list.ListLevels[1];
listLevel.Alignment = ListLevelAlignment.Right;
listLevel.NumberStyle = NumberStyle.Bullet;
listLevel.Font.Name = "Wingdings";
listLevel.Font.Color = Color.Blue;
listLevel.Font.Size = 24;

// Dieser NumberFormat-Wert erstellt sternförmige Aufzählungssymbole.
listLevel.NumberFormat = "\xf0af";
listLevel.TrailingCharacter = ListTrailingCharacter.Space;
listLevel.NumberPosition = 144;

// Absätze erstellen und beide Listenebenen unserer benutzerdefinierten Listenformatierung darauf anwenden.
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ListFormat.List = list;
builder.Writeln("The quick brown fox...");
builder.Writeln("The quick brown fox...");

builder.ListFormat.ListIndent();
builder.Writeln("jumped over the lazy dog.");
builder.Writeln("jumped over the lazy dog.");

builder.ListFormat.ListOutdent();
builder.Writeln("The quick brown fox...");

builder.ListFormat.RemoveNumbers();

builder.Document.Save(ArtifactsDir + "Lists.CreateCustomList.docx");
```

### Siehe auch

* class [ListLevel](../../listlevel/)
* class [ListLevelCollection](../)
* namensraum [Aspose.Words.Lists](../../listlevelcollection/)
* Montage [Aspose.Words](../../../)


