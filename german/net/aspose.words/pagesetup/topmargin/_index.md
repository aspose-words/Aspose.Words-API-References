---
title: PageSetup.TopMargin
second_title: Aspose.Words für .NET-API-Referenz
description: PageSetup eigendom. Gibt den Abstand in Punkt zwischen dem oberen Rand der Seite und der oberen Grenze des Textkörpers zurück oder legt ihn fest.
type: docs
weight: 440
url: /de/net/aspose.words/pagesetup/topmargin/
---
## PageSetup.TopMargin property

Gibt den Abstand (in Punkt) zwischen dem oberen Rand der Seite und der oberen Grenze des Textkörpers zurück oder legt ihn fest.

```csharp
public double TopMargin { get; set; }
```

### Beispiele

Zeigt, wie Papiergröße, Ausrichtung, Ränder und andere Einstellungen für einen Abschnitt angepasst werden.

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
* namensraum [Aspose.Words](../../pagesetup/)
* Montage [Aspose.Words](../../../)


