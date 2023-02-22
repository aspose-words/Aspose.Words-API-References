---
title: DocumentBuilder.InsertParagraph
second_title: Aspose.Words für .NET-API-Referenz
description: DocumentBuilder methode. Fügt einen Absatzumbruch in das Dokument ein.
type: docs
weight: 400
url: /de/net/aspose.words/documentbuilder/insertparagraph/
---
## DocumentBuilder.InsertParagraph method

Fügt einen Absatzumbruch in das Dokument ein.

```csharp
public Paragraph InsertParagraph()
```

### Rückgabewert

Der soeben eingefügte Absatzknoten. Es ist derselbe Knoten wie[`CurrentParagraph`](../currentparagraph/).

### Bemerkungen

Aktuelle Absatzformatierung durch die vorgegeben[`ParagraphFormat`](../paragraphformat/) Eigentum verwendet wird.

Teilt den aktuellen Absatz in zwei Teile. Nach dem Einfügen des Absatzes steht der Cursor am Anfang des neuen Absatzes.

### Beispiele

Zeigt, wie Sie einen Absatz in das Dokument einfügen.

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

// Die Methode "Writeln" beendet den Absatz nach dem Anhängen von Text
// und beginnt dann eine neue Zeile und fügt einen neuen Absatz hinzu.
builder.Writeln("Hello world!");

Assert.True(builder.CurrentParagraph.IsEndOfDocument);
```

### Siehe auch

* class [Paragraph](../../paragraph/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../documentbuilder/)
* Montage [Aspose.Words](../../../)


