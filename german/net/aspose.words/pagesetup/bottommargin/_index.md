---
title: PageSetup.BottomMargin
linktitle: BottomMargin
articleTitle: BottomMargin
second_title: Aspose.Words für .NET
description: Passen Sie das Layout Ihres Dokuments mit der Eigenschaft „PageSetup BottomMargin“ an und definieren Sie den Abstand zwischen der unteren Seitenkante und dem Fließtext für eine optimale Darstellung.
type: docs
weight: 80
url: /de/net/aspose.words/pagesetup/bottommargin/
---
## PageSetup.BottomMargin property

Gibt den Abstand (in Punkten) zwischen der unteren Seitenkante und der unteren Begrenzung des Fließtextes zurück oder legt ihn fest.

```csharp
public double BottomMargin { get; set; }
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
