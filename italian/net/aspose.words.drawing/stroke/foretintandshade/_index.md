---
title: Stroke.ForeTintAndShade
linktitle: ForeTintAndShade
articleTitle: ForeTintAndShade
second_title: Aspose.Words per .NET
description: Regola la proprietà Stroke ForeTintAndShade per schiarire o scurire senza sforzo il colore di primo piano del tratto, migliorando l'impatto visivo.
type: docs
weight: 150
url: /it/net/aspose.words.drawing/stroke/foretintandshade/
---
## Stroke.ForeTintAndShade property

Ottiene o imposta un valore double che schiarisce o scurisce il colore di primo piano del tratto.

```csharp
public double ForeTintAndShade { get; set; }
```

## Osservazioni

I valori consentiti per questa proprietà sono compresi tra -1 (il più scuro) e 1 (il più chiaro). Zero (0) è neutro. Il tentativo di impostare questa proprietà su un valore inferiore a -1 o superiore a 1 risulta inArgumentOutOfRangeException.

## Esempi

Mostra come impostare il colore, la tinta e l'ombra del tema principale.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.TextBox, 100, 40);
Stroke stroke = shape.Stroke;
stroke.ForeThemeColor = ThemeColor.Dark1;
stroke.ForeTintAndShade = 0.5;

doc.Save(ArtifactsDir + "Shape.StrokeForeThemeColors.docx");
```

### Guarda anche

* class [Stroke](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
