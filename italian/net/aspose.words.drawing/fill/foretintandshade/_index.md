---
title: Fill.ForeTintAndShade
linktitle: ForeTintAndShade
articleTitle: ForeTintAndShade
second_title: Aspose.Words per .NET
description: Regola la proprietà ForeTintAndShade per schiarire o scurire facilmente il colore di primo piano, migliorando il tuo design con precisione e creatività.
type: docs
weight: 90
url: /it/net/aspose.words.drawing/fill/foretintandshade/
---
## Fill.ForeTintAndShade property

Ottiene o imposta un valore double che schiarisce o scurisce il colore di primo piano.

```csharp
public double ForeTintAndShade { get; set; }
```

### Eccezioni

| eccezione | condizione |
| --- | --- |
| ArgumentOutOfRangeException | Genera un'eccezione se si imposta questa proprietà su un valore inferiore a -1 o superiore a 1. |

## Osservazioni

I valori consentiti per questa proprietà sono compresi tra -1 (il più scuro) e 1 (il più chiaro).

Zero (0) è neutro.

## Esempi

Mostra come gestire l'illuminazione e l'oscuramento del colore del carattere in primo piano.

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
