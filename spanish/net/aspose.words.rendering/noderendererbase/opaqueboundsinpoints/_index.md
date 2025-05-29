---
title: NodeRendererBase.OpaqueBoundsInPoints
linktitle: OpaqueBoundsInPoints
articleTitle: OpaqueBoundsInPoints
second_title: Aspose.Words para .NET
description: Descubra la propiedad NodeRendererBase OpaqueBoundsInPoints para acceder fácilmente a los límites de formas en puntos, mejorando la precisión y la eficiencia de su diseño.
type: docs
weight: 20
url: /es/net/aspose.words.rendering/noderendererbase/opaqueboundsinpoints/
---
## NodeRendererBase.OpaqueBoundsInPoints property

Obtiene los límites opacos de la forma en puntos.

```csharp
public RectangleF OpaqueBoundsInPoints { get; }
```

## Observaciones

Esta propiedad devuelve el cuadro delimitador opaco (es decir, se ignoran las partes transparentes de la forma) de la forma. Los límites tienen en cuenta la rotación de la forma.

## Ejemplos

Muestra cómo medir y escalar formas.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath officeMath = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);
OfficeMathRenderer renderer = new OfficeMathRenderer(officeMath);

// Verificar el tamaño de la imagen que el objeto OfficeMath creará cuando lo rendericemos.
Assert.AreEqual(122.0f, renderer.SizeInPoints.Width, 0.25f);
Assert.AreEqual(13.0f, renderer.SizeInPoints.Height, 0.15f);

Assert.AreEqual(122.0f, renderer.BoundsInPoints.Width, 0.25f);
Assert.AreEqual(13.0f, renderer.BoundsInPoints.Height, 0.15f);

// Las formas con partes transparentes pueden contener valores diferentes en las propiedades "OpaqueBoundsInPoints".
Assert.AreEqual(122.0f, renderer.OpaqueBoundsInPoints.Width, 0.25f);
Assert.AreEqual(14.2f, renderer.OpaqueBoundsInPoints.Height, 0.1f);

// Obtenga el tamaño de la forma en píxeles, con escala lineal a un DPI específico.
Rectangle bounds = renderer.GetBoundsInPixels(1.0f, 96.0f);

Assert.AreEqual(163, bounds.Width);
Assert.AreEqual(18, bounds.Height);

// Obtenga el tamaño de la forma en píxeles, pero con un DPI diferente para las dimensiones horizontales y verticales.
bounds = renderer.GetBoundsInPixels(1.0f, 96.0f, 150.0f);
Assert.AreEqual(163, bounds.Width);
Assert.AreEqual(27, bounds.Height);

// Los límites opacos también pueden variar aquí.
bounds = renderer.GetOpaqueBoundsInPixels(1.0f, 96.0f);

Assert.AreEqual(163, bounds.Width);
Assert.AreEqual(19, bounds.Height);

bounds = renderer.GetOpaqueBoundsInPixels(1.0f, 96.0f, 150.0f);

Assert.AreEqual(163, bounds.Width);
Assert.AreEqual(29, bounds.Height);
```

### Ver también

* class [NodeRendererBase](../)
* espacio de nombres [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* asamblea [Aspose.Words](../../../)
