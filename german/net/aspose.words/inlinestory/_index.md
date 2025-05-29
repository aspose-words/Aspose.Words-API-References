---
title: InlineStory Class
linktitle: InlineStory
articleTitle: InlineStory
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.InlineStory, die wesentliche Basis für Inline-Knoten, die eine nahtlose Integration von Absätzen und Tabellen in Ihre Dokumente ermöglicht.
type: docs
weight: 3720
url: /de/net/aspose.words/inlinestory/
---
## InlineStory class

Basisklasse für Knoten auf Inline-Ebene, die Absätze und Tabellen enthalten können.

Um mehr zu erfahren, besuchen Sie die[Logische Ebenen von Knoten in einem Dokument](https://docs.aspose.com/words/net/logical-levels-of-nodes-in-a-document/) Dokumentationsartikel.

```csharp
public abstract class InlineStory : CompositeNode
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Count](../../aspose.words/compositenode/count/) { get; } | Ruft die Anzahl der unmittelbar untergeordneten Elemente dieses Knotens ab. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Gibt die benutzerdefinierte Knotenkennung an. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Ruft das Dokument ab, zu dem dieser Knoten gehört. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Ruft das erste untergeordnete Element des Knotens ab. |
| [FirstParagraph](../../aspose.words/inlinestory/firstparagraph/) { get; } | Ruft den ersten Absatz der Geschichte ab. |
| [Font](../../aspose.words/inlinestory/font/) { get; } | Bietet Zugriff auf die Schriftformatierung des Ankerzeichens dieses Objekts. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Rückgaben`WAHR` wenn dieser Knoten untergeordnete Knoten hat. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Rückgaben`WAHR` da dieser Knoten untergeordnete Knoten haben kann. |
| [IsDeleteRevision](../../aspose.words/inlinestory/isdeleterevision/) { get; } | Gibt „true“ zurück, wenn dieses Objekt in Microsoft Word gelöscht wurde, während die Änderungsverfolgung aktiviert war. |
| [IsInsertRevision](../../aspose.words/inlinestory/isinsertrevision/) { get; } | Gibt „true“ zurück, wenn dieses Objekt in Microsoft Word eingefügt wurde, während die Änderungsverfolgung aktiviert war. |
| [IsMoveFromRevision](../../aspose.words/inlinestory/ismovefromrevision/) { get; } | Rückgaben`WAHR` wenn dieses Objekt in Microsoft Word verschoben (gelöscht) wurde, während die Änderungsverfolgung aktiviert war. |
| [IsMoveToRevision](../../aspose.words/inlinestory/ismovetorevision/) { get; } | Rückgaben`WAHR` wenn dieses Objekt in Microsoft Word verschoben (eingefügt) wurde, während die Änderungsverfolgung aktiviert war. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Ruft das letzte untergeordnete Element des Knotens ab. |
| [LastParagraph](../../aspose.words/inlinestory/lastparagraph/) { get; } | Ruft den letzten Absatz der Geschichte ab. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Ruft den Knoten ab, der diesem Knoten unmittelbar folgt. |
| abstract [NodeType](../../aspose.words/node/nodetype/) { get; } | Ruft den Typ dieses Knotens ab. |
| [Paragraphs](../../aspose.words/inlinestory/paragraphs/) { get; } | Ruft eine Sammlung von Absätzen ab, die unmittelbare untergeordnete Elemente der Story sind. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Ruft den unmittelbar übergeordneten Knoten dieses Knotens ab. |
| [ParentParagraph](../../aspose.words/inlinestory/parentparagraph/) { get; } | Ruft das übergeordnete Element ab[`Paragraph`](../paragraph/) dieses Knotens. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Ruft den Knoten ab, der diesem Knoten unmittelbar vorausgeht. |
| [Range](../../aspose.words/node/range/) { get; } | Gibt einen[`Range`](../range/)Objekt, das den Teil eines Dokuments darstellt, der in diesem Knoten enthalten ist. |
| abstract [StoryType](../../aspose.words/inlinestory/storytype/) { get; } | Gibt den Typ der Story zurück. |
| [Tables](../../aspose.words/inlinestory/tables/) { get; } | Ruft eine Sammlung von Tabellen ab, die unmittelbare untergeordnete Elemente der Story sind. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| abstract [Accept](../../aspose.words/node/accept/)(*[DocumentVisitor](../documentvisitor/)*) | Nimmt einen Besucher auf. |
| abstract [AcceptEnd](../../aspose.words/compositenode/acceptend/)(*[DocumentVisitor](../documentvisitor/)*) | Ruft bei Implementierung in einer abgeleiteten Klasse die Methode VisitXXXEnd des angegebenen Dokumentbesuchers auf. |
| abstract [AcceptStart](../../aspose.words/compositenode/acceptstart/)(*[DocumentVisitor](../documentvisitor/)*) | Ruft bei Implementierung in einer abgeleiteten Klasse die Methode VisitXXXStart des angegebenen Dokumentbesuchers auf. |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | Fügt den angegebenen Knoten am Ende der Liste der untergeordneten Knoten für diesen Knoten hinzu. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Erstellt ein Duplikat des Knotens. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Erstellt einen Navigator, der zum Durchlaufen und Lesen von Knoten verwendet werden kann. |
| [EnsureMinimum](../../aspose.words/inlinestory/ensureminimum/)() | Wenn das letzte untergeordnete Element kein Absatz ist, wird ein leerer Absatz erstellt und angehängt. |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../nodetype/)*) | Ruft den ersten Vorfahren des angegebenen[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Ruft den ersten Vorgänger des angegebenen Objekttyps ab. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../nodetype/), int, bool*) | Gibt einen N-ten untergeordneten Knoten zurück, der dem angegebenen Typ entspricht. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../nodetype/), bool*) | Gibt eine Live-Sammlung von untergeordneten Knoten zurück, die dem angegebenen Typ entsprechen. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Bietet Unterstützung für die Iteration des For-Each-Stils über die untergeordneten Knoten dieses Knotens. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Ruft den Text dieses Knotens und aller seiner untergeordneten Knoten ab. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../node/)*) | Gibt den Index des angegebenen untergeordneten Knotens im untergeordneten Knoten-Array zurück. |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(*T, [Node](../node/)*) | Fügt den angegebenen Knoten unmittelbar nach dem angegebenen Referenzknoten ein. |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(*T, [Node](../node/)*) | Fügt den angegebenen Knoten unmittelbar vor dem angegebenen Referenzknoten ein. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../node/)*) | Ruft den nächsten Knoten gemäß dem Pre-Order-Tree-Traversal-Algorithmus ab. |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(*T*) | Fügt den angegebenen Knoten am Anfang der Liste der untergeordneten Knoten für diesen Knoten hinzu. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../node/)*) | Ruft den vorherigen Knoten gemäß dem Pre-Order-Tree-Traversal-Algorithmus ab. |
| [Remove](../../aspose.words/node/remove/)() | Entfernt sich selbst vom übergeordneten Element. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Entfernt alle untergeordneten Knoten des aktuellen Knotens. |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(*T*) | Entfernt den angegebenen untergeordneten Knoten. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Entfernt alle[`SmartTag`](../../aspose.words.markup/smarttag/) Nachkommenknoten des aktuellen Knotens. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | Wählt eine Liste von Knoten aus, die dem XPath-Ausdruck entsprechen. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | Wählt den ersten[`Node`](../node/) das dem XPath-Ausdruck entspricht. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../saveformat/)*) | Exportiert den Inhalt des Knotens in eine Zeichenfolge im angegebenen Format. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Exportiert den Inhalt des Knotens unter Verwendung der angegebenen Speicheroptionen in eine Zeichenfolge. |

## Bemerkungen

`InlineStory` ist ein Container für Knoten auf Blockebene[`Paragraph`](../paragraph/) Und[`Table`](../../aspose.words.tables/table/).

Die Klassen, die abgeleitet sind von`InlineStory` sind Inline-Knoten, die eigenen Text (Absätze und Tabellen) enthalten können. Beispielsweise kann ein[`Comment`](../comment/) Knoten enthält Text eines Kommentars und eines[`Footnote`](../../aspose.words.notes/footnote/) enthält den Text einer Fußnote.

## Beispiele

Zeigt, wie man einem Absatz einen Kommentar hinzufügt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Hello world!");

Comment comment = new Comment(doc, "John Doe", "JD", DateTime.Today);
builder.CurrentParagraph.AppendChild(comment);
builder.MoveTo(comment.AppendChild(new Paragraph(doc)));
builder.Write("Comment text.");

Assert.AreEqual(DateTime.Today, comment.DateTime);

    // In Microsoft Word können wir mit der rechten Maustaste auf diesen Kommentar im Dokumenttext klicken, um ihn zu bearbeiten oder darauf zu antworten.
doc.Save(ArtifactsDir + "InlineStory.AddComment.docx");
```

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

* class [CompositeNode](../compositenode/)
* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
