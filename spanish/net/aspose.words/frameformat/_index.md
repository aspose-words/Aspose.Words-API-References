---
title: Class FrameFormat
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.FrameFormat clase. Representa el formato relacionado con el marco para un párrafo.
type: docs
weight: 3070
url: /es/net/aspose.words/frameformat/
---
## FrameFormat class

Representa el formato relacionado con el marco para un párrafo.

```csharp
public class FrameFormat
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Height](../../aspose.words/frameformat/height/) { get; } | Obtiene la altura del marco especificado. |
| [HeightRule](../../aspose.words/frameformat/heightrule/) { get; } | Obtiene la regla para determinar la altura del marco especificado. |
| [HorizontalAlignment](../../aspose.words/frameformat/horizontalalignment/) { get; } | Obtiene la alineación horizontal del marco especificado. |
| [HorizontalDistanceFromText](../../aspose.words/frameformat/horizontaldistancefromtext/) { get; } | Obtiene la distancia horizontal entre un marco y el texto circundante, en puntos. |
| [HorizontalPosition](../../aspose.words/frameformat/horizontalposition/) { get; } | Obtiene la distancia horizontal entre el borde del marco y el elemento especificado por el[`RelativeHorizontalPosition`](./relativehorizontalposition/) propiedad. |
| [IsFrame](../../aspose.words/frameformat/isframe/) { get; } | Devoluciones`verdadero` si el párrafo es un marco. |
| [RelativeHorizontalPosition](../../aspose.words/frameformat/relativehorizontalposition/) { get; } | Obtiene la posición horizontal relativa de un marco. |
| [RelativeVerticalPosition](../../aspose.words/frameformat/relativeverticalposition/) { get; } | Obtiene la posición vertical relativa de un marco. |
| [VerticalAlignment](../../aspose.words/frameformat/verticalalignment/) { get; } | Obtiene la alineación vertical del marco especificado. |
| [VerticalDistanceFromText](../../aspose.words/frameformat/verticaldistancefromtext/) { get; } | Especifica la distancia vertical (en puntos) entre un marco y el texto circundante. |
| [VerticalPosition](../../aspose.words/frameformat/verticalposition/) { get; } | Obtiene la distancia vertical entre el borde del marco y el elemento especificado por el[`RelativeVerticalPosition`](./relativeverticalposition/) propiedad. |
| [Width](../../aspose.words/frameformat/width/) { get; } | Obtiene el ancho del marco especificado, en puntos. |

### Observaciones

Este objeto siempre se crea. Si un párrafo es un marco, todas las propiedades contendrán los valores respectivos; de lo contrario, todas las propiedades se establecen en sus valores predeterminados.

Usar[`IsFrame`](./isframe/) para comprobar si el párrafo es un marco.

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

* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)


