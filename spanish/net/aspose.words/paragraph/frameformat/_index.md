---
title: Paragraph.FrameFormat
linktitle: FrameFormat
articleTitle: FrameFormat
second_title: Aspose.Words para .NET
description: Descubra la propiedad Paragraph FrameFormat, acceda y personalice fácilmente las propiedades de formato de marco para mejorar la presentación del documento.
type: docs
weight: 30
url: /es/net/aspose.words/paragraph/frameformat/
---
## Paragraph.FrameFormat property

Proporciona acceso a las propiedades de formato del marco.

```csharp
public FrameFormat FrameFormat { get; }
```

## Ejemplos

Muestra cómo obtener información sobre las propiedades de formato de los párrafos que son marcos.

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

### Ver también

* class [FrameFormat](../../frameformat/)
* class [Paragraph](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
