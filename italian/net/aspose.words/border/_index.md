---
title: Border Class
linktitle: Border
articleTitle: Border
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Border, la soluzione ideale per personalizzare i bordi degli oggetti nei documenti. Migliora i tuoi progetti con precisione e stile!
type: docs
weight: 270
url: /it/net/aspose.words/border/
---
## Border class

Rappresenta il bordo di un oggetto.

Per saperne di più, visita il[Programmazione con documenti](https://docs.aspose.com/words/net/programming-with-documents/) articolo di documentazione.

```csharp
public class Border : InternableComplexAttr
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Color](../../aspose.words/border/color/) { get; set; } | Ottiene o imposta il colore del bordo. |
| [DistanceFromText](../../aspose.words/border/distancefromtext/) { get; set; } | Ottiene o imposta la distanza del bordo dal testo o dal bordo della pagina in punti. |
| [IsVisible](../../aspose.words/border/isvisible/) { get; } | Restituisce`VERO` se il[`LineStyle`](./linestyle/) non èNone . |
| [LineStyle](../../aspose.words/border/linestyle/) { get; set; } | Ottiene o imposta lo stile del bordo. |
| [LineWidth](../../aspose.words/border/linewidth/) { get; set; } | Ottiene o imposta la larghezza del bordo in punti. |
| [Shadow](../../aspose.words/border/shadow/) { get; set; } | Ottiene o imposta un valore che indica se il bordo ha un'ombra. |
| [ThemeColor](../../aspose.words/border/themecolor/) { get; set; } | Ottiene o imposta il colore del tema nello schema di colori applicato associato a questo oggetto Border. |
| [TintAndShade](../../aspose.words/border/tintandshade/) { get; set; } | Ottiene o imposta un valore double che schiarisce o scurisce un colore. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [ClearFormatting](../../aspose.words/border/clearformatting/)() | Ripristina le proprietà del bordo ai valori predefiniti. |
| [Equals](../../aspose.words/border/equals/#equals)(*Border*) | Determina se il valore del bordo specificato è uguale al valore del bordo corrente. |
| override [Equals](../../aspose.words/border/equals/#equals_1)(*object*) | Determina se l'oggetto specificato ha un valore uguale all'oggetto corrente. |
| override [GetHashCode](../../aspose.words/border/gethashcode/)() | Serve come funzione hash per questo tipo. |

## Osservazioni

I bordi possono essere applicati a vari elementi del documento, tra cui paragrafi, sequenze di testo all'interno di un paragrafo o celle di una tabella.

## Esempi

Mostra come inserire una stringa circondata da un bordo in un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Border.Color = Color.Green;
builder.Font.Border.LineWidth = 2.5d;
builder.Font.Border.LineStyle = LineStyle.DashDotStroker;

builder.Write("Text surrounded by green border.");

doc.Save(ArtifactsDir + "Border.FontBorder.docx");
```

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

* class [InternableComplexAttr](../internablecomplexattr/)
* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)
