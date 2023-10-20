---
title: FrameFormat Class
linktitle: FrameFormat
articleTitle: FrameFormat
second_title: Aspose.Words per .NET
description: Aspose.Words.FrameFormat classe. Rappresenta la formattazione relativa al frame per un paragrafo in C#.
type: docs
weight: 3070
url: /it/net/aspose.words/frameformat/
---
## FrameFormat class

Rappresenta la formattazione relativa al frame per un paragrafo.

```csharp
public class FrameFormat
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Height](../../aspose.words/frameformat/height/) { get; } | Ottiene l'altezza del frame specificato. |
| [HeightRule](../../aspose.words/frameformat/heightrule/) { get; } | Ottiene la regola per determinare l'altezza del frame specificato. |
| [HorizontalAlignment](../../aspose.words/frameformat/horizontalalignment/) { get; } | Ottiene l'allineamento orizzontale del frame specificato. |
| [HorizontalDistanceFromText](../../aspose.words/frameformat/horizontaldistancefromtext/) { get; } | Ottiene la distanza orizzontale tra una cornice e il testo circostante, in punti. |
| [HorizontalPosition](../../aspose.words/frameformat/horizontalposition/) { get; } | Ottiene la distanza orizzontale tra il bordo del frame e l'elemento specificato da[`RelativeHorizontalPosition`](./relativehorizontalposition/) proprietà. |
| [IsFrame](../../aspose.words/frameformat/isframe/) { get; } | Restituisce`VERO` se il paragrafo è una cornice. |
| [RelativeHorizontalPosition](../../aspose.words/frameformat/relativehorizontalposition/) { get; } | Ottiene la posizione orizzontale relativa di un frame. |
| [RelativeVerticalPosition](../../aspose.words/frameformat/relativeverticalposition/) { get; } | Ottiene la posizione verticale relativa di un frame. |
| [VerticalAlignment](../../aspose.words/frameformat/verticalalignment/) { get; } | Ottiene l'allineamento verticale del frame specificato. |
| [VerticalDistanceFromText](../../aspose.words/frameformat/verticaldistancefromtext/) { get; } | Specifica la distanza verticale (in punti) tra una cornice e il testo circostante. |
| [VerticalPosition](../../aspose.words/frameformat/verticalposition/) { get; } | Ottiene la distanza verticale tra il bordo del frame e l'elemento specificato da[`RelativeVerticalPosition`](./relativeverticalposition/) proprietà. |
| [Width](../../aspose.words/frameformat/width/) { get; } | Ottiene la larghezza del frame specificato, in punti. |

## Osservazioni

Questo oggetto viene sempre creato. Se un paragrafo è una cornice, tutte le proprietà conterranno i rispettivi valori, altrimenti tutte le proprietà verranno impostate sui valori predefiniti.

Utilizzo[`IsFrame`](./isframe/) per verificare se il paragrafo è una cornice.

## Esempi

Mostra come ottenere informazioni sulle proprietà di formattazione dei paragrafi che sono frame.

```csharp
Document doc = new Document(MyDir + "Paragraph frame.docx");

Paragraph paragraphFrame = doc.FirstSection.Body.Paragraphs.OfType<Paragraph>().First(p => p.FrameFormat.IsFrame);

Assert.AreEqual(233.3d, paragraphFrame.FrameFormat.Width);
Assert.AreEqual(138.8d, paragraphFrame.FrameFormat.Height);
Assert.AreEqual(HeightRule.AtLeast, paragraphFrame.FrameFormat.HeightRule);
Assert.AreEqual(HorizontalAlignment.Default, paragraphFrame.FrameFormat.HorizontalAlignment);
Assert.AreEqual(VerticalAlignment.Default, paragraphFrame.FrameFormat.VerticalAlignment);
Assert.AreEqual(34.05d, paragraphFrame.FrameFormat.HorizontalPosition);
Assert.AreEqual(RelativeHorizontalPosition.Page, paragraphFrame.FrameFormat.RelativeHorizontalPosition);
Assert.AreEqual(9.0d, paragraphFrame.FrameFormat.HorizontalDistanceFromText);
Assert.AreEqual(20.5d, paragraphFrame.FrameFormat.VerticalPosition);
Assert.AreEqual(RelativeVerticalPosition.Paragraph, paragraphFrame.FrameFormat.RelativeVerticalPosition);
Assert.AreEqual(0.0d, paragraphFrame.FrameFormat.VerticalDistanceFromText);
```

### Guarda anche

* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)
