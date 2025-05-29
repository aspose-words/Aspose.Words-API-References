---
title: ConvertUtil Class
linktitle: ConvertUtil
articleTitle: ConvertUtil
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aspose.Words.ConvertUtil-Klasse für die nahtlose Einheitenumrechnung. Verbessern Sie Ihre Dokumentenverarbeitung noch heute mit wichtigen Hilfsfunktionen!
type: docs
weight: 560
url: /de/net/aspose.words/convertutil/
---
## ConvertUtil class

Bietet Hilfsfunktionen zum Umrechnen zwischen verschiedenen Maßeinheiten.

Um mehr zu erfahren, besuchen Sie die[Umrechnung zwischen Maßeinheiten](https://docs.aspose.com/words/net/convert-between-measurement-units/) Dokumentationsartikel.

```csharp
public static class ConvertUtil
```

## Methoden

| Name | Beschreibung |
| --- | --- |
| static [InchToPoint](../../aspose.words/convertutil/inchtopoint/)(*double*) | Wandelt Zoll in Punkte um. |
| static [MillimeterToPoint](../../aspose.words/convertutil/millimetertopoint/)(*double*) | Wandelt Millimeter in Punkte um. |
| static [PixelToNewDpi](../../aspose.words/convertutil/pixeltonewdpi/)(*double, double, double*) | Konvertiert Pixel von einer Auflösung in eine andere. |
| static [PixelToPoint](../../aspose.words/convertutil/pixeltopoint/#pixeltopoint)(*double*) | Wandelt Pixel in Punkte mit 96 dpi um. |
| static [PixelToPoint](../../aspose.words/convertutil/pixeltopoint/#pixeltopoint_1)(*double, double*) | Wandelt Pixel in Punkte mit der angegebenen Pixelauflösung um. |
| static [PointToInch](../../aspose.words/convertutil/pointtoinch/)(*double*) | Konvertiert Punkte in Zoll. |
| static [PointToPixel](../../aspose.words/convertutil/pointtopixel/#pointtopixel)(*double*) | Wandelt Punkte in Pixel mit 96 dpi um. |
| static [PointToPixel](../../aspose.words/convertutil/pointtopixel/#pointtopixel_1)(*double, double*) | Wandelt Punkte in Pixel mit der angegebenen Pixelauflösung um. |

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

Zeigt, wie Seiteneigenschaften in Zoll angegeben werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Die „Seiteneinrichtung“ eines Abschnitts definiert die Größe der Seitenränder in Punkten.
// Wir können auch die Klasse „ConvertUtil“ verwenden, um eine vertrautere Maßeinheit zu verwenden,
// wie Zoll beim Definieren von Grenzen.
PageSetup pageSetup = builder.PageSetup;
pageSetup.TopMargin = ConvertUtil.InchToPoint(1.0);
pageSetup.BottomMargin = ConvertUtil.InchToPoint(2.0);
pageSetup.LeftMargin = ConvertUtil.InchToPoint(2.5);
pageSetup.RightMargin = ConvertUtil.InchToPoint(1.5);

// Ein Zoll sind 72 Punkte.
Assert.AreEqual(72.0d, ConvertUtil.InchToPoint(1));
Assert.AreEqual(1.0d, ConvertUtil.PointToInch(72));

// Fügen Sie Inhalt hinzu, um die neuen Ränder zu demonstrieren.
builder.Writeln($"This Text is {pageSetup.LeftMargin} points/{ConvertUtil.PointToInch(pageSetup.LeftMargin)} inches from the left, " +
                $"{pageSetup.RightMargin} points/{ConvertUtil.PointToInch(pageSetup.RightMargin)} inches from the right, " +
                $"{pageSetup.TopMargin} points/{ConvertUtil.PointToInch(pageSetup.TopMargin)} inches from the top, " +
                $"and {pageSetup.BottomMargin} points/{ConvertUtil.PointToInch(pageSetup.BottomMargin)} inches from the bottom of the page.");

doc.Save(ArtifactsDir + "UtilityClasses.PointsAndInches.docx");
```

### Siehe auch

* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
