---
title: Paragraph.FrameFormat
linktitle: FrameFormat
articleTitle: FrameFormat
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Paragraph FrameFormat, accédez et personnalisez facilement les propriétés de formatage du cadre pour une présentation améliorée du document.
type: docs
weight: 30
url: /fr/net/aspose.words/paragraph/frameformat/
---
## Paragraph.FrameFormat property

Donne accès aux propriétés de formatage du cadre.

```csharp
public FrameFormat FrameFormat { get; }
```

## Exemples

Montre comment obtenir des informations sur les propriétés de formatage des paragraphes qui sont des cadres.

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

### Voir également

* class [FrameFormat](../../frameformat/)
* class [Paragraph](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
