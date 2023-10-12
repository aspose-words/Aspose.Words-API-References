---
title: DocumentBuilder.MoveToBookmark
second_title: Aspose.Words für .NET-API-Referenz
description: DocumentBuilder methode. Bewegt den Cursor zu einem Lesezeichen.
type: docs
weight: 500
url: /de/net/aspose.words/documentbuilder/movetobookmark/
---
## MoveToBookmark(string) {#movetobookmark}

Bewegt den Cursor zu einem Lesezeichen.

```csharp
public bool MoveToBookmark(string bookmarkName)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| bookmarkName | String | Der Name des Lesezeichens, zu dem der Cursor bewegt werden soll. |

### Rückgabewert

`WAHR` ob das Lesezeichen gefunden wurde;`FALSCH` ansonsten.

### Bemerkungen

Bewegt den Cursor an eine Position unmittelbar nach dem Anfang des Lesezeichens mit dem angegebenen Namen.

Beim Vergleich wird die Groß-/Kleinschreibung nicht beachtet. Wenn das Lesezeichen nicht gefunden wurde,`FALSCH` is wird zurückgegeben und der Cursor wird nicht bewegt.

Durch das Einfügen von neuem Text wird der vorhandene Text des Lesezeichens nicht ersetzt.

Beachten Sie, dass einige Lesezeichen im Dokument Formularfeldern zugewiesen sind. Wenn Sie zu einem solchen Lesezeichen wechseln und dort Text einfügen, wird der Text in den Formularfeldcode eingefügt. Obwohl dadurch das Formularfeld nicht ungültig wird, ist der eingefügte -Text nicht sichtbar, da er Teil des Feldcodes wird.

### Beispiele

Zeigt, wie der Cursor eines Document Builders zu verschiedenen Knoten in einem Dokument bewegt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Erstelle ein gültiges Lesezeichen, eine Entität, die aus Knoten besteht, die von einem Lesezeichen-Startknoten umgeben sind.
 // und ein Lesezeichen-Endknoten.
builder.StartBookmark("MyBookmark");
builder.Write("Bookmark contents.");
builder.EndBookmark("MyBookmark");

NodeCollection firstParagraphNodes = doc.FirstSection.Body.FirstParagraph.GetChildNodes(NodeType.Any, false);

Assert.AreEqual(NodeType.BookmarkStart, firstParagraphNodes[0].NodeType);
Assert.AreEqual(NodeType.Run, firstParagraphNodes[1].NodeType);
Assert.AreEqual("Bookmark contents.", firstParagraphNodes[1].GetText().Trim());
Assert.AreEqual(NodeType.BookmarkEnd, firstParagraphNodes[2].NodeType);

// Der Cursor des Document Builders steht immer vor dem Knoten, den wir zuletzt damit hinzugefügt haben.
// Wenn sich der Cursor des Builders am Ende des Dokuments befindet, ist sein aktueller Knoten null.
// Der vorherige Knoten ist der Lesezeichen-Endknoten, den wir zuletzt hinzugefügt haben.
// Durch das Hinzufügen neuer Knoten mit dem Builder werden diese an den letzten Knoten angehängt.
Assert.Null(builder.CurrentNode);

// Wenn wir einen anderen Teil des Dokuments mit dem Builder bearbeiten möchten,
// Wir müssen den Cursor auf den Knoten setzen, den wir bearbeiten möchten.
builder.MoveToBookmark("MyBookmark");

// Wenn Sie es in ein Lesezeichen verschieben, wird es zum ersten Knoten innerhalb der Start- und Endknoten des Lesezeichens verschoben, dem eingeschlossenen Lauf.
Assert.AreEqual(firstParagraphNodes[1], builder.CurrentNode);

// Wir können den Cursor auch so auf einen einzelnen Knoten bewegen.
builder.MoveTo(doc.FirstSection.Body.FirstParagraph.GetChildNodes(NodeType.Any, false)[0]);

Assert.AreEqual(NodeType.BookmarkStart, builder.CurrentNode.NodeType);
Assert.AreEqual(doc.FirstSection.Body.FirstParagraph, builder.CurrentParagraph);
Assert.IsTrue(builder.IsAtStartOfParagraph);

// Wir können bestimmte Methoden verwenden, um zum Anfang/Ende eines Dokuments zu gelangen.
builder.MoveToDocumentEnd();

Assert.IsTrue(builder.IsAtEndOfParagraph);

builder.MoveToDocumentStart();

Assert.IsTrue(builder.IsAtStartOfParagraph);
```

