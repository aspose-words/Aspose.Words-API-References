---
title: List.IsListStyleReference
linktitle: IsListStyleReference
articleTitle: IsListStyleReference
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „IsListStyleReference“. Sie gibt an, ob eine Liste auf einen bestimmten Stil verweist, und verbessert so die Formatierung und Organisation Ihres Dokuments.
type: docs
weight: 30
url: /de/net/aspose.words.lists/list/isliststylereference/
---
## List.IsListStyleReference property

Rückgaben`WAHR` wenn diese Liste ein Verweis auf einen Listenstil ist.

```csharp
public bool IsListStyleReference { get; }
```

## Bemerkungen

Beachten Sie, dass das Ändern der Eigenschaften einer Liste, die auf einen Listenstil verweist, keine Auswirkungen hat. Die im Listenstil selbst angegebene Listenformatierung hat immer Vorrang.

## Beispiele

Zeigt, wie Sie einen Listenstil erstellen und in einem Dokument verwenden.

```csharp
Document doc = new Document();

// Eine Liste ermöglicht es uns, Absatzsätze mit Präfixsymbolen und Einzügen zu organisieren und zu dekorieren.
    // Wir können verschachtelte Listen erstellen, indem wir die Einrückungsebene erhöhen.
    // Wir können eine Liste beginnen und beenden, indem wir die Eigenschaft „ListFormat“ eines Dokument-Generators verwenden.
// Jeder Absatz, den wir zwischen dem Anfang und dem Ende einer Liste hinzufügen, wird zu einem Element in der Liste.
// Wir können ein ganzes Listenobjekt in einem Stil enthalten.
Style listStyle = doc.Styles.Add(StyleType.List, "MyListStyle");

List list1 = listStyle.List;

Assert.True(list1.IsListStyleDefinition);
Assert.False(list1.IsListStyleReference);
Assert.True(list1.IsMultiLevel);
Assert.AreEqual(listStyle, list1.Style);

// Ändern Sie das Erscheinungsbild aller Listenebenen in unserer Liste.
foreach (ListLevel level in list1.ListLevels)
{
    level.Font.Name = "Verdana";
    level.Font.Color = Color.Blue;
    level.Font.Bold = true;
}

DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Using list style first time:");

// Erstellen Sie eine weitere Liste aus einer Liste innerhalb eines Stils.
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

// Erstellen und wenden Sie eine weitere Liste basierend auf dem Listenstil an.
List list3 = doc.Lists.Add(listStyle);
builder.ListFormat.List = list3;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

builder.Document.Save(ArtifactsDir + "Lists.CreateAndUseListStyle.docx");
```

### Siehe auch

* class [List](../)
* namensraum [Aspose.Words.Lists](../../../aspose.words.lists/)
* Montage [Aspose.Words](../../../)
