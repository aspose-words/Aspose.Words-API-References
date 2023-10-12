---
title: Border.LineStyle
second_title: Aspose.Words für .NET-API-Referenz
description: Border eigendom. Ruft den Rahmenstil ab oder legt ihn fest.
type: docs
weight: 40
url: /de/net/aspose.words/border/linestyle/
---
## Border.LineStyle property

Ruft den Rahmenstil ab oder legt ihn fest.

```csharp
public LineStyle LineStyle { get; set; }
```

### Bemerkungen

Wenn Sie den Linienstil auf „Keine“ festlegen, wird die Linienbreite automatisch auf Null geändert.

### Beispiele

Zeigt, wie man eine von einem Rahmen umgebene Zeichenfolge in ein Dokument einfügt.

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
* namensraum [Aspose.Words](../../border/)
* Montage [Aspose.Words](../../../)


