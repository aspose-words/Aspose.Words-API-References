---
title: Footnote Class
linktitle: Footnote
articleTitle: Footnote
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Notes.Footnote, Ihr unverzichtbares Tool für die einfache und präzise Verwaltung von Fußnoten und Endnoten in Ihren Dokumenten.
type: docs
weight: 4950
url: /de/net/aspose.words.notes/footnote/
---
## Footnote class

Stellt einen Container für Text einer Fußnote oder Endnote dar.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Fußnoten und Endnoten](https://docs.aspose.com/words/net/working-with-footnote-and-endnote/) Dokumentationsartikel.

```csharp
public class Footnote : InlineStory
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [Footnote](footnote/)(*[DocumentBase](../../aspose.words/documentbase/), [FootnoteType](../footnotetype/)*) | Initialisiert eine Instanz des`Footnote` Klasse. |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [ActualReferenceMark](../../aspose.words.notes/footnote/actualreferencemark/) { get; } | Ruft den tatsächlichen Text des Referenzzeichens ab, das im Dokument für diese Fußnote angezeigt wird. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Ruft die Anzahl der unmittelbar untergeordneten Elemente dieses Knotens ab. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Gibt die benutzerdefinierte Knotenkennung an. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Ruft das Dokument ab, zu dem dieser Knoten gehört. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Ruft das erste untergeordnete Element des Knotens ab. |
| [FirstParagraph](../../aspose.words/inlinestory/firstparagraph/) { get; } | Ruft den ersten Absatz der Geschichte ab. |
| [Font](../../aspose.words/inlinestory/font/) { get; } | Bietet Zugriff auf die Schriftformatierung des Ankerzeichens dieses Objekts. |
| [FootnoteType](../../aspose.words.notes/footnote/footnotetype/) { get; } | Gibt einen Wert zurück, der angibt, ob es sich um eine Fußnote oder eine Endnote handelt. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Rückgaben`WAHR` wenn dieser Knoten untergeordnete Knoten hat. |
| [IsAuto](../../aspose.words.notes/footnote/isauto/) { get; set; } | Enthält einen Wert, der angibt, ob es sich um eine automatisch nummerierte Fußnote oder eine Fußnote mit benutzerdefiniertem Referenzzeichen handelt. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Rückgaben`WAHR` da dieser Knoten untergeordnete Knoten haben kann. |
| [IsDeleteRevision](../../aspose.words/inlinestory/isdeleterevision/) { get; } | Gibt „true“ zurück, wenn dieses Objekt in Microsoft Word gelöscht wurde, während die Änderungsverfolgung aktiviert war. |
| [IsInsertRevision](../../aspose.words/inlinestory/isinsertrevision/) { get; } | Gibt „true“ zurück, wenn dieses Objekt in Microsoft Word eingefügt wurde, während die Änderungsverfolgung aktiviert war. |
| [IsMoveFromRevision](../../aspose.words/inlinestory/ismovefromrevision/) { get; } | Rückgaben`WAHR` wenn dieses Objekt in Microsoft Word verschoben (gelöscht) wurde, während die Änderungsverfolgung aktiviert war. |
| [IsMoveToRevision](../../aspose.words/inlinestory/ismovetorevision/) { get; } | Rückgaben`WAHR` wenn dieses Objekt in Microsoft Word verschoben (eingefügt) wurde, während die Änderungsverfolgung aktiviert war. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Ruft das letzte untergeordnete Element des Knotens ab. |
| [LastParagraph](../../aspose.words/inlinestory/lastparagraph/) { get; } | Ruft den letzten Absatz der Geschichte ab. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Ruft den Knoten ab, der diesem Knoten unmittelbar folgt. |
| override [NodeType](../../aspose.words.notes/footnote/nodetype/) { get; } | RückgabenFootnote . |
| [Paragraphs](../../aspose.words/inlinestory/paragraphs/) { get; } | Ruft eine Sammlung von Absätzen ab, die unmittelbare untergeordnete Elemente der Story sind. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Ruft den unmittelbar übergeordneten Knoten dieses Knotens ab. |
| [ParentParagraph](../../aspose.words/inlinestory/parentparagraph/) { get; } | Ruft das übergeordnete Element ab[`Paragraph`](../../aspose.words/paragraph/) dieses Knotens. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Ruft den Knoten ab, der diesem Knoten unmittelbar vorausgeht. |
| [Range](../../aspose.words/node/range/) { get; } | Gibt einen[`Range`](../../aspose.words/range/)Objekt, das den Teil eines Dokuments darstellt, der in diesem Knoten enthalten ist. |
| [ReferenceMark](../../aspose.words.notes/footnote/referencemark/) { get; set; } | Ruft das benutzerdefinierte Referenzzeichen ab/legt es fest, das für diese Fußnote verwendet werden soll. Der Standardwert ist**leere Zeichenfolge** (Empty ), d. h. es werden automatisch nummerierte Fußnoten verwendet. |
| override [StoryType](../../aspose.words.notes/footnote/storytype/) { get; } | RückgabenFootnotes oderEndnotes . |
| [Tables](../../aspose.words/inlinestory/tables/) { get; } | Ruft eine Sammlung von Tabellen ab, die unmittelbare untergeordnete Elemente der Story sind. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| override [Accept](../../aspose.words.notes/footnote/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Nimmt einen Besucher auf. |
| override [AcceptEnd](../../aspose.words.notes/footnote/acceptend/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Akzeptiert einen Besucher für den Besuch des Endes der Fußnote. |
| override [AcceptStart](../../aspose.words.notes/footnote/acceptstart/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Akzeptiert einen Besucher für den Besuch des Anfangs der Fußnote. |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | Fügt den angegebenen Knoten am Ende der Liste der untergeordneten Knoten für diesen Knoten hinzu. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Erstellt ein Duplikat des Knotens. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Erstellt einen Navigator, der zum Durchlaufen und Lesen von Knoten verwendet werden kann. |
| [EnsureMinimum](../../aspose.words/inlinestory/ensureminimum/)() | Wenn das letzte untergeordnete Element kein Absatz ist, wird ein leerer Absatz erstellt und angehängt. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../../aspose.words/nodetype/)*) | Ruft den ersten Vorfahren des angegebenen[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Ruft den ersten Vorgänger des angegebenen Objekttyps ab. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../../aspose.words/nodetype/), int, bool*) | Gibt einen N-ten untergeordneten Knoten zurück, der dem angegebenen Typ entspricht. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../../aspose.words/nodetype/), bool*) | Gibt eine Live-Sammlung von untergeordneten Knoten zurück, die dem angegebenen Typ entsprechen. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Bietet Unterstützung für die Iteration des For-Each-Stils über die untergeordneten Knoten dieses Knotens. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Ruft den Text dieses Knotens und aller seiner untergeordneten Knoten ab. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../../aspose.words/node/)*) | Gibt den Index des angegebenen untergeordneten Knotens im untergeordneten Knoten-Array zurück. |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(*T, [Node](../../aspose.words/node/)*) | Fügt den angegebenen Knoten unmittelbar nach dem angegebenen Referenzknoten ein. |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(*T, [Node](../../aspose.words/node/)*) | Fügt den angegebenen Knoten unmittelbar vor dem angegebenen Referenzknoten ein. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../../aspose.words/node/)*) | Ruft den nächsten Knoten gemäß dem Pre-Order-Tree-Traversal-Algorithmus ab. |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(*T*) | Fügt den angegebenen Knoten am Anfang der Liste der untergeordneten Knoten für diesen Knoten hinzu. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../../aspose.words/node/)*) | Ruft den vorherigen Knoten gemäß dem Pre-Order-Tree-Traversal-Algorithmus ab. |
| [Remove](../../aspose.words/node/remove/)() | Entfernt sich selbst vom übergeordneten Element. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Entfernt alle untergeordneten Knoten des aktuellen Knotens. |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(*T*) | Entfernt den angegebenen untergeordneten Knoten. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Entfernt alle[`SmartTag`](../../aspose.words.markup/smarttag/) Nachkommenknoten des aktuellen Knotens. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | Wählt eine Liste von Knoten aus, die dem XPath-Ausdruck entsprechen. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | Wählt den ersten[`Node`](../../aspose.words/node/) das dem XPath-Ausdruck entspricht. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../../aspose.words/saveformat/)*) | Exportiert den Inhalt des Knotens in eine Zeichenfolge im angegebenen Format. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Exportiert den Inhalt des Knotens unter Verwendung der angegebenen Speicheroptionen in eine Zeichenfolge. |

## Bemerkungen

Der`Footnote` Die Klasse wird verwendet, um sowohl Fußnoten als auch Endnoten in einem Word-Dokument darzustellen.

`Footnote` ist ein Inline-Level-Knoten und kann nur ein Kind von[`Paragraph`](../../aspose.words/paragraph/).

`Footnote` kann enthalten[`Paragraph`](../../aspose.words/paragraph/) Und[`Table`](../../aspose.words.tables/table/) untergeordnete Knoten.

## Beispiele

Zeigt, wie Fußnoten eingefügt und angepasst werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Text hinzufügen und mit einer Fußnote darauf verweisen. Diese Fußnote enthält einen kleinen hochgestellten Verweis
// Markieren Sie nach dem Text, auf den verwiesen wird, und erstellen Sie einen Eintrag unter dem Haupttext am unteren Seitenrand.
// Dieser Eintrag enthält das Referenzzeichen und den Referenztext der Fußnote,
// die wir an die Methode „InsertFootnote“ des Dokument-Generators übergeben.
builder.Write("Main body text.");
Footnote footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

// Wenn diese Eigenschaft auf "true" gesetzt ist, dann ist das Referenzzeichen unserer Fußnote
// wird sein Index unter allen Fußnoten des Abschnitts sein.
// Dies ist die erste Fußnote, daher lautet das Referenzzeichen „1“.
Assert.True(footnote.IsAuto);

    // Wir können den Dokumentgenerator in die Fußnote verschieben, um den Referenztext zu bearbeiten.
builder.MoveTo(footnote.FirstParagraph);
builder.Write(" More text added by a DocumentBuilder.");
builder.MoveToDocumentEnd();

Assert.AreEqual("\u0002 Footnote text. More text added by a DocumentBuilder.", footnote.GetText().Trim());

builder.Write(" More main body text.");
footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

// Wir können ein benutzerdefiniertes Referenzzeichen festlegen, das die Fußnote anstelle ihrer Indexnummer verwendet.
footnote.ReferenceMark = "RefMark";

Assert.False(footnote.IsAuto);

// Ein Lesezeichen mit dem Flag "IsAuto" auf true wird immer noch seinen tatsächlichen Index anzeigen
// Auch wenn vorherige Lesezeichen benutzerdefinierte Referenzzeichen anzeigen, ist das Referenzzeichen dieses Lesezeichens eine „3“.
builder.Write(" More main body text.");
footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

Assert.True(footnote.IsAuto);

doc.Save(ArtifactsDir + "InlineStory.AddFootnote.docx");
```

### Siehe auch

* class [InlineStory](../../aspose.words/inlinestory/)
* namensraum [Aspose.Words.Notes](../../aspose.words.notes/)
* Montage [Aspose.Words](../../)
