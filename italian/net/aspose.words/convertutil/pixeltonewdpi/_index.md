---
title: ConvertUtil.PixelToNewDpi
second_title: Aspose.Words per .NET API Reference
description: ConvertUtil metodo. Converte i pixel da una risoluzione allaltra.
type: docs
weight: 30
url: /it/net/aspose.words/convertutil/pixeltonewdpi/
---
## ConvertUtil.PixelToNewDpi method

Converte i pixel da una risoluzione all'altra.

```csharp
public static int PixelToNewDpi(double pixels, double oldDpi, double newDpi)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| pixels | Double | Il valore da convertire. |
| oldDpi | Double | L'attuale risoluzione dpi (punti per pollice). |
| newDpi | Double | La nuova risoluzione dpi (punti per pollice). |

### Esempi

Mostra come utilizzare i punti di conversione in pixel con risoluzione predefinita e personalizzata.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Definisce la dimensione del margine superiore di questa sezione in pixel, secondo un DPI personalizzato.
const double myDpi = 192;

PageSetup pageSetup = builder.PageSetup;
pageSetup.TopMargin = ConvertUtil.PixelToPoint(100, myDpi);

Assert.AreEqual(37.5d, pageSetup.TopMargin, 0.01d);

// Al valore DPI predefinito di 96, un pixel corrisponde a 0,75 punti.
Assert.AreEqual(0.75d, ConvertUtil.PixelToPoint(1));

builder.Writeln($"This Text is {pageSetup.TopMargin} points/{ConvertUtil.PointToPixel(pageSetup.TopMargin, myDpi)} " +
                $"pixels (at a DPI of {myDpi}) from the top of the page.");

// Imposta un nuovo DPI e regola di conseguenza il valore del margine superiore.
const double newDpi = 300;
pageSetup.TopMargin = ConvertUtil.PixelToNewDpi(pageSetup.TopMargin, myDpi, newDpi);
Assert.AreEqual(59.0d, pageSetup.TopMargin, 0.01d);

builder.Writeln($"At a DPI of {newDpi}, the text is now {pageSetup.TopMargin} points/{ConvertUtil.PointToPixel(pageSetup.TopMargin, myDpi)} " +
                "pixels from the top of the page.");

doc.Save(ArtifactsDir + "UtilityClasses.PointsAndPixelsDpi.docx");
```

### Guarda anche

* class [ConvertUtil](../)
* spazio dei nomi [Aspose.Words](../../convertutil/)
* assemblea [Aspose.Words](../../../)


