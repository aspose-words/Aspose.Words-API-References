---
title: FrameFormat.VerticalDistanceFromText
second_title: Referencia de API de Aspose.Words para .NET
description: FrameFormat propiedad. Especifica la distancia vertical en puntos entre un marco y el texto circundante.
type: docs
weight: 100
url: /es/net/aspose.words/frameformat/verticaldistancefromtext/
---
## FrameFormat.VerticalDistanceFromText property

Especifica la distancia vertical (en puntos) entre un marco y el texto circundante.

```csharp
public double VerticalDistanceFromText { get; }
```

### Ejemplos

Muestra cómo obtener información sobre las propiedades de formato de párrafos que son marcos.

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

* class [FrameFormat](../)
* espacio de nombres [Aspose.Words](../../frameformat/)
* asamblea [Aspose.Words](../../../)


