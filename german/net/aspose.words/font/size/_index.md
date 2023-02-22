---
title: Font.Size
second_title: Aspose.Words für .NET-API-Referenz
description: Font eigendom. Liest oder setzt die Schriftgröße in Punkt.
type: docs
weight: 340
url: /de/net/aspose.words/font/size/
---
## Font.Size property

Liest oder setzt die Schriftgröße in Punkt.

```csharp
public double Size { get; set; }
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

Zeigt, wie formatierter Text mit DocumentBuilder eingefügt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Schriftartformatierung angeben, dann Text hinzufügen.
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
* namensraum [Aspose.Words](../../font/)
* Montage [Aspose.Words](../../../)


