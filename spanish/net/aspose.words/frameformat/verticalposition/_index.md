---
title: FrameFormat.VerticalPosition
second_title: Referencia de API de Aspose.Words para .NET
description: FrameFormat propiedad. Obtiene la distancia vertical entre el borde del marco y el elemento especificado por elRelativeVerticalPosition propiedad.
type: docs
weight: 110
url: /es/net/aspose.words/frameformat/verticalposition/
---
## FrameFormat.VerticalPosition property

Obtiene la distancia vertical entre el borde del marco y el elemento especificado por el[`RelativeVerticalPosition`](../relativeverticalposition/) propiedad.

```csharp
public double VerticalPosition { get; }
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


