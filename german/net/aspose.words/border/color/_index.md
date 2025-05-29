---
title: Border.Color
linktitle: Color
articleTitle: Color
second_title: Aspose.Words für .NET
description: Passen Sie Ihre Designs mühelos mit der Eigenschaft „Rahmenfarbe“ an. So können Sie Rahmenfarben festlegen und ändern, um eine beeindruckende visuelle Wirkung zu erzielen.
type: docs
weight: 10
url: /de/net/aspose.words/border/color/
---
## Border.Color property

Ruft die Rahmenfarbe ab oder legt sie fest.

```csharp
public Color Color { get; set; }
```

## Beispiele

Zeigt, wie eine von einem Rahmen umgebene Zeichenfolge in ein Dokument eingefügt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Border.Color = Color.Green;
builder.Font.Border.LineWidth = 2.5d;
builder.Font.Border.LineStyle = LineStyle.DashDotStroker;

builder.Write("Text surrounded by green border.");

doc.Save(ArtifactsDir + "Border.FontBorder.docx");
```

### Siehe auch

* class [Border](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
