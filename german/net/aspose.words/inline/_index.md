---
title: Inline
second_title: Aspose.Words für .NET-API-Referenz
description: Basisklasse für Knoten auf Inline-Ebene denen eine Zeichenformatierung zugeordnet werden kann die jedoch keine eigenen untergeordneten Knoten haben können.
type: docs
weight: 3060
url: /de/net/aspose.words/inline/
---
## Inline class

Basisklasse für Knoten auf Inline-Ebene, denen eine Zeichenformatierung zugeordnet werden kann, die jedoch keine eigenen untergeordneten Knoten haben können.

```csharp
public abstract class Inline : Node
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | Gibt die benutzerdefinierte Knotenkennung an. |
| virtual [Document](../../aspose.words/node/document) { get; } | Ruft das Dokument ab, zu dem dieser Knoten gehört. |
| [Font](../../aspose.words/inline/font) { get; } | Bietet Zugriff auf die Schriftformatierung dieses Objekts. |
| virtual [IsComposite](../../aspose.words/node/iscomposite) { get; } | Gibt wahr zurück, wenn dieser Knoten andere Knoten enthalten kann. |
| [IsDeleteRevision](../../aspose.words/inline/isdeleterevision) { get; } | Gibt „true“ zurück, wenn dieses Objekt in Microsoft Word gelöscht wurde, während die Änderungsnachverfolgung aktiviert war. |
| [IsFormatRevision](../../aspose.words/inline/isformatrevision) { get; } | Gibt „true“ zurück, wenn die Formatierung des Objekts in Microsoft Word geändert wurde, während die Änderungsverfolgung aktiviert war. |
| [IsInsertRevision](../../aspose.words/inline/isinsertrevision) { get; } | Gibt „true“ zurück, wenn dieses Objekt in Microsoft Word eingefügt wurde, während die Änderungsverfolgung aktiviert war. |
| [IsMoveFromRevision](../../aspose.words/inline/ismovefromrevision) { get; } | gibt zurück **Stimmt** wenn dieses Objekt in Microsoft Word verschoben (gelöscht) wurde, während die Änderungsnachverfolgung aktiviert war. |
| [IsMoveToRevision](../../aspose.words/inline/ismovetorevision) { get; } | gibt zurück **Stimmt** wenn dieses Objekt in Microsoft Word verschoben (eingefügt) wurde, während die Änderungsnachverfolgung aktiviert war. |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | Ruft den Knoten ab, der diesem Knoten unmittelbar folgt. |
| abstract [NodeType](../../aspose.words/node/nodetype) { get; } | Ruft den Typ dieses Knotens ab. |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | Ruft den unmittelbar übergeordneten Knoten dieses Knotens ab. |
| [ParentParagraph](../../aspose.words/inline/parentparagraph) { get; } | Ruft das übergeordnete Element ab[`Paragraph`](../paragraph) dieses Knotens. |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | Ruft den Knoten unmittelbar vor diesem Knoten ab. |
| [Range](../../aspose.words/node/range) { get; } | Gibt a zurück **Bereich** Objekt, das den Teil eines Dokuments darstellt, das in diesem Knoten enthalten ist. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| abstract [Accept](../../aspose.words/node/accept)(DocumentVisitor) | Akzeptiert einen Besucher. |
| [Clone](../../aspose.words/node/clone)(bool) | Erstellt ein Duplikat des Knotens. |
| [GetAncestor](../../aspose.words/node/getancestor)(NodeType) | Ruft den ersten Vorfahren der angegebenen ab[`NodeType`](../nodetype) . |
| [GetAncestor](../../aspose.words/node/getancestor)(Type) | Ruft den ersten Vorfahren des angegebenen Objekttyps ab. |
| virtual [GetText](../../aspose.words/node/gettext)() | Ruft den Text dieses Knotens und aller seiner Kinder ab. |
| [NextPreOrder](../../aspose.words/node/nextpreorder)(Node) | Ruft den nächsten Knoten gemäß dem Traversalalgorithmus des Vorbestellungsbaums ab. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder)(Node) | Ruft den vorherigen Knoten gemäß dem Traversalalgorithmus des Vorbestellungsbaums ab. |
| [Remove](../../aspose.words/node/remove)() | Entfernt sich selbst vom übergeordneten Element. |
| [ToString](../../aspose.words/node/tostring)(SaveFormat) | Exportiert den Inhalt des Knotens in einen String im angegebenen Format. |
| [ToString](../../aspose.words/node/tostring)(SaveOptions) | Exportiert den Inhalt des Knotens unter Verwendung der angegebenen Speicheroptionen in einen String. |

### Bemerkungen

Eine Klasse abgeleitet von **In der Reihe** kann ein Kind von sein **Absatz**.

### Beispiele

Zeigt, wie der Revisionstyp eines Inline-Knotens bestimmt wird.

```csharp
Document doc = new Document(MyDir + "Revision runs.docx");

