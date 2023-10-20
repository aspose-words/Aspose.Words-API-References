---
title: FrameFormat.HeightRule
linktitle: HeightRule
articleTitle: HeightRule
second_title: Aspose.Words per .NET
description: FrameFormat HeightRule proprietà. Ottiene la regola per determinare laltezza del frame specificato in C#.
type: docs
weight: 20
url: /it/net/aspose.words/frameformat/heightrule/
---
## FrameFormat.HeightRule property

Ottiene la regola per determinare l'altezza del frame specificato.

```csharp
public HeightRule HeightRule { get; }
```

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

* enum [HeightRule](../../heightrule/)
* class [FrameFormat](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
