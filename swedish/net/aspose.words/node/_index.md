---
title: Node Class
linktitle: Node
articleTitle: Node
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Node, den viktiga grunden för alla Word-dokumentnoder, som möjliggör sömlös dokumenthantering och anpassning.
type: docs
weight: 4860
url: /sv/net/aspose.words/node/
---
## Node class

Basklass för alla noder i ett Word-dokument.

För att lära dig mer, besök[Aspose.Words-dokumentobjektmodell (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/) dokumentationsartikel.

```csharp
public abstract class Node
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Anger anpassad nodidentifierare. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Hämtar dokumentet som denna nod tillhör. |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | Returer`sann` om denna nod kan innehålla andra noder. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Hämtar noden som följer direkt efter denna nod. |
| abstract [NodeType](../../aspose.words/node/nodetype/) { get; } | Hämtar typen av denna nod. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Hämtar den omedelbara föräldern till denna nod. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Hämtar noden som omedelbart föregår denna nod. |
| [Range](../../aspose.words/node/range/) { get; } | Returnerar en[`Range`](../range/)objekt som representerar den del av ett dokument som finns i denna nod. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| abstract [Accept](../../aspose.words/node/accept/)(*[DocumentVisitor](../documentvisitor/)*) | Tar emot en besökare. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Skapar en duplikat av noden. |
| [GetAncestor](../../aspose.words/node/getancestor/#getancestor)(*[NodeType](../nodetype/)*) | Hämtar den första förfadern till den angivna[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/#getancestor_1)(*Type*) | Hämtar den första förfadern till den angivna objekttypen. |
| virtual [GetText](../../aspose.words/node/gettext/)() | Hämtar texten för denna nod och alla dess underordnade noder. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*Node*) | Hämtar nästa nod enligt algoritmen för förbeställningsträdtraversering. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*Node*) | Hämtar föregående nod enligt algoritmen för trädtraversering i förbeställning. |
| [Remove](../../aspose.words/node/remove/)() | Tar bort sig själv från föräldern. |
| [ToString](../../aspose.words/node/tostring/#tostring_1)(*[SaveFormat](../saveformat/)*) | Exporterar nodens innehåll till en sträng i det angivna formatet. |
| [ToString](../../aspose.words/node/tostring/#tostring_2)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Exporterar nodens innehåll till en sträng med de angivna sparalternativen. |
| static [NodeTypeToString](../../aspose.words/node/nodetypetostring/)(*[NodeType](../nodetype/)*) | En verktygsmetod som konverterar ett nodtypsuppräkningsvärde till en användarvänlig sträng. |

## Anmärkningar

Ett dokument representeras som ett träd av noder, liknande DOM eller XmlDocument.

För mer information, se mönstret för sammansatt design.

De`Node` klass:

* Definierar gränssnittet för undernoden.
* Definierar gränssnittet för besökande noder.
* Tillhandahåller standard kloningsfunktion.
* Implementerar mekanismer för föräldranod och ägardokument.
* Implementerar åtkomst till syskonnoder.

## Exempel

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

Visar hur man klonar en sammansatt nod.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;
para.AppendChild(new Run(doc, "Hello world!"));

// Nedan följer två sätt att klona en sammansatt nod.
// 1 - Skapa en klon av en nod och skapa även en klon av var och en av dess undernoder.
Node cloneWithChildren = para.Clone(true);

Assert.IsTrue(((CompositeNode)cloneWithChildren).HasChildNodes);
Assert.AreEqual("Hello world!", cloneWithChildren.GetText().Trim());

// 2 - Skapa en klon av en nod helt för sig själv utan några underordnade noder.
Node cloneWithoutChildren = para.Clone(false);

Assert.IsFalse(((CompositeNode)cloneWithoutChildren).HasChildNodes);
Assert.AreEqual(string.Empty, cloneWithoutChildren.GetText().Trim());
```

Visar hur man navigerar genom en sammansatt nods samling av underordnade noder.

```csharp
Document doc = new Document();

// Lägg till två körningar och en form som underordnade noder i det första stycket i detta dokument.
Paragraph paragraph = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);
paragraph.AppendChild(new Run(doc, "Hello world! "));

Shape shape = new Shape(doc, ShapeType.Rectangle);
shape.Width = 200;
shape.Height = 200;
// Observera att 'CustomNodeId' inte sparas i en utdatafil och endast finns under nodens livstid.
shape.CustomNodeId = 100;
shape.WrapType = WrapType.Inline;
paragraph.AppendChild(shape);

paragraph.AppendChild(new Run(doc, "Hello again!"));

// Iterera genom styckets samling av omedelbara underordnade,
// och skriv ut alla körningar eller former som vi hittar inuti.
NodeCollection children = paragraph.GetChildNodes(NodeType.Any, false);

Assert.AreEqual(3, paragraph.GetChildNodes(NodeType.Any, false).Count);

foreach (Node child in children)
    switch (child.NodeType)
    {
        case NodeType.Run:
            Console.WriteLine("Run contents:");
            Console.WriteLine($"\t\"{child.GetText().Trim()}\"");
            break;
        case NodeType.Shape:
            Shape childShape = (Shape)child;
            Console.WriteLine("Shape:");
            Console.WriteLine($"\t{childShape.ShapeType}, {childShape.Width}x{childShape.Height}");
            break;
    }
```

### Se även

* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)
