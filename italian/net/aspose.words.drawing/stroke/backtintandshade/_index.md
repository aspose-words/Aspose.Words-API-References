---
title: Stroke.BackTintAndShade
linktitle: BackTintAndShade
articleTitle: BackTintAndShade
second_title: Aspose.Words per .NET
description: Regola facilmente il colore di sfondo del tuo tratto con Stroke BackTintAndShade. Controlla luci e ombre per una finitura perfetta.
type: docs
weight: 30
url: /it/net/aspose.words.drawing/stroke/backtintandshade/
---
## Stroke.BackTintAndShade property

Ottiene o imposta un valore double che schiarisce o scurisce il colore di sfondo del tratto.

```csharp
public double BackTintAndShade { get; set; }
```

## Osservazioni

I valori consentiti per questa proprietà sono compresi tra -1 (il più scuro) e 1 (il più chiaro). Zero (0) è neutro. Il tentativo di impostare questa proprietà su un valore inferiore a -1 o superiore a 1 risulta inArgumentOutOfRangeException.

## Esempi

Mostra come ripristinare il colore, la tinta e l'ombra del tema.

```csharp
Document doc = new Document(MyDir + "Stroke gradient outline.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Stroke stroke = shape.Stroke;
stroke.BackThemeColor = ThemeColor.Dark2;
stroke.BackTintAndShade = 0.2d;

doc.Save(ArtifactsDir + "Shape.StrokeBackThemeColors.docx");
```

### Guarda anche

* class [Stroke](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
