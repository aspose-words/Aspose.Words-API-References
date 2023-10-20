---
title: Fill.BackTintAndShade
linktitle: BackTintAndShade
articleTitle: BackTintAndShade
second_title: Aspose.Words per .NET
description: Fill BackTintAndShade proprietà. Ottiene o imposta un valore double che schiarisce o scurisce il colore di sfondo in C#.
type: docs
weight: 30
url: /it/net/aspose.words.drawing/fill/backtintandshade/
---
## Fill.BackTintAndShade property

Ottiene o imposta un valore double che schiarisce o scurisce il colore di sfondo.

```csharp
public double BackTintAndShade { get; set; }
```

## Osservazioni

I valori consentiti sono compresi nell'intervallo da -1 (il più scuro) a 1 (il più chiaro) per questa proprietà. Zero (0) è neutro. Il tentativo di impostare questa proprietà su un valore inferiore a -1 o superiore a 1 risulta inArgumentOutOfRangeException.

## Esempi

Mostra come impostare il colore del tema per il colore della forma di primo piano/sfondo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.RoundRectangle, 80, 80);

Fill fill = shape.Fill;
fill.ForeThemeColor = ThemeColor.Dark1;
fill.BackThemeColor = ThemeColor.Background2;

// Nota: non utilizzare "BackThemeColor" e "BackTintAndShade" per il riempimento dei caratteri.
if (fill.BackTintAndShade == 0)
    fill.BackTintAndShade = 0.2;

doc.Save(ArtifactsDir + "Shape.FillThemeColor.docx");
```

### Guarda anche

* class [Fill](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
