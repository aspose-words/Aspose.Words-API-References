---
title: Font.TintAndShade
linktitle: TintAndShade
articleTitle: TintAndShade
second_title: Aspose.Words per .NET
description: Scopri la proprietà Font TintAndShade per regolare facilmente i colori! Schiarisci o scurisci le tonalità per design vivaci. Migliora i tuoi progetti senza sforzo!
type: docs
weight: 530
url: /it/net/aspose.words/font/tintandshade/
---
## Font.TintAndShade property

Ottiene o imposta un valore double che schiarisce o scurisce un colore.

```csharp
public double TintAndShade { get; set; }
```

### Eccezioni

| eccezione | condizione |
| --- | --- |
| ArgumentOutOfRangeException | Genera un'eccezione se si imposta questa proprietà su un valore inferiore a -1 o superiore a 1. |
| InvalidOperationException | Lancia se imposta questa proprietà per[`Font`](../) oggetto con colori non tematici. |

## Osservazioni

I valori consentiti per questa proprietà sono compresi tra -1 (il più scuro) e 1 (il più chiaro).

Zero (0) è neutro.

## Esempi

Mostra come creare e utilizzare uno stile a tema.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln();

// Crea uno stile con le proprietà del font del tema.
Style style = doc.Styles.Add(StyleType.Paragraph, "ThemedStyle");
style.Font.ThemeFont = ThemeFont.Major;
style.Font.ThemeColor = ThemeColor.Accent5;
style.Font.TintAndShade = 0.3;

builder.ParagraphFormat.StyleName = "ThemedStyle";
builder.Writeln("Text with themed style");
```

### Guarda anche

* class [Font](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
