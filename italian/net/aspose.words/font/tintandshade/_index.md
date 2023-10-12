---
title: Font.TintAndShade
second_title: Aspose.Words per .NET API Reference
description: Font proprietà. Ottiene o imposta un valore double che schiarisce o scurisce un colore.
type: docs
weight: 520
url: /it/net/aspose.words/font/tintandshade/
---
## Font.TintAndShade property

Ottiene o imposta un valore double che schiarisce o scurisce un colore.

```csharp
public double TintAndShade { get; set; }
```

### Osservazioni

I valori consentiti sono compresi nell'intervallo da -1 (più scuro) a 1 (più chiaro) per questa proprietà. Zero (0) è neutro. Il tentativo di impostare questa proprietà su un valore inferiore a -1 o superiore a 1 genera unArgumentOutOfRangeException.

Impostazione di questa proprietà per[`Font`](../) oggetto con colori non tematici risulta in aInvalidOperationException.

### Esempi

Mostra come creare e utilizzare lo stile a tema.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln();

// Crea uno stile con le proprietà dei caratteri del tema.
Style style = doc.Styles.Add(StyleType.Paragraph, "ThemedStyle");
style.Font.ThemeFont = ThemeFont.Major;
style.Font.ThemeColor = ThemeColor.Accent5;
style.Font.TintAndShade = 0.3;

builder.ParagraphFormat.StyleName = "ThemedStyle";
builder.Writeln("Text with themed style");
```

### Guarda anche

* class [Font](../)
* spazio dei nomi [Aspose.Words](../../font/)
* assemblea [Aspose.Words](../../../)


