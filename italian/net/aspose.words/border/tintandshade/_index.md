---
title: Border.TintAndShade
linktitle: TintAndShade
articleTitle: TintAndShade
second_title: Aspose.Words per .NET
description: Scopri Border TintAndShade, regola facilmente la luminosità del colore con un semplice doppio valore per straordinari miglioramenti del design. Perfetto per i tuoi progetti creativi!
type: docs
weight: 80
url: /it/net/aspose.words/border/tintandshade/
---
## Border.TintAndShade property

Ottiene o imposta un valore double che schiarisce o scurisce un colore.

```csharp
public double TintAndShade { get; set; }
```

### Eccezioni

| eccezione | condizione |
| --- | --- |
| ArgumentOutOfRangeException | Viene generato se si tenta di impostare questa proprietà su un valore inferiore a -1 o superiore a 1. |
| InvalidOperationException | Viene generato se si imposta questa proprietà per un oggetto Border con colori non a tema. |

## Osservazioni

valori consentiti per questa proprietà sono compresi tra -1 (il più scuro) e 1 (il più chiaro). Zero (0) è neutro.

## Esempi

Mostra come inserire un paragrafo con un bordo superiore.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Border topBorder = builder.ParagraphFormat.Borders.Top;
topBorder.LineWidth = 4.0d;
topBorder.LineStyle = LineStyle.DashSmallGap;
// Imposta ThemeColor solo quando è impostato LineWidth o LineStyle.
topBorder.ThemeColor = ThemeColor.Accent1;
topBorder.TintAndShade = 0.25d;

builder.Writeln("Text with a top border.");

doc.Save(ArtifactsDir + "Border.ParagraphTopBorder.docx");
```

### Guarda anche

* class [Border](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
