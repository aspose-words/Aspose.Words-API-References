---
title: FrameFormat.Height
second_title: Référence de l'API Aspose.Words pour .NET
description: FrameFormat propriété. Obtient la hauteur du cadre spécifié.
type: docs
weight: 10
url: /fr/net/aspose.words/frameformat/height/
---
## FrameFormat.Height property

Obtient la hauteur du cadre spécifié.

```csharp
public double Height { get; }
```

### Exemples

Montre comment obtenir des informations sur les propriétés de mise en forme des paragraphes qui sont des cadres.

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

* class [FrameFormat](../)
* espace de noms [Aspose.Words](../../frameformat/)
* Assemblée [Aspose.Words](../../../)


