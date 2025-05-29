---
title: Inline Class
linktitle: Inline
articleTitle: Inline
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Inline, die für die Zeichenformatierung in Inline-Knoten entwickelt wurde. Verbessern Sie den Stil Ihres Dokuments ohne untergeordnete Knoten!
type: docs
weight: 3710
url: /de/net/aspose.words/inline/
---
## Inline class

Basisklasse für Knoten auf Inline-Ebene, denen Zeichenformatierungen zugeordnet werden können, die jedoch keine eigenen untergeordneten Knoten haben können.

Um mehr zu erfahren, besuchen Sie die[Logische Ebenen von Knoten in einem Dokument](https://docs.aspose.com/words/net/logical-levels-of-nodes-in-a-document/) Dokumentationsartikel.

```csharp
public abstract class Inline : Node
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Gibt die benutzerdefinierte Knotenkennung an. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Ruft das Dokument ab, zu dem dieser Knoten gehört. |
| [Font](../../aspose.words/inline/font/) { get; } | Bietet Zugriff auf die Schriftformatierung dieses Objekts. |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | Rückgaben`WAHR` wenn dieser Knoten andere Knoten enthalten kann. |
| [IsDeleteRevision](../../aspose.words/inline/isdeleterevision/) { get; } | Gibt „true“ zurück, wenn dieses Objekt in Microsoft Word gelöscht wurde, während die Änderungsverfolgung aktiviert war. |
| [IsFormatRevision](../../aspose.words/inline/isformatrevision/) { get; } | Gibt „true“ zurück, wenn die Formatierung des Objekts in Microsoft Word geändert wurde, während die Änderungsverfolgung aktiviert war. |
| [IsInsertRevision](../../aspose.words/inline/isinsertrevision/) { get; } | Gibt „true“ zurück, wenn dieses Objekt in Microsoft Word eingefügt wurde, während die Änderungsverfolgung aktiviert war. |
| [IsMoveFromRevision](../../aspose.words/inline/ismovefromrevision/) { get; } | Rückgaben`WAHR` wenn dieses Objekt in Microsoft Word verschoben (gelöscht) wurde, während die Änderungsverfolgung aktiviert war. |
| [IsMoveToRevision](../../aspose.words/inline/ismovetorevision/) { get; } | Rückgaben`WAHR` wenn dieses Objekt in Microsoft Word verschoben (eingefügt) wurde, während die Änderungsverfolgung aktiviert war. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Ruft den Knoten ab, der diesem Knoten unmittelbar folgt. |
| abstract [NodeType](../../aspose.words/node/nodetype/) { get; } | Ruft den Typ dieses Knotens ab. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Ruft den unmittelbar übergeordneten Knoten dieses Knotens ab. |
| [ParentParagraph](../../aspose.words/inline/parentparagraph/) { get; } | Ruft das übergeordnete Element ab[`Paragraph`](../paragraph/) dieses Knotens. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Ruft den Knoten ab, der diesem Knoten unmittelbar vorausgeht. |
| [Range](../../aspose.words/node/range/) { get; } | Gibt einen[`Range`](../range/)Objekt, das den Teil eines Dokuments darstellt, der in diesem Knoten enthalten ist. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| abstract [Accept](../../aspose.words/node/accept/)(*[DocumentVisitor](../documentvisitor/)*) | Nimmt einen Besucher auf. |
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

Eine Klasse abgeleitet von`Inline` kann ein Kind sein von[`Paragraph`](../paragraph/).

## Beispiele

Zeigt, wie der Revisionstyp eines Inline-Knotens bestimmt wird.

```csharp
Document doc = new Document(MyDir + "Revision runs.docx");

// Wenn wir das Dokument bearbeiten, während die Option "Änderungen verfolgen" aktiviert ist, die Sie über Überprüfen -> Verfolgung finden,
// in Microsoft Word aktiviert ist, zählen die von uns vorgenommenen Änderungen als Revisionen.
// Wenn wir ein Dokument mit Aspose.Words bearbeiten, können wir mit der Verfolgung von Revisionen beginnen, indem wir
// Aufrufen der Methode „StartTrackRevisions“ des Dokuments und Beenden der Verfolgung mithilfe der Methode „StopTrackRevisions“.
// Wir können entweder Revisionen akzeptieren, um sie in das Dokument zu integrieren
// oder lehnen Sie sie ab, um die vorgeschlagene Änderung wirksam umzusetzen.
Assert.AreEqual(6, doc.Revisions.Count);

// Der übergeordnete Knoten einer Revision ist der Lauf, auf den sich die Revision bezieht. Ein Lauf ist ein Inline-Knoten.
Run run = (Run)doc.Revisions[0].ParentNode;

Paragraph firstParagraph = run.ParentParagraph;
RunCollection runs = firstParagraph.Runs;

Assert.AreEqual(6, runs.ToArray().Length);

// Unten sind fünf Revisionstypen aufgeführt, die einen Inline-Knoten kennzeichnen können.
// 1 - Eine "Insert"-Revision:
// Diese Überarbeitung erfolgt, wenn wir beim Verfolgen von Änderungen Text einfügen.
Assert.IsTrue(runs[2].IsInsertRevision);

// 2 - Eine „Format“-Revision:
// Diese Überarbeitung erfolgt, wenn wir die Formatierung des Textes ändern, während wir Änderungen verfolgen.
Assert.IsTrue(runs[2].IsFormatRevision);

// 3 - Eine „Move from“-Revision:
// Wenn wir Text in Microsoft Word markieren und ihn dann an eine andere Stelle im Dokument ziehen
// Beim Verfolgen von Änderungen werden zwei Revisionen angezeigt.
// Die „Verschieben von“-Revision ist eine Kopie des ursprünglichen Textes, bevor wir ihn verschoben haben.
Assert.IsTrue(runs[4].IsMoveFromRevision);

// 4 - Eine „Verschieben nach“-Revision:
// Die „Verschieben nach“-Revision ist der Text, den wir an seine neue Position im Dokument verschoben haben.
// Die Revisionen „Verschieben von“ und „Verschieben nach“ werden bei jeder von uns durchgeführten Verschiebungsrevision paarweise angezeigt.
// Das Akzeptieren einer Verschiebungsrevision löscht die „Verschieben von“-Revision und ihren Text,
// und behält den Text aus der „Verschieben nach“-Revision bei.
// Das Ablehnen einer Verschiebungsrevision behält umgekehrt die „Verschieben von“-Revision bei und löscht die „Verschieben nach“-Revision.
Assert.IsTrue(runs[1].IsMoveToRevision);

// 5 - Eine „Löschen“-Revision:
// Diese Überarbeitung erfolgt, wenn wir Text löschen, während wir Änderungen verfolgen. Wenn wir Text wie diesen löschen,
// es bleibt als Revision im Dokument, bis wir die Revision entweder akzeptieren,
// wodurch der Text endgültig gelöscht wird, oder die Überarbeitung abgelehnt wird, wodurch der gelöschte Text dort bleibt, wo er war.
Assert.IsTrue(runs[5].IsDeleteRevision);
```

### Siehe auch

* class [Node](../node/)
* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
