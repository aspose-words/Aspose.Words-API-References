---
title: ShapeBase.RelativeHorizontalSize
linktitle: RelativeHorizontalSize
articleTitle: RelativeHorizontalSize
second_title: Aspose.Words per .NET
description: Scopri la proprietà ShapeBase RelativeHorizontalSize per regolare facilmente le dimensioni delle forme orizzontalmente, per una maggiore flessibilità e precisione nella progettazione.
type: docs
weight: 460
url: /it/net/aspose.words.drawing/shapebase/relativehorizontalsize/
---
## ShapeBase.RelativeHorizontalSize property

Ottiene o imposta il valore della dimensione relativa della forma in direzione orizzontale.

```csharp
public RelativeHorizontalSize RelativeHorizontalSize { get; set; }
```

## Osservazioni

Il valore predefinito è[`RelativeHorizontalSize`](../../relativehorizontalsize/).

Ha effetto solo se[`WidthRelative`](../widthrelative/) è impostato.

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

* enum [RelativeHorizontalSize](../../relativehorizontalsize/)
* class [ShapeBase](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
