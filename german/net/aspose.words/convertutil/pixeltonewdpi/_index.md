---
title: ConvertUtil.PixelToNewDpi
second_title: Aspose.Words für .NET-API-Referenz
description: ConvertUtil methode. Konvertiert Pixel von einer Auflösung in eine andere.
type: docs
weight: 30
url: /de/net/aspose.words/convertutil/pixeltonewdpi/
---
## ConvertUtil.PixelToNewDpi method

Konvertiert Pixel von einer Auflösung in eine andere.

```csharp
public static int PixelToNewDpi(double pixels, double oldDpi, double newDpi)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| pixels | Double | Der zu konvertierende Wert. |
| oldDpi | Double | Die aktuelle dpi-Auflösung (Punkte pro Zoll). |
| newDpi | Double | Die neue dpi-Auflösung (Punkte pro Zoll). |

### Beispiele

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
* namensraum [Aspose.Words](../../convertutil/)
* Montage [Aspose.Words](../../../)


