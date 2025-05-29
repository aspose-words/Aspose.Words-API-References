---
title: Border.ThemeColor
linktitle: ThemeColor
articleTitle: ThemeColor
second_title: Aspose.Words per .NET
description: Scopri come utilizzare la proprietà Border ThemeColor per personalizzare la combinazione di colori e migliorare il tuo design con temi vivaci e personalizzati.
type: docs
weight: 70
url: /it/net/aspose.words/border/themecolor/
---
## Border.ThemeColor property

Ottiene o imposta il colore del tema nello schema di colori applicato associato a questo oggetto Border.

```csharp
public ThemeColor ThemeColor { get; set; }
```

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

* enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* class [Border](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
