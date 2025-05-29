---
title: DocumentBuilder.MoveToBookmark
linktitle: MoveToBookmark
articleTitle: MoveToBookmark
second_title: Aspose.Words für .NET
description: Navigieren Sie mühelos durch Ihre Dokumente mit der MoveToBookmark-Methode von DocumentBuilder und positionieren Sie den Cursor zur verbesserten Bearbeitung sofort auf einem beliebigen Lesezeichen.
type: docs
weight: 530
url: /de/net/aspose.words/documentbuilder/movetobookmark/
---
## MoveToBookmark(*string*) {#movetobookmark}

Bewegt den Cursor zu einem Lesezeichen.

```csharp
public bool MoveToBookmark(string bookmarkName)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| bookmarkName | String | Der Name des Lesezeichens, zu dem der Cursor bewegt werden soll. |

### Rückgabewert

`WAHR` ob das Lesezeichen gefunden wurde;`FALSCH` ansonsten.

## Bemerkungen

Verschiebt den Cursor an eine Position direkt hinter dem Anfang des Lesezeichens mit dem angegebenen Namen.

Der Vergleich berücksichtigt keine Groß- und Kleinschreibung. Wenn das Lesezeichen nicht gefunden wurde,`FALSCH` is wird zurückgegeben und der Cursor wird nicht bewegt.

Durch das Einfügen von neuem Text wird der vorhandene Text des Lesezeichens nicht ersetzt.

Beachten Sie, dass einige Lesezeichen im Dokument Formularfeldern zugewiesen sind. Wenn Sie zu einem solchen Lesezeichen gehen und dort Text einfügen, wird dieser in den Formularfeldcode eingefügt. Dadurch wird das Formularfeld zwar nicht ungültig, der eingefügte Text ist jedoch nicht sichtbar, da er Teil des Feldcodes wird.

## Beispiele

Zeigt, wie der Cursor eines Dokument-Generators zu verschiedenen Knoten in einem Dokument bewegt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Erstelle ein gültiges Lesezeichen, eine Entität, die aus Knoten besteht, die von einem Lesezeichen-Startknoten umschlossen sind,
    // und ein Lesezeichen-Endknoten.
builder.StartBookmark("MyBookmark");
builder.Write("Bookmark contents.");
builder.EndBookmark("MyBookmark");

NodeCollection firstParagraphNodes = doc.FirstSection.Body.FirstParagraph.GetChildNodes(NodeType.Any, false);

Assert.AreEqual(NodeType.BookmarkStart, firstParagraphNodes[0].NodeType);
Assert.AreEqual(NodeType.Run, firstParagraphNodes[1].NodeType);
Assert.AreEqual("Bookmark contents.", firstParagraphNodes[1].GetText().Trim());
Assert.AreEqual(NodeType.BookmarkEnd, firstParagraphNodes[2].NodeType);

// Der Cursor des Dokumentgenerators befindet sich immer vor dem Knoten, den wir zuletzt damit hinzugefügt haben.
// Wenn sich der Cursor des Builders am Ende des Dokuments befindet, ist sein aktueller Knoten null.
// Der vorherige Knoten ist der Lesezeichen-Endknoten, den wir zuletzt hinzugefügt haben.
// Wenn Sie mit dem Builder neue Knoten hinzufügen, werden diese an den letzten Knoten angehängt.
Assert.Null(builder.CurrentNode);

// Wenn wir einen anderen Teil des Dokuments mit dem Builder bearbeiten möchten,
// Wir müssen den Cursor auf den Knoten bewegen, den wir bearbeiten möchten.
builder.MoveToBookmark("MyBookmark");

// Durch Verschieben in ein Lesezeichen wird es zum ersten Knoten innerhalb der Start- und Endknoten des Lesezeichens verschoben, dem eingeschlossenen Lauf.
Assert.AreEqual(firstParagraphNodes[1], builder.CurrentNode);

// Wir können den Cursor auch auf einen einzelnen Knoten wie diesen bewegen.
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
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)

---

## MoveToBookmark(*string, bool, bool*) {#movetobookmark_1}

Verschiebt den Cursor mit größerer Präzision zu einem Lesezeichen.

```csharp
public bool MoveToBookmark(string bookmarkName, bool isStart, bool isAfter)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| bookmarkName | String | Der Name des Lesezeichens, zu dem der Cursor bewegt werden soll. |
| isStart | Boolean | Wann`WAHR` , bewegt den Cursor an den Anfang des Lesezeichens. Wenn`FALSCH`, bewegt den Cursor an das Ende des Lesezeichens. |
| isAfter | Boolean | Wann`WAHR` verschiebt den Cursor hinter die Start- oder Endposition von bookmark . Wenn`FALSCH`verschiebt den Cursor vor die Start- oder Endposition von bookmark . |

### Rückgabewert

`WAHR` ob das Lesezeichen gefunden wurde;`FALSCH` ansonsten.

## Bemerkungen

Bewegt den Cursor an eine Position vor oder nach dem Anfang oder Ende des Lesezeichens.

Wenn die gewünschte Position nicht auf Inline-Ebene liegt, wird zum nächsten Absatz gewechselt.

Der Vergleich berücksichtigt keine Groß- und Kleinschreibung. Wenn das Lesezeichen nicht gefunden wurde,`FALSCH` is wird zurückgegeben und der Cursor wird nicht bewegt.

## Beispiele

Zeigt, wie der Cursor der Knoteneinfügemarke eines Dokument-Generators zu einem Lesezeichen verschoben wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ein gültiges Lesezeichen besteht aus einem BookmarkStart-Knoten, einem BookmarkEnd-Knoten mit einem
// passender Lesezeichenname irgendwo danach und Inhalt, der von diesen Knoten umschlossen wird.
builder.StartBookmark("MyBookmark");
builder.Write("Hello world! ");
builder.EndBookmark("MyBookmark");

// Es gibt 4 Möglichkeiten, den Cursor eines Dokumentgenerators zu einem Lesezeichen zu bewegen.
// Wenn wir uns zwischen den Knoten „BookmarkStart“ und „BookmarkEnd“ befinden, befindet sich der Cursor innerhalb des Lesezeichens.
// Dies bedeutet, dass jeder vom Builder hinzugefügte Text Teil des Lesezeichens wird.
// 1 – Außerhalb des Lesezeichens, vor dem Knoten „BookmarkStart“:
Assert.True(builder.MoveToBookmark("MyBookmark", true, false));
builder.Write("1. ");

Assert.AreEqual("Hello world! ", doc.Range.Bookmarks["MyBookmark"].Text);
Assert.AreEqual("1. Hello world!", doc.GetText().Trim());

// 2 – Innerhalb des Lesezeichens, direkt nach dem Knoten „BookmarkStart“:
Assert.True(builder.MoveToBookmark("MyBookmark", true, true));
builder.Write("2. ");

Assert.AreEqual("2. Hello world! ", doc.Range.Bookmarks["MyBookmark"].Text);
Assert.AreEqual("1. 2. Hello world!", doc.GetText().Trim());

// 2 – Innerhalb des Lesezeichens, direkt vor dem Knoten „BookmarkEnd“:
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
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
