---
title: Font.HighlightColor
second_title: Aspose.Words für .NET-API-Referenz
description: Font eigendom. Ruft die Farbe der Hervorhebung Markierung ab oder legt sie fest.
type: docs
weight: 150
url: /de/net/aspose.words/font/highlightcolor/
---
## Font.HighlightColor property

Ruft die Farbe der Hervorhebung (Markierung) ab oder legt sie fest.

```csharp
public Color HighlightColor { get; set; }
```

### Beispiele

Zeigt, wie ein Textverlauf mithilfe seiner Eigenschaft font formatiert wird.

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
* namensraum [Aspose.Words](../../font/)
* Montage [Aspose.Words](../../../)


