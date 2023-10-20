---
title: ConvertUtil.MillimeterToPoint
linktitle: MillimeterToPoint
articleTitle: MillimeterToPoint
second_title: Aspose.Words per .NET
description: ConvertUtil MillimeterToPoint metodo. Converte i millimetri in punti in C#.
type: docs
weight: 20
url: /it/net/aspose.words/convertutil/millimetertopoint/
---
## ConvertUtil.MillimeterToPoint method

Converte i millimetri in punti.

```csharp
public static double MillimeterToPoint(double millimeters)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| millimeters | Double | Il valore da convertire. |

## Osservazioni

1 pollice equivale a 25,4 millimetri. 1 pollice equivale a 72 punti.

## Esempi

Mostra come specificare le proprietà della pagina in millimetri.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// "Imposta pagina" di una sezione definisce la dimensione dei margini della pagina in punti.
// Possiamo anche usare la classe "ConvertUtil" per usare un'unità di misura più familiare,
// come i millimetri quando si definiscono i confini.
PageSetup pageSetup = builder.PageSetup;
pageSetup.TopMargin = ConvertUtil.MillimeterToPoint(30);
pageSetup.BottomMargin = ConvertUtil.MillimeterToPoint(50);
pageSetup.LeftMargin = ConvertUtil.MillimeterToPoint(80);
pageSetup.RightMargin = ConvertUtil.MillimeterToPoint(40);

// Un centimetro equivale a circa 28,3 punti.
Assert.AreEqual(28.34d, ConvertUtil.MillimeterToPoint(10), 0.01d);

// Aggiungi contenuto per dimostrare i nuovi margini.
builder.Writeln($"This Text is {pageSetup.LeftMargin} points from the left, " +
                $"{pageSetup.RightMargin} points from the right, " +
                $"{pageSetup.TopMargin} points from the top, " +
                $"and {pageSetup.BottomMargin} points from the bottom of the page.");

doc.Save(ArtifactsDir + "UtilityClasses.PointsAndMillimeters.docx");
```

### Guarda anche

* class [ConvertUtil](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
