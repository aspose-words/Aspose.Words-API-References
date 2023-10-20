---
title: ConvertUtil.PointToPixel
linktitle: PointToPixel
articleTitle: PointToPixel
second_title: Aspose.Words für .NET
description: ConvertUtil PointToPixel methode. Konvertiert Punkte in Pixel mit 96 dpi in C#.
type: docs
weight: 60
url: /de/net/aspose.words/convertutil/pointtopixel/
---
## PointToPixel(*double*) {#pointtopixel}

Konvertiert Punkte in Pixel mit 96 dpi.

```csharp
public static double PointToPixel(double points)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| points | Double | Der zu konvertierende Wert. |

## Bemerkungen

1 Zoll entspricht 72 Punkten.

## Beispiele

Zeigt, wie Seiteneigenschaften in Pixeln angegeben werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Die „Seiteneinrichtung“ eines Abschnitts definiert die Größe der Seitenränder in Punkten.
// Wir können auch die Klasse „ConvertUtil“ verwenden, um eine andere Maßeinheit zu verwenden,
// wie Pixel beim Definieren von Grenzen.
PageSetup pageSetup = builder.PageSetup;
pageSetup.TopMargin = ConvertUtil.PixelToPoint(100);
pageSetup.BottomMargin = ConvertUtil.PixelToPoint(200);
pageSetup.LeftMargin = ConvertUtil.PixelToPoint(225);
pageSetup.RightMargin = ConvertUtil.PixelToPoint(125);

// Ein Pixel ist 0,75 Punkte.
Assert.AreEqual(0.75d, ConvertUtil.PixelToPoint(1));
Assert.AreEqual(1.0d, ConvertUtil.PointToPixel(0.75));

// Der standardmäßig verwendete DPI-Wert ist 96.
Assert.AreEqual(0.75d, ConvertUtil.PixelToPoint(1, 96));

// Inhalt hinzufügen, um die neuen Ränder zu demonstrieren.
builder.Writeln($"This Text is {pageSetup.LeftMargin} points/{ConvertUtil.PointToPixel(pageSetup.LeftMargin)} pixels from the left, " +
                $"{pageSetup.RightMargin} points/{ConvertUtil.PointToPixel(pageSetup.RightMargin)} pixels from the right, " +
                $"{pageSetup.TopMargin} points/{ConvertUtil.PointToPixel(pageSetup.TopMargin)} pixels from the top, " +
                $"and {pageSetup.BottomMargin} points/{ConvertUtil.PointToPixel(pageSetup.BottomMargin)} pixels from the bottom of the page.");

doc.Save(ArtifactsDir + "UtilityClasses.PointsAndPixels.docx");
```

### Siehe auch

* class [ConvertUtil](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)

---

## PointToPixel(*double, double*) {#pointtopixel_1}

Konvertiert Punkte in Pixel mit der angegebenen Pixelauflösung.

```csharp
public static double PointToPixel(double points, double resolution)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| points | Double | Der zu konvertierende Wert. |
| resolution | Double | Die dpi-Auflösung (Punkte pro Zoll). |

## Bemerkungen

1 Zoll entspricht 72 Punkten.

## Beispiele

Zeigt, wie Punkte in Pixel mit Standardauflösung und benutzerdefinierter Auflösung konvertiert werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Definieren Sie die Größe des oberen Randes dieses Abschnitts in Pixel entsprechend einer benutzerdefinierten DPI.
const double myDpi = 192;

PageSetup pageSetup = builder.PageSetup;
pageSetup.TopMargin = ConvertUtil.PixelToPoint(100, myDpi);

Assert.AreEqual(37.5d, pageSetup.TopMargin, 0.01d);

// Bei der Standard-DPI von 96 beträgt ein Pixel 0,75 Punkte.
Assert.AreEqual(0.75d, ConvertUtil.PixelToPoint(1));

builder.Writeln($"This Text is {pageSetup.TopMargin} points/{ConvertUtil.PointToPixel(pageSetup.TopMargin, myDpi)} " +
                $"pixels (at a DPI of {myDpi}) from the top of the page.");

// Legen Sie einen neuen DPI-Wert fest und passen Sie den oberen Randwert entsprechend an.
const double newDpi = 300;
pageSetup.TopMargin = ConvertUtil.PixelToNewDpi(pageSetup.TopMargin, myDpi, newDpi);
Assert.AreEqual(59.0d, pageSetup.TopMargin, 0.01d);

builder.Writeln($"At a DPI of {newDpi}, the text is now {pageSetup.TopMargin} points/{ConvertUtil.PointToPixel(pageSetup.TopMargin, myDpi)} " +
                "pixels from the top of the page.");

doc.Save(ArtifactsDir + "UtilityClasses.PointsAndPixelsDpi.docx");
```

### Siehe auch

* class [ConvertUtil](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
