---
title: Fill.ForeTintAndShade
linktitle: ForeTintAndShade
articleTitle: ForeTintAndShade
second_title: Aspose.Words per .NET
description: Fill ForeTintAndShade proprietà. Ottiene o imposta un valore double che schiarisce o scurisce il colore di primo piano in C#.
type: docs
weight: 80
url: /it/net/aspose.words.drawing/fill/foretintandshade/
---
## Fill.ForeTintAndShade property

Ottiene o imposta un valore double che schiarisce o scurisce il colore di primo piano.

```csharp
public double ForeTintAndShade { get; set; }
```

## Osservazioni

I valori consentiti sono compresi nell'intervallo da -1 (il più scuro) a 1 (il più chiaro) per questa proprietà. Zero (0) è neutro. Il tentativo di impostare questa proprietà su un valore inferiore a -1 o superiore a 1 risulta inArgumentOutOfRangeException.

## Esempi

Mostra come gestire lo schiarimento e lo scurimento del colore del carattere in primo piano.

```csharp
Document doc = new Document(MyDir + "Big document.docx");

Fill textFill = doc.FirstSection.Body.FirstParagraph.Runs[0].Font.Fill;
textFill.ForeThemeColor = ThemeColor.Accent1;
if (textFill.ForeTintAndShade == 0)
    textFill.ForeTintAndShade = 0.5;

doc.Save(ArtifactsDir + "Shape.FillTintAndShade.docx");
```

### Guarda anche

* class [Fill](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
