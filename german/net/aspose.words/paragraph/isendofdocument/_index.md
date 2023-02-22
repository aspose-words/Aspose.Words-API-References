---
title: Paragraph.IsEndOfDocument
second_title: Aspose.Words für .NET-API-Referenz
description: Paragraph eigendom. Wahr wenn dieser Absatz der letzte Absatz im letzten Abschnitt des Dokuments ist.
type: docs
weight: 60
url: /de/net/aspose.words/paragraph/isendofdocument/
---
## Paragraph.IsEndOfDocument property

Wahr, wenn dieser Absatz der letzte Absatz im letzten Abschnitt des Dokuments ist.

```csharp
public bool IsEndOfDocument { get; }
```

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

* class [Paragraph](../)
* namensraum [Aspose.Words](../../paragraph/)
* Montage [Aspose.Words](../../../)


