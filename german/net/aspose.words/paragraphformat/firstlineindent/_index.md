---
title: ParagraphFormat.FirstLineIndent
linktitle: FirstLineIndent
articleTitle: FirstLineIndent
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie Sie mit der Eigenschaft „ParagraphFormat FirstLineIndent“ die Einzüge der ersten Zeile oder hängende Einzüge in Ihren Dokumenten einfach anpassen können, um die Lesbarkeit zu verbessern.
type: docs
weight: 120
url: /de/net/aspose.words/paragraphformat/firstlineindent/
---
## ParagraphFormat.FirstLineIndent property

Ruft den Wert (in Punkten) für eine erste Zeile oder einen hängenden Einzug ab oder legt ihn fest.

Verwenden Sie positive Werte, um den Einzug der ersten Zeile festzulegen, und negative Werte, um den hängenden Einzug festzulegen.

```csharp
public double FirstLineIndent { get; set; }
```

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

* class [ParagraphFormat](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
