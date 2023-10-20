---
title: Style.List
linktitle: List
articleTitle: List
second_title: Aspose.Words für .NET
description: Style List eigendom. Ruft die Liste ab die die Formatierung dieses Listenstils definiert in C#.
type: docs
weight: 100
url: /de/net/aspose.words/style/list/
---
## Style.List property

Ruft die Liste ab, die die Formatierung dieses Listenstils definiert.

```csharp
public List List { get; }
```

## Bemerkungen

Diese Eigenschaft ist nur für Listenstile gültig. Für andere Stiltypen gibt diese Eigenschaft zurück`Null`.

## Beispiele

Zeigt, wie ein Listenstil erstellt und in einem Dokument verwendet wird.

```csharp
Document doc = new Document();

// Eine Liste ermöglicht es uns, Absätze mit Präfixsymbolen und Einzügen zu organisieren und zu dekorieren.
 // Wir können verschachtelte Listen erstellen, indem wir die Einrückungsebene erhöhen.
 // Wir können eine Liste beginnen und beenden, indem wir die „ListFormat“-Eigenschaft eines Document Builders verwenden.
// Jeder Absatz, den wir zwischen dem Anfang und dem Ende einer Liste hinzufügen, wird zu einem Element in der Liste.
// Wir können ein ganzes List-Objekt in einem Stil enthalten.
Style listStyle = doc.Styles.Add(StyleType.List, "MyListStyle");

List list1 = listStyle.List;

Assert.True(list1.IsListStyleDefinition);
Assert.False(list1.IsListStyleReference);
Assert.True(list1.IsMultiLevel);
Assert.AreEqual(listStyle, list1.Style);

// Ändere das Erscheinungsbild aller Listenebenen in unserer Liste.
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

// Einige Listenelemente hinzufügen, die unsere Liste formatieren wird.
builder.ListFormat.List = list2;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

builder.Writeln("Using list style second time:");

// Erstellen Sie eine weitere Liste basierend auf dem Listenstil und wenden Sie sie an.
List list3 = doc.Lists.Add(listStyle);
builder.ListFormat.List = list3;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

builder.Document.Save(ArtifactsDir + "Lists.CreateAndUseListStyle.docx");
```

### Siehe auch

* class [List](../../../aspose.words.lists/list/)
* class [Style](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
