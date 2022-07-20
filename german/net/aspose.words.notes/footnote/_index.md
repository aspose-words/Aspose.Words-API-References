---
title: Footnote
second_title: Aspose.Words für .NET-API-Referenz
description: Repräsentiert einen Container für Text einer Fußnote oder Endnote.
type: docs
weight: 4020
url: /de/net/aspose.words.notes/footnote/
---
## Footnote class

Repräsentiert einen Container für Text einer Fußnote oder Endnote.

```csharp
public class Footnote : InlineStory
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [Footnote](footnote)(DocumentBase, FootnoteType) | Initialisiert eine Instanz von **Fußnote** Klasse. |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [ChildNodes](../../aspose.words/compositenode/childnodes) { get; } | Ruft alle unmittelbar untergeordneten Knoten dieses Knotens ab. |
| [Count](../../aspose.words/compositenode/count) { get; } | Ruft die Anzahl der unmittelbaren Kinder dieses Knotens ab. |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | Gibt die benutzerdefinierte Knotenkennung an. |
| virtual [Document](../../aspose.words/node/document) { get; } | Ruft das Dokument ab, zu dem dieser Knoten gehört. |
| [FirstChild](../../aspose.words/compositenode/firstchild) { get; } | Ruft das erste untergeordnete Element des Knotens ab. |
| [FirstParagraph](../../aspose.words/inlinestory/firstparagraph) { get; } | Ruft den ersten Absatz in der Geschichte ab. |
| [Font](../../aspose.words/inlinestory/font) { get; } | Bietet Zugriff auf die Schriftartformatierung des Ankerzeichens dieses Objekts. |
| [FootnoteType](../../aspose.words.notes/footnote/footnotetype) { get; } | Gibt einen Wert zurück, der angibt, ob es sich um eine Fuß- oder Endnote handelt. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes) { get; } | Gibt wahr zurück, wenn dieser Knoten untergeordnete Knoten hat. |
| [IsAuto](../../aspose.words.notes/footnote/isauto) { get; set; } | Enthält einen Wert, der angibt, ob es sich um eine automatisch nummerierte Fußnote oder eine Fußnote mit benutzerdefiniertem Referenzzeichen handelt. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite) { get; } | Gibt wahr zurück, da dieser Knoten untergeordnete Knoten haben kann. |
| [IsDeleteRevision](../../aspose.words/inlinestory/isdeleterevision) { get; } | Gibt „true“ zurück, wenn dieses Objekt in Microsoft Word gelöscht wurde, während die Änderungsnachverfolgung aktiviert war. |
| [IsInsertRevision](../../aspose.words/inlinestory/isinsertrevision) { get; } | Gibt „true“ zurück, wenn dieses Objekt in Microsoft Word eingefügt wurde, während die Änderungsverfolgung aktiviert war. |
| [IsMoveFromRevision](../../aspose.words/inlinestory/ismovefromrevision) { get; } | gibt zurück **Stimmt** wenn dieses Objekt in Microsoft Word verschoben (gelöscht) wurde, während die Änderungsnachverfolgung aktiviert war. |
| [IsMoveToRevision](../../aspose.words/inlinestory/ismovetorevision) { get; } | gibt zurück **Stimmt** wenn dieses Objekt in Microsoft Word verschoben (eingefügt) wurde, während die Änderungsnachverfolgung aktiviert war. |
| [LastChild](../../aspose.words/compositenode/lastchild) { get; } | Ruft das letzte untergeordnete Element des Knotens ab. |
| [LastParagraph](../../aspose.words/inlinestory/lastparagraph) { get; } | Ruft den letzten Absatz in der Story ab. |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | Ruft den Knoten ab, der diesem Knoten unmittelbar folgt. |
| override [NodeType](../../aspose.words.notes/footnote/nodetype) { get; } | gibt zurück **Knotentyp.Fußnote** . |
| [Paragraphs](../../aspose.words/inlinestory/paragraphs) { get; } | Ruft eine Sammlung von Absätzen ab, die der Geschichte direkt untergeordnet sind. |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | Ruft den unmittelbar übergeordneten Knoten dieses Knotens ab. |
| [ParentParagraph](../../aspose.words/inlinestory/parentparagraph) { get; } | Ruft das übergeordnete Element ab[`Paragraph`](../../aspose.words/paragraph) dieses Knotens. |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | Ruft den Knoten unmittelbar vor diesem Knoten ab. |
| [Range](../../aspose.words/node/range) { get; } | Gibt a zurück **Bereich** Objekt, das den Teil eines Dokuments darstellt, das in diesem Knoten enthalten ist. |
| [ReferenceMark](../../aspose.words.notes/footnote/referencemark) { get; set; } | Ruft/legt benutzerdefiniertes Referenzzeichen ab, das für diese Fußnote verwendet werden soll. Standardwert ist **leerer String** (Empty ), was bedeutet, dass automatisch nummerierte Fußnoten verwendet werden. |
| override [StoryType](../../aspose.words.notes/footnote/storytype) { get; } | gibt zurück **StoryType.Fußnoten** oder **StoryType.Endnotes** . |
| [Tables](../../aspose.words/inlinestory/tables) { get; } | Ruft eine Sammlung von Tabellen ab, die unmittelbar untergeordnete Elemente der Story sind. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| override [Accept](../../aspose.words.notes/footnote/accept)(DocumentVisitor) | Akzeptiert einen Besucher. |
| [AppendChild](../../aspose.words/compositenode/appendchild)(Node) | Fügt den angegebenen Knoten am Ende der Liste der untergeordneten Knoten für diesen Knoten hinzu. |
| [Clone](../../aspose.words/node/clone)(bool) | Erstellt ein Duplikat des Knotens. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator)() | Reserviert für Systemnutzung. IXPfadNavigierbar. |
| [EnsureMinimum](../../aspose.words/inlinestory/ensureminimum)() | Wenn das letzte untergeordnete Element kein Absatz ist, wird ein leerer Absatz erstellt und angehängt. |
| [GetAncestor](../../aspose.words/node/getancestor)(NodeType) | Ruft den ersten Vorfahren der angegebenen ab[`NodeType`](../../aspose.words/nodetype) . |
| [GetAncestor](../../aspose.words/node/getancestor)(Type) | Ruft den ersten Vorfahren des angegebenen Objekttyps ab. |
| [GetChild](../../aspose.words/compositenode/getchild)(NodeType, int, bool) | Gibt einen N-ten untergeordneten Knoten zurück, der dem angegebenen Typ entspricht. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes)(NodeType, bool) | Gibt eine Live-Sammlung von untergeordneten Knoten zurück, die dem angegebenen Typ entsprechen. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator)() | Bietet Unterstützung für die Iteration für jeden Stil über die untergeordneten Knoten dieses Knotens. |
| override [GetText](../../aspose.words/compositenode/gettext)() | Ruft den Text dieses Knotens und aller seiner Kinder ab. |
| [IndexOf](../../aspose.words/compositenode/indexof)(Node) | Gibt den Index des angegebenen untergeordneten Knotens im untergeordneten Knotenarray zurück. |
| [InsertAfter](../../aspose.words/compositenode/insertafter)(Node, Node) | Fügt den angegebenen Knoten unmittelbar nach dem angegebenen Referenzknoten ein. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore)(Node, Node) | Fügt den angegebenen Knoten unmittelbar vor dem angegebenen Referenzknoten ein. |
| [NextPreOrder](../../aspose.words/node/nextpreorder)(Node) | Ruft den nächsten Knoten gemäß dem Traversalalgorithmus des Vorbestellungsbaums ab. |
| [PrependChild](../../aspose.words/compositenode/prependchild)(Node) | Fügt den angegebenen Knoten am Anfang der Liste der untergeordneten Knoten für diesen Knoten hinzu. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder)(Node) | Ruft den vorherigen Knoten gemäß dem Traversalalgorithmus des Vorbestellungsbaums ab. |
| [Remove](../../aspose.words/node/remove)() | Entfernt sich selbst vom übergeordneten Element. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren)() | Entfernt alle untergeordneten Knoten des aktuellen Knotens. |
| [RemoveChild](../../aspose.words/compositenode/removechild)(Node) | Entfernt den angegebenen untergeordneten Knoten. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags)() | Entfernt alle[`SmartTag`](../../aspose.words.markup/smarttag) Nachkommenknoten des aktuellen Knotens. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes)(string) | Wählt eine Liste von Knoten aus, die mit dem XPath-Ausdruck übereinstimmen. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode)(string) | Wählt den ersten Knoten aus, der mit dem XPath-Ausdruck übereinstimmt. |
| [ToString](../../aspose.words/node/tostring)(SaveFormat) | Exportiert den Inhalt des Knotens in einen String im angegebenen Format. |
| [ToString](../../aspose.words/node/tostring)(SaveOptions) | Exportiert den Inhalt des Knotens unter Verwendung der angegebenen Speicheroptionen in einen String. |

### Bemerkungen

Das **Fußnote** -Klasse wird verwendet, um sowohl Fußnoten als auch Endnoten in einem Word-Dokument darzustellen.

**Fußnote** ist ein Knoten auf Inline-Ebene und kann nur ein Kind von sein **Absatz**.

**Fußnote** enthalten kann **Absatz** und **Tisch** untergeordnete Knoten.

### Beispiele

Zeigt, wie Fußnoten eingefügt und angepasst werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Text hinzufügen und mit einer Fußnote darauf verweisen. Diese Fußnote platziert einen kleinen hochgestellten Verweis
// Markieren Sie nach dem Text, auf den es verweist, und erstellen Sie einen Eintrag unter dem Haupttext unten auf der Seite.
// Dieser Eintrag enthält das Referenzzeichen der Fußnote und den Referenztext,
// die wir an die "InsertFootnote"-Methode des Dokumenterstellers übergeben.
builder.Write("Main body text.");
Footnote footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

// Wenn diese Eigenschaft auf "true" gesetzt ist, dann das Referenzzeichen unserer Fußnote
// wird sein Index unter allen Fußnoten des Abschnitts sein.
// Dies ist die erste Fußnote, also ist die Referenzmarke "1".
Assert.True(footnote.IsAuto);

// Wir können den Document Builder in die Fußnote verschieben, um seinen Referenztext zu bearbeiten. 
builder.MoveTo(footnote.FirstParagraph);
builder.Write(" More text added by a DocumentBuilder.");
builder.MoveToDocumentEnd();

Assert.AreEqual("\u0002 Footnote text. More text added by a DocumentBuilder.", footnote.GetText().Trim());

builder.Write(" More main body text.");
footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

// Wir können eine benutzerdefinierte Referenzmarke setzen, die die Fußnote anstelle ihrer Indexnummer verwendet.
footnote.ReferenceMark = "RefMark";

Assert.False(footnote.IsAuto);

// Ein Lesezeichen, bei dem das Flag "IsAuto" auf "true" gesetzt ist, zeigt immer noch seinen echten Index
// Auch wenn frühere Lesezeichen benutzerdefinierte Referenzzeichen anzeigen, ist das Referenzzeichen dieses Lesezeichens eine "3".
builder.Write(" More main body text.");
footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

Assert.True(footnote.IsAuto);

doc.Save(ArtifactsDir + "InlineStory.AddFootnote.docx");
```

### Siehe auch

* class [InlineStory](../../aspose.words/inlinestory)
* namensraum [Aspose.Words.Notes](../../aspose.words.notes)
* Montage [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
