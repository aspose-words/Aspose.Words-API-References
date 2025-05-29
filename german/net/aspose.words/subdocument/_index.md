---
title: SubDocument Class
linktitle: SubDocument
articleTitle: SubDocument
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.SubDocument, verwalten und referenzieren Sie externe Dokumente effizient für eine nahtlose Integration und verbesserte Dokumentverarbeitung.
type: docs
weight: 7020
url: /de/net/aspose.words/subdocument/
---
## SubDocument class

Stellt eine**Unterdokument** - Dies ist ein Verweis auf ein extern gespeichertes Dokument.

Um mehr zu erfahren, besuchen Sie die[Aspose.Words Dokumentobjektmodell (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/) Dokumentationsartikel.

```csharp
public class SubDocument : Node
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Gibt die benutzerdefinierte Knotenkennung an. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Ruft das Dokument ab, zu dem dieser Knoten gehört. |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | Rückgaben`WAHR` wenn dieser Knoten andere Knoten enthalten kann. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Ruft den Knoten ab, der diesem Knoten unmittelbar folgt. |
| override [NodeType](../../aspose.words/subdocument/nodetype/) { get; } | RückgabenSubDocument . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Ruft den unmittelbar übergeordneten Knoten dieses Knotens ab. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Ruft den Knoten ab, der diesem Knoten unmittelbar vorausgeht. |
| [Range](../../aspose.words/node/range/) { get; } | Gibt einen[`Range`](../range/)Objekt, das den Teil eines Dokuments darstellt, der in diesem Knoten enthalten ist. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| override [Accept](../../aspose.words/subdocument/accept/)(*[DocumentVisitor](../documentvisitor/)*) | Nimmt einen Besucher auf. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Erstellt ein Duplikat des Knotens. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../nodetype/)*) | Ruft den ersten Vorfahren des angegebenen[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Ruft den ersten Vorgänger des angegebenen Objekttyps ab. |
| virtual [GetText](../../aspose.words/node/gettext/)() | Ruft den Text dieses Knotens und aller seiner untergeordneten Knoten ab. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../node/)*) | Ruft den nächsten Knoten gemäß dem Pre-Order-Tree-Traversal-Algorithmus ab. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../node/)*) | Ruft den vorherigen Knoten gemäß dem Pre-Order-Tree-Traversal-Algorithmus ab. |
| [Remove](../../aspose.words/node/remove/)() | Entfernt sich selbst vom übergeordneten Element. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../saveformat/)*) | Exportiert den Inhalt des Knotens in eine Zeichenfolge im angegebenen Format. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Exportiert den Inhalt des Knotens unter Verwendung der angegebenen Speicheroptionen in eine Zeichenfolge. |

## Bemerkungen

In dieser Version von Aspose.Words,`SubDocument`Knoten bieten keine öffentlichen Methoden und Eigenschaften zum Erstellen oder Ändern eines Unterdokuments. In dieser Version können Sie nicht instanziieren `SubDocument` Knoten oder vorhandene ändern, außer sie zu löschen.

`SubDocument` kann nur ein Kind sein von[`Paragraph`](../paragraph/).

## Beispiele

Zeigt, wie auf das Unterdokument eines Hauptdokuments zugegriffen wird.

```csharp
Document doc = new Document(MyDir + "Master document.docx");

NodeCollection subDocuments = doc.GetChildNodes(NodeType.SubDocument, true);
// Dieser Knoten dient als Verweis auf ein externes Dokument und auf seinen Inhalt kann nicht zugegriffen werden.
SubDocument subDocument = (SubDocument)subDocuments[0];

Assert.False(subDocument.IsComposite);
```

### Siehe auch

* class [Node](../node/)
* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
