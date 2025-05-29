---
title: DocumentBuilder.InsertParagraph
linktitle: InsertParagraph
articleTitle: InsertParagraph
second_title: Aspose.Words für .NET
description: Verbessern Sie Ihre Dokumente mühelos mit der InsertParagraph-Methode von DocumentBuilder, die nahtlose Absatzumbrüche für eine bessere Lesbarkeit ermöglicht.
type: docs
weight: 450
url: /de/net/aspose.words/documentbuilder/insertparagraph/
---
## DocumentBuilder.InsertParagraph method

Fügt einen Absatzumbruch in das Dokument ein.

```csharp
public Paragraph InsertParagraph()
```

### Rückgabewert

Der Absatzknoten, der gerade eingefügt wurde. Es handelt sich um denselben Knoten wie[`CurrentParagraph`](../currentparagraph/).

## Bemerkungen

Aktuelle Absatzformatierung, festgelegt durch[`ParagraphFormat`](../paragraphformat/) Eigenschaft verwendet wird.

Teilt den aktuellen Absatz in zwei Teile. Nach dem Einfügen des Absatzes wird der Cursor an den Anfang des neuen Absatzes gesetzt.

Eine Ausnahme wird ausgelöst, wenn es nicht möglich ist, an der aktuellen Cursorposition einen Absatzumbruch einzufügen.

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

// Die Methode "Writeln" beendet den Absatz nach dem Anhängen von Text
// und beginnt dann eine neue Zeile und fügt einen neuen Absatz hinzu.
builder.Writeln("Hello world!");

Assert.True(builder.CurrentParagraph.IsEndOfDocument);
```

### Siehe auch

* class [Paragraph](../../paragraph/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
