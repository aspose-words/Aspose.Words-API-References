---
title: Border.LineStyle
linktitle: LineStyle
articleTitle: LineStyle
second_title: Aspose.Words für .NET
description: Passen Sie Ihr Design mit der Eigenschaft „Border LineStyle“ an. So können Sie ganz einfach einzigartige Rahmenstile abrufen oder festlegen, um die visuelle Attraktivität zu steigern.
type: docs
weight: 40
url: /de/net/aspose.words/border/linestyle/
---
## Border.LineStyle property

Ruft den Rahmenstil ab oder legt ihn fest.

```csharp
public LineStyle LineStyle { get; set; }
```

## Bemerkungen

Wenn Sie den Linienstil auf „Keine“ setzen, wird die Linienbreite automatisch auf Null geändert.

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

* enum [LineStyle](../../linestyle/)
* class [Border](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