// Wenn wir das Dokument bearbeiten, während die Option „Änderungen nachverfolgen“ unter „Überprüfen“ -> Verfolgung,
// in Microsoft Word aktiviert ist, zählen die von uns vorgenommenen Änderungen als Überarbeitungen.
// Wenn wir ein Dokument mit Aspose.Words bearbeiten, können wir mit der Nachverfolgung von Revisionen beginnen
// die Methode „StartTrackRevisions“ des Dokuments aufrufen und die Nachverfolgung mit der Methode „StopTrackRevisions“ beenden.
// Wir können entweder Überarbeitungen akzeptieren, um sie in das Dokument zu integrieren
// oder sie ablehnen, um die vorgeschlagene Änderung wirksam zu ändern.
Assert.AreEqual(6, doc.Revisions.Count);

// Der übergeordnete Knoten einer Revision ist der Lauf, den die Revision betrifft. Ein Lauf ist ein Inline-Knoten.
Run run = (Run)doc.Revisions[0].ParentNode;

Paragraph firstParagraph = run.ParentParagraph;
RunCollection runs = firstParagraph.Runs;

Assert.AreEqual(6, runs.ToArray().Length);

// Nachfolgend sind fünf Arten von Revisionen aufgeführt, die einen Inline-Knoten kennzeichnen können.
// 1 - Eine "insert"-Revision:
// Diese Überarbeitung tritt auf, wenn wir Text einfügen, während wir Änderungen verfolgen.
Assert.IsTrue(runs[2].IsInsertRevision);

// 2 - Eine "Format"-Revision:
// Diese Überarbeitung tritt auf, wenn wir die Formatierung von Text ändern, während wir Änderungen nachverfolgen.
Assert.IsTrue(runs[2].IsFormatRevision);

// 3 - Eine "Move from"-Revision:
// Wenn wir Text in Microsoft Word markieren und ihn dann an eine andere Stelle im Dokument ziehen
// Beim Nachverfolgen von Änderungen werden zwei Revisionen angezeigt.
// Die „move from“-Revision ist eine Kopie des ursprünglichen Textes, bevor wir ihn verschoben haben.
Assert.IsTrue(runs[4].IsMoveFromRevision);

// 4 - Eine "Verschieben"-Revision:
// Die "move to"-Revision ist der Text, den wir an seine neue Position im Dokument verschoben haben.
// „Move from“- und „move to“-Revisionen erscheinen paarweise für jede Move-Revision, die wir durchführen.
// Das Akzeptieren einer Move-Revision löscht die "Move from"-Revision und ihren Text,
// und behält den Text aus der "move to"-Revision.
// Das Ablehnen einer Move-Revision behält umgekehrt die "Move from"-Revision und löscht die "Move to"-Revision.
Assert.IsTrue(runs[1].IsMoveToRevision);

// 5 - Eine "Lösch"-Revision:
// Diese Überarbeitung tritt auf, wenn wir Text löschen, während wir Änderungen nachverfolgen. Wenn wir solchen Text löschen,
// es bleibt als Überarbeitung im Dokument, bis wir entweder die Überarbeitung akzeptieren,
// wodurch der Text endgültig gelöscht wird, oder die Überarbeitung abgelehnt wird, wodurch der von uns gelöschte Text dort bleibt, wo er war.
Assert.IsTrue(runs[5].IsDeleteRevision);
```

### Siehe auch

* class [Node](../node)
* namensraum [Aspose.Words](../../aspose.words)
* Montage [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
