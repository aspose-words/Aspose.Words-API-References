---
title: Border.LineWidth
linktitle: LineWidth
articleTitle: LineWidth
second_title: Aspose.Words für .NET
description: Passen Sie die Eigenschaft „Border LineWidth“ an, um die Rahmenstärke in Punkten anzupassen und so die Präzision und visuelle Attraktivität Ihres Designs zu verbessern.
type: docs
weight: 50
url: /de/net/aspose.words/border/linewidth/
---
## Border.LineWidth property

Ruft die Rahmenbreite in Punkten ab oder legt sie fest.

```csharp
public double LineWidth { get; set; }
```

## Bemerkungen

Wenn Sie bei keinem Linienstil eine Linienbreite größer als Null festlegen, wird der Linienstil automatisch in eine einzelne Linie geändert.

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
