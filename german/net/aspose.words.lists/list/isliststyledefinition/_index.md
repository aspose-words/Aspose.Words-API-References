---
title: List.IsListStyleDefinition
second_title: Aspose.Words für .NET-API-Referenz
description: List eigendom. Gibt wahr zurück wenn diese Liste eine Definition eines Listenstils ist.
type: docs
weight: 20
url: /de/net/aspose.words.lists/list/isliststyledefinition/
---
## List.IsListStyleDefinition property

Gibt wahr zurück, wenn diese Liste eine Definition eines Listenstils ist.

```csharp
public bool IsListStyleDefinition { get; }
```

### Bemerkungen

Wenn diese Eigenschaft wahr ist, wird die[`Style`](../style/)Die Eigenschaft gibt den Listenstil zurück, den diese Liste definiert.

Indem Sie die Eigenschaften einer Liste ändern, die einen Listenstil definiert, ändern Sie die properties des Listenstils.

Eine Liste, die eine Definition eines Listenstils ist, kann nicht direkt auf Absätze angewendet werden, um sie zu nummerieren.

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

### Siehe auch

* class [List](../)
* namensraum [Aspose.Words.Lists](../../list/)
* Montage [Aspose.Words](../../../)


