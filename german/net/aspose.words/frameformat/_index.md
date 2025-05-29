---
title: FrameFormat Class
linktitle: FrameFormat
articleTitle: FrameFormat
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aspose.Words.FrameFormat-Klasse für erweiterte Rahmenformatierung in Absätzen. Optimieren Sie Ihr Dokumentdesign durch nahtlose Integration und Flexibilität.
type: docs
weight: 3500
url: /de/net/aspose.words/frameformat/
---
## FrameFormat class

Stellt die rahmenbezogene Formatierung für einen Absatz dar.

```csharp
public class FrameFormat
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Height](../../aspose.words/frameformat/height/) { get; } | Ruft die Höhe des angegebenen Rahmens ab. |
| [HeightRule](../../aspose.words/frameformat/heightrule/) { get; } | Ruft die Regel zum Bestimmen der Höhe des angegebenen Rahmens ab. |
| [HorizontalAlignment](../../aspose.words/frameformat/horizontalalignment/) { get; } | Ruft die horizontale Ausrichtung des angegebenen Rahmens ab. |
| [HorizontalDistanceFromText](../../aspose.words/frameformat/horizontaldistancefromtext/) { get; } | Ruft den horizontalen Abstand zwischen einem Rahmen und dem umgebenden Text in Punkten ab. |
| [HorizontalPosition](../../aspose.words/frameformat/horizontalposition/) { get; } | Ermittelt den horizontalen Abstand zwischen der Kante des Rahmens und dem durch den[`RelativeHorizontalPosition`](./relativehorizontalposition/) Eigenschaft. |
| [IsFrame](../../aspose.words/frameformat/isframe/) { get; } | Rückgaben`WAHR` wenn der Absatz ein Rahmen ist. |
| [RelativeHorizontalPosition](../../aspose.words/frameformat/relativehorizontalposition/) { get; } | Ruft die relative horizontale Position eines Frames ab. |
| [RelativeVerticalPosition](../../aspose.words/frameformat/relativeverticalposition/) { get; } | Ruft die relative vertikale Position eines Frames ab. |
| [VerticalAlignment](../../aspose.words/frameformat/verticalalignment/) { get; } | Ruft die vertikale Ausrichtung des angegebenen Rahmens ab. |
| [VerticalDistanceFromText](../../aspose.words/frameformat/verticaldistancefromtext/) { get; } | Gibt den vertikalen Abstand (in Punkten) zwischen einem Rahmen und dem umgebenden Text an. |
| [VerticalPosition](../../aspose.words/frameformat/verticalposition/) { get; } | Ermittelt den vertikalen Abstand zwischen dem Rand des Rahmens und dem durch den[`RelativeVerticalPosition`](./relativeverticalposition/) Eigenschaft. |
| [Width](../../aspose.words/frameformat/width/) { get; } | Ruft die Breite des angegebenen Rahmens in Punkten ab. |

## Bemerkungen

Dieses Objekt wird immer erstellt. Handelt es sich bei einem Absatz um einen Rahmen, enthalten alle Eigenschaften entsprechende Werte, andernfalls werden alle Eigenschaften auf ihre Standardwerte gesetzt.

Verwenden[`IsFrame`](./isframe/)um zu prüfen, ob der Absatz ein Rahmen ist.

## Beispiele

Zeigt, wie Sie Informationen zu Formatierungseigenschaften von Absätzen erhalten, die Rahmen sind.

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

### Siehe auch

* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
