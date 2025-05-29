---
title: FrameFormat.RelativeVerticalPosition
linktitle: RelativeVerticalPosition
articleTitle: RelativeVerticalPosition
second_title: Aspose.Words para .NET
description: Descubra la propiedad FrameFormat RelativeVerticalPosition para determinar fácilmente la alineación vertical de un marco, mejorando el diseño y la disposición de su documento.
type: docs
weight: 80
url: /es/net/aspose.words/frameformat/relativeverticalposition/
---
## FrameFormat.RelativeVerticalPosition property

Obtiene la posición vertical relativa de un marco.

```csharp
public RelativeVerticalPosition RelativeVerticalPosition { get; }
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

* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* class [FrameFormat](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
