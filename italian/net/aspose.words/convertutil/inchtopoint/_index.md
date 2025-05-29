---
title: ConvertUtil.InchToPoint
linktitle: InchToPoint
articleTitle: InchToPoint
second_title: Aspose.Words per .NET
description: Converti senza sforzo i pollici in punti con il metodo InchToPoint di ConvertUtil. Migliora la tua precisione nella progettazione e nelle misurazioni oggi stesso!
type: docs
weight: 10
url: /it/net/aspose.words/convertutil/inchtopoint/
---
## ConvertUtil.InchToPoint method

Converte i pollici in punti.

```csharp
public static double InchToPoint(double inches)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inches | Double | Il valore da convertire. |

## Osservazioni

1 pollice equivale a 72 punti.

## Esempi

Mostra come regolare il formato della carta, l'orientamento, i margini e altre impostazioni per una sezione.

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

Mostra come specificare le proprietà della pagina in pollici.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// L'impostazione di pagina di una sezione definisce la dimensione dei margini della pagina in punti.
// Possiamo anche utilizzare la classe "ConvertUtil" per utilizzare un'unità di misura più familiare,
// come i pollici quando si definiscono i confini.
PageSetup pageSetup = builder.PageSetup;
pageSetup.TopMargin = ConvertUtil.InchToPoint(1.0);
pageSetup.BottomMargin = ConvertUtil.InchToPoint(2.0);
pageSetup.LeftMargin = ConvertUtil.InchToPoint(2.5);
pageSetup.RightMargin = ConvertUtil.InchToPoint(1.5);

// Un pollice equivale a 72 punti.
Assert.AreEqual(72.0d, ConvertUtil.InchToPoint(1));
Assert.AreEqual(1.0d, ConvertUtil.PointToInch(72));

// Aggiungere contenuto per dimostrare i nuovi margini.
builder.Writeln($"This Text is {pageSetup.LeftMargin} points/{ConvertUtil.PointToInch(pageSetup.LeftMargin)} inches from the left, " +
                $"{pageSetup.RightMargin} points/{ConvertUtil.PointToInch(pageSetup.RightMargin)} inches from the right, " +
                $"{pageSetup.TopMargin} points/{ConvertUtil.PointToInch(pageSetup.TopMargin)} inches from the top, " +
                $"and {pageSetup.BottomMargin} points/{ConvertUtil.PointToInch(pageSetup.BottomMargin)} inches from the bottom of the page.");

doc.Save(ArtifactsDir + "UtilityClasses.PointsAndInches.docx");
```

### Guarda anche

* class [ConvertUtil](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
