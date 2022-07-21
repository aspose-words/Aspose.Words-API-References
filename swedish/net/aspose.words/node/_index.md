---
title: Node
second_title: Aspose.Words för .NET API Referens
description: Basklass för alla noder i ett Word-dokument.
type: docs
weight: 3930
url: /sv/net/aspose.words/node/
---
## Node class

Basklass för alla noder i ett Word-dokument.

```csharp
public abstract class Node
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | Anger anpassad nodidentifierare. |
| virtual [Document](../../aspose.words/node/document) { get; } | Hämtar dokumentet som denna nod tillhör. |
| virtual [IsComposite](../../aspose.words/node/iscomposite) { get; } | Returnerar sant om denna nod kan innehålla andra noder. |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | Hämtar noden omedelbart efter denna nod. |
| abstract [NodeType](../../aspose.words/node/nodetype) { get; } | Hämtar typen av denna nod. |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | Hämtar den omedelbara föräldern till denna nod. |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | Hämtar noden omedelbart före denna nod. |
| [Range](../../aspose.words/node/range) { get; } | Returnerar en **Räckvidd** objekt som representerar den del av ett dokument som finns i denna nod. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| abstract [Accept](../../aspose.words/node/accept)(DocumentVisitor) | Accepterar en besökare. |
| [Clone](../../aspose.words/node/clone)(bool) | Skapar en dubblett av noden. |
| [GetAncestor](../../aspose.words/node/getancestor#getancestor)(NodeType) | Hämtar den första förfadern till den angivna[`NodeType`](../nodetype) . |
| [GetAncestor](../../aspose.words/node/getancestor#getancestor_1)(Type) | Hämtar den första förfadern till den angivna objekttypen. |
| virtual [GetText](../../aspose.words/node/gettext)() | Hämtar texten för denna nod och alla dess underordnade. |
| [NextPreOrder](../../aspose.words/node/nextpreorder)(Node) | Hämtar nästa nod enligt algoritmen för förbeställningsträdet. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder)(Node) | Hämtar föregående nod enligt algoritmen för förbeställningsträdet. |
| [Remove](../../aspose.words/node/remove)() | Tar bort sig själv från föräldern. |
| [ToString](../../aspose.words/node/tostring#tostring_1)(SaveFormat) | Exporterar innehållet i noden till en sträng i angivet format. |
| [ToString](../../aspose.words/node/tostring#tostring_2)(SaveOptions) | Exporterar innehållet i noden till en sträng med de angivna sparalternativen. |
| static [NodeTypeToString](../../aspose.words/node/nodetypetostring)(NodeType) | En verktygsmetod som omvandlar ett nodtyps enumvärde till en användarvänlig sträng. |

### Anmärkningar

Ett dokument representeras som ett träd av noder, liknande DOM eller XmlDocument.

För mer information se Composite design mönster.

De[`Node`](../node)klass:

* Definierar gränssnittet för barnnoden.
* Definierar gränssnittet för besökande noder.
* Ger standard kloningsmöjlighet.
* Implementerar mekanismer för överordnad nod och ägardokument.
* Implementerar åtkomst till syskonnoder.

### Exempel

Visar hur man tar bort alla underordnade noder av en specifik typ från en sammansatt nod.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

Assert.AreEqual(2, doc.GetChildNodes(NodeType.Table, true).Count);

Node curNode = doc.FirstSection.Body.FirstChild;

while (curNode != null)
{
    // Spara nästa syskonnod som en variabel ifall vi vill flytta till den efter att ha tagit bort denna nod.
    Node nextNode = curNode.NextSibling;

    // En sektionskropp kan innehålla paragraf- och tabellnoder.
    // Om noden är en tabell, ta bort den från den överordnade.
    if (curNode.NodeType == NodeType.Table)
        curNode.Remove();

    curNode = nextNode;
}

Assert.AreEqual(0, doc.GetChildNodes(NodeType.Table, true).Count);
```

Visar hur man klona en sammansatt nod.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;
para.AppendChild(new Run(doc, "Hello world!"));

// Nedan finns två sätt att klona en sammansatt nod.
// 1 - Skapa en klon av en nod, och skapa en klon av var och en av dess undernoder.
Node cloneWithChildren = para.Clone(true);

Assert.IsTrue(((CompositeNode)cloneWithChildren).HasChildNodes);
Assert.AreEqual("Hello world!", cloneWithChildren.GetText().Trim());

// 2 - Skapa en klon av en nod helt av sig själv utan några barn.
Node cloneWithoutChildren = para.Clone(false);

Assert.IsFalse(((CompositeNode)cloneWithoutChildren).HasChildNodes);
Assert.AreEqual(string.Empty, cloneWithoutChildren.GetText().Trim());
```

Visar hur man går igenom en sammansatt nods samling av undernoder.

```csharp
Document doc = new Document();

// Lägg till två körningar och en form som underordnade noder i det första stycket i detta dokument.
Paragraph paragraph = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);
paragraph.AppendChild(new Run(doc, "Hello world! "));

Shape shape = new Shape(doc, ShapeType.Rectangle);
shape.Width = 200;
shape.Height = 200;
// Observera att 'CustomNodeId' inte sparas i en utdatafil och endast existerar under nodens livstid.
shape.CustomNodeId = 100;
shape.WrapType = WrapType.Inline;
paragraph.AppendChild(shape);

paragraph.AppendChild(new Run(doc, "Hello again!"));

// Iterera genom styckets samling av närmaste barn,
// och skriv ut alla körningar eller former som vi hittar inom.
NodeCollection children = paragraph.ChildNodes;

Assert.AreEqual(3, paragraph.ChildNodes.Count);

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
    }
```

### Se även

* namnutrymme [Aspose.Words](../../aspose.words)
* hopsättning [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
