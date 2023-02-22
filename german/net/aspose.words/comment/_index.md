---
title: Class Comment
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Comment klas. Repräsentiert einen Container für den Text eines Kommentars.
type: docs
weight: 220
url: /de/net/aspose.words/comment/
---
## Comment class

Repräsentiert einen Container für den Text eines Kommentars.

```csharp
public sealed class Comment : InlineStory
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [Comment](comment/#constructor)(DocumentBase) | Initialisiert eine neue Instanz von **Kommentar** Klasse. |
| [Comment](comment/#constructor_1)(DocumentBase, string, string, DateTime) | Initialisiert eine neue Instanz von **Kommentar** Klasse. |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Ancestor](../../aspose.words/comment/ancestor/) { get; } | Gibt das übergeordnete Kommentarobjekt zurück. Gibt null für Kommentare der obersten Ebene zurück. |
| [Author](../../aspose.words/comment/author/) { get; set; } | Gibt den Autorennamen für einen Kommentar zurück oder legt ihn fest. |
| [ChildNodes](../../aspose.words/compositenode/childnodes/) { get; } | Ruft alle unmittelbar untergeordneten Knoten dieses Knotens ab. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Ruft die Anzahl der unmittelbaren Kinder dieses Knotens ab. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Gibt die benutzerdefinierte Knotenkennung an. |
| [DateTime](../../aspose.words/comment/datetime/) { get; set; } | Ruft das Datum und die Uhrzeit ab, zu der der Kommentar erstellt wurde. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Ruft das Dokument ab, zu dem dieser Knoten gehört. |
| [Done](../../aspose.words/comment/done/) { get; set; } | Ruft oder setzt Flag, das anzeigt, dass der Kommentar als erledigt markiert wurde. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Ruft das erste untergeordnete Element des Knotens ab. |
| [FirstParagraph](../../aspose.words/inlinestory/firstparagraph/) { get; } | Ruft den ersten Absatz in der Geschichte ab. |
| [Font](../../aspose.words/inlinestory/font/) { get; } | Bietet Zugriff auf die Schriftartformatierung des Ankerzeichens dieses Objekts. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Gibt wahr zurück, wenn dieser Knoten untergeordnete Knoten hat. |
| [Id](../../aspose.words/comment/id/) { get; } | Ruft die Kommentarkennung ab. |
| [Initial](../../aspose.words/comment/initial/) { get; set; } | Gibt die Initialen des Benutzers zurück, der einem bestimmten Kommentar zugeordnet ist, oder legt sie fest. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Gibt wahr zurück, da dieser Knoten untergeordnete Knoten haben kann. |
| [IsDeleteRevision](../../aspose.words/inlinestory/isdeleterevision/) { get; } | Gibt „true“ zurück, wenn dieses Objekt in Microsoft Word gelöscht wurde, während die Änderungsnachverfolgung aktiviert war. |
| [IsInsertRevision](../../aspose.words/inlinestory/isinsertrevision/) { get; } | Gibt „true“ zurück, wenn dieses Objekt in Microsoft Word eingefügt wurde, während die Änderungsverfolgung aktiviert war. |
| [IsMoveFromRevision](../../aspose.words/inlinestory/ismovefromrevision/) { get; } | gibt zurück **Stimmt** wenn dieses Objekt in Microsoft Word verschoben (gelöscht) wurde, während die Änderungsnachverfolgung aktiviert war. |
| [IsMoveToRevision](../../aspose.words/inlinestory/ismovetorevision/) { get; } | gibt zurück **Stimmt** wenn dieses Objekt in Microsoft Word verschoben (eingefügt) wurde, während die Änderungsnachverfolgung aktiviert war. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Ruft das letzte untergeordnete Element des Knotens ab. |
| [LastParagraph](../../aspose.words/inlinestory/lastparagraph/) { get; } | Ruft den letzten Absatz in der Story ab. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Ruft den Knoten ab, der diesem Knoten unmittelbar folgt. |
| override [NodeType](../../aspose.words/comment/nodetype/) { get; } | gibt zurück **Knotentyp.Kommentar** . |
| [Paragraphs](../../aspose.words/inlinestory/paragraphs/) { get; } | Ruft eine Sammlung von Absätzen ab, die der Geschichte direkt untergeordnet sind. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Ruft den unmittelbar übergeordneten Knoten dieses Knotens ab. |
| [ParentParagraph](../../aspose.words/inlinestory/parentparagraph/) { get; } | Ruft das übergeordnete Element ab[`Paragraph`](../paragraph/) dieses Knotens. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Ruft den Knoten unmittelbar vor diesem Knoten ab. |
| [Range](../../aspose.words/node/range/) { get; } | Gibt a zurück **Bereich** Objekt, das den Teil eines Dokuments darstellt, das in diesem Knoten enthalten ist. |
| [Replies](../../aspose.words/comment/replies/) { get; } | Gibt eine Sammlung von zurück`Comment` Objekte, die unmittelbar untergeordnete Elemente des angegebenen Kommentars sind. |
| override [StoryType](../../aspose.words/comment/storytype/) { get; } | gibt zurück **StoryType.Kommentare** . |
| [Tables](../../aspose.words/inlinestory/tables/) { get; } | Ruft eine Sammlung von Tabellen ab, die unmittelbar untergeordnete Elemente der Story sind. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| override [Accept](../../aspose.words/comment/accept/)(DocumentVisitor) | Akzeptiert einen Besucher. |
| [AddReply](../../aspose.words/comment/addreply/)(string, string, DateTime, string) | Fügt diesem Kommentar eine Antwort hinzu. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(Node) | Fügt den angegebenen Knoten am Ende der Liste der untergeordneten Knoten für diesen Knoten hinzu. |
| [Clone](../../aspose.words/node/clone/)(bool) | Erstellt ein Duplikat des Knotens. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Reserviert für Systemnutzung. IXPfadNavigierbar. |
| [EnsureMinimum](../../aspose.words/inlinestory/ensureminimum/)() | Wenn das letzte untergeordnete Element kein Absatz ist, wird ein leerer Absatz erstellt und angehängt. |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Ruft den ersten Vorfahren der angegebenen ab[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | Ruft den ersten Vorfahren des angegebenen Objekttyps ab. |
| [GetChild](../../aspose.words/compositenode/getchild/)(NodeType, int, bool) | Gibt einen N-ten untergeordneten Knoten zurück, der dem angegebenen Typ entspricht. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(NodeType, bool) | Gibt eine Live-Sammlung von untergeordneten Knoten zurück, die dem angegebenen Typ entsprechen. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Bietet Unterstützung für die Iteration für jeden Stil über die untergeordneten Knoten dieses Knotens. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Ruft den Text dieses Knotens und aller seiner Kinder ab. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(Node) | Gibt den Index des angegebenen untergeordneten Knotens im untergeordneten Knotenarray zurück. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(Node, Node) | Fügt den angegebenen Knoten unmittelbar nach dem angegebenen Referenzknoten ein. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(Node, Node) | Fügt den angegebenen Knoten unmittelbar vor dem angegebenen Referenzknoten ein. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | Ruft den nächsten Knoten gemäß dem Traversalalgorithmus des Vorbestellungsbaums ab. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(Node) | Fügt den angegebenen Knoten am Anfang der Liste der untergeordneten Knoten für diesen Knoten hinzu. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | Ruft den vorherigen Knoten gemäß dem Traversalalgorithmus des Vorbestellungsbaums ab. |
| [Remove](../../aspose.words/node/remove/)() | Entfernt sich selbst vom übergeordneten Element. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Entfernt alle untergeordneten Knoten des aktuellen Knotens. |
| [RemoveAllReplies](../../aspose.words/comment/removeallreplies/)() | Entfernt alle Antworten auf diesen Kommentar. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(Node) | Entfernt den angegebenen untergeordneten Knoten. |
| [RemoveReply](../../aspose.words/comment/removereply/)(Comment) | Entfernt die angegebene Antwort auf diesen Kommentar. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Entfernt alle[`SmartTag`](../../aspose.words.markup/smarttag/) Nachkommenknoten des aktuellen Knotens. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(string) | Wählt eine Liste von Knoten aus, die mit dem XPath-Ausdruck übereinstimmen. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(string) | Wählt den ersten Knoten aus, der mit dem XPath-Ausdruck übereinstimmt. |
| [SetText](../../aspose.words/comment/settext/)(string) | Dies ist eine bequeme Methode, mit der Sie den Text des Kommentars einfach festlegen können. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | Exportiert den Inhalt des Knotens in einen String im angegebenen Format. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | Exportiert den Inhalt des Knotens unter Verwendung der angegebenen Speicheroptionen in einen String. |

### Bemerkungen

Ein Kommentar ist eine Anmerkung, die an einem Textbereich oder an einer Stelle im Text verankert ist. Ein Kommentar kann beliebig viele Inhalte auf Blockebene enthalten.

Wenn ein`Comment` Objekt alleine auftritt, wird der Kommentar an der Position des verankert`Comment` Objekt.

Um einen Kommentar in einem Textbereich zu verankern, sind drei Objekte erforderlich:`Comment` , [`CommentRangeStart`](../commentrangestart/) und[`CommentRangeEnd`](../commentrangeend/) Alle drei Objekte müssen dasselbe teilen[`Id`](./id/) Wert.

`Comment` ist ein Knoten auf Inline-Ebene und kann nur ein Kind von sein[`Paragraph`](../paragraph/).

`Comment` enthalten kann[`Paragraph`](../paragraph/) und[`Table`](../../aspose.words.tables/table/) untergeordnete Knoten.

### Beispiele

Zeigt, wie Sie einem Absatz einen Kommentar hinzufügen.

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

Zeigt, wie Sie einem Dokument einen Kommentar hinzufügen und darauf antworten.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("My comment.");

// Platziere den Kommentar an einem Knoten im Hauptteil des Dokuments.
// Dieser Kommentar wird an der Stelle seines Absatzes angezeigt,
// außerhalb des rechten Rands der Seite und mit einer gepunkteten Linie, die ihn mit seinem Absatz verbindet.
builder.CurrentParagraph.AppendChild(comment);

// Füge eine Antwort hinzu, die unter dem übergeordneten Kommentar angezeigt wird.
comment.AddReply("Joe Bloggs", "J.B.", DateTime.Now, "New reply");

// Kommentare und Antworten sind beide Kommentarknoten.
Assert.AreEqual(2, doc.GetChildNodes(NodeType.Comment, true).Count);

// Kommentare, die nicht auf andere Kommentare antworten, sind "oberste Ebene". Sie haben keine Vorfahrenkommentare.
Assert.Null(comment.Ancestor);

// Antworten haben einen übergeordneten Kommentar auf oberster Ebene.
Assert.AreEqual(comment, comment.Replies[0].Ancestor);

doc.Save(ArtifactsDir + "Comment.AddCommentWithReply.docx");
```

### Siehe auch

* class [InlineStory](../inlinestory/)
* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)


