---
title: DocumentBuilder.InsertParagraph
linktitle: InsertParagraph
articleTitle: InsertParagraph
second_title: Aspose.Words für .NET
description: DocumentBuilder InsertParagraph methode. Fügt einen Absatzumbruch in das Dokument ein in C#.
type: docs
weight: 420
url: /de/net/aspose.words/documentbuilder/insertparagraph/
---
## DocumentBuilder.InsertParagraph method

Fügt einen Absatzumbruch in das Dokument ein.

```csharp
public Paragraph InsertParagraph()
```

### Rückgabewert

Der gerade eingefügte Absatzknoten. Es ist derselbe Knoten wie[`CurrentParagraph`](../currentparagraph/).

## Bemerkungen

Aktuelle Absatzformatierung, die durch angegeben wird[`ParagraphFormat`](../paragraphformat/) Eigentum genutzt wird.

Teilt den aktuellen Absatz in zwei Teile. Nach dem Einfügen des Absatzes wird der Cursor am Anfang des neuen Absatzes platziert.

Wenn es nicht möglich ist, an der aktuellen Cursorposition einen Absatzumbruch einzufügen, wird eine Ausnahme ausgelöst.

## Beispiele

Zeigt, wie ein Absatz in das Dokument eingefügt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Font font = builder.Font;
font.Size = 16;
font.Bold = true;
font.Color = Color.Blue;
font.Name = "Arial";
font.Underline = Underline.Dash;

ParagraphFormat paragraphFormat = builder.ParagraphFormat;
paragraphFormat.FirstLineIndent = 8;
paragraphFormat.Alignment = ParagraphAlignment.Justify;
paragraphFormat.AddSpaceBetweenFarEastAndAlpha = true;
paragraphFormat.AddSpaceBetweenFarEastAndDigit = true;
paragraphFormat.KeepTogether = true;

// Die Methode „Writeln“ beendet den Absatz nach dem Anhängen von Text
// und beginnt dann eine neue Zeile und fügt einen neuen Absatz hinzu.
builder.Writeln("Hello world!");

Assert.True(builder.CurrentParagraph.IsEndOfDocument);
```

### Siehe auch

* class [Paragraph](../../paragraph/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
