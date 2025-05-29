---
title: List.IsMultiLevel
linktitle: IsMultiLevel
articleTitle: IsMultiLevel
second_title: Aspose.Words für .NET
description: Finden Sie heraus, ob Ihre Liste mehrere Ebenen unterstützt! Unser Tool zeigt „true“ für 9 Ebenen und „false“ für 1 Ebene an und steigert so die Effizienz Ihres Datenmanagements.
type: docs
weight: 40
url: /de/net/aspose.words.lists/list/ismultilevel/
---
## List.IsMultiLevel property

Rückgaben`WAHR` wenn die Liste 9 Ebenen enthält;`FALSCH` wenn 1 Ebene.

```csharp
public bool IsMultiLevel { get; }
```

## Bemerkungen

Die Listen, die Sie mit Aspose.Words erstellen, sind immer mehrstufige Listen und enthalten 9 Ebenen.

Microsoft Word 2003 und höher erstellen immer mehrstufige Listen mit 9 Ebenen. In einigen Dokumenten, die mit früheren Versionen von Microsoft Word erstellt wurden, stoßen Sie möglicherweise auf Listen, die nur über eine Ebene verfügen.

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
