---
title: Border.LineWidth
linktitle: LineWidth
articleTitle: LineWidth
second_title: Aspose.Words für .NET
description: Border LineWidth eigendom. Ruft die Rahmenbreite in Punkten ab oder legt sie fest in C#.
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

Wenn Sie die Linienbreite größer als Null festlegen, während der Linienstil „Keine“ ist, wird der Linienstil automatisch in „Einzeilig“ geändert.

## Beispiele

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

* class [Border](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