### Siehe auch

* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../documentbuilder/)
* Montage [Aspose.Words](../../../)

---

## MoveToBookmark(string, bool, bool) {#movetobookmark_1}

Bewegt den Cursor mit größerer Präzision zu einem Lesezeichen.

```csharp
public bool MoveToBookmark(string bookmarkName, bool isStart, bool isAfter)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| bookmarkName | String | Der Name des Lesezeichens, zu dem der Cursor bewegt werden soll. |
| isStart | Boolean | Wann`WAHR` , bewegt den Cursor an den Anfang des Lesezeichens. Wenn`FALSCH`, bewegt den Cursor an das Ende des Lesezeichens. |
| isAfter | Boolean | Wann`WAHR` , bewegt den Cursor hinter die Start- oder Endposition von bookmark . Wann`FALSCH`, verschiebt den Cursor vor die Start- oder Endposition von bookmark . |

### Rückgabewert

`WAHR` ob das Lesezeichen gefunden wurde;`FALSCH` ansonsten.

### Bemerkungen

Bewegt den Cursor an eine Position vor oder nach dem Anfang oder Ende des Lesezeichens.

Wenn die gewünschte Position nicht auf Inline-Ebene liegt, wird zum nächsten Absatz gewechselt.

Beim Vergleich wird die Groß-/Kleinschreibung nicht beachtet. Wenn das Lesezeichen nicht gefunden wurde,`FALSCH` is wird zurückgegeben und der Cursor wird nicht bewegt.

### Beispiele

Zeigt, wie der Knoteneinfügepunkt-Cursor eines Document Builders zu einem Lesezeichen verschoben wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ein gültiges Lesezeichen besteht aus einem BookmarkStart-Knoten, einem BookmarkEnd-Knoten mit einem
// passender Lesezeichenname irgendwo danach und von diesen Knoten eingeschlossener Inhalt.
builder.StartBookmark("MyBookmark");
builder.Write("Hello world! ");
builder.EndBookmark("MyBookmark");

// Es gibt vier Möglichkeiten, den Cursor eines Document Builders auf ein Lesezeichen zu bewegen.
// Wenn wir uns zwischen den Knoten BookmarkStart und BookmarkEnd befinden, befindet sich der Cursor innerhalb des Lesezeichens.
// Dies bedeutet, dass jeder vom Builder hinzugefügte Text Teil des Lesezeichens wird.
// 1 – Außerhalb des Lesezeichens, vor dem BookmarkStart-Knoten:
Assert.True(builder.MoveToBookmark("MyBookmark", true, false));
builder.Write("1. ");

Assert.AreEqual("Hello world! ", doc.Range.Bookmarks["MyBookmark"].Text);
Assert.AreEqual("1. Hello world!", doc.GetText().Trim());

// 2 – Im Lesezeichen, direkt nach dem BookmarkStart-Knoten:
Assert.True(builder.MoveToBookmark("MyBookmark", true, true));
builder.Write("2. ");

Assert.AreEqual("2. Hello world! ", doc.Range.Bookmarks["MyBookmark"].Text);
Assert.AreEqual("1. 2. Hello world!", doc.GetText().Trim());

// 2 – Innerhalb des Lesezeichens, direkt vor dem BookmarkEnd-Knoten:
Assert.True(builder.MoveToBookmark("MyBookmark", false, false));
builder.Write("3. ");

Assert.AreEqual("2. Hello world! 3. ", doc.Range.Bookmarks["MyBookmark"].Text);
Assert.AreEqual("1. 2. Hello world! 3.", doc.GetText().Trim());

// 4 – Außerhalb des Lesezeichens, nach dem BookmarkEnd-Knoten:
Assert.True(builder.MoveToBookmark("MyBookmark", false, true));
builder.Write("4.");

Assert.AreEqual("2. Hello world! 3. ", doc.Range.Bookmarks["MyBookmark"].Text);
Assert.AreEqual("1. 2. Hello world! 3. 4.", doc.GetText().Trim());
```

### Siehe auch

* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../documentbuilder/)
* Montage [Aspose.Words](../../../)


