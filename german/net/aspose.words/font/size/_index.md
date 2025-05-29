---
title: Font.Size
linktitle: Size
articleTitle: Size
second_title: Aspose.Words für .NET
description: Passen Sie die Schriftgröße mühelos mit der Eigenschaft „Schriftgröße“ an. Passen Sie Ihren Text in Punkten an, um die Lesbarkeit und das Design zu verbessern.
type: docs
weight: 350
url: /de/net/aspose.words/font/size/
---
## Font.Size property

Ruft die Schriftgröße in Punkten ab oder legt sie fest.

```csharp
public double Size { get; set; }
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

Zeigt, wie formatierter Text mit DocumentBuilder eingefügt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Geben Sie die Schriftformatierung an und fügen Sie dann Text hinzu.
Aspose.Words.Font font = builder.Font;
font.Size = 16;
font.Bold = true;
font.Color = Color.Blue;
font.Name = "Courier New";
font.Underline = Underline.Dash;

builder.Write("Hello world!");
```

### Siehe auch

* class [Font](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
