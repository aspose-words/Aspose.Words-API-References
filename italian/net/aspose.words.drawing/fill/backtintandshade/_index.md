---
title: Fill.BackTintAndShade
linktitle: BackTintAndShade
articleTitle: BackTintAndShade
second_title: Aspose.Words per .NET
description: Regola la proprietà BackTintAndShade per schiarire o scurire senza sforzo il colore di sfondo, migliorando l'aspetto visivo del tuo design e l'esperienza utente.
type: docs
weight: 30
url: /it/net/aspose.words.drawing/fill/backtintandshade/
---
## Fill.BackTintAndShade property

Ottiene o imposta un valore double che schiarisce o scurisce il colore di sfondo.

```csharp
public double BackTintAndShade { get; set; }
```

### Eccezioni

| eccezione | condizione |
| --- | --- |
| ArgumentOutOfRangeException | Genera un'eccezione se si imposta questa proprietà su un valore inferiore a -1 o superiore a 1. |

## Osservazioni

I valori consentiti per questa proprietà sono compresi tra -1 (il più scuro) e 1 (il più chiaro).

Zero (0) è neutro.

## Esempi

Mostra come impostare il colore del tema per il colore della forma in primo piano/sfondo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.RoundRectangle, 80, 80);

Fill fill = shape.Fill;
fill.ForeThemeColor = ThemeColor.Dark1;
fill.BackThemeColor = ThemeColor.Background2;

// Nota: non utilizzare "BackThemeColor" e "BackTintAndShade" per il riempimento del carattere.
if (fill.BackTintAndShade == 0)
    fill.BackTintAndShade = 0.2;

doc.Save(ArtifactsDir + "Shape.FillThemeColor.docx");
```

### Guarda anche

* class [Fill](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
