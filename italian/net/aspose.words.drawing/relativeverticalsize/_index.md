---
title: RelativeVerticalSize Enum
linktitle: RelativeVerticalSize
articleTitle: RelativeVerticalSize
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.Drawing.RelativeVerticalSize, che definisce i calcoli dell'altezza verticale per forme e cornici di testo, migliorando la precisione del layout del documento.
type: docs
weight: 1610
url: /it/net/aspose.words.drawing/relativeverticalsize/
---
## RelativeVerticalSize enumeration

Specifica in base a cosa viene calcolata l'altezza di una forma o di una cornice di testo in verticale.

```csharp
public enum RelativeVerticalSize
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Margin | `0` | Specifica che l'altezza viene calcolata in relazione allo spazio tra i margini superiore e inferiore. |
| Page | `1` | Specifica che l'altezza viene calcolata in relazione all'altezza della pagina. |
| TopMargin | `2` | Specifica che l'altezza viene calcolata in relazione alla dimensione dell'area del margine superiore. |
| BottomMargin | `3` | Specifica che l'altezza viene calcolata in relazione alla dimensione dell'area del margine inferiore. |
| InnerMargin | `4` | Specifica che l'altezza viene calcolata in relazione alla dimensione dell'area del margine interno, alla dimensione dell'area del margine superiore per le pagine dispari e alla dimensione dell'area del margine inferiore per le pagine pari. |
| OuterMargin | `5` | Specifica che l'altezza viene calcolata in relazione alla dimensione dell'area del margine esterno, alla dimensione dell'area del margine inferiore per le pagine dispari e alla dimensione dell'area del margine superiore per le pagine pari. |
| Default | `1` | Il valore predefinito èMargin . |

## Esempi

Mostra come impostare la dimensione e la posizione relative.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Aggiunta di una forma semplice con dimensione e posizione assolute.
Shape shape = builder.InsertShape(ShapeType.Rectangle, 100, 40);
// Imposta WrapType su WrapType.None poiché le forme in linea vengono automaticamente convertite in unità assolute.
shape.WrapType = WrapType.None;

// Controllo e impostazione della dimensione orizzontale relativa.
if (shape.RelativeHorizontalSize == RelativeHorizontalSize.Default)
{
    // Impostazione della rilegatura della dimensione orizzontale su Margine.
    shape.RelativeHorizontalSize = RelativeHorizontalSize.Margin;
    // Imposta la larghezza al 50% della larghezza del margine.
    shape.WidthRelative = 50;
}

// Controllo e impostazione della dimensione verticale relativa.
if (shape.RelativeVerticalSize == RelativeVerticalSize.Default)
{
    // Impostazione del limite di dimensione verticale su Margine.
    shape.RelativeVerticalSize = RelativeVerticalSize.Margin;
    // Imposta l'altezza al 30% dell'altezza del margine.
    shape.HeightRelative = 30;
}

// Controllo e impostazione della posizione verticale relativa.
if (shape.RelativeVerticalPosition == RelativeVerticalPosition.Paragraph)
{
    // impostazione del binding della posizione su TopMargin.
    shape.RelativeVerticalPosition = RelativeVerticalPosition.TopMargin;
    // Impostazione del valore Top relativo al 30% della posizione TopMargin.
    shape.TopRelative = 30;
}

// Controllo e impostazione della posizione orizzontale relativa.
if (shape.RelativeHorizontalPosition == RelativeHorizontalPosition.Default)
{
    // Impostazione del binding della posizione su RightMargin.
    shape.RelativeHorizontalPosition = RelativeHorizontalPosition.RightMargin;
    // Il valore relativo della posizione può essere negativo.
    shape.LeftRelative = -260;
}

doc.Save(ArtifactsDir + "Shape.RelativeSizeAndPosition.docx");
```

### Guarda anche

* property [RelativeVerticalSize](../shapebase/relativeverticalsize/)
* spazio dei nomi [Aspose.Words.Drawing](../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../)
