---
title: Comment Class
linktitle: Comment
articleTitle: Comment
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aspose.Words.Comment-Klasse, Ihr unverzichtbares Tool zur Verwaltung von Kommentartexten in Dokumenten. Verbessern Sie Ihren Workflow durch nahtlose Integration!
type: docs
weight: 420
url: /de/net/aspose.words/comment/
---
## Comment class

Stellt einen Container für den Text eines Kommentars dar.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Kommentaren](https://docs.aspose.com/words/net/working-with-comments/) Dokumentationsartikel.

```csharp
public sealed class Comment : InlineStory
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [Comment](comment/#constructor)(*[DocumentBase](../documentbase/)*) | Initialisiert eine neue Instanz des`Comment` Klasse. |
| [Comment](comment/#constructor_1)(*[DocumentBase](../documentbase/), string, string, DateTime*) | Initialisiert eine neue Instanz des`Comment` Klasse. |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Ancestor](../../aspose.words/comment/ancestor/) { get; } | Gibt das übergeordnete Element zurück`Comment`Objekt. Gibt zurück`null` für Kommentare der obersten Ebene. |
| [Author](../../aspose.words/comment/author/) { get; set; } | Gibt den Autorennamen für einen Kommentar zurück oder legt ihn fest. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Ruft die Anzahl der unmittelbar untergeordneten Elemente dieses Knotens ab. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Gibt die benutzerdefinierte Knotenkennung an. |
| [DateTime](../../aspose.words/comment/datetime/) { get; set; } | Ruft das Datum und die Uhrzeit ab, zu der der Kommentar erstellt wurde. |
| [DateTimeUtc](../../aspose.words/comment/datetimeutc/) { get; } | Ruft das UTC-Datum und die UTC-Uhrzeit ab, zu der der Kommentar erstellt wurde. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Ruft das Dokument ab, zu dem dieser Knoten gehört. |
| [Done](../../aspose.words/comment/done/) { get; set; } | Ruft ein Flag ab oder legt es fest, das angibt, dass der Kommentar als erledigt markiert wurde. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Ruft das erste untergeordnete Element des Knotens ab. |
| [FirstParagraph](../../aspose.words/inlinestory/firstparagraph/) { get; } | Ruft den ersten Absatz der Geschichte ab. |
| [Font](../../aspose.words/inlinestory/font/) { get; } | Bietet Zugriff auf die Schriftformatierung des Ankerzeichens dieses Objekts. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Rückgaben`WAHR` wenn dieser Knoten untergeordnete Knoten hat. |
| [Id](../../aspose.words/comment/id/) { get; set; } | Ruft die Kommentarkennung ab oder legt sie fest. |
| [Initial](../../aspose.words/comment/initial/) { get; set; } | Gibt die Initialen des Benutzers zurück, der mit einem bestimmten Kommentar verknüpft ist, oder legt sie fest. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Rückgaben`WAHR` da dieser Knoten untergeordnete Knoten haben kann. |
| [IsDeleteRevision](../../aspose.words/inlinestory/isdeleterevision/) { get; } | Gibt „true“ zurück, wenn dieses Objekt in Microsoft Word gelöscht wurde, während die Änderungsverfolgung aktiviert war. |
| [IsInsertRevision](../../aspose.words/inlinestory/isinsertrevision/) { get; } | Gibt „true“ zurück, wenn dieses Objekt in Microsoft Word eingefügt wurde, während die Änderungsverfolgung aktiviert war. |
| [IsMoveFromRevision](../../aspose.words/inlinestory/ismovefromrevision/) { get; } | Rückgaben`WAHR` wenn dieses Objekt in Microsoft Word verschoben (gelöscht) wurde, während die Änderungsverfolgung aktiviert war. |
| [IsMoveToRevision](../../aspose.words/inlinestory/ismovetorevision/) { get; } | Rückgaben`WAHR` wenn dieses Objekt in Microsoft Word verschoben (eingefügt) wurde, während die Änderungsverfolgung aktiviert war. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Ruft das letzte untergeordnete Element des Knotens ab. |
| [LastParagraph](../../aspose.words/inlinestory/lastparagraph/) { get; } | Ruft den letzten Absatz der Geschichte ab. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Ruft den Knoten ab, der diesem Knoten unmittelbar folgt. |
| override [NodeType](../../aspose.words/comment/nodetype/) { get; } | RückgabenComment . |
| [Paragraphs](../../aspose.words/inlinestory/paragraphs/) { get; } | Ruft eine Sammlung von Absätzen ab, die unmittelbare untergeordnete Elemente der Story sind. |
| [ParentId](../../aspose.words/comment/parentid/) { get; set; } | Ruft die übergeordnete Kommentar-ID ab oder legt sie fest. Ein Wert von`-1` bedeutet, dass der Kommentar keinen übergeordneten Kommentar hat. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Ruft den unmittelbar übergeordneten Knoten dieses Knotens ab. |
| [ParentParagraph](../../aspose.words/inlinestory/parentparagraph/) { get; } | Ruft das übergeordnete Element ab[`Paragraph`](../paragraph/) dieses Knotens. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Ruft den Knoten ab, der diesem Knoten unmittelbar vorausgeht. |
| [Range](../../aspose.words/node/range/) { get; } | Gibt einen[`Range`](../range/)Objekt, das den Teil eines Dokuments darstellt, der in diesem Knoten enthalten ist. |
| [Replies](../../aspose.words/comment/replies/) { get; } | Gibt eine Sammlung von`Comment` Objekte, die unmittelbare untergeordnete Objekte des angegebenen Kommentars sind. |
| override [StoryType](../../aspose.words/comment/storytype/) { get; } | RückgabenComments . |
| [Tables](../../aspose.words/inlinestory/tables/) { get; } | Ruft eine Sammlung von Tabellen ab, die unmittelbare untergeordnete Elemente der Story sind. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| override [Accept](../../aspose.words/comment/accept/)(*[DocumentVisitor](../documentvisitor/)*) | Nimmt einen Besucher auf. |
| override [AcceptEnd](../../aspose.words/comment/acceptend/)(*[DocumentVisitor](../documentvisitor/)*) | Akzeptiert einen Besucher für den Besuch des Kommentarendes. |
| override [AcceptStart](../../aspose.words/comment/acceptstart/)(*[DocumentVisitor](../documentvisitor/)*) | Akzeptiert einen Besucher für den Besuch des Kommentaranfangs. |
| [AddReply](../../aspose.words/comment/addreply/)(*string, string, DateTime, string*) | Fügt eine Antwort auf diesen Kommentar hinzu. |
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
| [RemoveAllReplies](../../aspose.words/comment/removeallreplies/)() | Entfernt alle Antworten auf diesen Kommentar. |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(*T*) | Entfernt den angegebenen untergeordneten Knoten. |
| [RemoveReply](../../aspose.words/comment/removereply/)(*Comment*) | Entfernt die angegebene Antwort auf diesen Kommentar. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Entfernt alle[`SmartTag`](../../aspose.words.markup/smarttag/) Nachkommenknoten des aktuellen Knotens. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | Wählt eine Liste von Knoten aus, die dem XPath-Ausdruck entsprechen. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | Wählt den ersten[`Node`](../node/) das dem XPath-Ausdruck entspricht. |
| [SetText](../../aspose.words/comment/settext/)(*string*) | Dies ist eine praktische Methode, mit der sich der Kommentartext einfach festlegen lässt. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../saveformat/)*) | Exportiert den Inhalt des Knotens in eine Zeichenfolge im angegebenen Format. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Exportiert den Inhalt des Knotens unter Verwendung der angegebenen Speicheroptionen in eine Zeichenfolge. |

## Bemerkungen

Ein Kommentar ist eine Anmerkung, die an einem Textbereich oder einer Textposition verankert ist. Ein Kommentar kann eine beliebige Menge an Inhalten auf Blockebene enthalten.

Wenn ein`Comment` Objekt tritt allein auf, der Kommentar ist verankert an der Position des`Comment` Objekt.

Um einen Kommentar in einem Textbereich zu verankern, sind drei Objekte erforderlich:`Comment` , [`CommentRangeStart`](../commentrangestart/) Und[`CommentRangeEnd`](../commentrangeend/) . Alle drei Objekte müssen die gleiche [`Id`](./id/) Wert.

`Comment` ist ein Inline-Level-Knoten und kann nur ein Kind von[`Paragraph`](../paragraph/).

`Comment` kann enthalten[`Paragraph`](../paragraph/) Und[`Table`](../../aspose.words.tables/table/) untergeordnete Knoten.

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

Zeigt, wie Sie einem Dokument einen Kommentar hinzufügen und dann darauf antworten.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("My comment.");

// Platzieren Sie den Kommentar an einem Knoten im Hauptteil des Dokuments.
// Dieser Kommentar wird an der Stelle seines Absatzes angezeigt,
// außerhalb des rechten Seitenrands und mit einer gepunkteten Linie, die es mit dem Absatz verbindet.
builder.CurrentParagraph.AppendChild(comment);

// Fügen Sie eine Antwort hinzu, die unter dem übergeordneten Kommentar angezeigt wird.
comment.AddReply("Joe Bloggs", "J.B.", DateTime.Now, "New reply");

// Kommentare und Antworten sind beides Kommentarknoten.
Assert.AreEqual(2, doc.GetChildNodes(NodeType.Comment, true).Count);

// Kommentare, die nicht auf andere Kommentare antworten, sind „Top-Level“. Sie haben keine übergeordneten Kommentare.
Assert.Null(comment.Ancestor);

// Antworten haben einen übergeordneten Kommentar auf oberster Ebene.
Assert.AreEqual(comment, comment.Replies[0].Ancestor);

doc.Save(ArtifactsDir + "Comment.AddCommentWithReply.docx");
```

### Siehe auch

* class [InlineStory](../inlinestory/)
* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
