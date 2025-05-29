---
title: PageSetup.RightMargin
linktitle: RightMargin
articleTitle: RightMargin
second_title: Aspose.Words für .NET
description: Entdecken Sie die PageSetup RightMargin-Eigenschaft und passen Sie den rechten Rand einfach in Punkten an, um ein optimales Textlayout und eine verbesserte Dokumentpräsentation zu erzielen.
type: docs
weight: 370
url: /de/net/aspose.words/pagesetup/rightmargin/
---
## PageSetup.RightMargin property

Gibt den Abstand (in Punkten) zwischen dem rechten Seitenrand und der rechten Begrenzung des Fließtextes zurück oder legt ihn fest.

```csharp
public double RightMargin { get; set; }
```

## Beispiele

Zeigt, wie Sie Papiergröße, Ausrichtung, Ränder und andere Einstellungen für einen Abschnitt anpassen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.PageSetup.PaperSize = PaperSize.Legal;
builder.PageSetup.Orientation = Orientation.Landscape;
builder.PageSetup.TopMargin = ConvertUtil.InchToPoint(1.0);
builder.PageSetup.BottomMargin = ConvertUtil.InchToPoint(1.0);
builder.PageSetup.LeftMargin = ConvertUtil.InchToPoint(1.5);
builder.PageSetup.RightMargin = ConvertUtil.InchToPoint(1.5);
builder.PageSetup.HeaderDistance = ConvertUtil.InchToPoint(0.2);
builder.PageSetup.FooterDistance = ConvertUtil.InchToPoint(0.2);

builder.Writeln("Hello world!");

doc.Save(ArtifactsDir + "PageSetup.PageMargins.docx");
```

### Siehe auch

* class [PageSetup](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
