---
title: Class Node
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Node klas. Basisklasse für alle Knoten eines WordDokuments.
type: docs
weight: 3930
url: /de/net/aspose.words/node/
---
## Node class

Basisklasse für alle Knoten eines Word-Dokuments.

```csharp
public abstract class Node
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Gibt die benutzerdefinierte Knotenkennung an. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Ruft das Dokument ab, zu dem dieser Knoten gehört. |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | Gibt wahr zurück, wenn dieser Knoten andere Knoten enthalten kann. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Ruft den Knoten ab, der diesem Knoten unmittelbar folgt. |
| abstract [NodeType](../../aspose.words/node/nodetype/) { get; } | Ruft den Typ dieses Knotens ab. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Ruft den unmittelbar übergeordneten Knoten dieses Knotens ab. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Ruft den Knoten unmittelbar vor diesem Knoten ab. |
| [Range](../../aspose.words/node/range/) { get; } | Gibt a zurück **Bereich** Objekt, das den Teil eines Dokuments darstellt, das in diesem Knoten enthalten ist. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| abstract [Accept](../../aspose.words/node/accept/)(DocumentVisitor) | Akzeptiert einen Besucher. |
| [Clone](../../aspose.words/node/clone/)(bool) | Erstellt ein Duplikat des Knotens. |
| [GetAncestor](../../aspose.words/node/getancestor/#getancestor)(NodeType) | Ruft den ersten Vorfahren der angegebenen ab[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/#getancestor_1)(Type) | Ruft den ersten Vorfahren des angegebenen Objekttyps ab. |
| virtual [GetText](../../aspose.words/node/gettext/)() | Ruft den Text dieses Knotens und aller seiner Kinder ab. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | Ruft den nächsten Knoten gemäß dem Traversalalgorithmus des Vorbestellungsbaums ab. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | Ruft den vorherigen Knoten gemäß dem Traversalalgorithmus des Vorbestellungsbaums ab. |
| [Remove](../../aspose.words/node/remove/)() | Entfernt sich selbst vom übergeordneten Element. |
| [ToString](../../aspose.words/node/tostring/#tostring_1)(SaveFormat) | Exportiert den Inhalt des Knotens in einen String im angegebenen Format. |
| [ToString](../../aspose.words/node/tostring/#tostring_2)(SaveOptions) | Exportiert den Inhalt des Knotens unter Verwendung der angegebenen Speicheroptionen in einen String. |
| static [NodeTypeToString](../../aspose.words/node/nodetypetostring/)(NodeType) | Eine Dienstprogrammmethode, die einen Aufzählungswert eines Knotentyps in eine benutzerfreundliche Zeichenfolge umwandelt. |

### Bemerkungen

Ein Dokument wird ähnlich wie DOM oder XmlDocument als Baum aus Knoten dargestellt.

Weitere Informationen finden Sie im Composite-Designmuster.

Das`Node`Klasse:

* Definiert die Schnittstelle des untergeordneten Knotens.
* Definiert die Schnittstelle für den Besuch von Knoten.
* Bietet standardmäßige Klonfunktion.
* Implementiert Mechanismen für übergeordnete Knoten und Eigentümerdokumente.
* Implementiert den Zugriff auf gleichgeordnete Knoten.

### Beispiele

Zeigt, wie alle untergeordneten Knoten eines bestimmten Typs aus einem zusammengesetzten Knoten entfernt werden.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

Assert.AreEqual(2, doc.GetChildNodes(NodeType.Table, true).Count);

Node curNode = doc.FirstSection.Body.FirstChild;

while (curNode != null)
{
    // Speichern Sie den nächsten Geschwisterknoten als Variable, falls wir nach dem Löschen dieses Knotens dorthin wechseln möchten.
    Node nextNode = curNode.NextSibling;

    // Ein Abschnittskörper kann Absatz- und Tabellenknoten enthalten.
    // Wenn der Knoten eine Tabelle ist, entferne ihn vom Elternknoten.
    if (curNode.NodeType == NodeType.Table)
        curNode.Remove();

    curNode = nextNode;
}

Assert.AreEqual(0, doc.GetChildNodes(NodeType.Table, true).Count);
```

Zeigt, wie ein zusammengesetzter Knoten geklont wird.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;
para.AppendChild(new Run(doc, "Hello world!"));

// Im Folgenden finden Sie zwei Möglichkeiten zum Klonen eines zusammengesetzten Knotens.
// 1 - Erstellen Sie einen Klon eines Knotens und erstellen Sie auch einen Klon von jedem seiner untergeordneten Knoten.
Node cloneWithChildren = para.Clone(true);

Assert.IsTrue(((CompositeNode)cloneWithChildren).HasChildNodes);
Assert.AreEqual("Hello world!", cloneWithChildren.GetText().Trim());

// 2 - Erstellen Sie einen Klon eines Knotens ohne Kinder.
Node cloneWithoutChildren = para.Clone(false);

Assert.IsFalse(((CompositeNode)cloneWithoutChildren).HasChildNodes);
Assert.AreEqual(string.Empty, cloneWithoutChildren.GetText().Trim());
```

Zeigt, wie die Sammlung untergeordneter Knoten eines zusammengesetzten Knotens durchlaufen wird.

```csharp
Document doc = new Document();

// Fügen Sie dem ersten Absatz dieses Dokuments zwei Läufe und eine Form als untergeordnete Knoten hinzu.
Paragraph paragraph = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);
paragraph.AppendChild(new Run(doc, "Hello world! "));

Shape shape = new Shape(doc, ShapeType.Rectangle);
shape.Width = 200;
shape.Height = 200;
// Beachten Sie, dass die 'CustomNodeId' nicht in einer Ausgabedatei gespeichert wird und nur während der Lebensdauer des Knotens existiert.
shape.CustomNodeId = 100;
shape.WrapType = WrapType.Inline;
paragraph.AppendChild(shape);

paragraph.AppendChild(new Run(doc, "Hello again!"));

// Durch die Sammlung der unmittelbaren Kinder des Absatzes iterieren,
// und drucken Sie alle Läufe oder Formen, die wir darin finden.
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

### Siehe auch

* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)


