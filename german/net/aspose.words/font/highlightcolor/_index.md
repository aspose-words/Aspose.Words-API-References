---
title: Font.HighlightColor
linktitle: HighlightColor
articleTitle: HighlightColor
second_title: Aspose.Words für .NET
description: Font HighlightColor eigendom. Ruft die Hervorhebungsfarbe Markerfarbe ab oder legt diese fest in C#.
type: docs
weight: 150
url: /de/net/aspose.words/font/highlightcolor/
---
## Font.HighlightColor property

Ruft die Hervorhebungsfarbe (Markerfarbe) ab oder legt diese fest.

```csharp
public Color HighlightColor { get; set; }
```

## Beispiele

Zeigt, wie eine Textzeile mithilfe ihrer Schriftarteigenschaft formatiert wird.

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
