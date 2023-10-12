---
title: Border.TintAndShade
second_title: Aspose.Words per .NET API Reference
description: Border proprietà. Ottiene o imposta un valore double che schiarisce o scurisce un colore.
type: docs
weight: 80
url: /it/net/aspose.words/border/tintandshade/
---
## Border.TintAndShade property

Ottiene o imposta un valore double che schiarisce o scurisce un colore.

```csharp
public double TintAndShade { get; set; }
```

### Osservazioni

I valori consentiti sono compresi nell'intervallo da -1 (il più scuro) a 1 (il più chiaro) per questa proprietà. Zero (0) è neutro. Il tentativo di impostare questa proprietà su un valore inferiore a -1 o superiore a 1 risulta inArgumentOutOfRangeException.

L'impostazione di questa proprietà per l'oggetto Border con colori non tematici risulta in:InvalidOperationException.

### Esempi

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
* spazio dei nomi [Aspose.Words](../../border/)
* assemblea [Aspose.Words](../../../)


