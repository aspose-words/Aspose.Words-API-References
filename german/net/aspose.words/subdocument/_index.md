---
title: Class SubDocument
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.SubDocument klas. steht für a Unterdokument  das ist ein Verweis auf ein extern gespeichertes Dokument.
type: docs
weight: 5870
url: /de/net/aspose.words/subdocument/
---
## SubDocument class

steht für a **Unterdokument** - das ist ein Verweis auf ein extern gespeichertes Dokument.

```csharp
public class SubDocument : Node
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Gibt die benutzerdefinierte Knotenkennung an. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Ruft das Dokument ab, zu dem dieser Knoten gehört. |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | Gibt wahr zurück, wenn dieser Knoten andere Knoten enthalten kann. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Ruft den Knoten ab, der diesem Knoten unmittelbar folgt. |
| override [NodeType](../../aspose.words/subdocument/nodetype/) { get; } | gibt zurück **NodeType.SubDocument** |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Ruft den unmittelbar übergeordneten Knoten dieses Knotens ab. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Ruft den Knoten unmittelbar vor diesem Knoten ab. |
| [Range](../../aspose.words/node/range/) { get; } | Gibt a zurück **Bereich** Objekt, das den Teil eines Dokuments darstellt, das in diesem Knoten enthalten ist. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| override [Accept](../../aspose.words/subdocument/accept/)(DocumentVisitor) | Akzeptiert einen Besucher. |
| [Clone](../../aspose.words/node/clone/)(bool) | Erstellt ein Duplikat des Knotens. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Ruft den ersten Vorfahren der angegebenen ab[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | Ruft den ersten Vorfahren des angegebenen Objekttyps ab. |
| virtual [GetText](../../aspose.words/node/gettext/)() | Ruft den Text dieses Knotens und aller seiner Kinder ab. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | Ruft den nächsten Knoten gemäß dem Traversalalgorithmus des Vorbestellungsbaums ab. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | Ruft den vorherigen Knoten gemäß dem Traversalalgorithmus des Vorbestellungsbaums ab. |
| [Remove](../../aspose.words/node/remove/)() | Entfernt sich selbst vom übergeordneten Element. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | Exportiert den Inhalt des Knotens in einen String im angegebenen Format. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | Exportiert den Inhalt des Knotens unter Verwendung der angegebenen Speicheroptionen in einen String. |

### Bemerkungen

In dieser Version von Aspose.Words,`SubDocument` Knoten stellen keine öffentlichen Methoden und Eigenschaften zum Erstellen oder Ändern eines Filialdokuments bereit. In dieser Version können Sie SubDocument-Knoten nicht instanziieren oder vorhandene ändern, außer sie zu löschen.

`SubDocument` kann nur ein Kind von sein[`Paragraph`](../paragraph/).

### Beispiele

Zeigt, wie auf das Filialdokument eines Globaldokuments zugegriffen wird.

```csharp
Document doc = new Document(MyDir + "Master document.docx");

NodeCollection subDocuments = doc.GetChildNodes(NodeType.SubDocument, true);
// Dieser Knoten dient als Verweis auf ein externes Dokument, auf dessen Inhalt nicht zugegriffen werden kann.
SubDocument subDocument = (SubDocument)subDocuments[0];

Assert.False(subDocument.IsComposite);
```

### Siehe auch

* class [Node](../node/)
* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)


