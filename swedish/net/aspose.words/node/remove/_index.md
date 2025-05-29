---
title: Node.Remove
linktitle: Remove
articleTitle: Remove
second_title: Aspose.Words för .NET
description: Upptäck Node Remove-metoden för att enkelt koppla bort noder från deras överordnade noder, vilket förbättrar din kodens effektivitet och struktur.
type: docs
weight: 150
url: /sv/net/aspose.words/node/remove/
---
## Node.Remove method

Tar bort sig själv från föräldern.

```csharp
public void Remove()
```

## Exempel

Visar hur man tar bort alla former med bilder från ett dokument.

```csharp
Document doc = new Document(MyDir + "Images.docx");
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);

Assert.AreEqual(9, shapes.OfType<Shape>().Count(s => s.HasImage));

foreach (Shape shape in shapes.OfType<Shape>())
    if (shape.HasImage) 
        shape.Remove();

Assert.AreEqual(0, shapes.OfType<Shape>().Count(s => s.HasImage));
```

Visar hur man tar bort alla underordnade noder av en specifik typ från en sammansatt nod.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

Assert.AreEqual(2, doc.GetChildNodes(NodeType.Table, true).Count);

Node curNode = doc.FirstSection.Body.FirstChild;

while (curNode != null)
{
    // Spara nästa syskonnod som en variabel ifall vi vill flytta till den efter att vi tagit bort den här noden.
    Node nextNode = curNode.NextSibling;

    // En sektionstext kan innehålla stycke- och tabellnoder.
    // Om noden är en tabell, ta bort den från föräldern.
    if (curNode.NodeType == NodeType.Table)
        curNode.Remove();

    curNode = nextNode;
}

Assert.AreEqual(0, doc.GetChildNodes(NodeType.Table, true).Count);
```

### Se även

* class [Node](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
