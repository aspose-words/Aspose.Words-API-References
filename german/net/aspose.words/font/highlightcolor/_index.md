---
title: Font.HighlightColor
linktitle: HighlightColor
articleTitle: HighlightColor
second_title: Aspose.Words für .NET
description: Entdecken Sie die Font HighlightColor-Eigenschaft – passen Sie die Hervorhebungsfarbe Ihres Textes ganz einfach an, um die Lesbarkeit und die visuelle Attraktivität zu verbessern. Werten Sie Ihr Design auf!
type: docs
weight: 150
url: /de/net/aspose.words/font/highlightcolor/
---
## Font.HighlightColor property

Ruft die Hervorhebungsfarbe (Markierung) ab oder legt sie fest.

```csharp
public Color HighlightColor { get; set; }
```

## Beispiele

Zeigt, wie ein Textlauf mithilfe seiner Schriftarteigenschaft formatiert wird.

```csharp
Document doc = new Document();
Run run = new Run(doc, "Hello world!");

Aspose.Words.Font font = run.Font;
font.Name = "Courier New";
font.Size = 36;
font.HighlightColor = Color.Yellow;

doc.FirstSection.Body.FirstParagraph.AppendChild(run);
doc.Save(ArtifactsDir + "Font.CreateFormattedRun.docx");
```

### Siehe auch

* class [Font](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
