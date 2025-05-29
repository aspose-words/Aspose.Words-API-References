---
title: ConvertUtil.PointToPixel
linktitle: PointToPixel
articleTitle: PointToPixel
second_title: Aspose.Words per .NET
description: Converti facilmente i punti in pixel con il metodo PointToPixel di ConvertUtil, ottimizzato per 96 dpi. Migliora la precisione del tuo design oggi stesso!
type: docs
weight: 60
url: /it/net/aspose.words/convertutil/pointtopixel/
---
## PointToPixel(*double*) {#pointtopixel}

Converte i punti in pixel a 96 dpi.

```csharp
public static double PointToPixel(double points)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| points | Double | Il valore da convertire. |

## Osservazioni

1 pollice equivale a 72 punti.

## Esempi

Mostra come specificare le proprietà della pagina in pixel.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// L'impostazione di pagina di una sezione definisce la dimensione dei margini della pagina in punti.
// Possiamo anche utilizzare la classe "ConvertUtil" per utilizzare un'unità di misura diversa,
// come i pixel quando si definiscono i confini.
PageSetup pageSetup = builder.PageSetup;
pageSetup.TopMargin = ConvertUtil.PixelToPoint(100);
pageSetup.BottomMargin = ConvertUtil.PixelToPoint(200);
pageSetup.LeftMargin = ConvertUtil.PixelToPoint(225);
pageSetup.RightMargin = ConvertUtil.PixelToPoint(125);

// Un pixel equivale a 0,75 punti.
Assert.AreEqual(0.75d, ConvertUtil.PixelToPoint(1));
Assert.AreEqual(1.0d, ConvertUtil.PointToPixel(0.75));

// Il valore DPI predefinito utilizzato è 96.
Assert.AreEqual(0.75d, ConvertUtil.PixelToPoint(1, 96));

// Aggiungere contenuto per dimostrare i nuovi margini.
builder.Writeln($"This Text is {pageSetup.LeftMargin} points/{ConvertUtil.PointToPixel(pageSetup.LeftMargin)} pixels from the left, " +
                $"{pageSetup.RightMargin} points/{ConvertUtil.PointToPixel(pageSetup.RightMargin)} pixels from the right, " +
                $"{pageSetup.TopMargin} points/{ConvertUtil.PointToPixel(pageSetup.TopMargin)} pixels from the top, " +
                $"and {pageSetup.BottomMargin} points/{ConvertUtil.PointToPixel(pageSetup.BottomMargin)} pixels from the bottom of the page.");

doc.Save(ArtifactsDir + "UtilityClasses.PointsAndPixels.docx");
```

### Guarda anche

* class [ConvertUtil](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)

---

## PointToPixel(*double, double*) {#pointtopixel_1}

Converte i punti in pixel alla risoluzione pixel specificata.

```csharp
public static double PointToPixel(double points, double resolution)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| points | Double | Il valore da convertire. |
| resolution | Double | La risoluzione dpi (punti per pollice). |

## Osservazioni

1 pollice equivale a 72 punti.

## Esempi

Mostra come usare la conversione dei punti in pixel con risoluzione predefinita e personalizzata.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Definisci la dimensione del margine superiore di questa sezione in pixel, in base a un DPI personalizzato.
const double myDpi = 192;

PageSetup pageSetup = builder.PageSetup;
pageSetup.TopMargin = ConvertUtil.PixelToPoint(100, myDpi);

Assert.AreEqual(37.5d, pageSetup.TopMargin, 0.01d);

// Con il DPI predefinito di 96, un pixel equivale a 0,75 punti.
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
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
