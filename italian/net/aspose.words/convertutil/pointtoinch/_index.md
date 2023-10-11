---
title: ConvertUtil.PointToInch
second_title: Aspose.Words per .NET API Reference
description: ConvertUtil metodo. Converte i punti in pollici.
type: docs
weight: 50
url: /it/net/aspose.words/convertutil/pointtoinch/
---
## ConvertUtil.PointToInch method

Converte i punti in pollici.

```csharp
public static double PointToInch(double points)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| points | Double | Il valore da convertire. |

### Osservazioni

1 pollice equivale a 72 punti.

### Esempi

Mostra come specificare le proprietà della pagina in pollici.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// "Imposta pagina" di una sezione definisce la dimensione dei margini della pagina in punti.
// Possiamo anche usare la classe "ConvertUtil" per usare un'unità di misura più familiare,
// come pollici quando si definiscono i confini.
PageSetup pageSetup = builder.PageSetup;
pageSetup.TopMargin = ConvertUtil.InchToPoint(1.0);
pageSetup.BottomMargin = ConvertUtil.InchToPoint(2.0);
pageSetup.LeftMargin = ConvertUtil.InchToPoint(2.5);
pageSetup.RightMargin = ConvertUtil.InchToPoint(1.5);

// Un pollice equivale a 72 punti.
Assert.AreEqual(72.0d, ConvertUtil.InchToPoint(1));
Assert.AreEqual(1.0d, ConvertUtil.PointToInch(72));

// Aggiungi contenuto per dimostrare i nuovi margini.
builder.Writeln($"This Text is {pageSetup.LeftMargin} points/{ConvertUtil.PointToInch(pageSetup.LeftMargin)} inches from the left, " +
                $"{pageSetup.RightMargin} points/{ConvertUtil.PointToInch(pageSetup.RightMargin)} inches from the right, " +
                $"{pageSetup.TopMargin} points/{ConvertUtil.PointToInch(pageSetup.TopMargin)} inches from the top, " +
                $"and {pageSetup.BottomMargin} points/{ConvertUtil.PointToInch(pageSetup.BottomMargin)} inches from the bottom of the page.");

doc.Save(ArtifactsDir + "UtilityClasses.PointsAndInches.docx");
```

### Guarda anche

* class [ConvertUtil](../)
* spazio dei nomi [Aspose.Words](../../convertutil/)
* assemblea [Aspose.Words](../../../)


