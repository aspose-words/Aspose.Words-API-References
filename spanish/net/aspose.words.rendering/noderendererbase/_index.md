---
title: Class NodeRendererBase
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Rendering.NodeRendererBase clase. Clase base paraShapeRenderer yOfficeMathRenderer .
type: docs
weight: 4550
url: /es/net/aspose.words.rendering/noderendererbase/
---
## NodeRendererBase class

Clase base para[`ShapeRenderer`](../shaperenderer/) y[`OfficeMathRenderer`](../officemathrenderer/) .

Para obtener más información, visite el[Trabajar con formas](https://docs.aspose.com/words/net/working-with-shapes/) artículo de documentación.

```csharp
public abstract class NodeRendererBase
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [BoundsInPoints](../../aspose.words.rendering/noderendererbase/boundsinpoints/) { get; } | Obtiene los límites reales de la forma en puntos. |
| [OpaqueBoundsInPoints](../../aspose.words.rendering/noderendererbase/opaqueboundsinpoints/) { get; } | Obtiene los límites opacos de la forma en puntos. |
| [SizeInPoints](../../aspose.words.rendering/noderendererbase/sizeinpoints/) { get; } | Obtiene el tamaño real de la forma en puntos. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [GetBoundsInPixels](../../aspose.words.rendering/noderendererbase/getboundsinpixels/#getboundsinpixels)(float, float) | Calcula los límites de la forma en píxeles para un factor de zoom y una resolución específicos. |
| [GetBoundsInPixels](../../aspose.words.rendering/noderendererbase/getboundsinpixels/#getboundsinpixels_1)(float, float, float) | Calcula los límites de la forma en píxeles para un factor de zoom y una resolución específicos. |
| [GetOpaqueBoundsInPixels](../../aspose.words.rendering/noderendererbase/getopaqueboundsinpixels/#getopaqueboundsinpixels)(float, float) | Calcula los límites opacos de la forma en píxeles para un factor de zoom y una resolución específicos. |
| [GetOpaqueBoundsInPixels](../../aspose.words.rendering/noderendererbase/getopaqueboundsinpixels/#getopaqueboundsinpixels_1)(float, float, float) | Calcula los límites opacos de la forma en píxeles para un factor de zoom y una resolución específicos. |
| [GetSizeInPixels](../../aspose.words.rendering/noderendererbase/getsizeinpixels/#getsizeinpixels)(float, float) | Calcula el tamaño de la forma en píxeles para un factor de zoom y una resolución específicos. |
| [GetSizeInPixels](../../aspose.words.rendering/noderendererbase/getsizeinpixels/#getsizeinpixels_1)(float, float, float) | Calcula el tamaño de la forma en píxeles para un factor de zoom y una resolución específicos. |
| [RenderToScale](../../aspose.words.rendering/noderendererbase/rendertoscale/)(Graphics, float, float, float) | Representa la forma en unGraphics objeto a una escala especificada. |
| [RenderToSize](../../aspose.words.rendering/noderendererbase/rendertosize/)(Graphics, float, float, float, float) | Representa la forma en unGraphics objeto a un tamaño especificado. |
| [Save](../../aspose.words.rendering/noderendererbase/save/#save)(Stream, ImageSaveOptions) | Representa la forma en una imagen y la guarda en una secuencia. |
| [Save](../../aspose.words.rendering/noderendererbase/save/#save_1)(string, ImageSaveOptions) | Representa la forma en una imagen y la guarda en un archivo. |

### Ejemplos

Muestra cómo medir y escalar formas.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath officeMath = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);
OfficeMathRenderer renderer = new OfficeMathRenderer(officeMath);

// Verificar el tamaño de la imagen que creará el objeto OfficeMath cuando lo rendericemos.
Assert.AreEqual(119.0f, renderer.SizeInPoints.Width, 0.2f);
Assert.AreEqual(13.0f, renderer.SizeInPoints.Height, 0.1f);

Assert.AreEqual(119.0f, renderer.BoundsInPoints.Width, 0.2f);
Assert.AreEqual(13.0f, renderer.BoundsInPoints.Height, 0.1f);

// Las formas con partes transparentes pueden contener diferentes valores en las propiedades "OpaqueBoundsInPoints".
Assert.AreEqual(119.0f, renderer.OpaqueBoundsInPoints.Width, 0.2f);
Assert.AreEqual(14.2f, renderer.OpaqueBoundsInPoints.Height, 0.1f);

// Obtenga el tamaño de la forma en píxeles, con escala lineal a un DPI específico.
Rectangle bounds = renderer.GetBoundsInPixels(1.0f, 96.0f);

Assert.AreEqual(159, bounds.Width);
Assert.AreEqual(18, bounds.Height);

// Obtenga el tamaño de la forma en píxeles, pero con un DPI diferente para las dimensiones horizontal y vertical.
bounds = renderer.GetBoundsInPixels(1.0f, 96.0f, 150.0f);
Assert.AreEqual(159, bounds.Width);
Assert.AreEqual(28, bounds.Height);

// Los límites opacos también pueden variar aquí.
bounds = renderer.GetOpaqueBoundsInPixels(1.0f, 96.0f);

Assert.AreEqual(159, bounds.Width);
Assert.AreEqual(18, bounds.Height);

bounds = renderer.GetOpaqueBoundsInPixels(1.0f, 96.0f, 150.0f);

Assert.AreEqual(159, bounds.Width);
Assert.AreEqual(30, bounds.Height);
```

### Ver también

* espacio de nombres [Aspose.Words.Rendering](../../aspose.words.rendering/)
* asamblea [Aspose.Words](../../)


